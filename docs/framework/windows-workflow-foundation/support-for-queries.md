---
description: 了解详细信息：支持查询
title: 查询支持
ms.date: 03/30/2017
ms.assetid: 093c22f5-3294-4642-857a-5252233d6796
ms.openlocfilehash: 418e511e8b845653b9f3ec86d90c6cbfb25d5671
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755208"
---
# <a name="support-for-queries"></a><span data-ttu-id="0e402-103">查询支持</span><span class="sxs-lookup"><span data-stu-id="0e402-103">Support for Queries</span></span>

<span data-ttu-id="0e402-104">SQL 工作流实例存储中记录了存储区中的一组已知属性。</span><span class="sxs-lookup"><span data-stu-id="0e402-104">The SQL Workflow Instance Store records a set of well-known properties in the store.</span></span> <span data-ttu-id="0e402-105">用户可以根据这些属性查询实例。</span><span class="sxs-lookup"><span data-stu-id="0e402-105">Users can query for instances based on these properties.</span></span> <span data-ttu-id="0e402-106">下面的列表包含这些已知属性的一部分：</span><span class="sxs-lookup"><span data-stu-id="0e402-106">The following list contains some of these well-known properties:</span></span>  
  
- <span data-ttu-id="0e402-107">**站点名称。**</span><span class="sxs-lookup"><span data-stu-id="0e402-107">**Site Name.**</span></span> <span data-ttu-id="0e402-108">包含服务的网站的名称。</span><span class="sxs-lookup"><span data-stu-id="0e402-108">Name of the Web site that contains the service.</span></span>  
  
- <span data-ttu-id="0e402-109">**相对应用程序路径。**</span><span class="sxs-lookup"><span data-stu-id="0e402-109">**Relative Application Path.**</span></span> <span data-ttu-id="0e402-110">应用程序相对于网站的路径。</span><span class="sxs-lookup"><span data-stu-id="0e402-110">Path of the application relative to the Web site.</span></span>  
  
- <span data-ttu-id="0e402-111">**相对服务路径。**</span><span class="sxs-lookup"><span data-stu-id="0e402-111">**Relative Service Path.**</span></span> <span data-ttu-id="0e402-112">服务相对于应用程序的路径。</span><span class="sxs-lookup"><span data-stu-id="0e402-112">Path of the service relative to the application.</span></span>  
  
- <span data-ttu-id="0e402-113">**服务名称。**</span><span class="sxs-lookup"><span data-stu-id="0e402-113">**Service Name.**</span></span> <span data-ttu-id="0e402-114">服务的名称。</span><span class="sxs-lookup"><span data-stu-id="0e402-114">Name of the service.</span></span>  
  
- <span data-ttu-id="0e402-115">**服务命名空间。**</span><span class="sxs-lookup"><span data-stu-id="0e402-115">**Service Namespace.**</span></span> <span data-ttu-id="0e402-116">服务使用的命名空间的名称。</span><span class="sxs-lookup"><span data-stu-id="0e402-116">Name of the namespace that the service uses.</span></span>  
  
- <span data-ttu-id="0e402-117">**当前计算机。**</span><span class="sxs-lookup"><span data-stu-id="0e402-117">**Current Machine.**</span></span>  
  
