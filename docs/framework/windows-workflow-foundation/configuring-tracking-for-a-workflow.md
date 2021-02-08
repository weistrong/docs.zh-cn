---
description: 了解详细信息：为工作流配置跟踪
title: 为工作流配置跟踪
ms.date: 03/30/2017
ms.assetid: 905adcc9-30a0-4918-acd6-563f86db988a
ms.openlocfilehash: 061a0edf107296e04d86ed1a50b9a8bfefd7bfce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792760"
---
# <a name="configuring-tracking-for-a-workflow"></a><span data-ttu-id="81829-103">为工作流配置跟踪</span><span class="sxs-lookup"><span data-stu-id="81829-103">Configuring Tracking for a Workflow</span></span>

<span data-ttu-id="81829-104">工作流可以按以下三种方法执行：</span><span class="sxs-lookup"><span data-stu-id="81829-104">A workflow can execute in three ways:</span></span>

- <span data-ttu-id="81829-105">在 <xref:System.ServiceModel.Activities.WorkflowServiceHost></span><span class="sxs-lookup"><span data-stu-id="81829-105">Hosted in <xref:System.ServiceModel.Activities.WorkflowServiceHost></span></span>

- <span data-ttu-id="81829-106">作为 <xref:System.Activities.WorkflowApplication> 执行</span><span class="sxs-lookup"><span data-stu-id="81829-106">Executed as a <xref:System.Activities.WorkflowApplication></span></span>

- <span data-ttu-id="81829-107">使用 <xref:System.Activities.WorkflowInvoker> 直接执行</span><span class="sxs-lookup"><span data-stu-id="81829-107">Executed directly using <xref:System.Activities.WorkflowInvoker></span></span>

<span data-ttu-id="81829-108">根据工作流承载选项的不同，可以通过代码或配置文件添加跟踪参与者。</span><span class="sxs-lookup"><span data-stu-id="81829-108">Depending on the workflow hosting option, a tracking participant can be added either through code or through a configuration file.</span></span> <span data-ttu-id="81829-109">本主题介绍如何通过向 <xref:System.Activities.WorkflowApplication> 和 <xref:System.ServiceModel.Activities.WorkflowServiceHost> 添加跟踪参与者来配置跟踪，并介绍在使用 <xref:System.Activities.WorkflowInvoker> 时如何启用跟踪。</span><span class="sxs-lookup"><span data-stu-id="81829-109">This topic describes how tracking is configured by adding a tracking participant to a <xref:System.Activities.WorkflowApplication> and to a <xref:System.ServiceModel.Activities.WorkflowServiceHost>, and how to enable tracking when using <xref:System.Activities.WorkflowInvoker>.</span></span>

## <a name="configuring-workflow-application-tracking"></a><span data-ttu-id="81829-110">配置工作流应用程序跟踪</span><span class="sxs-lookup"><span data-stu-id="81829-110">Configuring Workflow Application Tracking</span></span>

<span data-ttu-id="81829-111">工作流可以使用 <xref:System.Activities.WorkflowApplication> 类运行。</span><span class="sxs-lookup"><span data-stu-id="81829-111">A workflow can run using the <xref:System.Activities.WorkflowApplication> class.</span></span> <span data-ttu-id="81829-112">本主题演示如何通过向 [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] 工作流宿主添加跟踪参与者为 <xref:System.Activities.WorkflowApplication>工作流应用程序配置跟踪。</span><span class="sxs-lookup"><span data-stu-id="81829-112">This topic demonstrates how tracking is configured for a [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] workflow application by adding a tracking participant to the <xref:System.Activities.WorkflowApplication> workflow host.</span></span> <span data-ttu-id="81829-113">在这种情况下，工作流作为工作流应用程序运行。</span><span class="sxs-lookup"><span data-stu-id="81829-113">In this case, the workflow runs as a workflow application.</span></span> <span data-ttu-id="81829-114">通过代码（而不是通过配置文件）配置一个工作流应用程序，该工作流应用程序是一个使用 <xref:System.Activities.WorkflowApplication> 类的自承载的 .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="81829-114">You configure a workflow application through code (rather than by using a configuration file), which is a self-hosted .exe file using the <xref:System.Activities.WorkflowApplication> class.</span></span> <span data-ttu-id="81829-115">跟踪参与者将作为 <xref:System.Activities.WorkflowApplication> 实例的扩展添加。</span><span class="sxs-lookup"><span data-stu-id="81829-115">The tracking participant is added as an extension to the <xref:System.Activities.WorkflowApplication> instance.</span></span> <span data-ttu-id="81829-116">这是通过向 WorkflowApplication 实例的扩展集合添加 <xref:System.Activities.Tracking.TrackingParticipant> 来完成的。</span><span class="sxs-lookup"><span data-stu-id="81829-116">This is done by adding the <xref:System.Activities.Tracking.TrackingParticipant> to the extensions collection for the WorkflowApplication instance.</span></span>

