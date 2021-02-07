---
description: 了解详细信息：服务
title: 服务
ms.date: 03/30/2017
ms.assetid: 999806e1-6376-409e-b998-b0af391adfe7
ms.openlocfilehash: e66f9a23f8c182327899904c26ff6a6368b9bdc6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715621"
---
# <a name="service"></a><span data-ttu-id="acae5-103">服务</span><span class="sxs-lookup"><span data-stu-id="acae5-103">Service</span></span>

<span data-ttu-id="acae5-104">服务</span><span class="sxs-lookup"><span data-stu-id="acae5-104">Service</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acae5-105">语法</span><span class="sxs-lookup"><span data-stu-id="acae5-105">Syntax</span></span>  
  
```csharp
class Service  
{  
  string BaseAddresses[];  
  Behavior Behaviors[];  
  string ConfigurationName;  
  string CounterInstanceName;  
  string DistinguishedName;  
  string Extensions[];  
  string Metadata[];  
  string Name;  
  string Namespace;  
  datetime Opened;  
  Channel OutgoingChannels[];  
  sint32 ProcessId;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="acae5-106">方法</span><span class="sxs-lookup"><span data-stu-id="acae5-106">Methods</span></span>  

 <span data-ttu-id="acae5-107">Service 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="acae5-107">The Service class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="acae5-108">属性</span><span class="sxs-lookup"><span data-stu-id="acae5-108">Properties</span></span>  

 <span data-ttu-id="acae5-109">Service 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="acae5-109">The Service class has the following properties:</span></span>  
  
### <a name="baseaddresses"></a><span data-ttu-id="acae5-110">BaseAddresses</span><span class="sxs-lookup"><span data-stu-id="acae5-110">BaseAddresses</span></span>  

 <span data-ttu-id="acae5-111">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="acae5-111">Data type: string array</span></span>  
  
 <span data-ttu-id="acae5-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-113">服务使用的基址。</span><span class="sxs-lookup"><span data-stu-id="acae5-113">The base addresses used by the service.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="acae5-114">行为</span><span class="sxs-lookup"><span data-stu-id="acae5-114">Behaviors</span></span>  

 <span data-ttu-id="acae5-115">数据类型：Behavior array</span><span class="sxs-lookup"><span data-stu-id="acae5-115">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="acae5-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-117">与此服务关联的行为。</span><span class="sxs-lookup"><span data-stu-id="acae5-117">The behaviors associated with this service.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="acae5-118">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="acae5-118">ConfigurationName</span></span>  

 <span data-ttu-id="acae5-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="acae5-119">Data type: string</span></span>  
  
 <span data-ttu-id="acae5-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-121">ServiceElement_BehaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="acae5-121">ServiceElement_BehaviorConfiguration</span></span>  
  
### <a name="counterinstancename"></a><span data-ttu-id="acae5-122">CounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="acae5-122">CounterInstanceName</span></span>  

 <span data-ttu-id="acae5-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="acae5-123">Data type: string</span></span>  
  
 <span data-ttu-id="acae5-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-125">此服务的性能计数器实例的实例名称。</span><span class="sxs-lookup"><span data-stu-id="acae5-125">Instance name of the instance of the performance counters of the service.</span></span>  
  
### <a name="distinguishedname"></a><span data-ttu-id="acae5-126">DistinguishedName</span><span class="sxs-lookup"><span data-stu-id="acae5-126">DistinguishedName</span></span>  

 <span data-ttu-id="acae5-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="acae5-127">Data type: string</span></span>  
  
 <span data-ttu-id="acae5-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-129">该地址处的服务名称。</span><span class="sxs-lookup"><span data-stu-id="acae5-129">Service name at the address.</span></span>  
  
### <a name="extensions"></a><span data-ttu-id="acae5-130">Extensions</span><span class="sxs-lookup"><span data-stu-id="acae5-130">Extensions</span></span>  

 <span data-ttu-id="acae5-131">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="acae5-131">Data type: string array</span></span>  
  
 <span data-ttu-id="acae5-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-133">服务实例扩展的实例上下文。</span><span class="sxs-lookup"><span data-stu-id="acae5-133">The instance contexts for the extensions of the service instance.</span></span>  
  
### <a name="metadata"></a><span data-ttu-id="acae5-134">Metadata</span><span class="sxs-lookup"><span data-stu-id="acae5-134">Metadata</span></span>  

 <span data-ttu-id="acae5-135">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="acae5-135">Data type: string array</span></span>  
  
 <span data-ttu-id="acae5-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-137">服务元数据设置。</span><span class="sxs-lookup"><span data-stu-id="acae5-137">The service metadata settings.</span></span>  
  
### <a name="name"></a><span data-ttu-id="acae5-138">名称</span><span class="sxs-lookup"><span data-stu-id="acae5-138">Name</span></span>  

 <span data-ttu-id="acae5-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="acae5-139">Data type: string</span></span>  
  
 <span data-ttu-id="acae5-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-141">此服务的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="acae5-141">The unique name of this service.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="acae5-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="acae5-142">Namespace</span></span>  

 <span data-ttu-id="acae5-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="acae5-143">Data type: string</span></span>  
  
 <span data-ttu-id="acae5-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-145">服务的命名空间。</span><span class="sxs-lookup"><span data-stu-id="acae5-145">The namespace of the service.</span></span>  
  
### <a name="opened"></a><span data-ttu-id="acae5-146">已打开</span><span class="sxs-lookup"><span data-stu-id="acae5-146">Opened</span></span>  

 <span data-ttu-id="acae5-147">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="acae5-147">Data type: datetime</span></span>  
  
 <span data-ttu-id="acae5-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-149">服务打开的时间。</span><span class="sxs-lookup"><span data-stu-id="acae5-149">The time the service was opened.</span></span>  
  
### <a name="outgoingchannels"></a><span data-ttu-id="acae5-150">OutgoingChannels</span><span class="sxs-lookup"><span data-stu-id="acae5-150">OutgoingChannels</span></span>  

 <span data-ttu-id="acae5-151">数据类型：Channel array</span><span class="sxs-lookup"><span data-stu-id="acae5-151">Data type: Channel array</span></span>  
  
 <span data-ttu-id="acae5-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-153">从服务实例传出的通道。</span><span class="sxs-lookup"><span data-stu-id="acae5-153">The channels that are outgoing from the service instance.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="acae5-154">ProcessId</span><span class="sxs-lookup"><span data-stu-id="acae5-154">ProcessId</span></span>  

 <span data-ttu-id="acae5-155">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="acae5-155">Data type: sint32</span></span>  
  
 <span data-ttu-id="acae5-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="acae5-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="acae5-157">承载服务的进程的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="acae5-157">The process id of the process that hosts the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="acae5-158">要求</span><span class="sxs-lookup"><span data-stu-id="acae5-158">Requirements</span></span>  
  
|<span data-ttu-id="acae5-159">MOF</span><span class="sxs-lookup"><span data-stu-id="acae5-159">MOF</span></span>|<span data-ttu-id="acae5-160">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="acae5-160">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="acae5-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="acae5-161">Namespace</span></span>|<span data-ttu-id="acae5-162">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="acae5-162">Defined in root\ServiceModel</span></span>|
