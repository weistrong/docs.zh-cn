---
description: 了解详细信息：如何：创建自定义持久性参与者
title: 如何：创建自定义持久性参与者
ms.date: 03/30/2017
ms.assetid: 1d9cc47a-8966-4286-94d5-4221403d9c06
ms.openlocfilehash: a0bdd8407bf409e7e485f4f32a0dd3f61e6f82b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742090"
---
# <a name="how-to-create-a-custom-persistence-participant"></a><span data-ttu-id="4ef00-103">如何：创建自定义持久性参与者</span><span class="sxs-lookup"><span data-stu-id="4ef00-103">How to: Create a Custom Persistence Participant</span></span>

<span data-ttu-id="4ef00-104">下列过程包含持久性参与者的创建步骤。</span><span class="sxs-lookup"><span data-stu-id="4ef00-104">The following procedure has steps to create a persistence participant.</span></span> <span data-ttu-id="4ef00-105">有关持久性参与者的示例实现，请参阅 [参与暂留](/previous-versions/dotnet/netframework-4.0/dd699769(v=vs.100)) 示例和 [存储扩展性](store-extensibility.md) 主题。</span><span class="sxs-lookup"><span data-stu-id="4ef00-105">See the [Participating in Persistence](/previous-versions/dotnet/netframework-4.0/dd699769(v=vs.100)) sample and [Store Extensibility](store-extensibility.md) topic for sample implementations of persistence participants.</span></span>  
  
1. <span data-ttu-id="4ef00-106">创建一个派生自 <xref:System.Activities.Persistence.PersistenceParticipant> 或 <xref:System.Activities.Persistence.PersistenceIOParticipant> 类的类。</span><span class="sxs-lookup"><span data-stu-id="4ef00-106">Create a class deriving from the <xref:System.Activities.Persistence.PersistenceParticipant> or the <xref:System.Activities.Persistence.PersistenceIOParticipant> class.</span></span> <span data-ttu-id="4ef00-107">除了能够参与 i/o 操作以外，PersistenceIOParticipant 类还提供与 PersistenceParticipant 类相同的扩展点。</span><span class="sxs-lookup"><span data-stu-id="4ef00-107">The PersistenceIOParticipant class offers the same extensibility points as the PersistenceParticipant class in addition to being able to participate in I/O operations.</span></span> <span data-ttu-id="4ef00-108">请完成以下一个或多个步骤。</span><span class="sxs-lookup"><span data-stu-id="4ef00-108">Follow one or more of the following steps.</span></span>  
  
2. <span data-ttu-id="4ef00-109">实现 <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-109">Implement the <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> method.</span></span> <span data-ttu-id="4ef00-110">**CollectValues** 方法具有两个字典参数，一个用于存储读/写值，另一个用于存储只写值 (稍后在查询) 中使用。</span><span class="sxs-lookup"><span data-stu-id="4ef00-110">The **CollectValues** method has two dictionary parameters, one for storing read/write values and the other one for storing write-only values (used later in queries).</span></span> <span data-ttu-id="4ef00-111">在此方法中，应使用特定于持久性参与者的数据填充这些字典。</span><span class="sxs-lookup"><span data-stu-id="4ef00-111">In this method, you should populate these dictionaries with data that is specific to a persistence participant.</span></span> <span data-ttu-id="4ef00-112">每个字典都包含值的名称和值自身，前者作为键，后者作为 <xref:System.Runtime.DurableInstancing.InstanceValue> 对象。</span><span class="sxs-lookup"><span data-stu-id="4ef00-112">Each dictionary contains the name of the value as the key and the value itself as an <xref:System.Runtime.DurableInstancing.InstanceValue> object.</span></span>  
  
    <span data-ttu-id="4ef00-113">ReadWriteValues 字典中的值打包为 **InstanceValue** 对象。</span><span class="sxs-lookup"><span data-stu-id="4ef00-113">The values in the readWriteValues dictionary are packaged as **InstanceValue** objects.</span></span> <span data-ttu-id="4ef00-114">只写字典中的值打包为 **InstanceValue** 对象，并设置设置和 InstanceValueOption。</span><span class="sxs-lookup"><span data-stu-id="4ef00-114">The values in the write-only dictionary are packaged as **InstanceValue** objects with InstanceValueOptions.Optional and InstanceValueOption.WriteOnly set.</span></span> <span data-ttu-id="4ef00-115">**CollectValues** 实现跨所有持久性参与者提供的每个 **InstanceValue** 必须具有唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="4ef00-115">Each **InstanceValue** provided by the **CollectValues** implementations across all persistence participants must have a unique name.</span></span>
  
    ```csharp  
    protected virtual void CollectValues(out IDictionary<XName,Object> readWriteValues, out IDictionary<XName,Object> writeOnlyValues)
    {
    }
    ```  
  