<span data-ttu-id="81829-117">对于工作流应用程序，您可以添加 <xref:System.Activities.Tracking.EtwTrackingParticipant> 行为扩展，如以下代码所示。</span><span class="sxs-lookup"><span data-stu-id="81829-117">For a workflow application, you can add the <xref:System.Activities.Tracking.EtwTrackingParticipant> behavior extension as shown in the following code.</span></span>

```csharp
LogActivity activity = new LogActivity();

WorkflowApplication instance = new WorkflowApplication(activity);
EtwTrackingParticipant trackingParticipant =
    new EtwTrackingParticipant
{

        TrackingProfile = new TrackingProfile
           {
               Name = "SampleTrackingProfile",
               ActivityDefinitionId = "ProcessOrder",
               Queries = new WorkflowInstanceQuery
               {
                  States = { "*" }
              }
          }
       };
instance.Extensions.Add(trackingParticipant);
```

### <a name="configuring-workflow-service-tracking"></a><span data-ttu-id="81829-118">配置工作流服务跟踪</span><span class="sxs-lookup"><span data-stu-id="81829-118">Configuring Workflow Service Tracking</span></span>

<span data-ttu-id="81829-119">在服务主机中承载工作流时，该工作流可以作为 WCF 服务公开 <xref:System.ServiceModel.Activities.WorkflowServiceHost> 。</span><span class="sxs-lookup"><span data-stu-id="81829-119">A workflow can be exposed as a WCF service when hosted in the <xref:System.ServiceModel.Activities.WorkflowServiceHost> service host.</span></span> <span data-ttu-id="81829-120"><xref:System.ServiceModel.Activities.WorkflowServiceHost> 是基于工作流的服务的指定 .NET ServiceHost 实现。</span><span class="sxs-lookup"><span data-stu-id="81829-120"><xref:System.ServiceModel.Activities.WorkflowServiceHost> is a specialized .NET ServiceHost implementation for a workflow-based service.</span></span> <span data-ttu-id="81829-121">本节介绍如何为在 [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] 中运行的 <xref:System.ServiceModel.Activities.WorkflowServiceHost> 工作流服务配置跟踪。</span><span class="sxs-lookup"><span data-stu-id="81829-121">This section explains how to configure tracking for a [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] workflow service running in <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span></span> <span data-ttu-id="81829-122">通过在 Web.config 文件（对于 Web 承载的服务）或 App.config 文件（对于在独立的应用程序中承载的服务，例如在控制台应用程序中承载的服务）中指定服务行为，或通过使用代码向服务宿主的 <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> 集合中添加与跟踪相关的行为，可以完成上述配置。</span><span class="sxs-lookup"><span data-stu-id="81829-122">It is configured through a Web.config file (for a Web-hosted service) or an App.config file (for a service hosted in a stand-alone application, such as a console application) by specifying a service behavior or through code by adding a tracking-specific behavior to the <xref:System.ServiceModel.Description.ServiceDescription.Behaviors%2A> collection for the service host.</span></span>

<span data-ttu-id="81829-123">对于中承载的工作流服务 <xref:System.ServiceModel.WorkflowServiceHost> ，可以 <xref:System.Activities.Tracking.EtwTrackingParticipant> 使用 `behavior` 配置文件中的 <> 元素添加，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="81829-123">For a workflow service hosted in <xref:System.ServiceModel.WorkflowServiceHost>, you can add the <xref:System.Activities.Tracking.EtwTrackingParticipant> using the <`behavior`> element in a configuration file, as shown in the following example.</span></span>

