---
description: 了解详细信息：协定
title: 协定
ms.date: 03/30/2017
ms.assetid: aa00f6b3-7e1f-4213-841a-206463fca20b
ms.openlocfilehash: 3443a7d2eed1a34f07495bd3ceb98c1ba997fabf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757548"
---
# <a name="contract"></a><span data-ttu-id="d1399-103">协定</span><span class="sxs-lookup"><span data-stu-id="d1399-103">Contract</span></span>

<span data-ttu-id="d1399-104">协定</span><span class="sxs-lookup"><span data-stu-id="d1399-104">Contract</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1399-105">语法</span><span class="sxs-lookup"><span data-stu-id="d1399-105">Syntax</span></span>  
  
```csharp
class Contract  
{  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  string Name;  
  string Namespace;  
  Operation Operations[];  
  sint32 ProcessId;  
  Contract ref;  
  string SessionMode;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="d1399-106">方法</span><span class="sxs-lookup"><span data-stu-id="d1399-106">Methods</span></span>  

 <span data-ttu-id="d1399-107">Contract 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="d1399-107">The Contract class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="d1399-108">属性</span><span class="sxs-lookup"><span data-stu-id="d1399-108">Properties</span></span>  

 <span data-ttu-id="d1399-109">Contract 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="d1399-109">The Contract class has the following properties:</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="d1399-110">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="d1399-110">AppDomainId</span></span>  

 <span data-ttu-id="d1399-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="d1399-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="d1399-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-113">承载协定的 appdomain 的 appdomain ID。</span><span class="sxs-lookup"><span data-stu-id="d1399-113">The appdomain id of the appdomain that hosts the contract.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="d1399-114">行为</span><span class="sxs-lookup"><span data-stu-id="d1399-114">Behaviors</span></span>  

 <span data-ttu-id="d1399-115">数据类型：Behavior array</span><span class="sxs-lookup"><span data-stu-id="d1399-115">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="d1399-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-117">与此协定关联的行为。</span><span class="sxs-lookup"><span data-stu-id="d1399-117">The behaviors associated with this contract.</span></span>  
  
### <a name="name"></a><span data-ttu-id="d1399-118">名称</span><span class="sxs-lookup"><span data-stu-id="d1399-118">Name</span></span>  

 <span data-ttu-id="d1399-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d1399-119">Data type: string</span></span>  
  
 <span data-ttu-id="d1399-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-121">WSDL 中协定的名称。</span><span class="sxs-lookup"><span data-stu-id="d1399-121">The name of the contract in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="d1399-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1399-122">Namespace</span></span>  

 <span data-ttu-id="d1399-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d1399-123">Data type: string</span></span>  
  
 <span data-ttu-id="d1399-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-125">WSDL 中 `portType` 元素的命名空间。</span><span class="sxs-lookup"><span data-stu-id="d1399-125">The namespace of the `portType` element in WSDL.</span></span>  
  
### <a name="operations"></a><span data-ttu-id="d1399-126">操作</span><span class="sxs-lookup"><span data-stu-id="d1399-126">Operations</span></span>  

 <span data-ttu-id="d1399-127">数据类型：操作数组</span><span class="sxs-lookup"><span data-stu-id="d1399-127">Data type: Operation array</span></span>  
  
 <span data-ttu-id="d1399-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-129">此协定的操作。</span><span class="sxs-lookup"><span data-stu-id="d1399-129">The operations of this contract.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="d1399-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="d1399-130">ProcessId</span></span>  

 <span data-ttu-id="d1399-131">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="d1399-131">Data type: sint32</span></span>  
  
 <span data-ttu-id="d1399-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-133">承载此协定的进程的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="d1399-133">The process Id of the process that hosts the contract.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="d1399-134">ref</span><span class="sxs-lookup"><span data-stu-id="d1399-134">ref</span></span>  

 <span data-ttu-id="d1399-135">数据类型：Contract</span><span class="sxs-lookup"><span data-stu-id="d1399-135">Data type: Contract</span></span>  
  
 <span data-ttu-id="d1399-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-137">协定为双工协定时的回调类型。</span><span class="sxs-lookup"><span data-stu-id="d1399-137">The type of callback when the contract is a duplex contract.</span></span>  
  
### <a name="sessionmode"></a><span data-ttu-id="d1399-138">SessionMode</span><span class="sxs-lookup"><span data-stu-id="d1399-138">SessionMode</span></span>  

 <span data-ttu-id="d1399-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d1399-139">Data type: string</span></span>  
  
 <span data-ttu-id="d1399-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-141">指示协定是否要求与此协定关联的绑定来使用通道会话。</span><span class="sxs-lookup"><span data-stu-id="d1399-141">Indicates whether the contract requires the binding associated with this contract to use channel sessions.</span></span>  
  
### <a name="type"></a><span data-ttu-id="d1399-142">类型</span><span class="sxs-lookup"><span data-stu-id="d1399-142">Type</span></span>  

 <span data-ttu-id="d1399-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d1399-143">Data type: string</span></span>  
  
 <span data-ttu-id="d1399-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d1399-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d1399-145">协定的类型。</span><span class="sxs-lookup"><span data-stu-id="d1399-145">The type of the contract.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1399-146">要求</span><span class="sxs-lookup"><span data-stu-id="d1399-146">Requirements</span></span>  
  
|<span data-ttu-id="d1399-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d1399-147">MOF</span></span>|<span data-ttu-id="d1399-148">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="d1399-148">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="d1399-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1399-149">Namespace</span></span>|<span data-ttu-id="d1399-150">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="d1399-150">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d1399-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1399-151">See also</span></span>

- <xref:System.ServiceModel.Description.ContractDescription>
