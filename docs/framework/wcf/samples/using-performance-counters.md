---
description: 了解详细信息：使用性能计数器
title: 使用性能计数器
ms.date: 03/30/2017
ms.assetid: 00a787af-1876-473c-a48d-f52b51e28a3f
ms.openlocfilehash: f2305310238df9c11ebc2612248f2d7d1b6ea6f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755728"
---
# <a name="using-performance-counters"></a><span data-ttu-id="3208b-103">使用性能计数器</span><span class="sxs-lookup"><span data-stu-id="3208b-103">Using Performance Counters</span></span>

<span data-ttu-id="3208b-104">此示例演示如何访问 Windows Communication Foundation (WCF) 性能计数器以及如何创建用户定义的性能计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-104">This sample demonstrates how to access Windows Communication Foundation (WCF) performance counters and how to create user-defined performance counters.</span></span> <span data-ttu-id="3208b-105">此示例基于 [入门](getting-started-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="3208b-105">This sample is based on the [Getting Started](getting-started-sample.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3208b-106">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="3208b-106">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="3208b-107">在此示例中，客户端调用 `ICalculator` 服务的四个方法。</span><span class="sxs-lookup"><span data-stu-id="3208b-107">In this sample, the client calls the four methods of the `ICalculator` service.</span></span> <span data-ttu-id="3208b-108">客户端一直执行该操作，直到被用户中断。</span><span class="sxs-lookup"><span data-stu-id="3208b-108">The client continues to do this until it is interrupted by the user.</span></span> <span data-ttu-id="3208b-109">该服务保持不变。</span><span class="sxs-lookup"><span data-stu-id="3208b-109">The service remains unchanged.</span></span>  
  
 <span data-ttu-id="3208b-110">性能计数器在该服务的 Web.config 文件的诊断节中启用，如下面的示例配置所示。</span><span class="sxs-lookup"><span data-stu-id="3208b-110">Performance counters are enabled in the diagnostics section of the Web.config file for the service, as shown in the following sample configuration.</span></span>  
  
