---
description: 了解详细信息： LocalServiceSecuritySettings
title: LocalServiceSecuritySettings
ms.date: 03/30/2017
ms.assetid: 490aa0e5-5242-4f8d-b505-5ec6287633b4
ms.openlocfilehash: f7220e8253c6ab218414c1be7ed90e5d593b4692
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743936"
---
# <a name="localservicesecuritysettings"></a><span data-ttu-id="7de5e-103">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="7de5e-103">LocalServiceSecuritySettings</span></span>

<span data-ttu-id="7de5e-104">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="7de5e-104">LocalServiceSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7de5e-105">语法</span><span class="sxs-lookup"><span data-stu-id="7de5e-105">Syntax</span></span>  
  
```csharp
class LocalServiceSecuritySettings  
{  
  boolean DetectReplays;  
  datetime InactivityTimeout;  
  datetime IssuedCookieLifetime;  
  sint32 MaxCachedCookies;  
  datetime MaxClockSkew;  
  sint32 MaxPendingSessions;  
  sint32 MaxStatefulNegotiations;  
  datetime NegotiationTimeout;  
  boolean ReconnectTransportOnFailure;  
  sint32 ReplayCacheSize;  
  datetime ReplayWindow;  
  datetime SessionKeyRenewalInterval;  
  datetime SessionKeyRolloverInterval;  
  datetime TimestampValidityDuration;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="7de5e-106">方法</span><span class="sxs-lookup"><span data-stu-id="7de5e-106">Methods</span></span>  

 <span data-ttu-id="7de5e-107">LocalServiceSecuritySettings 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="7de5e-107">The LocalServiceSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7de5e-108">属性</span><span class="sxs-lookup"><span data-stu-id="7de5e-108">Properties</span></span>  

 <span data-ttu-id="7de5e-109">LocalServiceSecuritySettings 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="7de5e-109">The LocalServiceSecuritySettings class has the following properties:</span></span>  
  
### <a name="detectreplays"></a><span data-ttu-id="7de5e-110">DetectReplays</span><span class="sxs-lookup"><span data-stu-id="7de5e-110">DetectReplays</span></span>  

 <span data-ttu-id="7de5e-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="7de5e-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="7de5e-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-113">一个布尔值，指定是否自动检测和处理针对通道的重放攻击。</span><span class="sxs-lookup"><span data-stu-id="7de5e-113">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="7de5e-114">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="7de5e-114">InactivityTimeout</span></span>  

 <span data-ttu-id="7de5e-115">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-115">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-117">服务支持的最大挂起安全会话数。</span><span class="sxs-lookup"><span data-stu-id="7de5e-117">The maximum number of pending security sessions that the service supports.</span></span>  
  
### <a name="issuedcookielifetime"></a><span data-ttu-id="7de5e-118">IssuedCookieLifetime</span><span class="sxs-lookup"><span data-stu-id="7de5e-118">IssuedCookieLifetime</span></span>  

 <span data-ttu-id="7de5e-119">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-119">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-121">一个时间跨度，指定颁发给所有新的安全 Cookie 的生存期。</span><span class="sxs-lookup"><span data-stu-id="7de5e-121">A TimeSpan that specifies the lifetime issued to all new security cookies.</span></span>  
  
### <a name="maxcachedcookies"></a><span data-ttu-id="7de5e-122">MaxCachedCookies</span><span class="sxs-lookup"><span data-stu-id="7de5e-122">MaxCachedCookies</span></span>  

 <span data-ttu-id="7de5e-123">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="7de5e-123">Data type: sint32</span></span>  
  
 <span data-ttu-id="7de5e-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-125">可以缓存的最大 Cookie 数。</span><span class="sxs-lookup"><span data-stu-id="7de5e-125">The maximum number of cookies that can be cached.</span></span>  
  
### <a name="maxclockskew"></a><span data-ttu-id="7de5e-126">MaxClockSkew</span><span class="sxs-lookup"><span data-stu-id="7de5e-126">MaxClockSkew</span></span>  

 <span data-ttu-id="7de5e-127">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-127">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-129">一个时间跨度，指定通信双方系统时钟之间的最大时间差。</span><span class="sxs-lookup"><span data-stu-id="7de5e-129">A TimeSpan that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span>  
  
### <a name="maxpendingsessions"></a><span data-ttu-id="7de5e-130">MaxPendingSessions</span><span class="sxs-lookup"><span data-stu-id="7de5e-130">MaxPendingSessions</span></span>  

 <span data-ttu-id="7de5e-131">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="7de5e-131">Data type: sint32</span></span>  
  
 <span data-ttu-id="7de5e-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-133">服务上的最大挂起连接数。</span><span class="sxs-lookup"><span data-stu-id="7de5e-133">The maximum number of pending connections on the service.</span></span>  
  
### <a name="maxstatefulnegotiations"></a><span data-ttu-id="7de5e-134">MaxStatefulNegotiations</span><span class="sxs-lookup"><span data-stu-id="7de5e-134">MaxStatefulNegotiations</span></span>  

 <span data-ttu-id="7de5e-135">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="7de5e-135">Data type: sint32</span></span>  
  
 <span data-ttu-id="7de5e-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-137">可以同时处于活动状态的安全协商数。</span><span class="sxs-lookup"><span data-stu-id="7de5e-137">The number of security negotiations that can be active concurrently.</span></span>  
  
### <a name="negotiationtimeout"></a><span data-ttu-id="7de5e-138">NegotiationTimeout</span><span class="sxs-lookup"><span data-stu-id="7de5e-138">NegotiationTimeout</span></span>  

 <span data-ttu-id="7de5e-139">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-139">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-141">一个时间跨度，指定服务器和客户端之间的安全协商阶段的最大持续时间。</span><span class="sxs-lookup"><span data-stu-id="7de5e-141">A TimeSpan that specifies the maximum duration for the security negotiation phase between server and client.</span></span>  
  
### <a name="reconnecttransportonfailure"></a><span data-ttu-id="7de5e-142">ReconnectTransportOnFailure</span><span class="sxs-lookup"><span data-stu-id="7de5e-142">ReconnectTransportOnFailure</span></span>  

 <span data-ttu-id="7de5e-143">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="7de5e-143">Data type: boolean</span></span>  
  
 <span data-ttu-id="7de5e-144">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-144">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-145">一个布尔值，指定使用 WS-ReliableMessaging 的连接是否将在传输失败后尝试重新连接。</span><span class="sxs-lookup"><span data-stu-id="7de5e-145">A Boolean value that specifies whether connections using WS-Reliable messaging attempt to reconnect after transport failures.</span></span>  
  
### <a name="replaycachesize"></a><span data-ttu-id="7de5e-146">ReplayCacheSize</span><span class="sxs-lookup"><span data-stu-id="7de5e-146">ReplayCacheSize</span></span>  

 <span data-ttu-id="7de5e-147">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="7de5e-147">Data type: sint32</span></span>  
  
 <span data-ttu-id="7de5e-148">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-148">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-149">用于重播检测的缓存 Nonce 的数目。</span><span class="sxs-lookup"><span data-stu-id="7de5e-149">The number of cached nonces used for replay detection.</span></span>  
  
### <a name="replaywindow"></a><span data-ttu-id="7de5e-150">ReplayWindow</span><span class="sxs-lookup"><span data-stu-id="7de5e-150">ReplayWindow</span></span>  

 <span data-ttu-id="7de5e-151">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-151">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-152">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-152">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-153">一个时间跨度，指定单个消息 Nonce 的有效持续时间。</span><span class="sxs-lookup"><span data-stu-id="7de5e-153">A TimeSpan that specifies the duration in which individual message nonces are valid.</span></span>  
  
### <a name="sessionkeyrenewalinterval"></a><span data-ttu-id="7de5e-154">SessionKeyRenewalInterval</span><span class="sxs-lookup"><span data-stu-id="7de5e-154">SessionKeyRenewalInterval</span></span>  

 <span data-ttu-id="7de5e-155">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-155">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-156">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-156">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-157">一个时间跨度，指定一个持续时间，发起方将在此段时间之后续订安全会话的密钥。</span><span class="sxs-lookup"><span data-stu-id="7de5e-157">A TimeSpan that specifies the duration after which the initiator renews the key for the security session.</span></span>  
  
### <a name="sessionkeyrolloverinterval"></a><span data-ttu-id="7de5e-158">SessionKeyRolloverInterval</span><span class="sxs-lookup"><span data-stu-id="7de5e-158">SessionKeyRolloverInterval</span></span>  

 <span data-ttu-id="7de5e-159">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-159">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-160">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-160">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-161">一个时间跨度，指定在密钥续订期间，上一个会话密钥对于传入消息有效的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="7de5e-161">A TimeSpan that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span>  
  
### <a name="timestampvalidityduration"></a><span data-ttu-id="7de5e-162">TimestampValidityDuration</span><span class="sxs-lookup"><span data-stu-id="7de5e-162">TimestampValidityDuration</span></span>  

 <span data-ttu-id="7de5e-163">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="7de5e-163">Data type: datetime</span></span>  
  
 <span data-ttu-id="7de5e-164">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7de5e-164">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7de5e-165">一个时间跨度，指定时间戳的有效持续时间。</span><span class="sxs-lookup"><span data-stu-id="7de5e-165">A TimeSpan that specifies the duration in which a time stamp is valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7de5e-166">要求</span><span class="sxs-lookup"><span data-stu-id="7de5e-166">Requirements</span></span>  
  
|<span data-ttu-id="7de5e-167">MOF</span><span class="sxs-lookup"><span data-stu-id="7de5e-167">MOF</span></span>|<span data-ttu-id="7de5e-168">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="7de5e-168">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7de5e-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="7de5e-169">Namespace</span></span>|<span data-ttu-id="7de5e-170">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="7de5e-170">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7de5e-171">请参阅</span><span class="sxs-lookup"><span data-stu-id="7de5e-171">See also</span></span>

- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
