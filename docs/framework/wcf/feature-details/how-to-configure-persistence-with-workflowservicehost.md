---
description: 了解详细信息：如何：通过 WorkflowServiceHost 配置持久性
title: 如何：使用 WorkflowServiceHost 配置永久性
ms.date: 03/30/2017
ms.assetid: e31cd4df-13a3-4a9a-9be8-5243e0055356
ms.openlocfilehash: 79945fb791cc25bdf362302fa884636942fb5692
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780032"
---
# <a name="how-to-configure-persistence-with-workflowservicehost"></a><span data-ttu-id="755ae-103">如何：使用 WorkflowServiceHost 配置永久性</span><span class="sxs-lookup"><span data-stu-id="755ae-103">How to: Configure Persistence with WorkflowServiceHost</span></span>

<span data-ttu-id="755ae-104">本主题介绍如何使用配置文件配置 SQL 工作流实例存储功能，以便对 <xref:System.ServiceModel.Activities.WorkflowServiceHost> 中承载的工作流启用永久性。</span><span class="sxs-lookup"><span data-stu-id="755ae-104">This topic describes how to configure the SQL Workflow Instance Store feature to enable persistence for workflows hosted in <xref:System.ServiceModel.Activities.WorkflowServiceHost> by using a configuration file.</span></span> <span data-ttu-id="755ae-105">使用 SQL 工作流实例存储功能之前，必须创建用于保存工作流实例的 SQL 数据库。</span><span class="sxs-lookup"><span data-stu-id="755ae-105">Before using the SQL Workflow Instance Store feature you must create a SQL database that is used to persist workflow instances.</span></span> <span data-ttu-id="755ae-106">有关详细信息，请参阅 [如何：为工作流和工作流服务启用 SQL 持久性](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-106">For more information, see [How to: Enable SQL Persistence for Workflows and Workflow Services](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md).</span></span>  
  
### <a name="to-configure-the-sql-workflow-instance-store-in-configuration"></a><span data-ttu-id="755ae-107">在配置中配置 SQL 工作流实例存储</span><span class="sxs-lookup"><span data-stu-id="755ae-107">To Configure the SQL Workflow Instance Store in Configuration</span></span>  
  
1. <span data-ttu-id="755ae-108">可以通过 <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>（一个用于通过 XML 配置更改设置的服务行为）配置 SQL 工作流实例存储的属性。</span><span class="sxs-lookup"><span data-stu-id="755ae-108">The properties of the SQL workflow instance store can be configured through the <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>, a service behavior that allows you to change the settings through XML configuration.</span></span> <span data-ttu-id="755ae-109">下面的配置示例演示如何使用 `sqlWorkflowInstanceStore` 配置文件中的 <> 行为元素来配置 SQL 工作流实例存储区。</span><span class="sxs-lookup"><span data-stu-id="755ae-109">The following configuration example shows how to configure the SQL workflow instance store by using the <`sqlWorkflowInstanceStore`> behavior element in a configuration file.</span></span>  
  
    ```xml  
    <serviceBehaviors>  
        <behavior name="">  
            <sqlWorkflowInstanceStore
                 connectionString="provider=System.Data.SqlClient;Data Source=(local);Initial Catalog=DefaultPersistenceProviderDb;Integrated Security=True;Async=true"  
                 instanceEncodingOption="GZip | None"  
                 instanceCompletionAction="DeleteAll | DeleteNothing"  
                 instanceLockedExceptionAction="NoRetry | SimpleRetry | AggressiveRetry"  
                 hostLockRenewalPeriod="00:00:30"
                 runnableInstancesDetectionPeriod="00:00:05">  
            </sqlWorkflowInstanceStore>  
        </behavior>  
    </serviceBehaviors>  
    ```  
  
     <span data-ttu-id="755ae-110">有关如何配置 SQL 工作流实例存储的详细信息，请参阅 [如何：为工作流和工作流服务启用 SQL 持久性](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-110">For more information about how to configure the SQL workflow instance store, see [How to: Enable SQL Persistence for Workflows and Workflow Services](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md).</span></span> <span data-ttu-id="755ae-111">有关 <> 行为元素的各个设置的详细信息 `sqlWorkflowInstanceStore` ，请参阅 [SQL 工作流实例存储](../../windows-workflow-foundation/sql-workflow-instance-store.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-111">For more information about the individual settings for the <`sqlWorkflowInstanceStore`> behavior element, see [SQL Workflow Instance Store](../../windows-workflow-foundation/sql-workflow-instance-store.md).</span></span> <span data-ttu-id="755ae-112">Windows Server App Fabric 提供其自己的永久性存储。</span><span class="sxs-lookup"><span data-stu-id="755ae-112">Windows Server App Fabric provides its own persistence store.</span></span> <span data-ttu-id="755ae-113">有关详细信息，请参阅 [Windows Server App Fabric 暂留](/previous-versions/appfabric/ee677272(v=azure.10))。</span><span class="sxs-lookup"><span data-stu-id="755ae-113">For more information, see [Windows Server App Fabric Persistence](/previous-versions/appfabric/ee677272(v=azure.10)).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="755ae-114">上面的配置示例使用的是简化配置。</span><span class="sxs-lookup"><span data-stu-id="755ae-114">The preceding configuration example uses simplified configuration.</span></span> <span data-ttu-id="755ae-115">有关详细信息，请参阅 [简化配置](../simplified-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="755ae-115">For more information, see [Simplified Configuration](../simplified-configuration.md)</span></span>  
  
### <a name="to-configure-the-sql-workflow-instance-store-in-code"></a><span data-ttu-id="755ae-116">在代码中配置 SQL 工作流实例存储</span><span class="sxs-lookup"><span data-stu-id="755ae-116">To Configure the SQL Workflow Instance Store in Code</span></span>  
  
1. <span data-ttu-id="755ae-117">可以通过 <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>（一个用于通过代码更改设置的服务行为）配置 SQL 工作流实例存储的属性。</span><span class="sxs-lookup"><span data-stu-id="755ae-117">The properties of the SQL workflow instance store can be configured through the <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>, a service behavior that allows you to change the settings through code.</span></span> <span data-ttu-id="755ae-118">下面的示例演示如何在代码中使用 <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> 行为元素来配置 SQL 工作流实例存储。</span><span class="sxs-lookup"><span data-stu-id="755ae-118">The following example shows how to configure the SQL workflow instance store by using the <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> behavior element in a code</span></span>  
  
    ```csharp  
    host.Description.Behaviors.Add(new SqlWorkflowInstanceStoreBehavior  
    {  
       ConnectionString = "provider=System.Data.SqlClient;Data Source=(local);Initial Catalog=DefaultPersistenceProviderDb;Integrated Security=True;Async=true",  
       InstanceEncodingOption = "GZip | None",  
       InstanceCompletionAction = "DeleteAll | DeleteNothing",  
       InstanceLockedExceptionAction = "NoRetry | SimpleRetry | AggressiveRetry",  
       HostLockRenewalPeriod = new TimeSpan(00, 00, 30),  
       RunnableInstancesDetectionPeriod = new TimeSpan(00, 00, 05)  
    });  
    ```  
  
     <span data-ttu-id="755ae-119">有关如何配置 SQL 工作流实例存储的详细信息，请参阅 [如何：为工作流和工作流服务启用 SQL 持久性](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-119">For more information about how to configure the SQL workflow instance store, see [How to: Enable SQL Persistence for Workflows and Workflow Services](../../windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md).</span></span> <span data-ttu-id="755ae-120">有关行为元素的各个设置的详细信息 <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> ，请参阅 [SQL 工作流实例存储](../../windows-workflow-foundation/sql-workflow-instance-store.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-120">For more information about the individual settings for the <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> behavior element, see [SQL Workflow Instance Store](../../windows-workflow-foundation/sql-workflow-instance-store.md).</span></span> <span data-ttu-id="755ae-121">Windows Server App Fabric 提供其自己的永久性存储。</span><span class="sxs-lookup"><span data-stu-id="755ae-121">Windows Server App Fabric provides its own persistence store.</span></span> <span data-ttu-id="755ae-122">有关详细信息，请参阅 [Windows Server App Fabric 暂留](/previous-versions/appfabric/ee677272(v=azure.10))。</span><span class="sxs-lookup"><span data-stu-id="755ae-122">For more information, see [Windows Server App Fabric Persistence](/previous-versions/appfabric/ee677272(v=azure.10)).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="755ae-123">上面的配置示例使用的是简化配置。</span><span class="sxs-lookup"><span data-stu-id="755ae-123">The preceding configuration example uses simplified configuration.</span></span> <span data-ttu-id="755ae-124">有关详细信息，请参阅 [简化配置](../simplified-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="755ae-124">For more information, see [Simplified Configuration](../simplified-configuration.md)</span></span>  
  
     <span data-ttu-id="755ae-125">有关如何以编程方式配置持久性的示例，请参阅 [如何：为工作流和工作流服务启用持久性](../../windows-workflow-foundation/how-to-enable-persistence-for-workflows-and-workflow-services.md)。</span><span class="sxs-lookup"><span data-stu-id="755ae-125">For an example of how to configure persistence programmatically see [How to: Enable Persistence for Workflows and Workflow Services](../../windows-workflow-foundation/how-to-enable-persistence-for-workflows-and-workflow-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="755ae-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="755ae-126">See also</span></span>

- [<span data-ttu-id="755ae-127">工作流服务</span><span class="sxs-lookup"><span data-stu-id="755ae-127">Workflow Services</span></span>](workflow-services.md)
- [<span data-ttu-id="755ae-128">工作流持久性</span><span class="sxs-lookup"><span data-stu-id="755ae-128">Workflow Persistence</span></span>](../../windows-workflow-foundation/workflow-persistence.md)
- <span data-ttu-id="755ae-129">[Windows Server App Fabric 持久性](/previous-versions/appfabric/ee677272(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="755ae-129">[Windows Server App Fabric Persistence](/previous-versions/appfabric/ee677272(v=azure.10))</span></span>
