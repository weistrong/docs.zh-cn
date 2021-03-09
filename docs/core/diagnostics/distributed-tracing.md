---
title: 分布式跟踪 - .NET
description: 介绍了 .NET 分布式跟踪。
ms.date: 02/02/2021
ms.openlocfilehash: 44022232d4451f8d8a255a352206d7bdc9cb4e5c
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102105566"
---
# <a name="net-distributed-tracing"></a>.NET 分布式跟踪

分布式跟踪是在分布式系统中发布和观察跟踪数据的方法。
.NET Framework 和 .NET Core 一直支持通过 <xref:System.Diagnostics> API 进行跟踪。

- <xref:System.Diagnostics.Activity?displayProperty=nameWithType> 类，它允许存储和访问诊断上下文，并将其用于日志记录系统。
- <xref:System.Diagnostics.DiagnosticSource?displayProperty=nameWithType>，允许对代码进行检测，以便实现丰富数据有效负载的生产时日志记录，以供在检测到的进程中使用。

下面的示例展示了如何发布来自 HTTP 传入请求的跟踪数据：

```csharp
   public void OnIncomingRequest(DiagnosticListener httpListener, HttpContext context)
   {
       if (httpListener.IsEnabled("Http_In"))
       {
           var activity = new Activity("Http_In");

           //add tags, baggage, etc.
           activity.SetParentId(context.Request.headers["Request-id"])
           foreach (var pair in context.Request.Headers["Correlation-Context"])
           {
               var baggageItem = NameValueHeaderValue.Parse(pair);
               activity.AddBaggage(baggageItem.Key, baggageItem.Value);
           }
           httpListener.StartActivity(activity, new { context });
           try
           {
               //process request ...
           }
           finally
           {
               //stop activity
               httpListener.StopActivity(activity, new {context} );
           }
       }
   }
```

下面的示例展示了如何侦听 Activity 事件：

```csharp
    DiagnosticListener.AllListeners.Subscribe(delegate (DiagnosticListener listener)
    {
        if (listener.Name == "MyActivitySource")
        {
            listener.Subscribe(delegate (KeyValuePair<string, object> value)
            {
                if (value.Key.EndsWith("Start", StringComparison.Ordinal))
                    LogActivityStart();
                else if (value.Key.EndsWith("Stop", StringComparison.Ordinal))
                    LogActivityStop();
            });
        }
    }
```

