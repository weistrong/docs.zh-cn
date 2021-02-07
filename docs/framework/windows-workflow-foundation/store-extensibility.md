---
description: 了解有关以下内容的详细信息：存储扩展性
title: 存储扩展性
ms.date: 03/30/2017
ms.assetid: 7c3f4a46-4bac-4138-ae6a-a7c7ee0d28f5
ms.openlocfilehash: f04c466224aacd1c8f755e7aa60b18846d0c7180
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755221"
---
# <a name="store-extensibility"></a><span data-ttu-id="6c6b7-103">存储扩展性</span><span class="sxs-lookup"><span data-stu-id="6c6b7-103">Store Extensibility</span></span>

<span data-ttu-id="6c6b7-104"><xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> 允许用户提升自定义的特定于应用程序的属性，这些属性可用于查询持久性数据库中的实例。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-104"><xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> allows users to promote custom, application-specific properties that can be used to query for instances in the persistence database.</span></span> <span data-ttu-id="6c6b7-105">提升属性的操作将使属性值可用在数据库的特殊视图中。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-105">The act of promoting a property causes the value to be available within a special view in the database.</span></span> <span data-ttu-id="6c6b7-106">这些提升的属性（可用于用户查询的属性）可以是简单的类型，如 Int64、Guid、String 和 DateTime，也可以是序列化的二进制类型 (byte[])。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-106">These promoted properties (properties that can be used in user queries) can be of simple types such as Int64, Guid, String, and DateTime or of a serialized binary type (byte[]).</span></span>

<span data-ttu-id="6c6b7-107"><xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> 类具有 <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore.Promote%2A> 方法，可以使用该方法将某个属性提升为可以在查询中使用的属性。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-107">The <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> class has the <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore.Promote%2A> method that you can use to promote a property as a property that can be used in queries.</span></span> <span data-ttu-id="6c6b7-108">以下示例是存储扩展性的一个端对端示例。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-108">The following example is an end-to-end example of store extensibility.</span></span>

1. <span data-ttu-id="6c6b7-109">在此示例方案中，文档处理 (DP) 应用程序具有多个工作流，每个工作流都使用自定义的活动进行文档处理。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-109">In this example scenario, a document processing (DP) application has workflows, each of which uses custom activities for document processing.</span></span> <span data-ttu-id="6c6b7-110">这些工作流具有一组状态变量，最终用户需要看到这些变量。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-110">These workflows have a set of state variables that need to be made visible to the end user.</span></span> <span data-ttu-id="6c6b7-111">为了实现此目的，DP 应用程序提供了一个类型为 <xref:System.Activities.Persistence.PersistenceParticipant> 的实例扩展，活动使用该实例扩展来提供状态变量。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-111">To achieve this, the DP application provides an instance extension of type <xref:System.Activities.Persistence.PersistenceParticipant>, which is used by activities to supply the state variables.</span></span>

    ```csharp
    class DocumentStatusExtension : PersistenceParticipant
    {
        public string DocumentId;
        public string ApprovalStatus;
        public string UserName;
        public DateTime LastUpdateTime;
    }
    ```

