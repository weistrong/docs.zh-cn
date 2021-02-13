---
title: 分布式跟踪 - .NET
description: 介绍了 .NET 分布式跟踪。
ms.date: 02/02/2021
ms.openlocfilehash: d21d2a978cfe58d89db689dec07107f089363912
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640116"
---
# <a name="net-distributed-tracing"></a><span data-ttu-id="ac0c7-103">.NET 分布式跟踪</span><span class="sxs-lookup"><span data-stu-id="ac0c7-103">.NET Distributed Tracing</span></span>

<span data-ttu-id="ac0c7-104">分布式跟踪是在分布式系统中发布和观察跟踪数据的方法。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-104">Distributed tracing is the way to publish and observe tracing data in a distributed system.</span></span>
<span data-ttu-id="ac0c7-105">.NET Framework 和 .NET Core 一直支持通过 <xref:System.Diagnostics> API 进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-105">.NET Framework and .NET Core has been supporting tracing through the <xref:System.Diagnostics> APIs.</span></span>

- <span data-ttu-id="ac0c7-106"><xref:System.Diagnostics.Activity?displayProperty=nameWithType> 类，它允许存储和访问诊断上下文，并将其用于日志记录系统。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-106"><xref:System.Diagnostics.Activity?displayProperty=nameWithType> class which allows storing and accessing diagnostics context and consuming it with logging system.</span></span>
- <span data-ttu-id="ac0c7-107"><xref:System.Diagnostics.DiagnosticSource?displayProperty=nameWithType>，允许对代码进行检测，以便实现丰富数据有效负载的生产时日志记录，以供在检测到的进程中使用。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-107"><xref:System.Diagnostics.DiagnosticSource?displayProperty=nameWithType> that allows code to be instrumented for production-time logging of rich data payloads for consumption within the process that was instrumented.</span></span>

<span data-ttu-id="ac0c7-108">下面的示例展示了如何发布来自 HTTP 传入请求的跟踪数据：</span><span class="sxs-lookup"><span data-stu-id="ac0c7-108">Here is an example that shows how to publish tracing data from the HTTP incoming requests:</span></span>

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

<span data-ttu-id="ac0c7-109">下面的示例展示了如何侦听 Activity 事件：</span><span class="sxs-lookup"><span data-stu-id="ac0c7-109">Here is example for how to listen to the Activity events:</span></span>

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