.NET 5.0 扩展了分布式跟踪功能来允许 [OpenTelemetry](https://opentelemetry.io/) 跟踪方案，新增了采样功能，简化了跟踪编码模式，并使侦听 Activity 事件变得更容易、更灵活。

> [!NOTE]
> 若要访问所有新增的 .NET 5.0 功能，请确保你的项目引用了 [System.Diagnostics.DiagnosticSource](https://www.nuget.org/packages/System.Diagnostics.DiagnosticSource/) NuGet 包版本 5.0 或更高版本。 此包可用于以任何受支持的 .NET Framework、.NET Core 和 .NET Standard 版本为目标的库和应用。 如果以 .NET 5.0 或更高版本为目标，则无需手动引用此包，因为它包含在使用 .NET 运行时安装的共享库中。

## <a name="getting-started-with-tracing"></a>跟踪入门

应用程序和库可以直接使用 <xref:System.Diagnostics.ActivitySource?displayProperty=nameWithType> 和 <xref:System.Diagnostics.Activity?displayProperty=nameWithType> 类来轻松发布跟踪数据。

### <a name="activitysource"></a>ActivitySource

发布跟踪数据的第一步是，创建 ActivitySource 类的实例。 ActivitySource 是一个类，它提供 API 来创建和启动 Activity 对象，以及注册 ActivityListener 对象来侦听 Activity 事件。

```csharp
    private static ActivitySource source = new ActivitySource("MyCompany.MyComponent.SourceName", "v1");
```

#### <a name="best-practices"></a>最佳方案

- 创建一次 ActivitySource，将它存储在静态变量中，并根据需要使用相应实例。

- 传递给构造函数的源名称必须是唯一的，以免与其他任何源发生冲突。 建议使用包含公司名称、组件名称和源名称的分层名称。 例如，`Microsoft.System.HttpClient.HttpInOutRequests` 。

- version 是可选参数。 如果你计划发布多个版本的库或应用程序，并且希望区分不同版本的源，则建议提供版本。

### <a name="activity-creation"></a>创建 Activity 对象

现在，已创建的 ActivitySource 对象可用于创建和启动 Activity 对象，这些对象用于在代码中的任何所需位置记录任何跟踪数据。

```csharp
        using (Activity activity = source.StartActivity("OperationName"))
        {
            // Do something

            activity?.AddTag("key", "value"); // log the tracing
        }
```

此示例代码尝试创建 Activity 对象，然后记录一些跟踪标记 `key` 和 `value`。

#### <a name="notes"></a>说明

- `ActivitySource.StartActivity` 尝试同时创建和启动活动。 列出的代码模式使用的是 `using` 块，它会在执行此块后自动释放创建的 Activity 对象。 释放 Activity 对象将停止这个已启动的活动，代码不必显式地停止此活动。 这简化了编码模式。

- `ActivitySource.StartActivity` 会在内部确定是否有侦听此类事件的任何侦听器。 如果没有已注册的侦听器，或有不关注此类事件的侦听器，那么 `ActivitySource.StartActivity` 就会直接返回 `null`，并避免创建 Activity 对象。 这就是为什么代码在语句 `activity?.AddTag` 中使用了可以为 null 的运算符 `?`。 通常，在 `using` 块内部，总是在 Activity 对象名称后使用可以为 null 的运算符 `?`。

## <a name="listening-to-the-activity-events"></a>侦听 Activity 事件

.NET 提供了类 <xref:System.Diagnostics.ActivityListener?displayProperty=nameWithType>，可以用来侦听从一个或多个 ActivitySource 触发的 Activity 事件。
侦听器可用于收集跟踪数据、采样或强制创建 Activity 对象。

`ActivityListener` 类提供了不同的回叫函数来处理不同的事件。

```csharp
var listener = new ActivityListener
{
    ShouldListenTo = (activitySource) => object.ReferenceEquals(source, activitySource),
    ActivityStarted = activity => /* Handle the Activity start event here */ DoSomething(),
    ActivityStopped = activity => /* Handle the Activity stop event here */ DoSomething(),
    SampleUsingParentId = (ref ActivityCreationOptions<string> activityOptions) => ActivitySamplingResult.AllData,
    Sample = (ref ActivityCreationOptions<ActivityContext> activityOptions) => ActivitySamplingResult.AllData
};

// Enable the listener
ActivitySource.AddActivityListener(listener);
```

- `ShouldListenTo` 支持侦听特定的 `ActivitySource` 对象。 在此示例中，它支持侦听前面创建的 `ActivitySource` 对象。 通过检查输入 `ActivitySource` 的 `Name` 和 `Version`，可以更灵活地侦听其他任何 `ActivitySource` 对象。

- 使用 `ActivityStarted` 和 `ActivityStopped`，可以获取由 `ShouldListenTo` 回叫函数启用的 `ActivitySource` 对象所创建的所有 `Activity` 对象的 `Activity` Start 和 Stop 事件。

- `Sample` 和 `SampleUsingParentId` 是用于采样的主要回叫函数。 这两个回叫函数返回 `ActivitySamplingResult` 枚举值，它指明对当前的 `Activity` 创建请求进行输入采样还是输出采样。 如果回叫函数返回 `ActivitySamplingResult.None`，并且没有其他任何已启用的侦听器返回不同的值，那么 Activity 将不会被创建，`ActivitySource.StartActivity` 将返回 `null`。 否则，将创建 `Activity` 对象。

## <a name="net-50-new-features"></a>.NET 5.0 新功能

`Activity` 类支持跟踪方案已经有一段时间了。 它允许添加标记，即跟踪数据的键值对。 它一直支持 Baggage，即要在网上传播的键值对。

.NET 5.0 支持更多的功能，主要是为了支持 OpenTelemetry 方案。

### <a name="activitycontext"></a>ActivityContext

<xref:System.Diagnostics.ActivityContext?displayProperty=nameWithType> 是携带跟踪操作上下文（例如跟踪 ID、跨度 ID、跟踪标志和跟踪状态）的结构。 现在可以新建提供父跟踪上下文的 `Activity`。 此外，通过调用 `Activity.Context` 属性，可以很容易地从任何 `Activity` 对象中提取跟踪上下文。

### <a name="activitylink"></a>ActivityLink

<xref:System.Diagnostics.ActivityLink?displayProperty=nameWithType> 是包含跟踪上下文实例的结构，它可以链接到随意相关的 `Activity` 对象。 通过在创建 `Activity` 时将链接列表传递到 `ActivitySource.StartActivity` 方法，可以向 `Activity` 对象添加链接。 可以使用属性 `Activity.Links` 来检索 `Activity` 对象附加的链接。

### <a name="activityevent"></a>ActivityEvent

<xref:System.Diagnostics.ActivityEvent?displayProperty=nameWithType> 表示包含名称、时间戳以及可选标记列表的事件。 可以通过调用 `Activity.AddEvent` 方法将事件添加到 `Activity` 对象中。 可以使用属性 `Activity.Events` 来检索 `Activity` 对象事件的整个列表。

### <a name="activitykind"></a>ActivityKind

<xref:System.Diagnostics.ActivityKind?displayProperty=nameWithType> 描述了跟踪中的活动、它的父活动和子活动之间的关系。 通过在创建 `Activity` 时将种类值传递到 `ActivitySource.StartActivity` 方法，可以将种类设置为 `Activity` 对象。 可以使用 `Activity.Kind` 属性来检索 `Activity` 对象种类。

### <a name="isalldatarequested"></a>IsAllDataRequested

<xref:System.Diagnostics.Activity.IsAllDataRequested?displayProperty=nameWithType> 指明是否应使用所有传播信息以及所有其他属性（如链接、标记和事件）填充此活动。 `IsAllDataRequested` 的值由所有侦听器 `Sample` 和 `SampleUsingParentId` 回叫函数返回的结果决定。 可以使用 `Activity.IsAllDataRequested` 属性来检索此值。

### <a name="activitysource"></a>Activity.Source

<xref:System.Diagnostics.Activity.Source?displayProperty=nameWithType> 获取与此活动关联的活动源。

### <a name="activitydisplayname"></a>Activity.DisplayName

<xref:System.Diagnostics.Activity.DisplayName?displayProperty=nameWithType> 允许获取或设置活动的显示名称。

### <a name="activitytagobjects"></a>Activity.TagObjects

`Activity` 类有属性 `Activity.Tags`，它为键和值返回字符串类型的标记的键值对列表。 可以使用方法 `AddTag(string, string)` 将此类标记添加到 `Activity` 中。 `Activity` 通过提供允许任何类型的值的重载方法 `AddTag(string, object)` 扩展了对标记的支持。  可以使用 <xref:System.Diagnostics.Activity.TagObjects?displayProperty=nameWithType> 来检索此类标记的完整列表。

## <a name="sampling"></a>采样

采样是一种通过减少收集和发送到后端的跟踪样本数来控制干扰和开销的机制。 采样是重要的 OpenTelemetry 方案。 在 .NET 5.0 中，很容易允许进行采样。 一种很好的做法是使用 `ActivitySource.StartActivity` 新建 `Activity` 对象，并尝试在调用此方法时提供所有可能的可用数据（例如标记、种类、链接等）。 提供数据将允许使用 `ActivityListener` 实现的采样器有正确的采样决策。 如果性能对于避免在创建 `Activity` 对象之前创建数据至关重要，那么属性 `ActivitySource.HasListeners` 可以方便地用于在创建所需数据之前检查是否有任何侦听器。

## <a name="opentelemetry"></a>OpenTelemetry

OpenTelemetry SDK 随附了许多支持端到端分布式跟踪方案的功能。 它提供了多个采样器和导出程序，你可以从中进行选择。 它还允许创建自定义采样器和导出程序。

OpenTelemetry 支持将收集的跟踪数据导出到不同的后端（例如 Jaeger、Zipkin、New Relic 等）。 请参阅 [OpenTelemetry-dotnet](https://github.com/open-telemetry/opentelemetry-dotnet/) 来了解更多详情，并在 Nuget.org 中搜索以 `OpenTelemetry.Exporter.` 开头的包，以获取导出程序包列表。

下面是从 [OpenTelemetry-dotnet 入门](https://github.com/open-telemetry/opentelemetry-dotnet/tree/main/docs/trace/getting-started)移植的示例代码，展示了如何轻松地进行采样并将跟踪数据导出到控制台。

```csharp
// <copyright file="Program.cs" company="OpenTelemetry Authors">
// Copyright The OpenTelemetry Authors
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain a copy of the License at
//
//     http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.
// </copyright>

using System.Diagnostics;
using OpenTelemetry;
using OpenTelemetry.Trace;

public class Program
{
    private static readonly ActivitySource MyActivitySource = new ActivitySource(
        "MyCompany.MyProduct.MyLibrary");

    public static void Main()
    {
        using var tracerProvider = Sdk.CreateTracerProviderBuilder()
            .SetSampler(new AlwaysOnSampler())
            .AddSource("MyCompany.MyProduct.MyLibrary")
            .AddConsoleExporter()
            .Build();

        using (var activity = MyActivitySource.StartActivity("SayHello"))
        {
            activity?.SetTag("foo", 1);
            activity?.SetTag("bar", "Hello, World!");
            activity?.SetTag("baz", new int[] { 1, 2, 3 });
        }
    }
}
```

此示例需要引用 [OpenTelemetry.Exporter.Console](https://www.nuget.org/packages/OpenTelemetry.Exporter.Console/1.0.0-rc2) 包。
