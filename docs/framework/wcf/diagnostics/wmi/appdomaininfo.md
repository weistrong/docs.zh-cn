---
description: 了解详细信息： AppDomainInfo
title: AppDomainInfo
ms.date: 03/30/2017
ms.assetid: 6610b7d8-81eb-4bec-a543-9b72ad7b6f73
ms.openlocfilehash: 1e527f2a25c48a3bf35d974e3ac192d937a8a86e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757964"
---
# <a name="appdomaininfo"></a><span data-ttu-id="8f89a-103">AppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="8f89a-103">AppDomainInfo</span></span>

<span data-ttu-id="8f89a-104">应用程序域信息</span><span class="sxs-lookup"><span data-stu-id="8f89a-104">Application domain information</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f89a-105">语法</span><span class="sxs-lookup"><span data-stu-id="8f89a-105">Syntax</span></span>  
  
```csharp
class AppDomainInfo  
{  
  sint32 AppDomainId;  
  boolean IsDefault;  
  boolean LogMalformedMessages;  
  boolean LogMessagesAtServiceLevel;  
  boolean LogMessagesAtTransportLevel;  
  TraceListener MessageLoggingTraceListeners[];  
  string Name;  
  string PerformanceCounters;  
  sint32 ProcessId;  
  string ServiceConfigPath;  
  string TraceLevel;  
  TraceListener wmiTraceListeners[];  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8f89a-106">方法</span><span class="sxs-lookup"><span data-stu-id="8f89a-106">Methods</span></span>  

 <span data-ttu-id="8f89a-107">AppDomainInfo 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="8f89a-107">The AppDomainInfo class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="8f89a-108">属性</span><span class="sxs-lookup"><span data-stu-id="8f89a-108">Properties</span></span>  

 <span data-ttu-id="8f89a-109">AppDomainInfo 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="8f89a-109">The AppDomainInfo class has the following properties:</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="8f89a-110">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="8f89a-110">AppDomainId</span></span>  

 <span data-ttu-id="8f89a-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="8f89a-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="8f89a-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-113">Appdomain 的 ID。</span><span class="sxs-lookup"><span data-stu-id="8f89a-113">The Id of the appdomain.</span></span>  
  
### <a name="isdefault"></a><span data-ttu-id="8f89a-114">IsDefault</span><span class="sxs-lookup"><span data-stu-id="8f89a-114">IsDefault</span></span>  

 <span data-ttu-id="8f89a-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="8f89a-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="8f89a-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-117">指示该 appdomain 是否为默认 appdomain。</span><span class="sxs-lookup"><span data-stu-id="8f89a-117">Indicates whether the appdomain is the default appdomain.</span></span>  
  
### <a name="logmalformedmessages"></a><span data-ttu-id="8f89a-118">LogMalformedMessages</span><span class="sxs-lookup"><span data-stu-id="8f89a-118">LogMalformedMessages</span></span>  

 <span data-ttu-id="8f89a-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="8f89a-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="8f89a-120">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="8f89a-120">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="8f89a-121">一个值，指定是否记录格式不正确的消息。</span><span class="sxs-lookup"><span data-stu-id="8f89a-121">A value that specifies whether malformed messages are logged.</span></span>  
  
### <a name="logmessagesatservicelevel"></a><span data-ttu-id="8f89a-122">LogMessagesAtServiceLevel</span><span class="sxs-lookup"><span data-stu-id="8f89a-122">LogMessagesAtServiceLevel</span></span>  

 <span data-ttu-id="8f89a-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="8f89a-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="8f89a-124">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="8f89a-124">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="8f89a-125">一个值，指定是否在服务级别跟踪消息（在与加密和传输有关的转换之前）。</span><span class="sxs-lookup"><span data-stu-id="8f89a-125">A value that specifies whether messages are traced at the service level (before encryption and transport-related transforms).</span></span>  
  
### <a name="logmessagesattransportlevel"></a><span data-ttu-id="8f89a-126">LogMessagesAtTransportLevel</span><span class="sxs-lookup"><span data-stu-id="8f89a-126">LogMessagesAtTransportLevel</span></span>  

 <span data-ttu-id="8f89a-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="8f89a-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="8f89a-128">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="8f89a-128">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="8f89a-129">一个值，指定是否在传输级别跟踪消息。</span><span class="sxs-lookup"><span data-stu-id="8f89a-129">A value that specifies whether messages are traced at the transport level.</span></span>  
  
### <a name="messageloggingtracelisteners"></a><span data-ttu-id="8f89a-130">MessageLoggingTraceListeners</span><span class="sxs-lookup"><span data-stu-id="8f89a-130">MessageLoggingTraceListeners</span></span>  

 <span data-ttu-id="8f89a-131">数据类型：TraceListener 数组</span><span class="sxs-lookup"><span data-stu-id="8f89a-131">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="8f89a-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-133">侦听 System.Wmi.MessageLogging 跟踪源的集合跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="8f89a-133">The collection trace listeners that listen to the System.Wmi.MessageLogging trace source.</span></span>  
  
### <a name="name"></a><span data-ttu-id="8f89a-134">名称</span><span class="sxs-lookup"><span data-stu-id="8f89a-134">Name</span></span>  

 <span data-ttu-id="8f89a-135">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="8f89a-135">Data type: string</span></span>  
  
 <span data-ttu-id="8f89a-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-137">Appdomain 的名称。</span><span class="sxs-lookup"><span data-stu-id="8f89a-137">The name of the appdomain.</span></span>  
  
### <a name="performancecounters"></a><span data-ttu-id="8f89a-138">PerformanceCounters</span><span class="sxs-lookup"><span data-stu-id="8f89a-138">PerformanceCounters</span></span>  

 <span data-ttu-id="8f89a-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="8f89a-139">Data type: string</span></span>  
  
 <span data-ttu-id="8f89a-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-141">Appdomain 中的活动性能计数器的范围。</span><span class="sxs-lookup"><span data-stu-id="8f89a-141">The scope of active performance counters in the appdomain.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="8f89a-142">ProcessId</span><span class="sxs-lookup"><span data-stu-id="8f89a-142">ProcessId</span></span>  

 <span data-ttu-id="8f89a-143">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="8f89a-143">Data type: sint32</span></span>  
  
 <span data-ttu-id="8f89a-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-145">进程 ID。</span><span class="sxs-lookup"><span data-stu-id="8f89a-145">The process Id.</span></span>  
  
### <a name="serviceconfigpath"></a><span data-ttu-id="8f89a-146">ServiceConfigPath</span><span class="sxs-lookup"><span data-stu-id="8f89a-146">ServiceConfigPath</span></span>  

 <span data-ttu-id="8f89a-147">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="8f89a-147">Data type: string</span></span>  
  
 <span data-ttu-id="8f89a-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-149">服务配置的路径。</span><span class="sxs-lookup"><span data-stu-id="8f89a-149">The path to the configuration of the service.</span></span>  
  
### <a name="tracelevel"></a><span data-ttu-id="8f89a-150">TraceLevel</span><span class="sxs-lookup"><span data-stu-id="8f89a-150">TraceLevel</span></span>  

 <span data-ttu-id="8f89a-151">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="8f89a-151">Data type: string</span></span>  
  
 <span data-ttu-id="8f89a-152">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="8f89a-152">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="8f89a-153">System.Wmi 跟踪源的跟踪级别。</span><span class="sxs-lookup"><span data-stu-id="8f89a-153">The trace level of the System.Wmi trace source.</span></span>  
  
### <a name="servicemodeltracelisteners"></a><span data-ttu-id="8f89a-154">ServiceModelTraceListeners</span><span class="sxs-lookup"><span data-stu-id="8f89a-154">ServiceModelTraceListeners</span></span>  

 <span data-ttu-id="8f89a-155">数据类型：TraceListener 数组</span><span class="sxs-lookup"><span data-stu-id="8f89a-155">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="8f89a-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8f89a-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f89a-157">一个来自 System.ServiceModel 跟踪源的侦听器的集合。</span><span class="sxs-lookup"><span data-stu-id="8f89a-157">A collection of listeners from the System.ServiceModel trace source.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f89a-158">要求</span><span class="sxs-lookup"><span data-stu-id="8f89a-158">Requirements</span></span>  
  
|<span data-ttu-id="8f89a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="8f89a-159">MOF</span></span>|<span data-ttu-id="8f89a-160">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="8f89a-160">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="8f89a-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="8f89a-161">Namespace</span></span>|<span data-ttu-id="8f89a-162">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="8f89a-162">Defined in root\ServiceModel</span></span>|
