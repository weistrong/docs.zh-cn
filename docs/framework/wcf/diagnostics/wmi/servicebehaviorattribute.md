---
description: 了解详细信息： ServiceBehaviorAttribute
title: ServiceBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 5faa266f-587f-4e03-828d-1c7dd5acfe65
ms.openlocfilehash: 57ffa9103523618db752b3be6d43bb16603d1728
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715569"
---
# <a name="servicebehaviorattribute"></a><span data-ttu-id="b9337-103">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="b9337-103">ServiceBehaviorAttribute</span></span>

<span data-ttu-id="b9337-104">ServiceBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="b9337-104">ServiceBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9337-105">语法</span><span class="sxs-lookup"><span data-stu-id="b9337-105">Syntax</span></span>  
  
```csharp
class ServiceBehaviorAttribute : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  string ConfigurationName;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  string InstanceContextMode;  
  sint32 MaxItemsInObjectGraph;  
  string Name;  
  string Namespace;  
  boolean ReleaseServiceInstanceOnTransactionComplete;  
  boolean TransactionAutoCompleteOnSessionClose;  
  string TransactionIsolationLevel;  
  datetime TransactionTimeout;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b9337-106">方法</span><span class="sxs-lookup"><span data-stu-id="b9337-106">Methods</span></span>  

 <span data-ttu-id="b9337-107">ServiceBehaviorAttribute 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="b9337-107">The ServiceBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b9337-108">属性</span><span class="sxs-lookup"><span data-stu-id="b9337-108">Properties</span></span>  

 <span data-ttu-id="b9337-109">ServiceBehaviorAttribute 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="b9337-109">The ServiceBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="b9337-110">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="b9337-110">AutomaticSessionShutdown</span></span>  

 <span data-ttu-id="b9337-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-113">指示在客户端关闭输出会话时是否自动关闭会话。</span><span class="sxs-lookup"><span data-stu-id="b9337-113">Indicates whether to automatically close a session when a client closes an output session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="b9337-114">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="b9337-114">ConcurrencyMode</span></span>  

 <span data-ttu-id="b9337-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-115">Data type: string</span></span>  
<span data-ttu-id="b9337-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-117">指示服务是支持单线程、多线程还是支持可重入调用。</span><span class="sxs-lookup"><span data-stu-id="b9337-117">Indicates whether a service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="configurationname"></a><span data-ttu-id="b9337-118">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b9337-118">ConfigurationName</span></span>  

 <span data-ttu-id="b9337-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-119">Data type: string</span></span>  
  
 <span data-ttu-id="b9337-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-121">服务配置的名称。</span><span class="sxs-lookup"><span data-stu-id="b9337-121">The name of the service configuration.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="b9337-122">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="b9337-122">IgnoreExtensionDataObject</span></span>  

 <span data-ttu-id="b9337-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-125">指定是否要将未知序列化数据发送到网络上。</span><span class="sxs-lookup"><span data-stu-id="b9337-125">Specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="b9337-126">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="b9337-126">IncludeExceptionDetailInFaults</span></span>  

 <span data-ttu-id="b9337-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-129">指定是否在返回给客户端的 SOAP 错误详细信息中包含托管异常信息以供调试。</span><span class="sxs-lookup"><span data-stu-id="b9337-129">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
### <a name="instancecontextmode"></a><span data-ttu-id="b9337-130">InstanceContextMode</span><span class="sxs-lookup"><span data-stu-id="b9337-130">InstanceContextMode</span></span>  

 <span data-ttu-id="b9337-131">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-131">Data type: string</span></span>  
  
 <span data-ttu-id="b9337-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-133">指定何时创建新服务对象。</span><span class="sxs-lookup"><span data-stu-id="b9337-133">Specifies when a new service object is created.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="b9337-134">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="b9337-134">MaxItemsInObjectGraph</span></span>  

 <span data-ttu-id="b9337-135">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="b9337-135">Data type: sint32</span></span>  
  
 <span data-ttu-id="b9337-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-137">序列化对象中允许的最大项数。</span><span class="sxs-lookup"><span data-stu-id="b9337-137">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="name"></a><span data-ttu-id="b9337-138">名称</span><span class="sxs-lookup"><span data-stu-id="b9337-138">Name</span></span>  

 <span data-ttu-id="b9337-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-139">Data type: string</span></span>  
  
 <span data-ttu-id="b9337-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-141">WSDL 中服务的名称属性。</span><span class="sxs-lookup"><span data-stu-id="b9337-141">The name attribute of the service in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="b9337-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="b9337-142">Namespace</span></span>  

 <span data-ttu-id="b9337-143">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-143">Data type: string</span></span>  
  
 <span data-ttu-id="b9337-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-145">WSDL 中服务的目标命名空间。</span><span class="sxs-lookup"><span data-stu-id="b9337-145">The target namespace of the service in WSDL.</span></span>  
  
### <a name="releaseserviceinstanceontransactioncomplete"></a><span data-ttu-id="b9337-146">ReleaseServiceInstanceOnTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="b9337-146">ReleaseServiceInstanceOnTransactionComplete</span></span>  

 <span data-ttu-id="b9337-147">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-147">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-149">指定当前事务完成后，是否回收服务对象。</span><span class="sxs-lookup"><span data-stu-id="b9337-149">Specifies whether the service object is recycled when the current transaction completes.</span></span>  
  
### <a name="transactionautocompleteonsessionclose"></a><span data-ttu-id="b9337-150">TransactionAutoCompleteOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="b9337-150">TransactionAutoCompleteOnSessionClose</span></span>  

 <span data-ttu-id="b9337-151">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-151">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-153">指定当前会话关闭时，挂起的事务是否已完成。</span><span class="sxs-lookup"><span data-stu-id="b9337-153">Specifies whether pending transactions are completed when the current session closes.</span></span>  
  
### <a name="transactionisolationlevel"></a><span data-ttu-id="b9337-154">TransactionIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="b9337-154">TransactionIsolationLevel</span></span>  

 <span data-ttu-id="b9337-155">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b9337-155">Data type: string</span></span>  
  
 <span data-ttu-id="b9337-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-157">指定事务隔离级别。</span><span class="sxs-lookup"><span data-stu-id="b9337-157">Specifies the transaction isolation level.</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="b9337-158">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="b9337-158">TransactionTimeout</span></span>  

 <span data-ttu-id="b9337-159">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="b9337-159">Data type: datetime</span></span>  
  
 <span data-ttu-id="b9337-160">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-160">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-161">事务必须在此期间完成的时间段。</span><span class="sxs-lookup"><span data-stu-id="b9337-161">The period within which a transaction must complete.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="b9337-162">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="b9337-162">UseSynchronizationContext</span></span>  

 <span data-ttu-id="b9337-163">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-163">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-164">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-164">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-165">指定是否使用当前同步上下文来选择线程执行。</span><span class="sxs-lookup"><span data-stu-id="b9337-165">Specifies whether to use the current synchronization context to choose the thread execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="b9337-166">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="b9337-166">ValidateMustUnderstand</span></span>  

 <span data-ttu-id="b9337-167">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="b9337-167">Data type: boolean</span></span>  
  
 <span data-ttu-id="b9337-168">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b9337-168">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b9337-169">指定系统或应用程序是否强制执行 SOAP MustUnderstand 标头处理。</span><span class="sxs-lookup"><span data-stu-id="b9337-169">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9337-170">要求</span><span class="sxs-lookup"><span data-stu-id="b9337-170">Requirements</span></span>  
  
|<span data-ttu-id="b9337-171">MOF</span><span class="sxs-lookup"><span data-stu-id="b9337-171">MOF</span></span>|<span data-ttu-id="b9337-172">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="b9337-172">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b9337-173">命名空间</span><span class="sxs-lookup"><span data-stu-id="b9337-173">Namespace</span></span>|<span data-ttu-id="b9337-174">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="b9337-174">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b9337-175">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9337-175">See also</span></span>

- <xref:System.ServiceModel.ServiceBehaviorAttribute>