2. <span data-ttu-id="6c6b7-112">然后，将新的扩展添加到主机。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-112">The new extension is then added to the host.</span></span>

    ```csharp
    static Activity workflow = CreateWorkflow();
    WorkflowApplication application = new WorkflowApplication(workflow);
    DocumentStatusExtension documentStatusExtension = new DocumentStatusExtension ();
    application.Extensions.Add(documentStatusExtension);
    ```

     <span data-ttu-id="6c6b7-113">有关添加自定义持久性参与者的详细信息，请参阅 [持久性参与者](persistence-participants.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-113">For more details about adding a custom persistence participant, see the [Persistence Participants](persistence-participants.md) sample.</span></span>

3. <span data-ttu-id="6c6b7-114">DP 应用程序中的自定义活动在 **Execute** 方法中填充各种状态字段。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-114">The custom activities in the DP application populate various status fields in the **Execute** method.</span></span>

    ```csharp
    public override void Execute(CodeActivityContext context)
    {
        // ...
        context.GetExtension<DocumentStatusExtension>().DocumentId = Guid.NewGuid();
        context.GetExtension<DocumentStatusExtension>().UserName = "John Smith";
        context.GetExtension<DocumentStatusExtension>().ApprovalStatus = "Approved";
        context.GetExtension<DocumentStatusExtension>().LastUpdateTime = DateTime.Now();
        // ...
    }
    ```

4. <span data-ttu-id="6c6b7-115">当工作流实例到达持久性点时， **DocumentStatusExtension** 持久性参与者的 **CollectValues** 方法会将这些属性保存到持久性数据集合中。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-115">When a workflow instance reaches a persistence point, the **CollectValues** method of the **DocumentStatusExtension** persistence participant saves these properties into the persistence data collection.</span></span>

    ```csharp
    class DocumentStatusExtension : PersistenceParticipant
    {
        const XNamespace xNS = XNamespace.Get("http://contoso.com/DocumentStatus");

        protected override void CollectValues(out IDictionary<XName, object> readWriteValues, out IDictionary<XName, object> writeOnlyValues)
        {
            readWriteValues = new Dictionary<XName, object>();
            readWriteValues.Add(xNS.GetName("UserName"), this.UserName);
            readWriteValues.Add(xNS.GetName("ApprovalStatus"), this.ApprovalStatus);
            readWriteValues.Add(xNS.GetName("DocumentId"), this.DocumentId);
            readWriteValues.Add(xNS.GetName("LastModifiedTime"), this.LastUpdateTime);

            writeOnlyValues = null;
        }
        // ...
    }
    ```

    > [!NOTE]
    > <span data-ttu-id="6c6b7-116">持久性框架通过 **SaveWorkflowCommand. InstanceData** 集合将所有这些属性传递给 **SqlWorkflowInstanceStore** 。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-116">All these properties are passed to **SqlWorkflowInstanceStore** by the persistence framework through the **SaveWorkflowCommand.InstanceData** collection.</span></span>

5. <span data-ttu-id="6c6b7-117">DP 应用程序初始化 SQL 工作流实例存储并调用 **升级** 方法来升级此数据。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-117">The DP application initializes the SQL Workflow Instance Store and invokes the **Promote** method to promote this data.</span></span>

    ```csharp
    SqlWorkflowInstanceStore store = new SqlWorkflowInstanceStore(connectionString);

    List<XName> variantProperties = new List<XName>()
    {
        xNS.GetName("UserName"),
        xNS.GetName("ApprovalStatus"),
        xNS.GetName("DocumentId"),
        xNS.GetName("LastModifiedTime")
    };

    store.Promote("DocumentStatus", variantProperties, null);
    ```

    <span data-ttu-id="6c6b7-118">根据此促销信息， **SqlWorkflowInstanceStore** 将数据属性置于 [InstancePromotedProperties](#InstancePromotedProperties) 视图的列中。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-118">Based on this promotion information, **SqlWorkflowInstanceStore** places the data properties in the columns of the [InstancePromotedProperties](#InstancePromotedProperties) view.</span></span>

6. <span data-ttu-id="6c6b7-119">为了从提升表中查询某个数据子集，DP 应用程序在提升视图之上添加一个自定义视图。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-119">To query a subset of the data from the promotion table, the DP application adds a customized view on top of the promotion view.</span></span>

    ```sql
    create view [dbo].[DocumentStatus] with schemabinding
    as
        select  P.[InstanceId] as [InstanceId],
            P.Value1 as [UserName],
            P.Value2 as [ApprovalStatus],
            P.Value3 as [DocumentId],
            P.Value4 as [LastUpdatedTime]
    from [System.Activities.DurableInstancing].[InstancePromotedProperties] as P
    where P.PromotionName = N'DocumentStatus'
    go
    ```

## <a name="systemactivitiesdurableinstancinginstancepromotedproperties-view"></a><a name="InstancePromotedProperties"></a> <span data-ttu-id="6c6b7-120">[InstancePromotedProperties] 视图</span><span class="sxs-lookup"><span data-stu-id="6c6b7-120">[System.Activities.DurableInstancing.InstancePromotedProperties] view</span></span>

|<span data-ttu-id="6c6b7-121">列名</span><span class="sxs-lookup"><span data-stu-id="6c6b7-121">Column Name</span></span>|<span data-ttu-id="6c6b7-122">列类型</span><span class="sxs-lookup"><span data-stu-id="6c6b7-122">Column Type</span></span>|<span data-ttu-id="6c6b7-123">说明</span><span class="sxs-lookup"><span data-stu-id="6c6b7-123">Description</span></span>|
|-----------------|-----------------|-----------------|
|<span data-ttu-id="6c6b7-124">InstanceId</span><span class="sxs-lookup"><span data-stu-id="6c6b7-124">InstanceId</span></span>|<span data-ttu-id="6c6b7-125">GUID</span><span class="sxs-lookup"><span data-stu-id="6c6b7-125">GUID</span></span>|<span data-ttu-id="6c6b7-126">此提升所属的工作流实例。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-126">The workflow instance that this promotion belongs to.</span></span>|
|<span data-ttu-id="6c6b7-127">PromotionName</span><span class="sxs-lookup"><span data-stu-id="6c6b7-127">PromotionName</span></span>|<span data-ttu-id="6c6b7-128">nvarchar(400)</span><span class="sxs-lookup"><span data-stu-id="6c6b7-128">nvarchar(400)</span></span>|<span data-ttu-id="6c6b7-129">提升本身的名称。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-129">The name of the promotion itself.</span></span>|
|<span data-ttu-id="6c6b7-130">Value1、Value2、Value3、..、Value32</span><span class="sxs-lookup"><span data-stu-id="6c6b7-130">Value1, Value2, Value3,..,Value32</span></span>|<span data-ttu-id="6c6b7-131">sql_variant</span><span class="sxs-lookup"><span data-stu-id="6c6b7-131">sql_variant</span></span>|<span data-ttu-id="6c6b7-132">已提升属性本身的值。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-132">The value of the promoted property itself.</span></span> <span data-ttu-id="6c6b7-133">除了长度超过 8000 个字节的二进制 Blob 和字符串之外，多数 SQL 基元数据类型都可适合 sql_variant。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-133">Most SQL primitive data types except binary blobs and strings over 8000 bytes in length can fit in sql_variant.</span></span>|
|<span data-ttu-id="6c6b7-134">Value33、Value34、Value35、…、Value64</span><span class="sxs-lookup"><span data-stu-id="6c6b7-134">Value33, Value34, Value35, …, Value64</span></span>|<span data-ttu-id="6c6b7-135">varbinary(max)</span><span class="sxs-lookup"><span data-stu-id="6c6b7-135">varbinary(max)</span></span>|<span data-ttu-id="6c6b7-136">显式声明为 varbinary(max) 的已提升属性的值。</span><span class="sxs-lookup"><span data-stu-id="6c6b7-136">The value of promoted properties that are explicitly declared as varbinary(max).</span></span>|
