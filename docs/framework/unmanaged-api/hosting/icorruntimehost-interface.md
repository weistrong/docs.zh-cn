---
description: 了解详细信息： ICorRuntimeHost 接口
title: ICorRuntimeHost 接口
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost
helpviewer_keywords:
- ICorRuntimeHost interface [.NET Framework hosting]
ms.assetid: 4369533d-7834-4497-bc37-bfea0ad737b1
topic_type:
- apiref
ms.openlocfilehash: cd50d31668b2dd0718dbe644343bfe314a0afdbe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789653"
---
# <a name="icorruntimehost-interface"></a><span data-ttu-id="de7b1-103">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="de7b1-103">ICorRuntimeHost Interface</span></span>

<span data-ttu-id="de7b1-104">提供一些方法，这些方法使宿主可以显式启动和停止公共语言运行时 (CLR) ，以创建和配置应用程序域、访问默认域以及枚举在进程中运行的所有域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-104">Provides methods that enable the host to start and stop the common language runtime (CLR) explicitly, to create and configure application domains, to access the default domain, and to enumerate all domains running in the process.</span></span>  
  
 <span data-ttu-id="de7b1-105">在 .NET Framework 版本2.0 中，此接口由 [ICLRRuntimeHost](iclrruntimehost-interface.md)取代。</span><span class="sxs-lookup"><span data-stu-id="de7b1-105">In the .NET Framework version 2.0, this interface is superceded by [ICLRRuntimeHost](iclrruntimehost-interface.md).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="de7b1-106">方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-106">Methods</span></span>  
  