- <span data-ttu-id="0e402-118">**上一台计算机**。</span><span class="sxs-lookup"><span data-stu-id="0e402-118">**Last Machine**.</span></span> <span data-ttu-id="0e402-119">上次运行工作流服务实例的计算机。</span><span class="sxs-lookup"><span data-stu-id="0e402-119">The computer on which the workflow service instance ran the last time.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0e402-120">对于使用工作流服务主机的自承载方案，仅填充最后四个属性。</span><span class="sxs-lookup"><span data-stu-id="0e402-120">For self-hosted scenarios using Workflow Service Host, only the last four properties are populated.</span></span> <span data-ttu-id="0e402-121">对于工作流应用程序方案，仅填充最后一个属性。</span><span class="sxs-lookup"><span data-stu-id="0e402-121">For Workflow Application scenarios, only the last property is populated.</span></span>  
  
 <span data-ttu-id="0e402-122">工作流运行时为前三个属性提供值。</span><span class="sxs-lookup"><span data-stu-id="0e402-122">The workflow runtime supplies values for the first three properties.</span></span> <span data-ttu-id="0e402-123">工作流服务主机提供 " **挂起原因** " 属性的值。</span><span class="sxs-lookup"><span data-stu-id="0e402-123">The workflow service host supplies the value for the **Suspend Reason** property.</span></span> <span data-ttu-id="0e402-124">SQL 工作流实例存储区本身提供 **上次更新的计算机** 属性的值。</span><span class="sxs-lookup"><span data-stu-id="0e402-124">The SQL Workflow Instance Store itself supplies values for the **Last Updated Machine** property.</span></span>  
  
 <span data-ttu-id="0e402-125">使用 SQL 工作流实例存储的功能还可以指定自定义属性，您可以在持久性数据库中存储这些属性的值并且在查询中使用这些属性。</span><span class="sxs-lookup"><span data-stu-id="0e402-125">The SQL Workflow Instance Store feature also lets you specify the custom properties for which you want to store the values in the persistence database and that you want to use in queries.</span></span> <span data-ttu-id="0e402-126">有关自定义促销的详细信息，请参阅 [存储扩展性](store-extensibility.md)。</span><span class="sxs-lookup"><span data-stu-id="0e402-126">For more information about custom promotions, see [Store Extensibility](store-extensibility.md).</span></span>  
  
