---
description: 了解更多：弃用的 CLR 承载函数
title: 弃用的 CLR 承载函数
ms.date: 03/30/2017
helpviewer_keywords:
- .NET Framework 1.1, hosting global static functions
- global static functions [.NET Framework hosting], version 2.0
- .NET Framework 2.0, hosting global static functions
- hosting global static functions [.NET Framework], version 2.0
ms.assetid: 91fbbb35-e543-4814-b806-371cebae8c5a
ms.openlocfilehash: 3d16b5829e29c5c963f4790bbb3be7adcaeedbfc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785661"
---
# <a name="deprecated-clr-hosting-functions"></a><span data-ttu-id="466da-103">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="466da-103">Deprecated CLR Hosting Functions</span></span>

<span data-ttu-id="466da-104">本部分介绍了早期版本的托管 API 使用的非托管全局静态函数。</span><span class="sxs-lookup"><span data-stu-id="466da-104">This section describes the unmanaged global static functions that earlier versions of the hosting API used.</span></span>  
  
 <span data-ttu-id="466da-105">除了基础结构函数 (`_Cor*` 函数) （仅由 .NET Framework 使用），这些函数在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-105">With the exception of the infrastructure functions (`_Cor*` functions), which are used only by the .NET Framework, these functions have been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="activation-functions"></a><span data-ttu-id="466da-106">激活函数</span><span class="sxs-lookup"><span data-stu-id="466da-106">Activation functions</span></span>  

 [<span data-ttu-id="466da-107">ClrCreateManagedInstance 函数</span><span class="sxs-lookup"><span data-stu-id="466da-107">ClrCreateManagedInstance Function</span></span>](clrcreatemanagedinstance-function.md)  
 <span data-ttu-id="466da-108">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-108">Deprecated.</span></span> <span data-ttu-id="466da-109">创建指定托管类型的实例。</span><span class="sxs-lookup"><span data-stu-id="466da-109">Creates an instance of the specified managed type.</span></span>  
  
 [<span data-ttu-id="466da-110">CoInitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="466da-110">CoInitializeCor Function</span></span>](coinitializecor-function.md)  
 <span data-ttu-id="466da-111">已过时。</span><span class="sxs-lookup"><span data-stu-id="466da-111">Obsolete.</span></span> <span data-ttu-id="466da-112">若要 (CLR) 初始化公共语言运行时，请使用 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 或 [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md)。</span><span class="sxs-lookup"><span data-stu-id="466da-112">To initialize the common language runtime (CLR), use either [CorBindToRuntimeEx](corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md).</span></span>  
  
 [<span data-ttu-id="466da-113">CoInitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="466da-113">CoInitializeEE Function</span></span>](coinitializeee-function.md)  
 <span data-ttu-id="466da-114">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-114">Deprecated.</span></span> <span data-ttu-id="466da-115">确保 CLR 执行引擎已加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="466da-115">Ensures that the CLR execution engine is loaded into a process.</span></span> <span data-ttu-id="466da-116">改为使用 [ICLRRuntimeHost：： Start](iclrruntimehost-start-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="466da-116">Use the [ICLRRuntimeHost::Start](iclrruntimehost-start-method.md) method instead.</span></span>  
  
 [<span data-ttu-id="466da-117">CorBindToCurrentRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="466da-117">CorBindToCurrentRuntime Function</span></span>](corbindtocurrentruntime-function.md)  
 <span data-ttu-id="466da-118">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-118">Deprecated.</span></span> <span data-ttu-id="466da-119">通过使用存储在 XML 文件中的版本信息，将 (CLR) 中的公共语言运行时加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="466da-119">Loads the common language runtime (CLR) into a process by using version information stored in an XML file.</span></span>  
  
 [<span data-ttu-id="466da-120">CorBindToRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="466da-120">CorBindToRuntime Function</span></span>](corbindtoruntime-function.md)  
 <span data-ttu-id="466da-121">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-121">Deprecated.</span></span> <span data-ttu-id="466da-122">使非托管宿主能够将 CLR 加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="466da-122">Enables unmanaged hosts to load the CLR into a process.</span></span>  
  
 [<span data-ttu-id="466da-123">CorBindToRuntimeByCfg 函数</span><span class="sxs-lookup"><span data-stu-id="466da-123">CorBindToRuntimeByCfg Function</span></span>](corbindtoruntimebycfg-function.md)  
 <span data-ttu-id="466da-124">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-124">Deprecated.</span></span> <span data-ttu-id="466da-125">使用从 XML 文件读取的版本信息将 CLR 加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="466da-125">Loads the CLR into a process by using version information that is read from an XML file.</span></span>  
  
 [<span data-ttu-id="466da-126">CorBindToRuntimeEx 函数</span><span class="sxs-lookup"><span data-stu-id="466da-126">CorBindToRuntimeEx Function</span></span>](corbindtoruntimeex-function.md)  
 <span data-ttu-id="466da-127">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-127">Deprecated.</span></span> <span data-ttu-id="466da-128">使非托管宿主能够将 CLR 加载到进程中，并允许您设置标志来指定 CLR 的行为。</span><span class="sxs-lookup"><span data-stu-id="466da-128">Enables unmanaged hosts to load the CLR into a process, and allows you to set flags to specify the behavior of the CLR.</span></span>  
  
 [<span data-ttu-id="466da-129">CorBindToRuntimeHost 函数</span><span class="sxs-lookup"><span data-stu-id="466da-129">CorBindToRuntimeHost Function</span></span>](corbindtoruntimehost-function.md)  
 <span data-ttu-id="466da-130">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-130">Deprecated.</span></span> <span data-ttu-id="466da-131">使宿主可以将指定版本的 CLR 加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="466da-131">Enables hosts to load a specified version of the CLR into a process.</span></span>  
  
 [<span data-ttu-id="466da-132">GetCORRequiredVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-132">GetCORRequiredVersion Function</span></span>](getcorrequiredversion-function.md)  
 <span data-ttu-id="466da-133">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-133">Deprecated.</span></span> <span data-ttu-id="466da-134">获取所需的 CLR 版本号。</span><span class="sxs-lookup"><span data-stu-id="466da-134">Gets the required CLR version number.</span></span>  
  
 [<span data-ttu-id="466da-135">GetCORSystemDirectory 函数</span><span class="sxs-lookup"><span data-stu-id="466da-135">GetCORSystemDirectory Function</span></span>](getcorsystemdirectory-function.md)  
 <span data-ttu-id="466da-136">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-136">Deprecated.</span></span> <span data-ttu-id="466da-137">返回加载到进程中的 CLR 的安装目录。</span><span class="sxs-lookup"><span data-stu-id="466da-137">Returns the installation directory of the CLR that is loaded into the process.</span></span>  
  
 [<span data-ttu-id="466da-138">GetRealProcAddress 函数</span><span class="sxs-lookup"><span data-stu-id="466da-138">GetRealProcAddress Function</span></span>](getrealprocaddress-function.md)  
 <span data-ttu-id="466da-139">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-139">Deprecated.</span></span> <span data-ttu-id="466da-140">获取从安装的最新版本的 CLR 导出的指定函数的地址。</span><span class="sxs-lookup"><span data-stu-id="466da-140">Gets the address of the specified function that is exported from the latest installed version of the CLR.</span></span>  
  
 [<span data-ttu-id="466da-141">GetRequestedRuntimeInfo 函数</span><span class="sxs-lookup"><span data-stu-id="466da-141">GetRequestedRuntimeInfo Function</span></span>](getrequestedruntimeinfo-function.md)  
 <span data-ttu-id="466da-142">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-142">Deprecated.</span></span> <span data-ttu-id="466da-143">获取有关应用程序请求的 CLR 的版本和目录信息。</span><span class="sxs-lookup"><span data-stu-id="466da-143">Gets version and directory information about the CLR requested by an application.</span></span>  
  
## <a name="clr-version-functions"></a><span data-ttu-id="466da-144">CLR 版本函数</span><span class="sxs-lookup"><span data-stu-id="466da-144">CLR version functions</span></span>  

 <span data-ttu-id="466da-145">本节中的函数返回 CLR 版本;它们不激活 CLR。</span><span class="sxs-lookup"><span data-stu-id="466da-145">The functions in this section return a CLR version; they do not activate the CLR.</span></span>  
  
 [<span data-ttu-id="466da-146">GetCORVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-146">GetCORVersion Function</span></span>](getcorversion-function.md)  
 <span data-ttu-id="466da-147">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-147">Deprecated.</span></span> <span data-ttu-id="466da-148">返回当前进程中正在运行的 CLR 的版本号。</span><span class="sxs-lookup"><span data-stu-id="466da-148">Returns the version number of the CLR that is running in the current process.</span></span>  
  
 [<span data-ttu-id="466da-149">GetFileVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-149">GetFileVersion Function</span></span>](getfileversion-function.md)  
 <span data-ttu-id="466da-150">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-150">Deprecated.</span></span> <span data-ttu-id="466da-151">使用指定的缓冲区获取指定文件的 CLR 版本信息。</span><span class="sxs-lookup"><span data-stu-id="466da-151">Gets the CLR version information of the specified file, using the specified buffer.</span></span>  
  
 [<span data-ttu-id="466da-152">GetRequestedRuntimeVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-152">GetRequestedRuntimeVersion Function</span></span>](getrequestedruntimeversion-function.md)  
 <span data-ttu-id="466da-153">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-153">Deprecated.</span></span> <span data-ttu-id="466da-154">获取指定应用程序请求的 CLR 的版本号。</span><span class="sxs-lookup"><span data-stu-id="466da-154">Gets the version number of the CLR requested by the specified application.</span></span> <span data-ttu-id="466da-155">如果未安装该版本，则获取在请求版本之前安装的最新版本。</span><span class="sxs-lookup"><span data-stu-id="466da-155">If that version is not installed, gets the most recent version that is installed before the requested version.</span></span>  
  
 [<span data-ttu-id="466da-156">GetRequestedRuntimeVersionForCLSID 函数</span><span class="sxs-lookup"><span data-stu-id="466da-156">GetRequestedRuntimeVersionForCLSID Function</span></span>](getrequestedruntimeversionforclsid-function.md)  
 <span data-ttu-id="466da-157">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-157">Deprecated.</span></span> <span data-ttu-id="466da-158">获取具有指定 CLSID 的类的相应 CLR 版本信息。</span><span class="sxs-lookup"><span data-stu-id="466da-158">Gets the appropriate CLR version information for the class with the specified CLSID.</span></span>  
  
 [<span data-ttu-id="466da-159">GetVersionFromProcess 函数</span><span class="sxs-lookup"><span data-stu-id="466da-159">GetVersionFromProcess Function</span></span>](getversionfromprocess-function.md)  
 <span data-ttu-id="466da-160">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-160">Deprecated.</span></span> <span data-ttu-id="466da-161">获取与指定的进程句柄关联的 CLR 的版本号。</span><span class="sxs-lookup"><span data-stu-id="466da-161">Gets the version number of the CLR that is associated with the specified process handle.</span></span>  
  
 [<span data-ttu-id="466da-162">LockClrVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-162">LockClrVersion Function</span></span>](lockclrversion-function.md)  
 <span data-ttu-id="466da-163">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-163">Deprecated.</span></span> <span data-ttu-id="466da-164">允许主机在显式初始化 CLR 之前确定将在进程内使用的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="466da-164">Allows the host to determine which version of the CLR will be used within the process before explicitly initializing the CLR.</span></span>  
  
## <a name="hosting-functions"></a><span data-ttu-id="466da-165">承载函数</span><span class="sxs-lookup"><span data-stu-id="466da-165">Hosting functions</span></span>  

 [<span data-ttu-id="466da-166">CallFunctionShim 函数</span><span class="sxs-lookup"><span data-stu-id="466da-166">CallFunctionShim Function</span></span>](callfunctionshim-function.md)  
 <span data-ttu-id="466da-167">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-167">Deprecated.</span></span> <span data-ttu-id="466da-168">对指定库中具有指定名称和参数的函数进行调用。</span><span class="sxs-lookup"><span data-stu-id="466da-168">Makes a call to the function that has the specified name and parameters in the specified library.</span></span>  
  
 [<span data-ttu-id="466da-169">CoEEShutDownCOM 函数</span><span class="sxs-lookup"><span data-stu-id="466da-169">CoEEShutDownCOM Function</span></span>](coeeshutdowncom-function.md)  
 <span data-ttu-id="466da-170">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-170">Deprecated.</span></span> <span data-ttu-id="466da-171">从进程中卸载 COM 程序集。</span><span class="sxs-lookup"><span data-stu-id="466da-171">Unloads a COM assembly from the process.</span></span>  
  
 [<span data-ttu-id="466da-172">CorExitProcess 函数</span><span class="sxs-lookup"><span data-stu-id="466da-172">CorExitProcess Function</span></span>](corexitprocess-function.md)  
 <span data-ttu-id="466da-173">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-173">Deprecated.</span></span> <span data-ttu-id="466da-174">关闭当前的非托管进程。</span><span class="sxs-lookup"><span data-stu-id="466da-174">Shuts down the current unmanaged process.</span></span>  
  
 [<span data-ttu-id="466da-175">CorLaunchApplication 函数</span><span class="sxs-lookup"><span data-stu-id="466da-175">CorLaunchApplication Function</span></span>](corlaunchapplication-function.md)  
 <span data-ttu-id="466da-176">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-176">Deprecated.</span></span> <span data-ttu-id="466da-177">使用指定的清单和其他应用程序数据，在指定的网络路径下启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="466da-177">Starts the application at the specified network path, using the specified manifests and other application data.</span></span>  
  
 [<span data-ttu-id="466da-178">CorMarkThreadInThreadPool 函数</span><span class="sxs-lookup"><span data-stu-id="466da-178">CorMarkThreadInThreadPool Function</span></span>](cormarkthreadinthreadpool-function.md)  
 <span data-ttu-id="466da-179">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-179">Deprecated.</span></span> <span data-ttu-id="466da-180">标记当前正在执行的线程池线程以执行托管代码。</span><span class="sxs-lookup"><span data-stu-id="466da-180">Marks the currently executing thread-pool thread for the execution of managed code.</span></span> <span data-ttu-id="466da-181">从 .NET Framework 版本2.0 开始，此函数不起作用。</span><span class="sxs-lookup"><span data-stu-id="466da-181">Starting with the .NET Framework version 2.0, this function has no effect.</span></span> <span data-ttu-id="466da-182">这不是必需的，并且可以从代码中删除。</span><span class="sxs-lookup"><span data-stu-id="466da-182">It is not required, and can be removed from your code.</span></span>  
  
 [<span data-ttu-id="466da-183">CoUninitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="466da-183">CoUninitializeCor Function</span></span>](couninitializecor-function.md)  
 <span data-ttu-id="466da-184">已过时。</span><span class="sxs-lookup"><span data-stu-id="466da-184">Obsolete.</span></span> <span data-ttu-id="466da-185">CLR 无法从进程中卸载。</span><span class="sxs-lookup"><span data-stu-id="466da-185">The CLR cannot be unloaded from a process.</span></span>  
  
 [<span data-ttu-id="466da-186">CoUninitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="466da-186">CoUninitializeEE Function</span></span>](couninitializeee-function.md)  
 <span data-ttu-id="466da-187">已过时。</span><span class="sxs-lookup"><span data-stu-id="466da-187">Obsolete.</span></span>  
  
 [<span data-ttu-id="466da-188">CreateDebuggingInterfaceFromVersion 函数</span><span class="sxs-lookup"><span data-stu-id="466da-188">CreateDebuggingInterfaceFromVersion Function</span></span>](createdebugginginterfacefromversion-function.md)  
 <span data-ttu-id="466da-189">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-189">Deprecated.</span></span> <span data-ttu-id="466da-190">基于指定的版本信息创建 [ICorDebug](../debugging/icordebug-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="466da-190">Creates an [ICorDebug](../debugging/icordebug-interface.md) object based on the specified version information.</span></span>  
  
 [<span data-ttu-id="466da-191">CreateICeeFileGen 函数</span><span class="sxs-lookup"><span data-stu-id="466da-191">CreateICeeFileGen Function</span></span>](createiceefilegen-function.md)  
 <span data-ttu-id="466da-192">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-192">Deprecated.</span></span> <span data-ttu-id="466da-193">创建 [ICeeFileGen](iceefilegen-class.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="466da-193">Creates an [ICeeFileGen](iceefilegen-class.md) object.</span></span>  
  
 [<span data-ttu-id="466da-194">DestroyICeeFileGen 函数</span><span class="sxs-lookup"><span data-stu-id="466da-194">DestroyICeeFileGen Function</span></span>](destroyiceefilegen-function.md)  
 <span data-ttu-id="466da-195">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-195">Deprecated.</span></span> <span data-ttu-id="466da-196">销毁 [ICeeFileGen](iceefilegen-class.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="466da-196">Destroys an [ICeeFileGen](iceefilegen-class.md) object.</span></span>  
  
 [<span data-ttu-id="466da-197">FExecuteInAppDomainCallback 函数指针</span><span class="sxs-lookup"><span data-stu-id="466da-197">FExecuteInAppDomainCallback Function Pointer</span></span>](fexecuteinappdomaincallback-function-pointer.md)  
 <span data-ttu-id="466da-198">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-198">Deprecated.</span></span> <span data-ttu-id="466da-199">指向 CLR 调用以执行托管代码的函数。</span><span class="sxs-lookup"><span data-stu-id="466da-199">Points to a function that the CLR calls to execute managed code.</span></span>  
  
 [<span data-ttu-id="466da-200">FLockClrVersionCallback 函数指针</span><span class="sxs-lookup"><span data-stu-id="466da-200">FLockClrVersionCallback Function Pointer</span></span>](flockclrversioncallback-function-pointer.md)  
 <span data-ttu-id="466da-201">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-201">Deprecated.</span></span> <span data-ttu-id="466da-202">指向一个函数，CLR 将调用该函数以通知宿主初始化已启动或已完成。</span><span class="sxs-lookup"><span data-stu-id="466da-202">Points to a function that the CLR calls to notify the host that initialization has either started or completed.</span></span>  
  
 [<span data-ttu-id="466da-203">GetCLRIdentityManager 函数</span><span class="sxs-lookup"><span data-stu-id="466da-203">GetCLRIdentityManager Function</span></span>](getclridentitymanager-function.md)  
 <span data-ttu-id="466da-204">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-204">Deprecated.</span></span> <span data-ttu-id="466da-205">获取一个指向接口的指针，该接口允许 CLR 管理标识。</span><span class="sxs-lookup"><span data-stu-id="466da-205">Gets a pointer to an interface that allows the CLR to manage identities.</span></span>  
  
 [<span data-ttu-id="466da-206">LoadLibraryShim 函数</span><span class="sxs-lookup"><span data-stu-id="466da-206">LoadLibraryShim Function</span></span>](loadlibraryshim-function.md)  
 <span data-ttu-id="466da-207">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-207">Deprecated.</span></span> <span data-ttu-id="466da-208">加载 .NET Framework DLL 的指定版本。</span><span class="sxs-lookup"><span data-stu-id="466da-208">Loads a specified version of a .NET Framework DLL.</span></span>  
  
 [<span data-ttu-id="466da-209">LoadStringRC 函数</span><span class="sxs-lookup"><span data-stu-id="466da-209">LoadStringRC Function</span></span>](loadstringrc-function.md)  
 <span data-ttu-id="466da-210">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-210">Deprecated.</span></span> <span data-ttu-id="466da-211">使用当前线程的默认区域性将 HRESULT 值转换为错误消息。</span><span class="sxs-lookup"><span data-stu-id="466da-211">Translates an HRESULT value into an error message by using the default culture of the current thread.</span></span>  
  
 [<span data-ttu-id="466da-212">LoadStringRCEx 函数</span><span class="sxs-lookup"><span data-stu-id="466da-212">LoadStringRCEx Function</span></span>](loadstringrcex-function.md)  
 <span data-ttu-id="466da-213">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-213">Deprecated.</span></span> <span data-ttu-id="466da-214">将 HRESULT 值转换为指定区域性的适当错误消息。</span><span class="sxs-lookup"><span data-stu-id="466da-214">Translates an HRESULT value to an appropriate error message for the specified culture.</span></span>  
  
 [<span data-ttu-id="466da-215">LPOVERLAPPED_COMPLETION_ROUTINE 函数指针</span><span class="sxs-lookup"><span data-stu-id="466da-215">LPOVERLAPPED_COMPLETION_ROUTINE Function Pointer</span></span>](lpoverlapped-completion-routine-function-pointer.md)  
 <span data-ttu-id="466da-216">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-216">Deprecated.</span></span> <span data-ttu-id="466da-217">指向一个函数，该函数在重叠 (即设备的异步) i/o 完成时通知宿主。</span><span class="sxs-lookup"><span data-stu-id="466da-217">Points to a function that notifies the host when an overlapped (that is, asynchronous) I/O to a device has completed.</span></span>  
  
 [<span data-ttu-id="466da-218">LPTHREAD_START_ROUTINE 函数指针</span><span class="sxs-lookup"><span data-stu-id="466da-218">LPTHREAD_START_ROUTINE Function Pointer</span></span>](lpthread-start-routine-function-pointer.md)  
 <span data-ttu-id="466da-219">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-219">Deprecated.</span></span> <span data-ttu-id="466da-220">指向一个函数，该函数通知宿主线程已开始执行。</span><span class="sxs-lookup"><span data-stu-id="466da-220">Points to a function that notifies the host that a thread has started to execute.</span></span>  
  
 [<span data-ttu-id="466da-221">RunDll32ShimW 函数</span><span class="sxs-lookup"><span data-stu-id="466da-221">RunDll32ShimW Function</span></span>](rundll32shimw-function.md)  
 <span data-ttu-id="466da-222">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-222">Deprecated.</span></span> <span data-ttu-id="466da-223">执行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="466da-223">Executes the specified command.</span></span>  
  
 [<span data-ttu-id="466da-224">WAITORTIMERCALLBACK 函数指针</span><span class="sxs-lookup"><span data-stu-id="466da-224">WAITORTIMERCALLBACK Function Pointer</span></span>](waitortimercallback-function-pointer.md)  
 <span data-ttu-id="466da-225">已弃用。</span><span class="sxs-lookup"><span data-stu-id="466da-225">Deprecated.</span></span> <span data-ttu-id="466da-226">指向一个函数，该函数通知宿主等待句柄已终止或超时。</span><span class="sxs-lookup"><span data-stu-id="466da-226">Points to a function that notifies the host that a wait handle has either been signaled or timed out.</span></span>  
  
## <a name="infrastructure-functions"></a><span data-ttu-id="466da-227">基础结构函数</span><span class="sxs-lookup"><span data-stu-id="466da-227">Infrastructure functions</span></span>  

 <span data-ttu-id="466da-228">本节中的函数仅供 .NET Framework 使用。</span><span class="sxs-lookup"><span data-stu-id="466da-228">The functions in this section are for use by the .NET Framework only.</span></span>  
  
 [<span data-ttu-id="466da-229">_CorDllMain 函数</span><span class="sxs-lookup"><span data-stu-id="466da-229">_CorDllMain Function</span></span>](cordllmain-function.md)  
 <span data-ttu-id="466da-230">初始化 CLR，查找 DLL 程序集的 CLR 头中的托管入口点，然后开始执行。</span><span class="sxs-lookup"><span data-stu-id="466da-230">Initializes the CLR, locates the managed entry point in the DLL assembly's CLR header, and begins execution.</span></span>  
  
 [<span data-ttu-id="466da-231">_CorExeMain 函数</span><span class="sxs-lookup"><span data-stu-id="466da-231">_CorExeMain Function</span></span>](corexemain-function.md)  
 <span data-ttu-id="466da-232">初始化 CLR，查找可执行程序集的 CLR 头中的托管入口点，然后开始执行。</span><span class="sxs-lookup"><span data-stu-id="466da-232">Initializes the CLR, locates the managed entry point in the executable assembly's CLR header, and begins execution.</span></span>  
  
 [<span data-ttu-id="466da-233">_CorExeMain2 函数</span><span class="sxs-lookup"><span data-stu-id="466da-233">_CorExeMain2 Function</span></span>](corexemain2-function.md)  
 <span data-ttu-id="466da-234">执行指定的内存映射代码中的入口点。</span><span class="sxs-lookup"><span data-stu-id="466da-234">Executes the entry point in the specified memory-mapped code.</span></span> <span data-ttu-id="466da-235">此函数由操作系统加载程序调用。</span><span class="sxs-lookup"><span data-stu-id="466da-235">This function is called by the operating system loader.</span></span>  
  
 [<span data-ttu-id="466da-236">_CorImageUnloading 函数</span><span class="sxs-lookup"><span data-stu-id="466da-236">_CorImageUnloading Function</span></span>](corimageunloading-function.md)  
 <span data-ttu-id="466da-237">卸载托管模块映像时通知加载程序。</span><span class="sxs-lookup"><span data-stu-id="466da-237">Notifies the loader when the managed module images are unloaded.</span></span>  
  
 [<span data-ttu-id="466da-238">_CorValidateImage 函数</span><span class="sxs-lookup"><span data-stu-id="466da-238">_CorValidateImage Function</span></span>](corvalidateimage-function.md)  
 <span data-ttu-id="466da-239">验证托管模块映像，并在加载后通知操作系统加载程序。</span><span class="sxs-lookup"><span data-stu-id="466da-239">Validates managed module images, and notifies the operating system loader after they have been loaded.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="466da-240">请参阅</span><span class="sxs-lookup"><span data-stu-id="466da-240">See also</span></span>

- [<span data-ttu-id="466da-241">.NET Framework 4 承载全局静态函数</span><span class="sxs-lookup"><span data-stu-id="466da-241">.NET Framework 4 Hosting Global Static Functions</span></span>](net-framework-4-hosting-global-static-functions.md)