```xml
<behaviors>
   <serviceBehaviors>
        <behavior>
          <etwTracking profileName="Sample Tracking Profile" />
        </behavior>
   </serviceBehaviors>
</behaviors>
```

<span data-ttu-id="81829-124">此外，对于 <xref:System.ServiceModel.WorkflowServiceHost> 中承载的工作流服务，你可以通过代码添加 <xref:System.Activities.Tracking.EtwTrackingParticipant> 行为扩展。</span><span class="sxs-lookup"><span data-stu-id="81829-124">Alternatively, for a workflow service hosted in <xref:System.ServiceModel.WorkflowServiceHost>, you can add the <xref:System.Activities.Tracking.EtwTrackingParticipant> behavior extension through code.</span></span> <span data-ttu-id="81829-125">若要添加自定义跟踪参与者，请创建一个新的行为扩展并将其添加到 <xref:System.ServiceModel.ServiceHost> 中，如以下代码示例中所示。</span><span class="sxs-lookup"><span data-stu-id="81829-125">To add a custom tracking participant, create a new behavior extension and add it to the <xref:System.ServiceModel.ServiceHost> as shown in the following example code.</span></span>

> [!NOTE]
> <span data-ttu-id="81829-126">若要查看演示如何创建添加自定义跟踪参与者的自定义行为元素的示例代码，请参阅 [跟踪](./samples/tracking.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="81829-126">If you want to view sample code that shows how to create a custom behavior element that adds a custom tracking participant, refer to the [Tracking](./samples/tracking.md) samples.</span></span>

```csharp
ServiceHost svcHost = new ServiceHost(typeof(WorkflowService), new
                                 Uri("http://localhost:8001/Sample"));
EtwTrackingBehavior trackingBehavior =
    new EtwTrackingBehavior
    {
        ProfileName = "Sample Tracking Profile"
    };
svcHost.Description.Behaviors.Add(trackingBehavior);
svcHost.Open();
```

<span data-ttu-id="81829-127">跟踪参与者将作为行为的扩展添加到工作流服务主机中。</span><span class="sxs-lookup"><span data-stu-id="81829-127">The tracking participant is added to the workflow service host as an extension to the behavior.</span></span>

<span data-ttu-id="81829-128">下面的这个代码示例演示如何从配置文件读取跟踪配置文件。</span><span class="sxs-lookup"><span data-stu-id="81829-128">This sample code below shows how to read a tracking profile from configuration file.</span></span>

```csharp
TrackingProfile GetProfile(string profileName, string displayName)
        {
            TrackingProfile trackingProfile = null;
            TrackingSection trackingSection = (TrackingSection)WebConfigurationManager.GetSection("system.serviceModel/tracking");
            if (trackingSection == null)
            {
                return null;
            }

            profileName ??= "";

            //Find the profile with the specified profile name in the list of profile found in config
            var match = from p in new List<TrackingProfile>(trackingSection.TrackingProfiles)
                        where (p.Name == profileName) && ((p.ActivityDefinitionId == displayName) || (p.ActivityDefinitionId == "*"))
                        select p;

            if (match.Count() == 0)
            {
                //return an empty profile
                trackingProfile = new TrackingProfile()
                {
                    ActivityDefinitionId = displayName
                };

            }
            else
            {
                trackingProfile = match.First();
            }

            return trackingProfile;
```

<span data-ttu-id="81829-129">此代码示例演示如何向工作流主机添加跟踪配置文件。</span><span class="sxs-lookup"><span data-stu-id="81829-129">This sample code shows how to add a tracking profile to a workflow host.</span></span>

```csharp
WorkflowServiceHost workflowServiceHost = serviceHostBase as WorkflowServiceHost;
if (null != workflowServiceHost)
{
    string workflowDisplayName = workflowServiceHost.Activity.DisplayName;
    TrackingProfile trackingProfile = GetProfile(this.profileName, workflowDisplayName);
    workflowServiceHost.WorkflowExtensions.Add(()  => new EtwTrackingParticipant {
        TrackingProfile = trackingProfile
    });
 }
```

> [!NOTE]
> <span data-ttu-id="81829-130">有关跟踪配置文件的详细信息，请参阅 [跟踪配置文件](tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="81829-130">For more information on tracking profiles, refer to [Tracking Profiles](tracking-profiles.md).</span></span>

### <a name="configuring-tracking-using-workflowinvoker"></a><span data-ttu-id="81829-131">配置使用 WorkflowInvoker 的跟踪</span><span class="sxs-lookup"><span data-stu-id="81829-131">Configuring tracking using WorkflowInvoker</span></span>

<span data-ttu-id="81829-132">若要对使用 <xref:System.Activities.WorkflowInvoker> 执行的工作流配置跟踪，请添加跟踪提供程序作为 <xref:System.Activities.WorkflowInvoker> 实例的扩展。</span><span class="sxs-lookup"><span data-stu-id="81829-132">To configure tracking for a workflow executed using <xref:System.Activities.WorkflowInvoker>, add the tracking provider as an extension to a <xref:System.Activities.WorkflowInvoker> instance.</span></span> <span data-ttu-id="81829-133">下面的代码示例来自 [自定义跟踪](./samples/custom-tracking.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="81829-133">The following code example is from the [Custom Tracking](./samples/custom-tracking.md) sample.</span></span>

```csharp
WorkflowInvoker invoker = new WorkflowInvoker(BuildSampleWorkflow());
invoker.Extensions.Add(customTrackingParticipant);
invoker.Invoke();
```

### <a name="viewing-tracking-records-in-event-viewer"></a><span data-ttu-id="81829-134">在事件查看器中查看跟踪记录</span><span class="sxs-lookup"><span data-stu-id="81829-134">Viewing tracking records in Event Viewer</span></span>

<span data-ttu-id="81829-135">在跟踪 WF 执行时有两种特殊的事件查看器日志可供查看 - 分析日志和调试日志。</span><span class="sxs-lookup"><span data-stu-id="81829-135">There are two Event Viewer logs of particular interest to view when tracking WF execution - the Analytic log and the Debug log.</span></span> <span data-ttu-id="81829-136">两者都驻留在 Microsoft&#124;Windows&#124;应用程序 Server-Applications 节点下。</span><span class="sxs-lookup"><span data-stu-id="81829-136">Both reside under the Microsoft&#124;Windows&#124;Application Server-Applications node.</span></span> <span data-ttu-id="81829-137">此部分内的日志包含来自单一应用程序的事件，而不包含对整个系统范围产生影响的事件。</span><span class="sxs-lookup"><span data-stu-id="81829-137">Logs within this section contain events from a single application rather than events that have an impact on the entire system.</span></span>

<span data-ttu-id="81829-138">调试跟踪事件将写入调试日志。</span><span class="sxs-lookup"><span data-stu-id="81829-138">Debug trace events are written to the Debug Log.</span></span> <span data-ttu-id="81829-139">若要收集事件查看器中的 WF 调试跟踪事件，请启用调试日志。</span><span class="sxs-lookup"><span data-stu-id="81829-139">To collect WF debug trace events in the Event Viewer, enable the Debug Log.</span></span>

1. <span data-ttu-id="81829-140">若要打开事件查看器，请单击 " **开始**"，然后单击 " **运行"。**</span><span class="sxs-lookup"><span data-stu-id="81829-140">To open Event Viewer, click **Start**, and then click **Run.**</span></span> <span data-ttu-id="81829-141">在 "运行" 对话框中，键入 `eventvwr` 。</span><span class="sxs-lookup"><span data-stu-id="81829-141">In the Run dialog, type `eventvwr`.</span></span>

2. <span data-ttu-id="81829-142">在 "事件查看器" 对话框中，展开 " **应用程序和服务日志** " 节点。</span><span class="sxs-lookup"><span data-stu-id="81829-142">In the Event Viewer dialog, expand the **Applications and Services Logs** node.</span></span>

3. <span data-ttu-id="81829-143">展开 " **Microsoft**"、" **Windows**" 和 " **应用程序服务器** " 节点。</span><span class="sxs-lookup"><span data-stu-id="81829-143">Expand the **Microsoft**, **Windows**, and **Application Server-Applications** nodes.</span></span>

4. <span data-ttu-id="81829-144">右键单击 "**应用程序服务器-应用程序**" 节点下的 "**调试**" 节点，然后选择 "**启用日志**"。</span><span class="sxs-lookup"><span data-stu-id="81829-144">Right-click the **Debug** node under the **Application Server-Applications** node, and select **Enable Log**.</span></span>

5. <span data-ttu-id="81829-145">执行启用跟踪的应用程序以生成跟踪事件。</span><span class="sxs-lookup"><span data-stu-id="81829-145">Execute your tracing-enabled application to generate tracing events.</span></span>

6. <span data-ttu-id="81829-146">右键单击 " **调试** " 节点，然后选择 " **刷新"。**</span><span class="sxs-lookup"><span data-stu-id="81829-146">Right-click the **Debug** node and select **Refresh.**</span></span> <span data-ttu-id="81829-147">跟踪事件应显示在中心窗格中。</span><span class="sxs-lookup"><span data-stu-id="81829-147">Tracing events should be visible in the center pane.</span></span>

<span data-ttu-id="81829-148">WF 4 提供跟踪参与者，可将跟踪记录写入 ETW（Windows 事件跟踪）会话。</span><span class="sxs-lookup"><span data-stu-id="81829-148">WF 4 provides a tracking participant that writes tracking records to an ETW (Event Tracing for Windows) session.</span></span> <span data-ttu-id="81829-149">ETW 跟踪参与者通过跟踪配置文件配置为订阅跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="81829-149">The ETW tracking participant is configured with a tracking profile to subscribe to tracking records.</span></span> <span data-ttu-id="81829-150">当启用跟踪时，向 ETW 发出错误跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="81829-150">When tracking is enabled, errors tracking records are emitted to ETW.</span></span> <span data-ttu-id="81829-151">与 ETW 跟踪参与者发出的跟踪事件相对应的 ETW 跟踪事件（范围介于 100 到 113 之间）将写入分析日志。 </span><span class="sxs-lookup"><span data-stu-id="81829-151">ETW tracking events (between the range of 100-113) corresponding to the tracking events emitted by the ETW tracking participant are written to the Analytic Log.</span></span>

<span data-ttu-id="81829-152">若要查看跟踪记录，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="81829-152">To view tracking records, follow these steps.</span></span>

1. <span data-ttu-id="81829-153">若要打开事件查看器，请单击 " **开始**"，然后单击 " **运行"。**</span><span class="sxs-lookup"><span data-stu-id="81829-153">To open Event Viewer, click **Start**, and then click **Run.**</span></span> <span data-ttu-id="81829-154">在 "运行" 对话框中，键入 `eventvwr` 。</span><span class="sxs-lookup"><span data-stu-id="81829-154">In the Run dialog, type `eventvwr`.</span></span>

2. <span data-ttu-id="81829-155">在 "事件查看器" 对话框中，展开 " **应用程序和服务日志** " 节点。</span><span class="sxs-lookup"><span data-stu-id="81829-155">In the Event Viewer dialog, expand the **Applications and Services Logs** node.</span></span>

3. <span data-ttu-id="81829-156">展开 " **Microsoft**"、" **Windows**" 和 " **应用程序服务器** " 节点。</span><span class="sxs-lookup"><span data-stu-id="81829-156">Expand the **Microsoft**, **Windows**, and **Application Server-Applications** nodes.</span></span>

4. <span data-ttu-id="81829-157">右键单击 "**应用程序服务器-应用程序**" 节点下的 "**分析**" 节点，然后选择 "**启用日志**"。</span><span class="sxs-lookup"><span data-stu-id="81829-157">Right-click the **Analytic** node under the **Application Server-Applications** node, and select **Enable Log**.</span></span>

5. <span data-ttu-id="81829-158">执行启用跟踪的应用程序以生成跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="81829-158">Execute your tracking-enabled application to generate tracking records.</span></span>

6. <span data-ttu-id="81829-159">右键单击 " **分析** " 节点，然后选择 " **刷新"。**</span><span class="sxs-lookup"><span data-stu-id="81829-159">Right-click the **Analytic** node and select **Refresh.**</span></span> <span data-ttu-id="81829-160">跟踪记录应会显示在中心窗格中。</span><span class="sxs-lookup"><span data-stu-id="81829-160">Tracking records should be visible in the center pane.</span></span>

<span data-ttu-id="81829-161">下图显示了事件查看器中的跟踪事件：</span><span class="sxs-lookup"><span data-stu-id="81829-161">The following image shows tracking events in the event viewer:</span></span>

![显示跟踪记录的事件查看器屏幕截图。](./media/configuring-tracking-for-a-workflow/tracking-event-viewer.png)

### <a name="registering-an-application-specific-provider-id"></a><span data-ttu-id="81829-163">注册应用程序特定的提供程序 ID</span><span class="sxs-lookup"><span data-stu-id="81829-163">Registering an application-specific provider ID</span></span>

<span data-ttu-id="81829-164">如果需要将事件写入到特定的应用程序日志中，请按照以下步骤注册新的提供程序清单。</span><span class="sxs-lookup"><span data-stu-id="81829-164">If events need to be written to a specific application log, follow these steps to register the new provider manifest.</span></span>

1. <span data-ttu-id="81829-165">在应用程序配置文件中声明提供程序 ID。</span><span class="sxs-lookup"><span data-stu-id="81829-165">Declare the provider ID in the application configuration file.</span></span>

    ```xml
    <system.serviceModel>
        <diagnostics etwProviderId="2720e974-9fe9-477a-bb60-81fe3bf91eec"/>
    </system.serviceModel>
    ```

2. <span data-ttu-id="81829-166">将清单文件从%windir%\Microsoft.NET\Framework \\ \<latest version of [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)]> \microsoft.windows.applicationserver.applications.man 复制复制到临时位置，并将其重命名为 Microsoft.Windows.ApplicationServer.Applications_Provider1。</span><span class="sxs-lookup"><span data-stu-id="81829-166">Copy the manifest file from %windir%\Microsoft.NET\Framework\\\<latest version of [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)]>\Microsoft.Windows.ApplicationServer.Applications.man to a temporary location, and rename it to Microsoft.Windows.ApplicationServer.Applications_Provider1.man</span></span>

3. <span data-ttu-id="81829-167">将清单文件中的 GUID 更改为新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="81829-167">Change the GUID in the manifest file to the new GUID.</span></span>

    ```xml
    <provider name="Microsoft-Windows-Application Server-Applications" guid="{2720e974-9fe9-477a-bb60-81fe3bf91eec}" />
    ```

4. <span data-ttu-id="81829-168">如果您不想卸载默认提供程序，请更改提供程序名称。</span><span class="sxs-lookup"><span data-stu-id="81829-168">Change the provider name if you do not want to uninstall the default provider.</span></span>

    ```xml
    <provider name="Microsoft-Windows-Application Server-Applications" guid="{2720e974-9fe9-477a-bb60-81fe3bf91eec}" />
    ```

5. <span data-ttu-id="81829-169">如果您在第一步中更改了提供程序名称，请将清单文件中的通道名称更改为新的提供程序名称。</span><span class="sxs-lookup"><span data-stu-id="81829-169">If you changed the provider name in the previous step, change the channel names in the manifest file to the new provider name.</span></span>

    ```xml
    <channel name="Microsoft-Windows-Application Server-Applications_Provider1/Admin" chid="ADMIN_CHANNEL" symbol="ADMIN_CHANNEL" type="Admin" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.ADMIN_CHANNEL.message)" />
    <channel name="Microsoft-Windows-Application Server-Applications_Provider1/Operational" chid="OPERATIONAL_CHANNEL" symbol="OPERATIONAL_CHANNEL" type="Operational" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.OPERATIONAL_CHANNEL.message)" />
    <channel name="Microsoft-Windows-Application Server-Applications_Provider1/Analytic" chid="ANALYTIC_CHANNEL" symbol="ANALYTIC_CHANNEL" type="Analytic" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.ANALYTIC_CHANNEL.message)" />
    <channel name="Microsoft-Windows-Application Server-Applications_Provider1/Debug" chid="DEBUG_CHANNEL" symbol="DEBUG_CHANNEL" type="Debug" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.DEBUG_CHANNEL.message)" />
    <channel name="Microsoft-Windows-Application Server-Applications_Provider1/Perf" chid="PERF_CHANNEL" symbol="PERF_CHANNEL" type="Analytic" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.PERF_CHANNEL.message)" />
    ```

6. <span data-ttu-id="81829-170">按照以下这些步骤生成资源 DLL。</span><span class="sxs-lookup"><span data-stu-id="81829-170">Generate the resource DLL by following these steps.</span></span>

    1. <span data-ttu-id="81829-171">安装 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="81829-171">Install the Windows SDK.</span></span> <span data-ttu-id="81829-172">Windows SDK 包括消息编译器 ([mc.exe](/windows/win32/wes/message-compiler--mc-exe-)) 和资源[编译器 (rc.exe) 。](/windows/win32/menurc/using-rc-the-rc-command-line-)</span><span class="sxs-lookup"><span data-stu-id="81829-172">The Windows SDK includes the message compiler ([mc.exe](/windows/win32/wes/message-compiler--mc-exe-)) and resource compiler ([rc.exe](/windows/win32/menurc/using-rc-the-rc-command-line-)).</span></span>

    2. <span data-ttu-id="81829-173">在 Windows SDK 命令提示中，对新清单文件运行 mc.exe。</span><span class="sxs-lookup"><span data-stu-id="81829-173">In a Windows SDK command prompt, run mc.exe on the new manifest file.</span></span>

        ```console
        mc.exe Microsoft.Windows.ApplicationServer.Applications_Provider1.man
        ```

    3. <span data-ttu-id="81829-174">对在上一步中生成的资源文件运行 rc.exe。</span><span class="sxs-lookup"><span data-stu-id="81829-174">Run rc.exe on the resource file generated in the previous step.</span></span>

        ```console
        rc.exe  Microsoft.Windows.ApplicationServer.Applications_Provider1.rc
        ```

    4. <span data-ttu-id="81829-175">创建一个名为 NewProviderReg.cs 的空 cs 文件。</span><span class="sxs-lookup"><span data-stu-id="81829-175">Create an empty cs file called NewProviderReg.cs.</span></span>

    5. <span data-ttu-id="81829-176">使用 C# 编译器创建一个资源 DLL。</span><span class="sxs-lookup"><span data-stu-id="81829-176">Create a resource DLL using the C# compiler.</span></span>

        ```console
        csc /target:library /win32res:Microsoft.Windows.ApplicationServer.Applications_Provider1.res NewProviderReg.cs /out:Microsoft.Windows.ApplicationServer.Applications_Provider1.dll
        ```

    6. <span data-ttu-id="81829-177">将清单文件中的资源和消息 dll 名称从更改 `Microsoft.Windows.ApplicationServer.Applications.Provider1.man` 为新的 dll 名称。</span><span class="sxs-lookup"><span data-stu-id="81829-177">Change the resource and message dll name in the manifest file from `Microsoft.Windows.ApplicationServer.Applications.Provider1.man` to the new dll name.</span></span>

        ```xml
        <provider name="Microsoft-Windows-Application Server-Applications_Provider1" guid="{2720e974-9fe9-477a-bb60-81fe3bf91eec}" symbol="Microsoft_Windows_ApplicationServer_ApplicationEvents" resourceFileName="<dll directory>\Microsoft.Windows.ApplicationServer.Applications_Provider1.dll" messageFileName="<dll directory>\Microsoft.Windows.ApplicationServer.Applications_Provider1.dll" />
        ```

    7. <span data-ttu-id="81829-178">使用 [wevtutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732848(v=ws.10)) 注册清单。</span><span class="sxs-lookup"><span data-stu-id="81829-178">Use [wevtutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732848(v=ws.10)) to register the manifest.</span></span>

        ```console
        wevtutil im Microsoft.Windows.ApplicationServer.Applications_Provider1.man
        ```

## <a name="see-also"></a><span data-ttu-id="81829-179">请参阅</span><span class="sxs-lookup"><span data-stu-id="81829-179">See also</span></span>

- <span data-ttu-id="81829-180">[Windows Server App Fabric 监视](/previous-versions/appfabric/ee677251(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="81829-180">[Windows Server App Fabric Monitoring](/previous-versions/appfabric/ee677251(v=azure.10))</span></span>
- <span data-ttu-id="81829-181">[用 App Fabric 监视应用程序](/previous-versions/appfabric/ee677276(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="81829-181">[Monitoring Applications with App Fabric](/previous-versions/appfabric/ee677276(v=azure.10))</span></span>
