---
description: 了解详细信息：操作类
title: 操作类
ms.date: 03/30/2017
ms.assetid: b19d1496-ef06-4d0c-b2ae-e728ec00cca0
ms.openlocfilehash: 035c02bc05b7a64c5d15538001dbdcf2ec0b135b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803069"
---
# <a name="operation-class"></a><span data-ttu-id="86e8a-103">操作类</span><span class="sxs-lookup"><span data-stu-id="86e8a-103">Operation class</span></span>

<span data-ttu-id="86e8a-104">操作</span><span class="sxs-lookup"><span data-stu-id="86e8a-104">Operation</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86e8a-105">语法</span><span class="sxs-lookup"><span data-stu-id="86e8a-105">Syntax</span></span>  
  
```csharp
class Operation  
{  
  string Action;  
  boolean AsyncPattern;  
  Behavior Behaviors[];  
  boolean IsCallback;  
  boolean IsInitiating;  
  boolean IsOneWay;  
  boolean IsTerminating;  
  string MethodSignature;  
  string Name;  
  string ParameterTypes[];  
  string ReplyAction;  
  string ReturnType;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="86e8a-106">方法</span><span class="sxs-lookup"><span data-stu-id="86e8a-106">Methods</span></span>  

 <span data-ttu-id="86e8a-107">Operation 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="86e8a-107">The Operation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="86e8a-108">属性</span><span class="sxs-lookup"><span data-stu-id="86e8a-108">Properties</span></span>  

 <span data-ttu-id="86e8a-109">Operation 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="86e8a-109">The Operation class has the following properties:</span></span>  
  
### <a name="action"></a><span data-ttu-id="86e8a-110">操作</span><span class="sxs-lookup"><span data-stu-id="86e8a-110">Action</span></span>  

 <span data-ttu-id="86e8a-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="86e8a-111">Data type: string</span></span>  
  
 <span data-ttu-id="86e8a-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-113">请求消息的 WS-Addressing 操作。</span><span class="sxs-lookup"><span data-stu-id="86e8a-113">The WS-Addressing action of the request message.</span></span>  
  
### <a name="asyncpattern"></a><span data-ttu-id="86e8a-114">AsyncPattern</span><span class="sxs-lookup"><span data-stu-id="86e8a-114">AsyncPattern</span></span>  

 <span data-ttu-id="86e8a-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="86e8a-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="86e8a-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-117">指示操作是使用 `Begin` 服务协定中的 [左/右尖括号] 和 `End` [左/右尖括号] 方法对异步实现的。</span><span class="sxs-lookup"><span data-stu-id="86e8a-117">Indicates that an operation is implemented asynchronously using a `Begin`[open/close angle brackets] and `End`[open/close angle brackets] method pair in a service contract.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="86e8a-118">行为</span><span class="sxs-lookup"><span data-stu-id="86e8a-118">Behaviors</span></span>  

 <span data-ttu-id="86e8a-119">数据类型：Behavior array</span><span class="sxs-lookup"><span data-stu-id="86e8a-119">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="86e8a-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-121">与此操作关联的行为。</span><span class="sxs-lookup"><span data-stu-id="86e8a-121">The behaviors associated with this operation.</span></span>  
  
### <a name="iscallback"></a><span data-ttu-id="86e8a-122">IsCallback</span><span class="sxs-lookup"><span data-stu-id="86e8a-122">IsCallback</span></span>  

 <span data-ttu-id="86e8a-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="86e8a-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="86e8a-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-125">如果操作为回调操作，则为 True。</span><span class="sxs-lookup"><span data-stu-id="86e8a-125">True when the operation is a callback operation.</span></span>  
  
### <a name="isinitiating"></a><span data-ttu-id="86e8a-126">IsInitiating</span><span class="sxs-lookup"><span data-stu-id="86e8a-126">IsInitiating</span></span>  

 <span data-ttu-id="86e8a-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="86e8a-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="86e8a-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-129">指示方法是否实现了可以启动服务器上的某个会话的操作。</span><span class="sxs-lookup"><span data-stu-id="86e8a-129">Indicates whether the method implements an operation that can initiate a session on the server.</span></span>  
  
### <a name="isoneway"></a><span data-ttu-id="86e8a-130">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="86e8a-130">IsOneWay</span></span>  

 <span data-ttu-id="86e8a-131">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="86e8a-131">Data type: boolean</span></span>  
  
 <span data-ttu-id="86e8a-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-133">指示操作是否返回答复消息。</span><span class="sxs-lookup"><span data-stu-id="86e8a-133">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="isterminating"></a><span data-ttu-id="86e8a-134">IsTerminating</span><span class="sxs-lookup"><span data-stu-id="86e8a-134">IsTerminating</span></span>  

 <span data-ttu-id="86e8a-135">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="86e8a-135">Data type: boolean</span></span>  
  
 <span data-ttu-id="86e8a-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-137">指示操作是否返回答复消息。</span><span class="sxs-lookup"><span data-stu-id="86e8a-137">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="methodsignature"></a><span data-ttu-id="86e8a-138">MethodSignature</span><span class="sxs-lookup"><span data-stu-id="86e8a-138">MethodSignature</span></span>  

 <span data-ttu-id="86e8a-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="86e8a-139">Data type: string</span></span>  
  
 <span data-ttu-id="86e8a-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-141">操作的方法签名。</span><span class="sxs-lookup"><span data-stu-id="86e8a-141">The method signature of the operation.</span></span>  
  
### <a name="name"></a><span data-ttu-id="86e8a-142">名称</span><span class="sxs-lookup"><span data-stu-id="86e8a-142">Name</span></span>  

 <span data-ttu-id="86e8a-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="86e8a-143">Data type: string</span></span>  
  
 <span data-ttu-id="86e8a-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-145">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="86e8a-145">The name of the operation.</span></span>  
  
### <a name="parametertypes"></a><span data-ttu-id="86e8a-146">ParameterTypes</span><span class="sxs-lookup"><span data-stu-id="86e8a-146">ParameterTypes</span></span>  

 <span data-ttu-id="86e8a-147">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="86e8a-147">Data type: string array</span></span>  
  
 <span data-ttu-id="86e8a-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-149">操作的参数类型。</span><span class="sxs-lookup"><span data-stu-id="86e8a-149">The types of the parameters of the operation.</span></span>  
  
### <a name="replyaction"></a><span data-ttu-id="86e8a-150">ReplyAction</span><span class="sxs-lookup"><span data-stu-id="86e8a-150">ReplyAction</span></span>  

 <span data-ttu-id="86e8a-151">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="86e8a-151">Data type: string</span></span>  
  
 <span data-ttu-id="86e8a-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-153">用于该操作答复消息的 SOAP 操作的值。</span><span class="sxs-lookup"><span data-stu-id="86e8a-153">The value of the SOAP action for the reply message of the operation.</span></span>  
  
### <a name="returntype"></a><span data-ttu-id="86e8a-154">ReturnType</span><span class="sxs-lookup"><span data-stu-id="86e8a-154">ReturnType</span></span>  

 <span data-ttu-id="86e8a-155">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="86e8a-155">Data type: string</span></span>  
  
 <span data-ttu-id="86e8a-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="86e8a-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="86e8a-157">操作的返回类型。</span><span class="sxs-lookup"><span data-stu-id="86e8a-157">The return type of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86e8a-158">要求</span><span class="sxs-lookup"><span data-stu-id="86e8a-158">Requirements</span></span>  
  
|<span data-ttu-id="86e8a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="86e8a-159">MOF</span></span>|<span data-ttu-id="86e8a-160">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="86e8a-160">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="86e8a-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="86e8a-161">Namespace</span></span>|<span data-ttu-id="86e8a-162">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="86e8a-162">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="86e8a-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="86e8a-163">See also</span></span>

- <xref:System.ServiceModel.Description.OperationDescription>
