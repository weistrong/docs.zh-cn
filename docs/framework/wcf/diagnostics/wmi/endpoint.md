---
description: 了解更多：终结点
title: 终结点
ms.date: 03/30/2017
ms.assetid: fe63370d-81a1-40f3-97c2-59cb357c78d2
ms.openlocfilehash: 1c28be37d1b1abfe1813e6da8903809affd309e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757457"
---
# <a name="endpoint"></a><span data-ttu-id="3a5ad-103">终结点</span><span class="sxs-lookup"><span data-stu-id="3a5ad-103">Endpoint</span></span>

<span data-ttu-id="3a5ad-104">终结点</span><span class="sxs-lookup"><span data-stu-id="3a5ad-104">Endpoint</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a5ad-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a5ad-105">Syntax</span></span>  
  
```csharp
class Endpoint  
{  
  string Address;  
  string AddressHeaders[];  
  string AddressIdentity;  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  Binding Binding;  
  string ContractName;  
  string CounterInstanceName;  
  string ListenUri;  
  string Name;  
  sint32 ProcessId;  
  Contract ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3a5ad-106">方法</span><span class="sxs-lookup"><span data-stu-id="3a5ad-106">Methods</span></span>  

 <span data-ttu-id="3a5ad-107">该终结点类定义以下方法。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-107">The Endpoint class defines the following method.</span></span>  
  
|<span data-ttu-id="3a5ad-108">方法</span><span class="sxs-lookup"><span data-stu-id="3a5ad-108">Method</span></span>|<span data-ttu-id="3a5ad-109">说明</span><span class="sxs-lookup"><span data-stu-id="3a5ad-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3a5ad-110">GetOperationCounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="3a5ad-110">GetOperationCounterInstanceName</span></span>](getoperationcounterinstancename.md)|<span data-ttu-id="3a5ad-111">检索操作性能计数器实例名称</span><span class="sxs-lookup"><span data-stu-id="3a5ad-111">Retrieves the operation performance counter instance name</span></span>|  
  
## <a name="properties"></a><span data-ttu-id="3a5ad-112">属性</span><span class="sxs-lookup"><span data-stu-id="3a5ad-112">Properties</span></span>  

 <span data-ttu-id="3a5ad-113">该终结点类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="3a5ad-113">The Endpoint class has the following properties:</span></span>  
  
### <a name="address"></a><span data-ttu-id="3a5ad-114">地址</span><span class="sxs-lookup"><span data-stu-id="3a5ad-114">Address</span></span>  

 <span data-ttu-id="3a5ad-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-115">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-117">一个包含终结点地址的 URI。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-117">A URI that contains the address of the endpoint.</span></span>  
  
### <a name="addressheaders"></a><span data-ttu-id="3a5ad-118">AddressHeaders</span><span class="sxs-lookup"><span data-stu-id="3a5ad-118">AddressHeaders</span></span>  

 <span data-ttu-id="3a5ad-119">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="3a5ad-119">Data type: string array</span></span>  
  
 <span data-ttu-id="3a5ad-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-121">附加到此终结点的地址头的集合。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-121">The collection of address headers attached to this endpoint.</span></span>  
  
### <a name="addressidentity"></a><span data-ttu-id="3a5ad-122">AddressIdentity</span><span class="sxs-lookup"><span data-stu-id="3a5ad-122">AddressIdentity</span></span>  

 <span data-ttu-id="3a5ad-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-123">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-125">终结点的标识。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-125">The identity of the endpoint.</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="3a5ad-126">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="3a5ad-126">AppDomainId</span></span>  

 <span data-ttu-id="3a5ad-127">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="3a5ad-127">Data type: sint32</span></span>  
  
 <span data-ttu-id="3a5ad-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-129">承载终结点的 AppDomain 的 AppDomain ID。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-129">The appdomain id of the appdomain that hosts the endpoint.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="3a5ad-130">行为</span><span class="sxs-lookup"><span data-stu-id="3a5ad-130">Behaviors</span></span>  

 <span data-ttu-id="3a5ad-131">数据类型：Behavior array</span><span class="sxs-lookup"><span data-stu-id="3a5ad-131">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="3a5ad-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-133">此终结点所实现的行为的集合。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-133">The collection of behaviors implemented by this endpoint.</span></span>  
  
### <a name="binding"></a><span data-ttu-id="3a5ad-134">绑定</span><span class="sxs-lookup"><span data-stu-id="3a5ad-134">Binding</span></span>  

 <span data-ttu-id="3a5ad-135">数据类型：绑定</span><span class="sxs-lookup"><span data-stu-id="3a5ad-135">Data type: Binding</span></span>  
  
 <span data-ttu-id="3a5ad-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-137">此终结点所使用的绑定。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-137">The binding used by this endpoint.</span></span>  
  
### <a name="contractname"></a><span data-ttu-id="3a5ad-138">ContractName</span><span class="sxs-lookup"><span data-stu-id="3a5ad-138">ContractName</span></span>  

 <span data-ttu-id="3a5ad-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-139">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-141">一个字符串，指定此终结点公开了哪个协定。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-141">A string that specifies which contract this endpoint is exposing.</span></span>  
  
### <a name="counterinstancename"></a><span data-ttu-id="3a5ad-142">CounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="3a5ad-142">CounterInstanceName</span></span>  

 <span data-ttu-id="3a5ad-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-143">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-145">该终结点的性能计数器的实例名称。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-145">The name of the instance of performance counters of the endpoint.</span></span>  
  
### <a name="listenuri"></a><span data-ttu-id="3a5ad-146">ListenUri</span><span class="sxs-lookup"><span data-stu-id="3a5ad-146">ListenUri</span></span>  

 <span data-ttu-id="3a5ad-147">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-147">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-149">终结点在其上侦听的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-149">The Uri the endpoint listens on.</span></span>  
  
### <a name="name"></a><span data-ttu-id="3a5ad-150">名称</span><span class="sxs-lookup"><span data-stu-id="3a5ad-150">Name</span></span>  

 <span data-ttu-id="3a5ad-151">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a5ad-151">Data type: string</span></span>  
  
 <span data-ttu-id="3a5ad-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-153">此终结点的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-153">The unique name of this endpoint.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="3a5ad-154">ProcessId</span><span class="sxs-lookup"><span data-stu-id="3a5ad-154">ProcessId</span></span>  

 <span data-ttu-id="3a5ad-155">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="3a5ad-155">Data type: sint32</span></span>  
  
 <span data-ttu-id="3a5ad-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-157">承载该终结点的进程的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-157">The process Id of the process that hosts the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="3a5ad-158">ref</span><span class="sxs-lookup"><span data-stu-id="3a5ad-158">ref</span></span>  

 <span data-ttu-id="3a5ad-159">数据类型：Contract</span><span class="sxs-lookup"><span data-stu-id="3a5ad-159">Data type: Contract</span></span>  
  
 <span data-ttu-id="3a5ad-160">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a5ad-160">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a5ad-161">此终结点公开的协定。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-161">The contract this endpoint is exposing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a5ad-162">要求</span><span class="sxs-lookup"><span data-stu-id="3a5ad-162">Requirements</span></span>  
  
|<span data-ttu-id="3a5ad-163">MOF</span><span class="sxs-lookup"><span data-stu-id="3a5ad-163">MOF</span></span>|<span data-ttu-id="3a5ad-164">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="3a5ad-164">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3a5ad-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a5ad-165">Namespace</span></span>|<span data-ttu-id="3a5ad-166">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="3a5ad-166">Defined in root\ServiceModel</span></span>|
