---
description: 了解详细信息： CallbackBehavior
title: CallbackBehavior
ms.date: 03/30/2017
ms.assetid: 42acd302-2b62-4849-a2d1-a03084343ecd
ms.openlocfilehash: fa9e403324afe818e247d1f751cce0ce7d5a6fb6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757756"
---
# <a name="callbackbehavior"></a><span data-ttu-id="50f3a-103">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="50f3a-103">CallbackBehavior</span></span>

<span data-ttu-id="50f3a-104">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="50f3a-104">CallbackBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50f3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="50f3a-105">Syntax</span></span>  
  
```csharp
class CallbackBehavior : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  boolean MaxItemsInObjectGraph;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="50f3a-106">方法</span><span class="sxs-lookup"><span data-stu-id="50f3a-106">Methods</span></span>  

 <span data-ttu-id="50f3a-107">CallbackBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="50f3a-107">The CallbackBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="50f3a-108">属性</span><span class="sxs-lookup"><span data-stu-id="50f3a-108">Properties</span></span>  

 <span data-ttu-id="50f3a-109">CallbackBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="50f3a-109">The CallbackBehavior class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="50f3a-110">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="50f3a-110">AutomaticSessionShutdown</span></span>  

 <span data-ttu-id="50f3a-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-113">如果为 true，则会话在服务关闭双工会话时自动关闭。</span><span class="sxs-lookup"><span data-stu-id="50f3a-113">When true, the session is automatically closed when a service closes a duplex session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="50f3a-114">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="50f3a-114">ConcurrencyMode</span></span>  

 <span data-ttu-id="50f3a-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="50f3a-115">Data type: string</span></span>  
<span data-ttu-id="50f3a-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-117">指定服务是支持一个线程、多个线程还是支持可重入调用。</span><span class="sxs-lookup"><span data-stu-id="50f3a-117">Specifies whether the service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="50f3a-118">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="50f3a-118">IgnoreExtensionDataObject</span></span>  

 <span data-ttu-id="50f3a-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-121">一个值，指定是否将未知序列化数据发送到网络上。</span><span class="sxs-lookup"><span data-stu-id="50f3a-121">A value that specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="50f3a-122">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="50f3a-122">IncludeExceptionDetailInFaults</span></span>  

 <span data-ttu-id="50f3a-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-125">如果启用，则回调异常的详细信息被附加到服务所返回的错误中。</span><span class="sxs-lookup"><span data-stu-id="50f3a-125">When enabled, details about exceptions on the callback are attached to the faults returned to the service.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="50f3a-126">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="50f3a-126">MaxItemsInObjectGraph</span></span>  

 <span data-ttu-id="50f3a-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-129">序列化对象中允许的最大项数。</span><span class="sxs-lookup"><span data-stu-id="50f3a-129">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="50f3a-130">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="50f3a-130">UseSynchronizationContext</span></span>  

 <span data-ttu-id="50f3a-131">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-131">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-133">指定是否使用当前同步上下文来选择执行的线程。</span><span class="sxs-lookup"><span data-stu-id="50f3a-133">Specifies whether to use the current synchronization context to choose the thread of execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="50f3a-134">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="50f3a-134">ValidateMustUnderstand</span></span>  

 <span data-ttu-id="50f3a-135">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="50f3a-135">Data type: boolean</span></span>  
  
 <span data-ttu-id="50f3a-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="50f3a-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="50f3a-137">指定系统或应用程序是否强制执行 SOAP MustUnderstand 标头处理。</span><span class="sxs-lookup"><span data-stu-id="50f3a-137">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50f3a-138">要求</span><span class="sxs-lookup"><span data-stu-id="50f3a-138">Requirements</span></span>  
  
|<span data-ttu-id="50f3a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="50f3a-139">MOF</span></span>|<span data-ttu-id="50f3a-140">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="50f3a-140">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="50f3a-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="50f3a-141">Namespace</span></span>|<span data-ttu-id="50f3a-142">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="50f3a-142">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="50f3a-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="50f3a-143">See also</span></span>

- <xref:System.ServiceModel.CallbackBehaviorAttribute>