|<span data-ttu-id="de7b1-107">方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-107">Method</span></span>|<span data-ttu-id="de7b1-108">说明</span><span class="sxs-lookup"><span data-stu-id="de7b1-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="de7b1-109">CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-109">CloseEnum Method</span></span>](icorruntimehost-closeenum-method.md)|<span data-ttu-id="de7b1-110">将域枚举器重置回域列表的开头。</span><span class="sxs-lookup"><span data-stu-id="de7b1-110">Resets a domain enumerator back to the beginning of the domain list.</span></span>|  
|[<span data-ttu-id="de7b1-111">CreateDomain 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-111">CreateDomain Method</span></span>](icorruntimehost-createdomain-method.md)|<span data-ttu-id="de7b1-112">创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-112">Creates an application domain.</span></span> <span data-ttu-id="de7b1-113">调用方接收类型为的实例的接口指针 <xref:System._AppDomain> <xref:System.AppDomain?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="de7b1-113">The caller receives an interface pointer of type <xref:System._AppDomain> to an instance of type <xref:System.AppDomain?displayProperty=nameWithType>.</span></span>|  
|[<span data-ttu-id="de7b1-114">CreateDomainEx 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-114">CreateDomainEx Method</span></span>](icorruntimehost-createdomainex-method.md)|<span data-ttu-id="de7b1-115">创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-115">Creates an application domain.</span></span> <span data-ttu-id="de7b1-116">此方法允许调用方传递 IAppDomainSetup 实例，以配置返回的实例的附加功能 <xref:System._AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="de7b1-116">This method allows the caller to pass an IAppDomainSetup instance to configure additional features of the returned <xref:System._AppDomain> instance.</span></span>|  
|[<span data-ttu-id="de7b1-117">CreateDomainSetup 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-117">CreateDomainSetup Method</span></span>](icorruntimehost-createdomainsetup-method.md)|<span data-ttu-id="de7b1-118">获取实例的类型的接口指针 `IAppDomainSetup` <xref:System.AppDomainSetup> 。</span><span class="sxs-lookup"><span data-stu-id="de7b1-118">Gets an interface pointer of type `IAppDomainSetup` to an <xref:System.AppDomainSetup> instance.</span></span> <span data-ttu-id="de7b1-119">`IAppDomainSetup` 提供用于配置应用程序域在创建之前的各个方面的方法。</span><span class="sxs-lookup"><span data-stu-id="de7b1-119">`IAppDomainSetup` provides methods to configure aspects of an application domain before it is created.</span></span>|  
|[<span data-ttu-id="de7b1-120">CreateEvidence 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-120">CreateEvidence Method</span></span>](icorruntimehost-createevidence-method.md)|<span data-ttu-id="de7b1-121">获取类型的接口指针 <xref:System.Security.Principal.IIdentity> ，该指针允许主机创建要传递给 [CreateDomain](icorruntimehost-createdomain-method.md) 或 [CreateDomainEx](icorruntimehost-createdomainex-method.md)的安全证据。</span><span class="sxs-lookup"><span data-stu-id="de7b1-121">Gets an interface pointer of type <xref:System.Security.Principal.IIdentity>, which allows the host to create security evidence to pass to [CreateDomain](icorruntimehost-createdomain-method.md) or [CreateDomainEx](icorruntimehost-createdomainex-method.md).</span></span>|  
|[<span data-ttu-id="de7b1-122">CreateLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-122">CreateLogicalThreadState Method</span></span>](icorruntimehost-createlogicalthreadstate-method.md)|<span data-ttu-id="de7b1-123">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="de7b1-123">Do not use.</span></span>|  
|[<span data-ttu-id="de7b1-124">CurrentDomain 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-124">CurrentDomain Method</span></span>](icorruntimehost-currentdomain-method.md)|<span data-ttu-id="de7b1-125">获取类型的接口指针 <xref:System._AppDomain> ，该指针表示当前线程上加载的域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-125">Gets an interface pointer of type <xref:System._AppDomain> that represents the domain loaded on the current thread.</span></span>|  
|[<span data-ttu-id="de7b1-126">DeleteLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-126">DeleteLogicalThreadState Method</span></span>](icorruntimehost-deletelogicalthreadstate-method.md)|<span data-ttu-id="de7b1-127">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="de7b1-127">Do not use.</span></span>|  
|[<span data-ttu-id="de7b1-128">EnumDomains 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-128">EnumDomains Method</span></span>](icorruntimehost-enumdomains-method.md)|<span data-ttu-id="de7b1-129">获取当前进程中的域的枚举数。</span><span class="sxs-lookup"><span data-stu-id="de7b1-129">Gets an enumerator for the domains in the current process.</span></span>|  
|[<span data-ttu-id="de7b1-130">GetConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-130">GetConfiguration Method</span></span>](icorruntimehost-getconfiguration-method.md)|<span data-ttu-id="de7b1-131">获取一个对象，该对象允许宿主指定 CLR 的回调配置。</span><span class="sxs-lookup"><span data-stu-id="de7b1-131">Gets an object that allows the host to specify the callback configuration of the CLR.</span></span>|  
|[<span data-ttu-id="de7b1-132">GetDefaultDomain 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-132">GetDefaultDomain Method</span></span>](icorruntimehost-getdefaultdomain-method.md)|<span data-ttu-id="de7b1-133">获取类型的接口指针 <xref:System._AppDomain> ，该指针表示当前进程的默认域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-133">Gets an interface pointer of type <xref:System._AppDomain> that represents the default domain for the current process.</span></span>|  
|[<span data-ttu-id="de7b1-134">LocksHeldByLogicalThread 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-134">LocksHeldByLogicalThread Method</span></span>](icorruntimehost-locksheldbylogicalthread-method.md)|<span data-ttu-id="de7b1-135">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="de7b1-135">Do not use.</span></span>|  
|[<span data-ttu-id="de7b1-136">MapFile 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-136">MapFile Method</span></span>](icorruntimehost-mapfile-method.md)|<span data-ttu-id="de7b1-137">将指定的文件映射到内存。</span><span class="sxs-lookup"><span data-stu-id="de7b1-137">Maps the specified file into memory.</span></span> <span data-ttu-id="de7b1-138">此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="de7b1-138">This method is obsolete.</span></span>|  
|[<span data-ttu-id="de7b1-139">NextDomain 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-139">NextDomain Method</span></span>](icorruntimehost-nextdomain-method.md)|<span data-ttu-id="de7b1-140">获取一个接口指针，该指针指向枚举中的下一个域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-140">Gets an interface pointer to the next domain in the enumeration.</span></span>|  
|[<span data-ttu-id="de7b1-141">Start 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-141">Start Method</span></span>](icorruntimehost-start-method.md)|<span data-ttu-id="de7b1-142">启动 CLR。</span><span class="sxs-lookup"><span data-stu-id="de7b1-142">Starts the CLR.</span></span>|  
|[<span data-ttu-id="de7b1-143">Stop 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-143">Stop Method</span></span>](icorruntimehost-stop-method.md)|<span data-ttu-id="de7b1-144">停止执行当前进程的运行时中的代码。</span><span class="sxs-lookup"><span data-stu-id="de7b1-144">Stops the execution of code in the runtime for the current process.</span></span>|  
|[<span data-ttu-id="de7b1-145">SwitchInLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-145">SwitchInLogicalThreadState Method</span></span>](icorruntimehost-switchinlogicalthreadstate-method.md)|<span data-ttu-id="de7b1-146">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="de7b1-146">Do not use.</span></span>|  
|[<span data-ttu-id="de7b1-147">SwitchOutLogicalThreadState 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-147">SwitchOutLogicalThreadState Method</span></span>](icorruntimehost-switchoutlogicalthreadstate-method.md)|<span data-ttu-id="de7b1-148">请勿使用。</span><span class="sxs-lookup"><span data-stu-id="de7b1-148">Do not use.</span></span>|  
|[<span data-ttu-id="de7b1-149">UnloadDomain 方法</span><span class="sxs-lookup"><span data-stu-id="de7b1-149">UnloadDomain Method</span></span>](icorruntimehost-unloaddomain-method.md)|<span data-ttu-id="de7b1-150">从当前进程中卸载指定的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="de7b1-150">Unloads the specified application domain from the current process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="de7b1-151">要求</span><span class="sxs-lookup"><span data-stu-id="de7b1-151">Requirements</span></span>  

 <span data-ttu-id="de7b1-152">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="de7b1-152">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de7b1-153">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="de7b1-153">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="de7b1-154">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="de7b1-154">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="de7b1-155">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="de7b1-155">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de7b1-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="de7b1-156">See also</span></span>

- <xref:System.AppDomain>
- [<span data-ttu-id="de7b1-157">承载</span><span class="sxs-lookup"><span data-stu-id="de7b1-157">Hosting</span></span>](index.md)
- [<span data-ttu-id="de7b1-158">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="de7b1-158">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)
- <span data-ttu-id="de7b1-159">[运行时主机](/previous-versions/dotnet/netframework-4.0/a51xd4ze(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="de7b1-159">[Runtime Hosts](/previous-versions/dotnet/netframework-4.0/a51xd4ze(v=vs.100))</span></span>
- [<span data-ttu-id="de7b1-160">承载接口</span><span class="sxs-lookup"><span data-stu-id="de7b1-160">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="de7b1-161">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="de7b1-161">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)