## <a name="views"></a><span data-ttu-id="0e402-127">视图</span><span class="sxs-lookup"><span data-stu-id="0e402-127">Views</span></span>  

 <span data-ttu-id="0e402-128">实例存储区包含下列视图。</span><span class="sxs-lookup"><span data-stu-id="0e402-128">The instance store contains the following views.</span></span> <span data-ttu-id="0e402-129">有关更多详细信息，请参阅 [持久性数据库架构](persistence-database-schema.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e402-129">See [Persistence Database Schema](persistence-database-schema.md) for further details.</span></span>  
  
### <a name="the-instances-view"></a><span data-ttu-id="0e402-130">Instances 视图</span><span class="sxs-lookup"><span data-stu-id="0e402-130">The Instances View</span></span>  

 <span data-ttu-id="0e402-131">Instances 视图包含下列字段：</span><span class="sxs-lookup"><span data-stu-id="0e402-131">The Instances view contains the following fields:</span></span>  
  
1. <span data-ttu-id="0e402-132">Id</span><span class="sxs-lookup"><span data-stu-id="0e402-132">**Id**</span></span>  
  
2. <span data-ttu-id="0e402-133">**PendingTimer**</span><span class="sxs-lookup"><span data-stu-id="0e402-133">**PendingTimer**</span></span>  
  
3. <span data-ttu-id="0e402-134">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0e402-134">**CreationTime**</span></span>  
  
4. <span data-ttu-id="0e402-135">**LastUpdatedTime**</span><span class="sxs-lookup"><span data-stu-id="0e402-135">**LastUpdatedTime**</span></span>  
  
5. <span data-ttu-id="0e402-136">**ServiceDeploymentId**</span><span class="sxs-lookup"><span data-stu-id="0e402-136">**ServiceDeploymentId**</span></span>  
  
6. <span data-ttu-id="0e402-137">**SuspensionExceptionName**</span><span class="sxs-lookup"><span data-stu-id="0e402-137">**SuspensionExceptionName**</span></span>  
  
7. <span data-ttu-id="0e402-138">**SuspensionReason**</span><span class="sxs-lookup"><span data-stu-id="0e402-138">**SuspensionReason**</span></span>  
  
8. <span data-ttu-id="0e402-139">**ActiveBookmarks**</span><span class="sxs-lookup"><span data-stu-id="0e402-139">**ActiveBookmarks**</span></span>  
  
9. <span data-ttu-id="0e402-140">**CurrentMachine**</span><span class="sxs-lookup"><span data-stu-id="0e402-140">**CurrentMachine**</span></span>  
  
10. <span data-ttu-id="0e402-141">**LastMachine**</span><span class="sxs-lookup"><span data-stu-id="0e402-141">**LastMachine**</span></span>  
  
11. <span data-ttu-id="0e402-142">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="0e402-142">**ExecutionStatus**</span></span>  
  
12. <span data-ttu-id="0e402-143">**IsInitialized**</span><span class="sxs-lookup"><span data-stu-id="0e402-143">**IsInitialized**</span></span>  
  
13. <span data-ttu-id="0e402-144">**IsSuspended**</span><span class="sxs-lookup"><span data-stu-id="0e402-144">**IsSuspended**</span></span>  
  
14. <span data-ttu-id="0e402-145">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="0e402-145">**IsCompleted**</span></span>  
  
15. <span data-ttu-id="0e402-146">**EncodingOption**</span><span class="sxs-lookup"><span data-stu-id="0e402-146">**EncodingOption**</span></span>  
  
16. <span data-ttu-id="0e402-147">**ReadWritePrimitiveDataProperties**</span><span class="sxs-lookup"><span data-stu-id="0e402-147">**ReadWritePrimitiveDataProperties**</span></span>  
  
17. <span data-ttu-id="0e402-148">**WriteOnlyPrimitiveDataProperties**</span><span class="sxs-lookup"><span data-stu-id="0e402-148">**WriteOnlyPrimitiveDataProperties**</span></span>  
  
18. <span data-ttu-id="0e402-149">**ReadWriteComplexDataProperties**</span><span class="sxs-lookup"><span data-stu-id="0e402-149">**ReadWriteComplexDataProperties**</span></span>  
  
19. <span data-ttu-id="0e402-150">**WriteOnlyComplexDataProperties**</span><span class="sxs-lookup"><span data-stu-id="0e402-150">**WriteOnlyComplexDataProperties**</span></span>  
  
### <a name="the-servicedeployments-view"></a><span data-ttu-id="0e402-151">ServiceDeployments 视图</span><span class="sxs-lookup"><span data-stu-id="0e402-151">The ServiceDeployments view</span></span>  

 <span data-ttu-id="0e402-152">ServiceDeployments 视图包含下列字段：</span><span class="sxs-lookup"><span data-stu-id="0e402-152">The ServiceDeployments view contains the following fields:</span></span>  
  
1. <span data-ttu-id="0e402-153">**名**</span><span class="sxs-lookup"><span data-stu-id="0e402-153">**SiteName**</span></span>  
  
2. <span data-ttu-id="0e402-154">**RelativeServicePath**</span><span class="sxs-lookup"><span data-stu-id="0e402-154">**RelativeServicePath**</span></span>  
  
3. <span data-ttu-id="0e402-155">**RelativeApplicationPath**</span><span class="sxs-lookup"><span data-stu-id="0e402-155">**RelativeApplicationPath**</span></span>  
  
4. <span data-ttu-id="0e402-156">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="0e402-156">**ServiceName**</span></span>  
  
5. <span data-ttu-id="0e402-157">**ServiceNamespace**</span><span class="sxs-lookup"><span data-stu-id="0e402-157">**ServiceNamespace**</span></span>  
  
### <a name="the-instancepromotedproperties-view"></a><span data-ttu-id="0e402-158">InstancePromotedProperties 视图</span><span class="sxs-lookup"><span data-stu-id="0e402-158">The InstancePromotedProperties view</span></span>  

 <span data-ttu-id="0e402-159">InstancePromotedProperties 视图包含下列字段。</span><span class="sxs-lookup"><span data-stu-id="0e402-159">The InstancePromotedProperties view contains the following fields.</span></span> <span data-ttu-id="0e402-160">有关升级属性的详细信息，请参阅 [存储扩展性](store-extensibility.md) 主题。</span><span class="sxs-lookup"><span data-stu-id="0e402-160">For details on promoted properties, see the [Store Extensibility](store-extensibility.md) topic.</span></span>  
  
1. <span data-ttu-id="0e402-161">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="0e402-161">**InstanceId**</span></span>  
  
2. <span data-ttu-id="0e402-162">**EncodingOption**</span><span class="sxs-lookup"><span data-stu-id="0e402-162">**EncodingOption**</span></span>  
  
3. <span data-ttu-id="0e402-163">**PromotionName**</span><span class="sxs-lookup"><span data-stu-id="0e402-163">**PromotionName**</span></span>  
  
4. <span data-ttu-id="0e402-164">**值 #** (**Value1** 到 **Value64**) 中的一系列字段。</span><span class="sxs-lookup"><span data-stu-id="0e402-164">**Value#** (a range of fields from **Value1** to **Value64**).</span></span>