<span data-ttu-id="ac0c7-110">.NET 5.0 扩展了分布式跟踪功能来允许 [OpenTelemetry](https://opentelemetry.io/) 跟踪方案，新增了采样功能，简化了跟踪编码模式，并使侦听 Activity 事件变得更容易、更灵活。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-110">.NET 5.0 has extended the capability of the distributed tracing to allow the [OpenTelemetry](https://opentelemetry.io/) tracing scenarios, added Sampling capabilities, simplified the tracing coding pattern, and made listening to the Activity events easier and flexible.</span></span>

> [!NOTE]
> <span data-ttu-id="ac0c7-111">若要访问所有新增的 .NET 5.0 功能，请确保你的项目引用了 [System.Diagnostics.DiagnosticSource](https://www.nuget.org/packages/System.Diagnostics.DiagnosticSource/) NuGet 包版本 5.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-111">To access all added .NET 5.0 capabilities, ensure your project references the [System.Diagnostics.DiagnosticSource](https://www.nuget.org/packages/System.Diagnostics.DiagnosticSource/) NuGet package version 5.0 or later.</span></span> <span data-ttu-id="ac0c7-112">此包可用于以任何受支持的 .NET Framework、.NET Core 和 .NET Standard 版本为目标的库和应用。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-112">This package can be used in libraries and apps targeting any supported version of the .NET Framework, .NET Core, and .NET Standard.</span></span> <span data-ttu-id="ac0c7-113">如果以 .NET 5.0 或更高版本为目标，则无需手动引用此包，因为它包含在使用 .NET 运行时安装的共享库中。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-113">If targeting .NET 5.0 or later, there is no need to manually reference the package as it is included in the shared library installed with the .NET Runtime.</span></span>

## <a name="getting-started-with-tracing"></a><span data-ttu-id="ac0c7-114">跟踪入门</span><span class="sxs-lookup"><span data-stu-id="ac0c7-114">Getting Started With Tracing</span></span>

<span data-ttu-id="ac0c7-115">应用程序和库可以直接使用 <xref:System.Diagnostics.ActivitySource?displayProperty=nameWithType> 和 <xref:System.Diagnostics.Activity?displayProperty=nameWithType> 类来轻松发布跟踪数据。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-115">Applications and libraries can easily publish tracing data by simply using the <xref:System.Diagnostics.ActivitySource?displayProperty=nameWithType> and the <xref:System.Diagnostics.Activity?displayProperty=nameWithType> classes.</span></span>

### <a name="activitysource"></a><span data-ttu-id="ac0c7-116">ActivitySource</span><span class="sxs-lookup"><span data-stu-id="ac0c7-116">ActivitySource</span></span>

<span data-ttu-id="ac0c7-117">发布跟踪数据的第一步是，创建 ActivitySource 类的实例。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-117">The first step to publish tracing data is to create an instance of the ActivitySource class.</span></span> <span data-ttu-id="ac0c7-118">ActivitySource 是一个类，它提供 API 来创建和启动 Activity 对象，以及注册 ActivityListener 对象来侦听 Activity 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-118">The ActivitySource is the class that provides APIs to create and start Activity objects and to register ActivityListener objects to listen to the Activity events.</span></span>

```csharp
    internal static ActivitySource source = new ActivitySource("MyCompany.MyComponent.SourceName", "v1");
```

#### <a name="best-practices"></a><span data-ttu-id="ac0c7-119">最佳方案</span><span class="sxs-lookup"><span data-stu-id="ac0c7-119">Best Practices</span></span>

- <span data-ttu-id="ac0c7-120">创建一次 ActivitySource，将它存储在静态变量中，并根据需要使用相应实例。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-120">Create the ActivitySource once and store it in a static variable and use that instance as long as needed.</span></span>

- <span data-ttu-id="ac0c7-121">传递给构造函数的源名称必须是唯一的，以免与其他任何源发生冲突。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-121">The source name passed to the constructor has to be unique to avoid the conflicts with any other sources.</span></span> <span data-ttu-id="ac0c7-122">建议使用包含公司名称、组件名称和源名称的分层名称。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-122">It is recommended to use a hierarchical name contains the company name, the component name, and the source name.</span></span> <span data-ttu-id="ac0c7-123">例如，`Microsoft.System.HttpClient.HttpInOutRequests` 。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-123">For example, `Microsoft.System.HttpClient.HttpInOutRequests`.</span></span>

- <span data-ttu-id="ac0c7-124">version 是可选参数。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-124">The version parameter is optional.</span></span> <span data-ttu-id="ac0c7-125">如果你计划发布多个版本的库或应用程序，并且希望区分不同版本的源，则建议提供版本。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-125">It is recommended to provide the version in case you plan to release multiple versions of the library or the application and want to distinguish between the sources of different versions.</span></span>

### <a name="activity-creation"></a><span data-ttu-id="ac0c7-126">创建 Activity 对象</span><span class="sxs-lookup"><span data-stu-id="ac0c7-126">Activity Creation</span></span>

<span data-ttu-id="ac0c7-127">现在，已创建的 ActivitySource 对象可用于创建和启动 Activity 对象，这些对象用于在代码中的任何所需位置记录任何跟踪数据。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-127">Now the created ActivitySource object can be used to create and start Activity objects which are used to log any tracing data in any desired places in the code.</span></span>

```csharp
        using (Activity activity = source.StartActivity("OperationName"))
        {
            // Do something

            activity?.AddTag("key", "value"); // log the tracing
        }
```

<span data-ttu-id="ac0c7-128">此示例代码尝试创建 Activity 对象，然后记录一些跟踪标记 `key` 和 `value`。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-128">This sample code tries to create the Activity object and then logs some tracing tag `key` and `value`.</span></span>

#### <a name="notes"></a><span data-ttu-id="ac0c7-129">说明</span><span class="sxs-lookup"><span data-stu-id="ac0c7-129">Notes</span></span>

- <span data-ttu-id="ac0c7-130">`ActivitySource.StartActivity` 尝试同时创建和启动活动。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-130">`ActivitySource.StartActivity` tries to create and start the activity at the same time.</span></span> <span data-ttu-id="ac0c7-131">列出的代码模式使用的是 `using` 块，它会在执行此块后自动释放创建的 Activity 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-131">The listed code pattern is using the `using` block which automatically disposes the created Activity object after executing the block.</span></span> <span data-ttu-id="ac0c7-132">释放 Activity 对象将停止这个已启动的活动，代码不必显式地停止此活动。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-132">Disposing the Activity object will stop this started activity and the code doesn't have to explicitly stop the activity.</span></span> <span data-ttu-id="ac0c7-133">这简化了编码模式。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-133">That simplifies the coding pattern.</span></span>

- <span data-ttu-id="ac0c7-134">`ActivitySource.StartActivity` 会在内部确定是否有侦听此类事件的任何侦听器。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-134">`ActivitySource.StartActivity` internally figures out if there are any listeners to such events.</span></span> <span data-ttu-id="ac0c7-135">如果没有已注册的侦听器，或有不关注此类事件的侦听器，那么 `ActivitySource.StartActivity` 就会直接返回 `null`，并避免创建 Activity 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-135">If there are no registered listeners or there are listeners which are not interested in such an event, `ActivitySource.StartActivity` simply will return `null` and avoid creating the Activity object.</span></span> <span data-ttu-id="ac0c7-136">这就是为什么代码在语句 `activity?.AddTag` 中使用了可以为 null 的运算符 `?`。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-136">That is why the code used the nullable operator `?`  in the statement `activity?.AddTag`.</span></span> <span data-ttu-id="ac0c7-137">通常，在 `using` 块内部，总是在 Activity 对象名称后使用可以为 null 的运算符 `?`。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-137">In general, inside the `using` block, always use the nullable operator `?` after the activity object name.</span></span>

## <a name="listening-to-the-activity-events"></a><span data-ttu-id="ac0c7-138">侦听 Activity 事件</span><span class="sxs-lookup"><span data-stu-id="ac0c7-138">Listening to the Activity Events</span></span>

<span data-ttu-id="ac0c7-139">.NET 提供了类 <xref:System.Diagnostics.ActivityListener?displayProperty=nameWithType>，可以用来侦听从一个或多个 ActivitySource 触发的 Activity 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-139">.NET provides the class <xref:System.Diagnostics.ActivityListener?displayProperty=nameWithType> which can be used to listen to the Activity events triggered from one or more ActivitySources.</span></span>
<span data-ttu-id="ac0c7-140">侦听器可用于收集跟踪数据、采样或强制创建 Activity 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-140">The listener can be used to collect tracing data, sample, or force creating the Activity object.</span></span>

<span data-ttu-id="ac0c7-141">`ActivityListener` 类提供了不同的回叫函数来处理不同的事件。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-141">The `ActivityListener` class provides a different callbacks to handle different events.</span></span>

```csharp

ActivityListener listener = new ActivityListener()

ShouldListenTo = (activitySource) => object.ReferenceEquals(source, activitySource),
ActivityStarted = activity => /* Handle the Activity start event here */ DoSomething(),
ActivityStopped = activity => /* Handle the Activity stop event here */ DoSomething(),
SampleUsingParentId = (ref ActivityCreationOptions<string> activityOptions) => ActivitySamplingResult.AllData,
Sample = (ref ActivityCreationOptions<ActivityContext> activityOptions) => ActivitySamplingResult.AllData

// Enable the listener
ActivitySource.AddActivityListener(listener);
```

- <span data-ttu-id="ac0c7-142">`ShouldListenTo` 支持侦听特定的 `ActivitySource` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-142">`ShouldListenTo` enables listening to specific `ActivitySource` objects.</span></span> <span data-ttu-id="ac0c7-143">在此示例中，它支持侦听前面创建的 `ActivitySource` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-143">In the example, it enables listening to the `ActivitySource` object we have previously created.</span></span> <span data-ttu-id="ac0c7-144">通过检查输入 `ActivitySource` 的 `Name` 和 `Version`，可以更灵活地侦听其他任何 `ActivitySource` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-144">There is more flexibility to listen to any other `ActivitySource` objects by checking the `Name` and `Version` of the input `ActivitySource`.</span></span>

- <span data-ttu-id="ac0c7-145">使用 `ActivityStarted` 和 `ActivityStopped`，可以获取由 `ShouldListenTo` 回叫函数启用的 `ActivitySource` 对象所创建的所有 `Activity` 对象的 `Activity` Start 和 Stop 事件。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-145">`ActivityStarted` and `ActivityStopped` enable getting the `Activity` Start and Stop events for all `Activity` objects created by the `ActivitySource` objects which were enabled by the `ShouldListenTo` callback.</span></span>

- <span data-ttu-id="ac0c7-146">`Sample` 和 `SampleUsingParentId` 是用于采样的主要回叫函数。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-146">`Sample` and `SampleUsingParentId` are the main callbacks which intended for sampling.</span></span> <span data-ttu-id="ac0c7-147">这两个回叫函数返回 `ActivitySamplingResult` 枚举值，它指明对当前的 `Activity` 创建请求进行输入采样还是输出采样。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-147">These two callbacks return the `ActivitySamplingResult` enum value which can tell either to sample in or out the current `Activity` creation request.</span></span> <span data-ttu-id="ac0c7-148">如果回叫函数返回 `ActivitySamplingResult.None`，并且没有其他任何已启用的侦听器返回不同的值，那么 Activity 将不会被创建，`ActivitySource.StartActivity` 将返回 `null`。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-148">If the callback returns `ActivitySamplingResult.None` and no other enabled listeners return different value, then the Activity will not get created and `ActivitySource.StartActivity` will return `null`.</span></span> <span data-ttu-id="ac0c7-149">否则，将创建 `Activity` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-149">Otherwise, the `Activity` object will get created.</span></span>

## <a name="net-50-new-features"></a><span data-ttu-id="ac0c7-150">.NET 5.0 新功能</span><span class="sxs-lookup"><span data-stu-id="ac0c7-150">.NET 5.0 New Features</span></span>

<span data-ttu-id="ac0c7-151">`Activity` 类支持跟踪方案已经有一段时间了。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-151">For awhile the `Activity` class has been supporting tracing scenarios.</span></span> <span data-ttu-id="ac0c7-152">它允许添加标记，即跟踪数据的键值对。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-152">It allowed adding tags which are key-value pairs of tracing data.</span></span> <span data-ttu-id="ac0c7-153">它一直支持 Baggage，即要在网上传播的键值对。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-153">It has been supporting Baggage which is are key-value pairs intended to be propagated across the wire.</span></span>

<span data-ttu-id="ac0c7-154">.NET 5.0 支持更多的功能，主要是为了支持 OpenTelemetry 方案。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-154">.NET 5.0 supports more features mainly to enable OpenTelemetry scenarios.</span></span>

### <a name="activitycontext"></a><span data-ttu-id="ac0c7-155">ActivityContext</span><span class="sxs-lookup"><span data-stu-id="ac0c7-155">ActivityContext</span></span>

<span data-ttu-id="ac0c7-156"><xref:System.Diagnostics.ActivityContext?displayProperty=nameWithType> 是携带跟踪操作上下文（例如跟踪 ID、跨度 ID、跟踪标志和跟踪状态）的结构。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-156"><xref:System.Diagnostics.ActivityContext?displayProperty=nameWithType> is the struct carrying the context of the tracing operations (e.g. the trace Id, Span Id, trace flags, and trace state).</span></span> <span data-ttu-id="ac0c7-157">现在可以新建提供父跟踪上下文的 `Activity`。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-157">Now it is possible to create a new `Activity` providing the parent tracing context.</span></span> <span data-ttu-id="ac0c7-158">此外，通过调用 `Activity.Context` 属性，可以很容易地从任何 `Activity` 对象中提取跟踪上下文。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-158">Also, it is easy to extract the tracing context from any `Activity` object by calling `Activity.Context` property.</span></span>

### <a name="activitylink"></a><span data-ttu-id="ac0c7-159">ActivityLink</span><span class="sxs-lookup"><span data-stu-id="ac0c7-159">ActivityLink</span></span>

<span data-ttu-id="ac0c7-160"><xref:System.Diagnostics.ActivityLink?displayProperty=nameWithType> 是包含跟踪上下文实例的结构，它可以链接到随意相关的 `Activity` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-160"><xref:System.Diagnostics.ActivityLink?displayProperty=nameWithType> is the struct containing the tracing context instance which can be linked to casually related `Activity` objects.</span></span> <span data-ttu-id="ac0c7-161">通过在创建 `Activity` 时将链接列表传递到 `ActivitySource.StartActivity` 方法，可以向 `Activity` 对象添加链接。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-161">Links can be added to the `Activity` object by passing the links list to `ActivitySource.StartActivity` method when creating the `Activity`.</span></span> <span data-ttu-id="ac0c7-162">可以使用属性 `Activity.Links` 来检索 `Activity` 对象附加的链接。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-162">The `Activity` object attached links can be retrieved using the property `Activity.Links`.</span></span>

### <a name="activityevent"></a><span data-ttu-id="ac0c7-163">ActivityEvent</span><span class="sxs-lookup"><span data-stu-id="ac0c7-163">ActivityEvent</span></span>

<span data-ttu-id="ac0c7-164"><xref:System.Diagnostics.ActivityEvent?displayProperty=nameWithType> 表示包含名称、时间戳以及可选标记列表的事件。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-164"><xref:System.Diagnostics.ActivityEvent?displayProperty=nameWithType> represents an event containing a name and a timestamp, as well as an optional list of tags.</span></span> <span data-ttu-id="ac0c7-165">可以通过调用 `Activity.AddEvent` 方法将事件添加到 `Activity` 对象中。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-165">Events can be added to the `Activity` object by calling `Activity.AddEvent` method.</span></span> <span data-ttu-id="ac0c7-166">可以使用属性 `Activity.Events` 来检索 `Activity` 对象事件的整个列表。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-166">The whole list of the `Activity` object Events can be retrieved using the property `Activity.Events`.</span></span>

### <a name="activitykind"></a><span data-ttu-id="ac0c7-167">ActivityKind</span><span class="sxs-lookup"><span data-stu-id="ac0c7-167">ActivityKind</span></span>

<span data-ttu-id="ac0c7-168"><xref:System.Diagnostics.ActivityKind?displayProperty=nameWithType> 描述了跟踪中的活动、它的父活动和子活动之间的关系。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-168"><xref:System.Diagnostics.ActivityKind?displayProperty=nameWithType> describes the relationship between the activity, its parents and its children in a trace.</span></span> <span data-ttu-id="ac0c7-169">通过在创建 `Activity` 时将种类值传递到 `ActivitySource.StartActivity` 方法，可以将种类设置为 `Activity` 对象。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-169">Kind can be set to the `Activity` object by passing the kind value to `ActivitySource.StartActivity` method when creating the `Activity`.</span></span> <span data-ttu-id="ac0c7-170">可以使用 `Activity.Kind` 属性来检索 `Activity` 对象种类。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-170">The `Activity` object kind can be retrieved using the property `Activity.Kind`.</span></span>

### <a name="isalldatarequested"></a><span data-ttu-id="ac0c7-171">IsAllDataRequested</span><span class="sxs-lookup"><span data-stu-id="ac0c7-171">IsAllDataRequested</span></span>

<span data-ttu-id="ac0c7-172"><xref:System.Diagnostics.Activity.IsAllDataRequested?displayProperty=nameWithType> 指明是否应使用所有传播信息以及所有其他属性（如链接、标记和事件）填充此活动。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-172"><xref:System.Diagnostics.Activity.IsAllDataRequested?displayProperty=nameWithType> indicates whether this activity should be populated with all the propagation information, as well as all the other properties, such as links, tags, and events.</span></span> <span data-ttu-id="ac0c7-173">`IsAllDataRequested` 的值由所有侦听器 `Sample` 和 `SampleUsingParentId` 回叫函数返回的结果决定。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-173">The value of `IsAllDataRequested` is determined from the result returned from all listeners `Sample` and `SampleUsingParentId` callbacks.</span></span> <span data-ttu-id="ac0c7-174">可以使用 `Activity.IsAllDataRequested` 属性来检索此值。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-174">The value can be retrieved using `Activity.IsAllDataRequested` property.</span></span>

### <a name="activitysource"></a><span data-ttu-id="ac0c7-175">Activity.Source</span><span class="sxs-lookup"><span data-stu-id="ac0c7-175">Activity.Source</span></span>

<span data-ttu-id="ac0c7-176"><xref:System.Diagnostics.Activity.Source?displayProperty=nameWithType> 获取与此活动关联的活动源。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-176"><xref:System.Diagnostics.Activity.Source?displayProperty=nameWithType> gets the activity source associated with this activity.</span></span>

### <a name="activitydisplayname"></a><span data-ttu-id="ac0c7-177">Activity.DisplayName</span><span class="sxs-lookup"><span data-stu-id="ac0c7-177">Activity.DisplayName</span></span>

<span data-ttu-id="ac0c7-178"><xref:System.Diagnostics.Activity.DisplayName?displayProperty=nameWithType> 允许获取或设置活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-178"><xref:System.Diagnostics.Activity.DisplayName?displayProperty=nameWithType> allows getting or setting a display name for the activity.</span></span>

### <a name="activitytagobjects"></a><span data-ttu-id="ac0c7-179">Activity.TagObjects</span><span class="sxs-lookup"><span data-stu-id="ac0c7-179">Activity.TagObjects</span></span>

<span data-ttu-id="ac0c7-180">`Activity` 类有属性 `Activity.Tags`，它为键和值返回字符串类型的标记的键值对列表。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-180">`Activity` class has the property `Activity.Tags` which return the a key-value pair list of the tags of type string for the key and value.</span></span> <span data-ttu-id="ac0c7-181">可以使用方法 `AddTag(string, string)` 将此类标记添加到 `Activity` 中。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-181">Such Tags can be added to the `Activity` using the method `AddTag(string, string)`.</span></span> <span data-ttu-id="ac0c7-182">`Activity` 通过提供允许任何类型的值的重载方法 `AddTag(string, object)` 扩展了对标记的支持。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-182">`Activity` has extended the support of tags by providing the overloaded method `AddTag(string, object)` allowing values of any type.</span></span>  <span data-ttu-id="ac0c7-183">可以使用 <xref:System.Diagnostics.Activity.TagObjects?displayProperty=nameWithType> 来检索此类标记的完整列表。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-183">The complete list of such tags can be retrieved using <xref:System.Diagnostics.Activity.TagObjects?displayProperty=nameWithType>.</span></span>

## <a name="sampling"></a><span data-ttu-id="ac0c7-184">采样</span><span class="sxs-lookup"><span data-stu-id="ac0c7-184">Sampling</span></span>

<span data-ttu-id="ac0c7-185">采样是一种通过减少收集和发送到后端的跟踪样本数来控制干扰和开销的机制。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-185">Sampling is a mechanism to control the noise and overhead by reducing the number of samples of traces collected and sent to the backend.</span></span> <span data-ttu-id="ac0c7-186">采样是重要的 OpenTelemetry 方案。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-186">Sampling is an important OpenTelemetry scenario.</span></span> <span data-ttu-id="ac0c7-187">在 .NET 5.0 中，很容易允许进行采样。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-187">In .NET 5.0 it is easy to allow sampling.</span></span> <span data-ttu-id="ac0c7-188">一种很好的做法是使用 `ActivitySource.StartActivity` 新建 `Activity` 对象，并尝试在调用此方法时提供所有可能的可用数据（例如标记、种类、链接等）。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-188">A good practice is to create the new `Activity` objects using `ActivitySource.StartActivity` and try to provide all possible available data (e.g. tags, kind, links, ...etc.) when calling this method.</span></span> <span data-ttu-id="ac0c7-189">提供数据将允许使用 `ActivityListener` 实现的采样器有正确的采样决策。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-189">Providing the data will allow the samplers implemented using the `ActivityListener` to have a proper sampling decision.</span></span> <span data-ttu-id="ac0c7-190">如果性能对于避免在创建 `Activity` 对象之前创建数据至关重要，那么属性 `ActivitySource.HasListeners` 可以方便地用于在创建所需数据之前检查是否有任何侦听器。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-190">If the performance is critical to avoid creating the data before creating the `Activity` object, the property `ActivitySource.HasListeners` comes in handy to check if there are any listeners before creating the needed data.</span></span>

## <a name="opentelemetry"></a><span data-ttu-id="ac0c7-191">OpenTelemetry</span><span class="sxs-lookup"><span data-stu-id="ac0c7-191">OpenTelemetry</span></span>

<span data-ttu-id="ac0c7-192">OpenTelemetry SDK 随附了许多支持端到端分布式跟踪方案的功能。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-192">OpenTelemetry SDK comes with many features that support end-to-end distributed tracing scenarios.</span></span> <span data-ttu-id="ac0c7-193">它提供了多个采样器和导出程序，你可以从中进行选择。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-193">It provides multiple samplers and exporters which you can choose from.</span></span> <span data-ttu-id="ac0c7-194">它还允许创建自定义采样器和导出程序。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-194">It allows creating a custom samplers and exporters too.</span></span>

<span data-ttu-id="ac0c7-195">OpenTelemetry 支持将收集的跟踪数据导出到不同的后端（例如 Jaeger、Zipkin、New Relic 等）。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-195">OpenTelemetry supports exporting the collected tracing data to different backends (e.g. Jaeger, Zipkin, New Relic,...etc.).</span></span> <span data-ttu-id="ac0c7-196">请参阅 [OpenTelemetry-dotnet](https://github.com/open-telemetry/opentelemetry-dotnet/) 来了解更多详情，并在 Nuget.org 中搜索以 `OpenTelemetry.Exporter.` 开头的包，以获取导出程序包列表。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-196">Refer to [OpenTelemetry-dotnet](https://github.com/open-telemetry/opentelemetry-dotnet/) for more details and search Nuget.org for packages starting with `OpenTelemetry.Exporter.` to get the exporter packages list.</span></span>

<span data-ttu-id="ac0c7-197">下面是从 [OpenTelemetry-dotnet 入门](https://github.com/open-telemetry/opentelemetry-dotnet/tree/main/docs/trace/getting-started)移植的示例代码，展示了如何轻松地进行采样并将跟踪数据导出到控制台。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-197">Here is sample code ported from [OpenTelemetry-dotnet getting started](https://github.com/open-telemetry/opentelemetry-dotnet/tree/main/docs/trace/getting-started) showing how easy it is to sample and export tracing data to the console.</span></span>

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

<span data-ttu-id="ac0c7-198">此示例需要引用 [OpenTelemetry.Exporter.Console](https://www.nuget.org/packages/OpenTelemetry.Exporter.Console/1.0.0-rc2) 包。</span><span class="sxs-lookup"><span data-stu-id="ac0c7-198">The sample needs to reference the package [OpenTelemetry.Exporter.Console](https://www.nuget.org/packages/OpenTelemetry.Exporter.Console/1.0.0-rc2).</span></span>
