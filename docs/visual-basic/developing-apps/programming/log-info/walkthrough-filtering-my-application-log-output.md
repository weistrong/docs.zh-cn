---
description: 详细了解：演练：筛选 My.Application.Log 输出 (Visual Basic)
title: 筛选 My.Application.Log 输出
ms.date: 07/20/2015
helpviewer_keywords:
- My.Log object, filtering output
- My.Application.Log object, filtering output
- application event logs, output filtering
ms.assetid: 2c0a457a-38a4-49e1-934d-a51320b7b4ca
ms.openlocfilehash: 0fa64bde27be17b1809e45bfe294e70c7dd33563
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792253"
---
# <a name="walkthrough-filtering-myapplicationlog-output-visual-basic"></a><span data-ttu-id="65de2-103">演练：筛选 My.Application.Log 输出 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="65de2-103">Walkthrough: Filtering My.Application.Log Output (Visual Basic)</span></span>

<span data-ttu-id="65de2-104">本演练演示如何更改对 `My.Application.Log` 对象的默认日志筛选，以控制哪些信息可从 `Log` 对象传递到侦听器以及哪些信息可由侦听器编写。</span><span class="sxs-lookup"><span data-stu-id="65de2-104">This walkthrough demonstrates how to change the default log filtering for the `My.Application.Log` object, to control what information is passed from the `Log` object to the listeners and what information is written by the listeners.</span></span> <span data-ttu-id="65de2-105">生成应用程序后仍可以更改日志记录行为，因为配置信息存储在应用程序的配置文件中。</span><span class="sxs-lookup"><span data-stu-id="65de2-105">You can change the logging behavior even after building the application, because the configuration information is stored in the application's configuration file.</span></span>

## <a name="getting-started"></a><span data-ttu-id="65de2-106">入门</span><span class="sxs-lookup"><span data-stu-id="65de2-106">Getting Started</span></span>

<span data-ttu-id="65de2-107">`My.Application.Log` 编写的每条消息均具有相关严重级别，筛选机制使用此级别控制日志输出。</span><span class="sxs-lookup"><span data-stu-id="65de2-107">Each message that `My.Application.Log` writes has an associated severity level, which filtering mechanisms use to control the log output.</span></span> <span data-ttu-id="65de2-108">此示例应用程序使用 `My.Application.Log` 方法编写具有不同严重级别的若干日志消息。</span><span class="sxs-lookup"><span data-stu-id="65de2-108">This sample application uses `My.Application.Log` methods to write several log messages with different severity levels.</span></span>

#### <a name="to-build-the-sample-application"></a><span data-ttu-id="65de2-109">生成示例应用程序</span><span class="sxs-lookup"><span data-stu-id="65de2-109">To build the sample application</span></span>

1. <span data-ttu-id="65de2-110">打开一个新的 Visual Basic Windows 应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="65de2-110">Open a new Visual Basic Windows Application project.</span></span>

2. <span data-ttu-id="65de2-111">向 Form1 添加一个名为 Button1 的按钮。</span><span class="sxs-lookup"><span data-stu-id="65de2-111">Add a button named Button1 to Form1.</span></span>