```xml  
<configuration>  
  <system.serviceModel>  
    <diagnostics performanceCounters="All" />
  </system.serviceModel>  
</configuration>  
```  
  
 <span data-ttu-id="3208b-111">还可以使用 [配置编辑器工具 ( # A0) ](../configuration-editor-tool-svcconfigeditor-exe.md)来完成此任务。</span><span class="sxs-lookup"><span data-stu-id="3208b-111">This task can also be done using the [Configuration Editor Tool (SvcConfigEditor.exe)](../configuration-editor-tool-svcconfigeditor-exe.md).</span></span>  
  
 <span data-ttu-id="3208b-112">启用性能计数器后，将为服务启用整个 WCF 性能计数器套件。</span><span class="sxs-lookup"><span data-stu-id="3208b-112">When performance counters are enabled, the entire suite of WCF performance counters is enabled for the service.</span></span> <span data-ttu-id="3208b-113">.NET Framework 自动在三个级别维护性能数据：`ServiceModelService`、`ServiceModelEndpoint` 和 `ServiceModelOperation`。</span><span class="sxs-lookup"><span data-stu-id="3208b-113">The .NET Framework automatically maintains performance data at three levels: `ServiceModelService`, `ServiceModelEndpoint` and `ServiceModelOperation`.</span></span> <span data-ttu-id="3208b-114">其中每个级别都有“Calls”（调用）、“Calls per Second”（每秒调用次数）和“Security Calls Not Authorized”（未授权的安全调用次数）等性能计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-114">Each of these levels has performance counters such as "Calls", "Calls per Second", and "Security Calls Not Authorized".</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="3208b-115">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="3208b-115">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="3208b-116">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="3208b-116">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="3208b-117">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="3208b-117">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="3208b-118">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="3208b-118">To run the sample in a single- or cross-computer configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
### <a name="to-view-performance-data"></a><span data-ttu-id="3208b-119">查看性能数据</span><span class="sxs-lookup"><span data-stu-id="3208b-119">To view performance data</span></span>  
  
1. <span data-ttu-id="3208b-120">通过依次单击 " **开始**"、" **运行 ...**"，输入 `perfmon` 并单击 **"确定** "，或从 "控制面板" 中选择 " **管理工具** "，然后双击 " **性能**"。</span><span class="sxs-lookup"><span data-stu-id="3208b-120">Start the Performance Monitor Tool by clicking **Start**, **Run…**, enter `perfmon` and click **OK,** or from Control Panel, select **Administrative Tools** and double-click **Performance**.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="3208b-121">在示例代码运行之前无法添加计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-121">You cannot add counters until the sample code is running.</span></span>  
  
2. <span data-ttu-id="3208b-122">选择列出的性能计数器并按 Delete 键以移除它们。</span><span class="sxs-lookup"><span data-stu-id="3208b-122">Remove the performance counters that are listed by selecting them and pressing the Delete key.</span></span>  
  
3. <span data-ttu-id="3208b-123">通过右键单击 "关系图" 窗格并选择 " **添加计数器**" 来添加 WCF 计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-123">Add WCF counters by right-clicking the graph pane and selecting **Add Counters**.</span></span> <span data-ttu-id="3208b-124">在 " **添加计数器** " 对话框中，选择 "性能对象" 下拉列表框中的 **ServiceModelOperation 3.0.0.0、ServiceModelEndpoint 3.0.0.0 或 ServiceModelService 3.0.0.0** 。</span><span class="sxs-lookup"><span data-stu-id="3208b-124">In the **Add Counters** dialog box, select **ServiceModelOperation 3.0.0.0, ServiceModelEndpoint 3.0.0.0, or ServiceModelService 3.0.0.0** in the Performance object drop down list box.</span></span> <span data-ttu-id="3208b-125">从列表中选择要查看的计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-125">Select the counters you want to view from the list.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="3208b-126">如果未在计算机上运行任何 WCF 服务，则不会为服务提供 WCF 性能计数器。</span><span class="sxs-lookup"><span data-stu-id="3208b-126">There are no WCF performance counters for a service if there are no WCF services running on the computer.</span></span>  
  
### <a name="to-use-the-configuration-editor-to-enable-counters"></a><span data-ttu-id="3208b-127">使用配置编辑器来启用计数器</span><span class="sxs-lookup"><span data-stu-id="3208b-127">To use the Configuration Editor to enable counters</span></span>  
  
1. <span data-ttu-id="3208b-128">打开 SvcConfigEditor.exe 的一个实例。</span><span class="sxs-lookup"><span data-stu-id="3208b-128">Open an instance of the SvcConfigEditor.exe.</span></span>  
  
2. <span data-ttu-id="3208b-129">在 "文件" 菜单上，单击 " **打开** "，然后单击 " **配置文件 ...**"。</span><span class="sxs-lookup"><span data-stu-id="3208b-129">On the File menu, click **Open** and then click **Config file…**.</span></span>  
  
3. <span data-ttu-id="3208b-130">导航到示例应用程序的服务文件夹并打开 Web.config 文件。</span><span class="sxs-lookup"><span data-stu-id="3208b-130">Navigate to the sample application's service folder and open the Web.config file.</span></span>  
  
4. <span data-ttu-id="3208b-131">在配置树中单击 " **诊断** "。</span><span class="sxs-lookup"><span data-stu-id="3208b-131">Click **Diagnostics** on the Configuration tree.</span></span>  
  
5. <span data-ttu-id="3208b-132">切换 "**诊断**" 窗口中的 "**性能计数器**" 以显示 "全部"。</span><span class="sxs-lookup"><span data-stu-id="3208b-132">Toggle **Performance Counter** in the **Diagnostics** window to show 'All'.</span></span>  
  
6. <span data-ttu-id="3208b-133">保存该配置文件并退出编辑器。</span><span class="sxs-lookup"><span data-stu-id="3208b-133">Save the configuration file and exit the editor.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="3208b-134">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="3208b-134">The samples may already be installed on your computer.</span></span> <span data-ttu-id="3208b-135">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="3208b-135">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="3208b-136">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3208b-136">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="3208b-137">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="3208b-137">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\PerfCounters`  
  
## <a name="see-also"></a><span data-ttu-id="3208b-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="3208b-138">See also</span></span>

- <span data-ttu-id="3208b-139">[AppFabric 监视示例](/previous-versions/appfabric/ff383407(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="3208b-139">[AppFabric Monitoring Samples](/previous-versions/appfabric/ff383407(v=azure.10))</span></span>