3. <span data-ttu-id="4ef00-116">实现 <xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-116">Implement the <xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A> method.</span></span> <span data-ttu-id="4ef00-117">**MapValues** 方法采用两个参数，类似于 **CollectValues** 方法接收的参数。</span><span class="sxs-lookup"><span data-stu-id="4ef00-117">The **MapValues** method takes two parameters that are similar to the parameters that the **CollectValues** method receives.</span></span> <span data-ttu-id="4ef00-118">在 **CollectValues** 阶段收集的所有值都将通过这些字典参数传递。</span><span class="sxs-lookup"><span data-stu-id="4ef00-118">All the values collected in the **CollectValues** stage are passed through these dictionary parameters.</span></span> <span data-ttu-id="4ef00-119">**MapValues** 阶段添加的新值将添加到只写值。</span><span class="sxs-lookup"><span data-stu-id="4ef00-119">The new values added by the **MapValues** stage are added to the write-only values.</span></span>  <span data-ttu-id="4ef00-120">只写字典用于向外部源提供不直接与实例值相关联的数据。</span><span class="sxs-lookup"><span data-stu-id="4ef00-120">The write-only dictionary is used to provide data to an external source not directly associated with the instance values.</span></span> <span data-ttu-id="4ef00-121">跨所有持久性参与者的 **MapValues** 方法实现提供的每个值都必须具有唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="4ef00-121">Each value provided by implementations of the **MapValues** method across all persistence participants must have a unique name.</span></span>  
  
    ```csharp  
    protected virtual IDictionary<XName,Object> MapValues(IDictionary<XName,Object> readWriteValues,IDictionary<XName,Object> writeOnlyValues)
    {
    }
    ```  
  
     <span data-ttu-id="4ef00-122"><xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A> 方法提供 <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> 不实现的功能，因为它允许由另一个持久性参与者提供另一个值的依赖项，该参与者尚未经过 <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> 的处理。</span><span class="sxs-lookup"><span data-stu-id="4ef00-122">The <xref:System.Activities.Persistence.PersistenceParticipant.MapValues%2A> method provides functionality that <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> does not, in that it allows for a dependency on another value provided by another persistence participant that hasn’t been processed by <xref:System.Activities.Persistence.PersistenceParticipant.CollectValues%2A> yet.</span></span>  
  
4. <span data-ttu-id="4ef00-123">实现 **PublishValues** 方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-123">Implement the **PublishValues** method.</span></span> <span data-ttu-id="4ef00-124">**PublishValues** 方法接收包含从持久性存储区加载的所有值的字典。</span><span class="sxs-lookup"><span data-stu-id="4ef00-124">The **PublishValues** method receives a dictionary containing all the values loaded from the persistence store.</span></span>  
  
    ```csharp  
    protected virtual void PublishValues(IDictionary<XName,Object> readWriteValues)
    {
    }
    ```  
  
5. <span data-ttu-id="4ef00-125">如果参与者是持久性 i/o 参与者，请实现 **BeginOnSave** 方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-125">Implement the **BeginOnSave** method if the participant is a persistence I/O participant.</span></span> <span data-ttu-id="4ef00-126">在执行保存操作期间，将调用此方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-126">This method is called during a Save operation.</span></span> <span data-ttu-id="4ef00-127">在此方法中，应执行保存) 工作流实例的持久性 (的 i/o 附属项。</span><span class="sxs-lookup"><span data-stu-id="4ef00-127">In this method, you should perform I/O adjunct to the persisting (saving) workflow instances.</span></span>  <span data-ttu-id="4ef00-128">如果主机正将事务用于相应的持久性命令，则会在 Transaction.Current 中提供相同事务。</span><span class="sxs-lookup"><span data-stu-id="4ef00-128">If the host is using a transaction for the corresponding persistence command, the same transaction is provided in Transaction.Current.</span></span>  <span data-ttu-id="4ef00-129">此外，持久性 IO 参与者可公布事务一致性需求，在这种情况中，主机将为持久性段创建一个事务（如果不会在其他情况下使用该事务）。</span><span class="sxs-lookup"><span data-stu-id="4ef00-129">Additionally, PersistenceIOParticipants may advertise a transactional consistency requirement, in which case the host creates a transaction for the persistence episode if one would not otherwise be used.</span></span>  
  
    ```csharp  
    protected virtual IAsyncResult BeginOnSave(IDictionary<XName,Object> readWriteValues, IDictionary<XName,Object> writeOnlyValues, TimeSpan timeout, AsyncCallback callback, Object state)
    {
    }
    ```  
  
6. <span data-ttu-id="4ef00-130">如果参与者是持久性 i/o 参与者，请实现 **BeginOnLoad** 方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-130">Implement the **BeginOnLoad** method if the participant is a persistence I/O participant.</span></span> <span data-ttu-id="4ef00-131">在执行加载操作期间，将调用此方法。</span><span class="sxs-lookup"><span data-stu-id="4ef00-131">This method is called during a Load operation.</span></span> <span data-ttu-id="4ef00-132">在此方法中，应执行工作流实例加载的 i/o 附属项。</span><span class="sxs-lookup"><span data-stu-id="4ef00-132">In this method, you should perform I/O adjunct to the loading of workflow instances.</span></span> <span data-ttu-id="4ef00-133">如果主机正将事务用于相应的持久性命令，则会在 Transaction.Current 中提供相同事务。</span><span class="sxs-lookup"><span data-stu-id="4ef00-133">If the host is using a transaction for the corresponding persistence command, the same transaction is provided in Transaction.Current.</span></span> <span data-ttu-id="4ef00-134">此外，持久性 i/o 参与者可能会公布事务一致性要求，在这种情况下，主机将为持久性剧集创建一个事务（如果不以其他方式使用它）。</span><span class="sxs-lookup"><span data-stu-id="4ef00-134">Additionally, Persistence I/O participants may advertise a transactional consistency requirement, in which case the host creates a transaction for the persistence episode if one would not otherwise be used.</span></span>  
  
    ```csharp  
    protected virtual IAsyncResult BeginOnLoad(IDictionary<XName,Object> readWriteValues, TimeSpan timeout, AsyncCallback callback, Object state)
    {
    }
    ```