3. <span data-ttu-id="65de2-112">在 Button1 的 <xref:System.Windows.Forms.Control.Click> 事件处理程序中，添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="65de2-112">In the <xref:System.Windows.Forms.Control.Click> event handler for Button1, add the following code:</span></span>

     [!code-vb[VbVbcnMyApplicationLogFiltering#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyApplicationLogFiltering/VB/Form1.vb#1)]

4. <span data-ttu-id="65de2-113">在调试器中运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-113">Run the application in the debugger.</span></span>

5. <span data-ttu-id="65de2-114">按“Button1”。 </span><span class="sxs-lookup"><span data-stu-id="65de2-114">Press **Button1**.</span></span>

     <span data-ttu-id="65de2-115">应用程序将向应用程序的调试输出和日志文件中写入以下信息。</span><span class="sxs-lookup"><span data-stu-id="65de2-115">The application writes the following information to the application's debug output and log file.</span></span>

     `DefaultSource Information: 0 : In Button1_Click`

     `DefaultSource Error: 2 : Error in the application.`

6. <span data-ttu-id="65de2-116">关闭该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-116">Close the application.</span></span>

     <span data-ttu-id="65de2-117">有关如何查看应用程序的调试输出窗口的信息，请参阅[输出窗口](/visualstudio/ide/reference/output-window)。</span><span class="sxs-lookup"><span data-stu-id="65de2-117">For information on how to view the application's debug output window, see [Output Window](/visualstudio/ide/reference/output-window).</span></span> <span data-ttu-id="65de2-118">有关应用程序日志文件的位置的信息，请参阅[演练：确定 My.Application.Log 写入信息的位置](walkthrough-determining-where-my-application-log-writes-information.md)。</span><span class="sxs-lookup"><span data-stu-id="65de2-118">For information on the location of the application's log file, see [Walkthrough: Determining Where My.Application.Log Writes Information](walkthrough-determining-where-my-application-log-writes-information.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="65de2-119">默认情况下，应用程序关闭时将刷新日志文件输出。</span><span class="sxs-lookup"><span data-stu-id="65de2-119">By default, the application flushes the log-file output when the application closes.</span></span>

     <span data-ttu-id="65de2-120">在上面的示例中，对 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A> 方法的第二次调用和对 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A> 方法的调用会产生日志输出，而对 `WriteEntry` 方法的第一次和最后一次调用则不会。</span><span class="sxs-lookup"><span data-stu-id="65de2-120">In the example above, the second call to the <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A> method and the call to the <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A> method produces log output, while the first and last calls to the `WriteEntry` method do not.</span></span> <span data-ttu-id="65de2-121">这是因为 `WriteEntry` 和 `WriteException` 的严重级别为“信息”和“错误”，而 `My.Application.Log` 对象的默认日志筛选支持这两种级别。</span><span class="sxs-lookup"><span data-stu-id="65de2-121">This is because the severity levels of `WriteEntry` and `WriteException` are "Information" and "Error", both of which are allowed by the `My.Application.Log` object's default log filtering.</span></span> <span data-ttu-id="65de2-122">但是，不允许严重级别为“开始”和“停止”的事件生成日志输出。</span><span class="sxs-lookup"><span data-stu-id="65de2-122">However, events with "Start" and "Stop" severity levels are prevented from producing log output.</span></span>

## <a name="filtering-for-all-myapplicationlog-listeners"></a><span data-ttu-id="65de2-123">对所有 My.Application.Log 侦听器的筛选</span><span class="sxs-lookup"><span data-stu-id="65de2-123">Filtering for All My.Application.Log Listeners</span></span>

<span data-ttu-id="65de2-124">`My.Application.Log` 对象使用名为 `DefaultSwitch` 的 <xref:System.Diagnostics.SourceSwitch>，以控制将哪些消息从 `WriteEntry` 和 `WriteException` 方法传递到日志侦听器。</span><span class="sxs-lookup"><span data-stu-id="65de2-124">The `My.Application.Log` object uses a <xref:System.Diagnostics.SourceSwitch> named `DefaultSwitch` to control which messages it passes from the `WriteEntry` and `WriteException` methods to the log listeners.</span></span> <span data-ttu-id="65de2-125">通过将 `DefaultSwitch` 的值设置为 <xref:System.Diagnostics.SourceLevels> 枚举值的其中一个，可在应用程序的配置文件中对其进行配置。</span><span class="sxs-lookup"><span data-stu-id="65de2-125">You can configure `DefaultSwitch` in the application's configuration file by setting its value to one of the <xref:System.Diagnostics.SourceLevels> enumeration values.</span></span> <span data-ttu-id="65de2-126">默认情况下，其值为“信息”。</span><span class="sxs-lookup"><span data-stu-id="65de2-126">By default, its value is "Information".</span></span>

<span data-ttu-id="65de2-127">此表显示了在给定的特定 `DefaultSwitch` 设置下，日志将消息写入侦听器所需的严重级别。</span><span class="sxs-lookup"><span data-stu-id="65de2-127">This table shows the severity level required for Log to write a message to the listeners, given a particular `DefaultSwitch` setting.</span></span>

|<span data-ttu-id="65de2-128">DefaultSwitch 值</span><span class="sxs-lookup"><span data-stu-id="65de2-128">DefaultSwitch Value</span></span>|<span data-ttu-id="65de2-129">输出所需的消息严重级别</span><span class="sxs-lookup"><span data-stu-id="65de2-129">Message severity required for output</span></span>|
|---|---|
|`Critical`|`Critical`|
|`Error`|<span data-ttu-id="65de2-130">`Critical` 或 `Error`</span><span class="sxs-lookup"><span data-stu-id="65de2-130">`Critical` or `Error`</span></span>|
|`Warning`|<span data-ttu-id="65de2-131">`Critical`、`Error` 或 `Warning`</span><span class="sxs-lookup"><span data-stu-id="65de2-131">`Critical`, `Error`, or `Warning`</span></span>|
|`Information`|<span data-ttu-id="65de2-132">`Critical`、 `Error`、 `Warning`或 `Information`</span><span class="sxs-lookup"><span data-stu-id="65de2-132">`Critical`, `Error`, `Warning`, or `Information`</span></span>|
|`Verbose`|<span data-ttu-id="65de2-133">`Critical`、`Error`、`Warning`、`Information` 或 `Verbose`</span><span class="sxs-lookup"><span data-stu-id="65de2-133">`Critical`, `Error`, `Warning`, `Information`, or `Verbose`</span></span>|
|`ActivityTracing`|<span data-ttu-id="65de2-134">`Start`、`Stop`、`Suspend`、`Resume` 或 `Transfer`</span><span class="sxs-lookup"><span data-stu-id="65de2-134">`Start`, `Stop`, `Suspend`, `Resume`, or `Transfer`</span></span>|
|`All`|<span data-ttu-id="65de2-135">允许所有消息。</span><span class="sxs-lookup"><span data-stu-id="65de2-135">All messages are allowed.</span></span>|
|`Off`|<span data-ttu-id="65de2-136">阻止所有消息。</span><span class="sxs-lookup"><span data-stu-id="65de2-136">All messages are blocked.</span></span>|

> [!NOTE]
> <span data-ttu-id="65de2-137">`WriteEntry` 和 `WriteException` 方法分别具有一个未指定严重级别的重载。</span><span class="sxs-lookup"><span data-stu-id="65de2-137">The `WriteEntry` and `WriteException` methods each have an overload that does not specify a severity level.</span></span> <span data-ttu-id="65de2-138">`WriteEntry` 重载的隐式严重级别是“信息”，`WriteException` 重载的隐式严重级别是“错误”。</span><span class="sxs-lookup"><span data-stu-id="65de2-138">The implicit severity level for the `WriteEntry` overload is "Information", and the implicit severity level for the `WriteException` overload is "Error".</span></span>

<span data-ttu-id="65de2-139">此表说明上一示例中显示的日志输出：在 `DefaultSwitch` 默认设置为“信息”的情况下，只有对 `WriteEntry` 方法的第二次调用和对 `WriteException` 方法的调用能生成日志输出。</span><span class="sxs-lookup"><span data-stu-id="65de2-139">This table explains the log output shown in the previous example: with the default `DefaultSwitch` setting of "Information", only the second call to the `WriteEntry` method and the call to the `WriteException` method produce log output.</span></span>

#### <a name="to-log-only-activity-tracing-events"></a><span data-ttu-id="65de2-140">仅记录活动跟踪事件</span><span class="sxs-lookup"><span data-stu-id="65de2-140">To log only activity tracing events</span></span>

1. <span data-ttu-id="65de2-141">在“解决方案资源管理器”中右键单击 app.config，然后选择“打开”。  </span><span class="sxs-lookup"><span data-stu-id="65de2-141">Right-click app.config in the **Solution Explorer** and select **Open**.</span></span>

     <span data-ttu-id="65de2-142">或</span><span class="sxs-lookup"><span data-stu-id="65de2-142">-or-</span></span>

     <span data-ttu-id="65de2-143">如果其中没有 app.config 文件：</span><span class="sxs-lookup"><span data-stu-id="65de2-143">If there is no app.config file:</span></span>

    1. <span data-ttu-id="65de2-144">在 **“项目”** 菜单上选择 **“添加新项”** 。</span><span class="sxs-lookup"><span data-stu-id="65de2-144">On the **Project** menu, choose **Add New Item**.</span></span>

    2. <span data-ttu-id="65de2-145">在“添加新项”  对话框中，选择“应用程序配置文件”  。</span><span class="sxs-lookup"><span data-stu-id="65de2-145">From the **Add New Item** dialog box, choose **Application Configuration File**.</span></span>

    3. <span data-ttu-id="65de2-146">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="65de2-146">Click **Add**.</span></span>

2. <span data-ttu-id="65de2-147">找到 `<switches>` 部分，该部分位于 `<system.diagnostics>` 部分中，后者位于顶级 `<configuration>` 部分中。</span><span class="sxs-lookup"><span data-stu-id="65de2-147">Locate the `<switches>` section, which is in the `<system.diagnostics>` section, which is in the top-level `<configuration>` section.</span></span>

3. <span data-ttu-id="65de2-148">找到将 `DefaultSwitch` 添加到开关集合的元素。</span><span class="sxs-lookup"><span data-stu-id="65de2-148">Find the element that adds `DefaultSwitch` to the collection of switches.</span></span> <span data-ttu-id="65de2-149">此元素应与下面的元素类似：</span><span class="sxs-lookup"><span data-stu-id="65de2-149">It should look similar to this element:</span></span>

     `<add name="DefaultSwitch" value="Information" />`

4. <span data-ttu-id="65de2-150">将 `value` 属性的值更改为“ActivityTracing”。</span><span class="sxs-lookup"><span data-stu-id="65de2-150">Change the value of the `value` attribute to "ActivityTracing".</span></span>

5. <span data-ttu-id="65de2-151">app.config 文件的内容应类似于下面的 XML：</span><span class="sxs-lookup"><span data-stu-id="65de2-151">The content of the app.config file should be similar to the following XML:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <system.diagnostics>
        <sources>
          <!-- This section configures My.Application.Log -->
          <source name="DefaultSource" switchName="DefaultSwitch">
            <listeners>
              <add name="FileLog"/>
            </listeners>
          </source>
        </sources>
        <switches>
          <add name="DefaultSwitch" value="ActivityTracing" />
        </switches>
        <sharedListeners>
          <add name="FileLog"
               type="Microsoft.VisualBasic.Logging.FileLogTraceListener,
                     Microsoft.VisualBasic, Version=8.0.0.0,
                     Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a,
                     processorArchitecture=MSIL"
               initializeData="FileLogWriter"/>
        </sharedListeners>
      </system.diagnostics>
    </configuration>
    ```

6. <span data-ttu-id="65de2-152">在调试器中运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-152">Run the application in the debugger.</span></span>

7. <span data-ttu-id="65de2-153">按“Button1”。 </span><span class="sxs-lookup"><span data-stu-id="65de2-153">Press **Button1**.</span></span>

     <span data-ttu-id="65de2-154">应用程序将向应用程序的调试输出和日志文件中写入以下信息：</span><span class="sxs-lookup"><span data-stu-id="65de2-154">The application writes the following information to the application's debug output and log file:</span></span>

     `DefaultSource Start: 4 : Entering Button1_Click`

     `DefaultSource Stop: 5 : Leaving Button1_Click`

8. <span data-ttu-id="65de2-155">关闭该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-155">Close the application.</span></span>

9. <span data-ttu-id="65de2-156">将 `value` 属性的值改回“信息”。</span><span class="sxs-lookup"><span data-stu-id="65de2-156">Change the value of the `value` attribute back to "Information".</span></span>

    > [!NOTE]
    > <span data-ttu-id="65de2-157">`DefaultSwitch` 开关设置仅控制 `My.Application.Log`。</span><span class="sxs-lookup"><span data-stu-id="65de2-157">The `DefaultSwitch` switch setting controls only `My.Application.Log`.</span></span> <span data-ttu-id="65de2-158">它不会更改 .NET <xref:System.Diagnostics.Trace?displayProperty=nameWithType> 和 <xref:System.Diagnostics.Debug?displayProperty=nameWithType> 类的行为方式。</span><span class="sxs-lookup"><span data-stu-id="65de2-158">It does not change how the .NET <xref:System.Diagnostics.Trace?displayProperty=nameWithType> and <xref:System.Diagnostics.Debug?displayProperty=nameWithType> classes behave.</span></span>

## <a name="individual-filtering-for-myapplicationlog-listeners"></a><span data-ttu-id="65de2-159">对 My.Application.Log 侦听器的单独筛选</span><span class="sxs-lookup"><span data-stu-id="65de2-159">Individual Filtering For My.Application.Log Listeners</span></span>

<span data-ttu-id="65de2-160">上面的示例演示如何更改对所有 `My.Application.Log` 输出的筛选。</span><span class="sxs-lookup"><span data-stu-id="65de2-160">The previous example shows how to change the filtering for all `My.Application.Log` output.</span></span> <span data-ttu-id="65de2-161">此示例演示如何筛选单个日志侦听器。</span><span class="sxs-lookup"><span data-stu-id="65de2-161">This example demonstrates how to filter an individual log listener.</span></span> <span data-ttu-id="65de2-162">默认情况下，应用程序有两个可写入应用程序的调试输出和日志文件的侦听器。</span><span class="sxs-lookup"><span data-stu-id="65de2-162">By default, an application has two listeners that write to the application's debug output and the log file.</span></span>

<span data-ttu-id="65de2-163">配置文件控制日志侦听器的行为，方法是允许每个侦听器拥有一个筛选器，这类似于 `My.Application.Log` 的开关。</span><span class="sxs-lookup"><span data-stu-id="65de2-163">The configuration file controls the behavior of the log listeners by allowing each one to have a filter, which is similar to a switch for `My.Application.Log`.</span></span> <span data-ttu-id="65de2-164">仅当日志的 `DefaultSwitch` 和日志侦听器的筛选器均支持消息的严重级别时，日志侦听器才会输出消息。</span><span class="sxs-lookup"><span data-stu-id="65de2-164">A log listener will output a message only if the message's severity is allowed by both the log's `DefaultSwitch` and the log listener's filter.</span></span>

<span data-ttu-id="65de2-165">此示例演示如何为新的调试侦听器配置筛选并将其添加到 `Log` 对象。</span><span class="sxs-lookup"><span data-stu-id="65de2-165">This example demonstrates how to configure filtering for a new debug listener and add it to the `Log` object.</span></span> <span data-ttu-id="65de2-166">应删除 `Log` 对象中的默认调试侦听器，以便明确调试消息来自新的调试侦听器。</span><span class="sxs-lookup"><span data-stu-id="65de2-166">The default debug listener should be removed from the `Log` object, so it is clear that the debug messages come from the new debug listener.</span></span>

#### <a name="to-log-only-activity-tracing-events"></a><span data-ttu-id="65de2-167">仅记录活动跟踪事件</span><span class="sxs-lookup"><span data-stu-id="65de2-167">To log only activity-tracing events</span></span>

1. <span data-ttu-id="65de2-168">在“解决方案资源管理器”中右键单击 app.config，然后选择“打开”。  </span><span class="sxs-lookup"><span data-stu-id="65de2-168">Right-click app.config in the **Solution Explorer** and choose **Open**.</span></span>

     <span data-ttu-id="65de2-169">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="65de2-169">\-or-</span></span>

     <span data-ttu-id="65de2-170">如果其中没有 app.config 文件：</span><span class="sxs-lookup"><span data-stu-id="65de2-170">If there is no app.config file:</span></span>

    1. <span data-ttu-id="65de2-171">在 **“项目”** 菜单上选择 **“添加新项”** 。</span><span class="sxs-lookup"><span data-stu-id="65de2-171">On the **Project** menu, choose **Add New Item**.</span></span>

    2. <span data-ttu-id="65de2-172">在“添加新项”  对话框中，选择“应用程序配置文件”  。</span><span class="sxs-lookup"><span data-stu-id="65de2-172">From the **Add New Item** dialog box, choose **Application Configuration File**.</span></span>

    3. <span data-ttu-id="65de2-173">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="65de2-173">Click **Add**.</span></span>

2. <span data-ttu-id="65de2-174">在“解决方案资源管理器”中右键单击 app.config。 </span><span class="sxs-lookup"><span data-stu-id="65de2-174">Right-click app.config in **Solution Explorer**.</span></span> <span data-ttu-id="65de2-175">选择“打开”。 </span><span class="sxs-lookup"><span data-stu-id="65de2-175">Choose **Open**.</span></span>

3. <span data-ttu-id="65de2-176">找到 `<listeners>` 部分，该部分位于 `name` 属性为“DefaultSource”的 `<source>` 部分中，后者位于 `<sources>` 部分中。</span><span class="sxs-lookup"><span data-stu-id="65de2-176">Locate the `<listeners>` section, in the `<source>` section with the `name` attribute "DefaultSource", which is under the `<sources>` section.</span></span> <span data-ttu-id="65de2-177">`<sources>` 部分位于 `<system.diagnostics>` 部分中，后者位于顶级 `<configuration>` 部分中。</span><span class="sxs-lookup"><span data-stu-id="65de2-177">The `<sources>` section is under the `<system.diagnostics>` section, in the top-level `<configuration>` section.</span></span>

4. <span data-ttu-id="65de2-178">将此元素添加到 `<listeners>` 部分：</span><span class="sxs-lookup"><span data-stu-id="65de2-178">Add this element to the `<listeners>` section:</span></span>

    ```xml
    <!-- Remove the default debug listener. -->
    <remove name="Default"/>
    <!-- Add a filterable debug listener. -->
    <add name="NewDefault"/>
    ```

5. <span data-ttu-id="65de2-179">找到 `<sharedListeners>` 部分，该部分位于 `<system.diagnostics>` 部分当中，后者又位于顶级 `<configuration>` 部分之下。</span><span class="sxs-lookup"><span data-stu-id="65de2-179">Locate the `<sharedListeners>` section, in the `<system.diagnostics>` section, in the top-level `<configuration>` section.</span></span>

6. <span data-ttu-id="65de2-180">将此元素添加到该 `<sharedListeners>` 部分：</span><span class="sxs-lookup"><span data-stu-id="65de2-180">Add this element to that `<sharedListeners>` section:</span></span>

    ```xml
    <add name="NewDefault"
         type="System.Diagnostics.DefaultTraceListener,
               System, Version=2.0.0.0, Culture=neutral,
               PublicKeyToken=b77a5c561934e089,
               processorArchitecture=MSIL">
        <filter type="System.Diagnostics.EventTypeFilter"
                initializeData="Error" />
    </add>
    ```

     <span data-ttu-id="65de2-181"><xref:System.Diagnostics.EventTypeFilter> 筛选器将其中一个 <xref:System.Diagnostics.SourceLevels> 枚举值用作其 `initializeData` 属性。</span><span class="sxs-lookup"><span data-stu-id="65de2-181">The <xref:System.Diagnostics.EventTypeFilter> filter takes one of the <xref:System.Diagnostics.SourceLevels> enumeration values as its `initializeData` attribute.</span></span>

7. <span data-ttu-id="65de2-182">app.config 文件的内容应类似于下面的 XML：</span><span class="sxs-lookup"><span data-stu-id="65de2-182">The content of the app.config file should be similar to the following XML:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <system.diagnostics>
        <sources>
          <!-- This section configures My.Application.Log -->
          <source name="DefaultSource" switchName="DefaultSwitch">
            <listeners>
              <add name="FileLog"/>
              <!-- Remove the default debug listener. -->
              <remove name="Default"/>
              <!-- Add a filterable debug listener. -->
              <add name="NewDefault"/>
            </listeners>
          </source>
        </sources>
        <switches>
          <add name="DefaultSwitch" value="Information" />
        </switches>
        <sharedListeners>
          <add name="FileLog"
               type="Microsoft.VisualBasic.Logging.FileLogTraceListener,
                     Microsoft.VisualBasic, Version=8.0.0.0,
                     Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a,
                     processorArchitecture=MSIL"
               initializeData="FileLogWriter"/>
          <add name="NewDefault"
               type="System.Diagnostics.DefaultTraceListener,
                     System, Version=2.0.0.0, Culture=neutral,
                     PublicKeyToken=b77a5c561934e089,
                     processorArchitecture=MSIL">
            <filter type="System.Diagnostics.EventTypeFilter"
                    initializeData="Error" />
          </add>
        </sharedListeners>
      </system.diagnostics>
    </configuration>
    ```

8. <span data-ttu-id="65de2-183">在调试器中运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-183">Run the application in the debugger.</span></span>

9. <span data-ttu-id="65de2-184">按“Button1”。 </span><span class="sxs-lookup"><span data-stu-id="65de2-184">Press **Button1**.</span></span>

     <span data-ttu-id="65de2-185">应用程序将以下信息写入应用程序的日志文件：</span><span class="sxs-lookup"><span data-stu-id="65de2-185">The application writes the following information to the application's log file:</span></span>

     `Default Information: 0 : In Button1_Click`

     `Default Error: 2 : Error in the application.`

     <span data-ttu-id="65de2-186">由于筛选限制性更强，应用程序将较少的信息写入应用程序的调试输出。</span><span class="sxs-lookup"><span data-stu-id="65de2-186">The application writes less information to the application's debug output because of the more restrictive filtering.</span></span>

     `Default Error   2   Error`

10. <span data-ttu-id="65de2-187">关闭该应用程序。</span><span class="sxs-lookup"><span data-stu-id="65de2-187">Close the application.</span></span>

<span data-ttu-id="65de2-188">有关在部署后更改日志设置的详细信息，请参阅[使用应用程序日志](working-with-application-logs.md)。</span><span class="sxs-lookup"><span data-stu-id="65de2-188">For more information about changing log settings after deployment, see [Working with Application Logs](working-with-application-logs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="65de2-189">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65de2-189">See also</span></span>

- [<span data-ttu-id="65de2-190">演练：确定 My.Application.Log 写入信息的位置</span><span class="sxs-lookup"><span data-stu-id="65de2-190">Walkthrough: Determining Where My.Application.Log Writes Information</span></span>](walkthrough-determining-where-my-application-log-writes-information.md)
- [<span data-ttu-id="65de2-191">演练：更改 My.Application.Log 写入信息的位置</span><span class="sxs-lookup"><span data-stu-id="65de2-191">Walkthrough: Changing Where My.Application.Log Writes Information</span></span>](walkthrough-changing-where-my-application-log-writes-information.md)
- [<span data-ttu-id="65de2-192">演练：创建自定义日志侦听器</span><span class="sxs-lookup"><span data-stu-id="65de2-192">Walkthrough: Creating Custom Log Listeners</span></span>](walkthrough-creating-custom-log-listeners.md)
- [<span data-ttu-id="65de2-193">如何：编写日志消息</span><span class="sxs-lookup"><span data-stu-id="65de2-193">How to: Write Log Messages</span></span>](how-to-write-log-messages.md)
- [<span data-ttu-id="65de2-194">跟踪开关</span><span class="sxs-lookup"><span data-stu-id="65de2-194">Trace Switches</span></span>](../../../../framework/debug-trace-profile/trace-switches.md)
- [<span data-ttu-id="65de2-195">记录来自应用程序的信息</span><span class="sxs-lookup"><span data-stu-id="65de2-195">Logging Information from the Application</span></span>](index.md)
