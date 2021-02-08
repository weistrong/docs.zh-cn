---
description: 了解详细信息： OperationBehaviorAttribute
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: c1f1b80134163ee65d5015e52017f5bb455aeac7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803056"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="13daa-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="13daa-103">OperationBehaviorAttribute</span></span>

<span data-ttu-id="13daa-104">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="13daa-104">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13daa-105">语法</span><span class="sxs-lookup"><span data-stu-id="13daa-105">Syntax</span></span>  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="13daa-106">方法</span><span class="sxs-lookup"><span data-stu-id="13daa-106">Methods</span></span>  

 <span data-ttu-id="13daa-107">OperationBehaviorAttribute 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="13daa-107">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="13daa-108">属性</span><span class="sxs-lookup"><span data-stu-id="13daa-108">Properties</span></span>  

 <span data-ttu-id="13daa-109">OperationBehaviorAttribute 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="13daa-109">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="13daa-110">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="13daa-110">AutoDisposeParameters</span></span>  

 <span data-ttu-id="13daa-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="13daa-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="13daa-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="13daa-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="13daa-113">参数自动释放功能的状态。</span><span class="sxs-lookup"><span data-stu-id="13daa-113">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="13daa-114">模拟</span><span class="sxs-lookup"><span data-stu-id="13daa-114">Impersonation</span></span>  

 <span data-ttu-id="13daa-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="13daa-115">Data type: string</span></span>  
  
 <span data-ttu-id="13daa-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="13daa-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="13daa-117">指示操作支持的调用方模拟级别。</span><span class="sxs-lookup"><span data-stu-id="13daa-117">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="13daa-118">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="13daa-118">ReleaseInstanceMode</span></span>  

 <span data-ttu-id="13daa-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="13daa-119">Data type: string</span></span>  
  
 <span data-ttu-id="13daa-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="13daa-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="13daa-121">指示操作调用过程中何时回收对象。</span><span class="sxs-lookup"><span data-stu-id="13daa-121">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="13daa-122">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="13daa-122">TransactionAutoComplete</span></span>  

 <span data-ttu-id="13daa-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="13daa-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="13daa-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="13daa-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="13daa-125">指示在未发生未处理的异常的情况下是否自动提交当前事务。</span><span class="sxs-lookup"><span data-stu-id="13daa-125">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="13daa-126">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="13daa-126">TransactionScopeRequired</span></span>  

 <span data-ttu-id="13daa-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="13daa-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="13daa-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="13daa-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="13daa-129">指示操作是否需要事务处理。</span><span class="sxs-lookup"><span data-stu-id="13daa-129">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13daa-130">要求</span><span class="sxs-lookup"><span data-stu-id="13daa-130">Requirements</span></span>  
  
|<span data-ttu-id="13daa-131">MOF</span><span class="sxs-lookup"><span data-stu-id="13daa-131">MOF</span></span>|<span data-ttu-id="13daa-132">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="13daa-132">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="13daa-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="13daa-133">Namespace</span></span>|<span data-ttu-id="13daa-134">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="13daa-134">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="13daa-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="13daa-135">See also</span></span>

- <xref:System.ServiceModel.OperationBehaviorAttribute>
