---
description: 了解详细信息：配置通道工厂
title: 配置通道工厂
ms.date: 03/30/2017
ms.assetid: 3b749493-bd8a-4ccb-893e-5948901a1486
ms.openlocfilehash: 7868f9b9e3a97a67ac513668be09de4d9c5073bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778407"
---
# <a name="configuration-channel-factory"></a><span data-ttu-id="711c2-103">配置通道工厂</span><span class="sxs-lookup"><span data-stu-id="711c2-103">Configuration Channel Factory</span></span>

<span data-ttu-id="711c2-104">此示例介绍 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> 的用法。</span><span class="sxs-lookup"><span data-stu-id="711c2-104">This sample covers the usage of the <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>.</span></span> <span data-ttu-id="711c2-105"><xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>允许对 WCF 客户端配置进行集中管理。</span><span class="sxs-lookup"><span data-stu-id="711c2-105">The <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> allows central management of WCF client configuration.</span></span> <span data-ttu-id="711c2-106">这可能在应用程序域加载时间之后选择或更改配置的方案中也非常有用。</span><span class="sxs-lookup"><span data-stu-id="711c2-106">This can also be useful in scenarios in which configuration is selected or changed after the application domain load time.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="711c2-107">演示</span><span class="sxs-lookup"><span data-stu-id="711c2-107">Demonstrates</span></span>

 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601>

## <a name="discussion"></a><span data-ttu-id="711c2-108">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="711c2-108">Discussion</span></span>

 <span data-ttu-id="711c2-109">此示例演示如何使用 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> 将特定配置文件添加到客户端应用程序，而不必使用默认的应用程序文件。</span><span class="sxs-lookup"><span data-stu-id="711c2-109">This sample shows how to use <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> to add a particular configuration file to a client application, without having to use the default application configuration file.</span></span>

 <span data-ttu-id="711c2-110">此示例由两个项目组成。</span><span class="sxs-lookup"><span data-stu-id="711c2-110">The sample consists of two projects.</span></span> <span data-ttu-id="711c2-111">第一个项目是一个简单服务，运行该服务可答复来自客户端的消息。</span><span class="sxs-lookup"><span data-stu-id="711c2-111">The first project is a simple service that runs to reply to messages coming from the clients.</span></span> <span data-ttu-id="711c2-112">第二个项目是一个客户端应用程序，它使用 <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> 为 Test.config 配置文件生成两个 <xref:System.Configuration.ExeConfigurationFileMap> 对象，然后使用这两个对象与服务通信。</span><span class="sxs-lookup"><span data-stu-id="711c2-112">The second project is a client application that builds two <xref:System.ServiceModel.Configuration.ConfigurationChannelFactory%601> objects using a <xref:System.Configuration.ExeConfigurationFileMap> for the Test.config configuration file and uses them to communicate with the service.</span></span> <span data-ttu-id="711c2-113">两个客户端都使用 Test.config 中指定的配置与服务通信。</span><span class="sxs-lookup"><span data-stu-id="711c2-113">Both clients communicate with the service using the configuration specified in Test.config.</span></span>

 <span data-ttu-id="711c2-114">以下代码可将自定义配置文件添加到客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="711c2-114">The following code adds a custom configuration file to a client application.</span></span>

```csharp
ExeConfigurationFileMap fileMap = new ExeConfigurationFileMap();
fileMap.ExeConfigFilename = "Test.config";
Configuration newConfiguration = ConfigurationManager.OpenMappedExeConfiguration(fileMap, ConfigurationUserLevel.None);

ConfigurationChannelFactory<ICalculatorChannel> factory1 = new ConfigurationChannelFactory<ICalculatorChannel>("endpoint1", newConfiguration, new EndpointAddress("http://localhost:8000/servicemodelsamples/service"));
ICalculatorChannel client1 = factory1.CreateChannel();
```

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="711c2-115">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="711c2-115">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="711c2-116">以管理员权限打开 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="711c2-116">Open Visual Studio 2012 with administrator privileges.</span></span>

2. <span data-ttu-id="711c2-117">右键单击 ConfigurationChannelFactory 解决方案 (2 个项目) 然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="711c2-117">Right-click the ConfigurationChannelFactory solution (2 projects) and then select **Properties**.</span></span>

3. <span data-ttu-id="711c2-118">在 " **通用属性**" 中，选择 " **启动项目**"，然后单击 " **多个启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="711c2-118">In **Common Properties**, select **Startup Project**, and then click **Multiple startup projects**.</span></span>

4. <span data-ttu-id="711c2-119">将 **服务** 项目移动到列表的开头，**操作为 "start"**，然后将该 **客户端** 项目与 "**启动" 操作** 一起移动到 **服务** 项目之后，以便在 **服务** 项目后执行 **客户端** 项目。</span><span class="sxs-lookup"><span data-stu-id="711c2-119">Move the **Service** project to the beginning of the list, with the **Action ‘Start’**, and then move the **Client** project after the **Service** project, also with the **Action ‘Start’**, so the **Client** project is executed after the **Service** project.</span></span>

5. <span data-ttu-id="711c2-120">单击 **"确定"**，然后按 F5 (或 CTRL + F5) 运行该示例。</span><span class="sxs-lookup"><span data-stu-id="711c2-120">Click **OK**, and then press F5 (or CTRL+F5) to run the sample.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="711c2-121">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="711c2-121">The samples may already be installed on your machine.</span></span> <span data-ttu-id="711c2-122">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="711c2-122">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="711c2-123">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="711c2-123">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="711c2-124">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="711c2-124">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\ConfigurationChannelFactory`
