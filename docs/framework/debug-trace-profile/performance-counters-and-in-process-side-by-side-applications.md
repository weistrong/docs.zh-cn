---
title: 性能计数器和进程内并行应用程序
description: 查看 .NET 中的性能计数器和进程内并行应用程序。 使用 Perfmon.exe 来区分每个运行时的性能计数器。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- performance counters
- performance counters,and in-process side-by-side applications
- performance,.NET Framework applications
- performance monitoring,counters
ms.assetid: 6888f9be-c65b-4b03-a07b-df7ebdee2436
ms.openlocfilehash: 5cc3951c65a0be37294324c767a00bc7a35634b8
ms.sourcegitcommit: 78eb25647b0c750cd80354ebd6ce83a60668e22c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2021
ms.locfileid: "99065033"
---
# <a name="performance-counters-and-in-process-side-by-side-applications"></a><span data-ttu-id="e4568-104">性能计数器和进程内并行应用程序</span><span class="sxs-lookup"><span data-stu-id="e4568-104">Performance Counters and In-Process Side-By-Side Applications</span></span>

<span data-ttu-id="e4568-105">使用性能监视器 (Perfmon.exe) 有可能在每个运行时基础上区分性能计数器。</span><span class="sxs-lookup"><span data-stu-id="e4568-105">Using the Performance Monitor (Perfmon.exe), it is possible to differentiate the performance counters on a per-runtime basis.</span></span> <span data-ttu-id="e4568-106">本主题介绍启用此功能所需的注册表更改。</span><span class="sxs-lookup"><span data-stu-id="e4568-106">This topic describes the registry change needed to enable this functionality.</span></span>  
  
## <a name="the-default-behavior"></a><span data-ttu-id="e4568-107">默认行为</span><span class="sxs-lookup"><span data-stu-id="e4568-107">The Default Behavior</span></span>  

 <span data-ttu-id="e4568-108">默认情况下，性能监视器基于每个应用程序显示性能计数器。</span><span class="sxs-lookup"><span data-stu-id="e4568-108">By default, the Performance Monitor displays performance counters on a per-application basis.</span></span> <span data-ttu-id="e4568-109">但是，这在两种情形下会出现问题：</span><span class="sxs-lookup"><span data-stu-id="e4568-109">However, there are two scenarios in which this is problematic:</span></span>  
  
- <span data-ttu-id="e4568-110">当监视两个名称相同的应用程序时。</span><span class="sxs-lookup"><span data-stu-id="e4568-110">When you monitor two applications that have the same name.</span></span> <span data-ttu-id="e4568-111">例如，如果两个应用程序的名称都为 myapp.exe，二者在“实例”列中将分别显示为“myapp”和“myapp#1”。</span><span class="sxs-lookup"><span data-stu-id="e4568-111">For example, if both applications are named myapp.exe, one will be displayed as **myapp** and the other as **myapp#1** in the **Instance** column.</span></span> <span data-ttu-id="e4568-112">在这种情况下很难将性能计数器与特定的应用程序相匹配。</span><span class="sxs-lookup"><span data-stu-id="e4568-112">In this case, it is difficult to match a performance counter to a particular application.</span></span> <span data-ttu-id="e4568-113">无法确定为“myapp#1”收集的数据指的是第一个 myapp.exe，还是第二个 myapp.exe。</span><span class="sxs-lookup"><span data-stu-id="e4568-113">It is not clear whether the data collected for **myapp#1** refers to the first myapp.exe or the second myapp.exe.</span></span>  
  
- <span data-ttu-id="e4568-114">当应用程序使用多个公共语言运行时实例时。</span><span class="sxs-lookup"><span data-stu-id="e4568-114">When an application uses multiple instances of the common language runtime.</span></span> <span data-ttu-id="e4568-115">.NET Framework 4 支持进程内并行承载方案;也就是说，一个进程或应用程序可以加载公共语言运行时的多个实例。</span><span class="sxs-lookup"><span data-stu-id="e4568-115">The .NET Framework 4 supports in-process side-by-side hosting scenarios; that is, a single process or application can load multiple instances of the common language runtime.</span></span> <span data-ttu-id="e4568-116">如果一个名为 myapp.exe 的应用程序加载两个运行时实例，则默认情况下会在“实例”列中将这两个实例分别指定为“myapp”和“myapp#1”。</span><span class="sxs-lookup"><span data-stu-id="e4568-116">If a single application named myapp.exe loads two runtime instances, by default, they will be designated in the **Instance** column as **myapp** and **myapp#1**.</span></span> <span data-ttu-id="e4568-117">在这种情况下，无法确定“myapp”和“myapp#1”指的是两个名称相同的应用程序，还是具有两个运行时的同一应用程序。</span><span class="sxs-lookup"><span data-stu-id="e4568-117">In this case, it is not clear whether **myapp** and **myapp#1** refer to two applications with the same name, or to the same application with two runtimes.</span></span> <span data-ttu-id="e4568-118">如果名称相同的多个应用程序加载多个运行时，则这种歧义性会更大。</span><span class="sxs-lookup"><span data-stu-id="e4568-118">If multiple applications with the same name load multiple runtimes, the ambiguity is even greater.</span></span>  
  
 <span data-ttu-id="e4568-119">可以设置注册表项来消除此歧义性。</span><span class="sxs-lookup"><span data-stu-id="e4568-119">You can set a registry key to eliminate this ambiguity.</span></span> <span data-ttu-id="e4568-120">对于使用 .NET Framework 4 开发的应用程序，此注册表更改将向 **实例** 列中的应用程序名称添加一个进程标识符，后跟一个运行时实例标识符。</span><span class="sxs-lookup"><span data-stu-id="e4568-120">For applications developed using the .NET Framework 4, this registry change adds a process identifier followed by a runtime instance identifier to the application name in the **Instance** column.</span></span> <span data-ttu-id="e4568-121">现在，应用程序会  `p`  \_ `r` 在 "**实例**" 列中标识为应用程序 _ runtimeID，而不是应用程序或应用程序 #1。</span><span class="sxs-lookup"><span data-stu-id="e4568-121">Instead of *application* or *application*#1, the application is now identified as *application* _`p`*processID*\_`r`*runtimeID* in the **Instance** column.</span></span> <span data-ttu-id="e4568-122">如果应用程序是使用以前版本的公共语言运行时开发的，则该实例将表示 *为 \_ 应用程序* `p` *processID* ，前提是安装了 .NET Framework 4。</span><span class="sxs-lookup"><span data-stu-id="e4568-122">If an application was developed using a previous version of the common language runtime, that instance is represented as *application\_*`p`*processID* provided that the .NET Framework 4 is installed.</span></span>  
  
## <a name="performance-counters-for-in-process-side-by-side-applications"></a><span data-ttu-id="e4568-123">进程内并行应用程序的性能计数器</span><span class="sxs-lookup"><span data-stu-id="e4568-123">Performance Counters for In-Process Side-by-Side Applications</span></span>  

 <span data-ttu-id="e4568-124">若要处理单个应用程序中承载的多个公共语言运行时版本的性能计数器，必须如下表所示更改一个注册表项设置。</span><span class="sxs-lookup"><span data-stu-id="e4568-124">To handle performance counters for multiple common language runtime versions that are hosted in a single application, you must change a single registry key setting, as shown in the following table.</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e4568-125">项名称</span><span class="sxs-lookup"><span data-stu-id="e4568-125">Key name</span></span>|<span data-ttu-id="e4568-126">HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\\.NETFramework\Performance</span><span class="sxs-lookup"><span data-stu-id="e4568-126">HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\\.NETFramework\Performance</span></span>|  
|<span data-ttu-id="e4568-127">值名称</span><span class="sxs-lookup"><span data-stu-id="e4568-127">Value name</span></span>|<span data-ttu-id="e4568-128">ProcessNameFormat</span><span class="sxs-lookup"><span data-stu-id="e4568-128">ProcessNameFormat</span></span>|  
|<span data-ttu-id="e4568-129">值类型</span><span class="sxs-lookup"><span data-stu-id="e4568-129">Value type</span></span>|<span data-ttu-id="e4568-130">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e4568-130">REG_DWORD</span></span>|  
|<span data-ttu-id="e4568-131">值</span><span class="sxs-lookup"><span data-stu-id="e4568-131">Value</span></span>|<span data-ttu-id="e4568-132">2 (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e4568-132">2 (0x00000002)</span></span>|
  
 <span data-ttu-id="e4568-133">`ProcessNameFormat` 的值为 0 表示启用了默认行为；也就是说，Perfmon.exe 将基于每个应用程序显示性能计数器。</span><span class="sxs-lookup"><span data-stu-id="e4568-133">A value of 0 for `ProcessNameFormat` indicates that the default behavior is enabled; that is, Perfmon.exe displays performance counters on a per-application basis.</span></span> <span data-ttu-id="e4568-134">将此值设置为2时，Perfmon.exe 消除应用程序的多个版本，并基于每个运行时提供性能计数器。</span><span class="sxs-lookup"><span data-stu-id="e4568-134">When you set this value to 2, Perfmon.exe disambiguates multiple versions of an application and provides performance counters on a per-runtime basis.</span></span> <span data-ttu-id="e4568-135">`ProcessNameFormat` 注册表项设置的任何其他值均不受支持，留待将来使用。</span><span class="sxs-lookup"><span data-stu-id="e4568-135">Any other value for the `ProcessNameFormat` registry key setting is unsupported and reserved for future use.</span></span>
  
 <span data-ttu-id="e4568-136">更新 `ProcessNameFormat` 注册表项设置之后，必须重新启动 Perfmon.exe 或任何其他性能计数器的使用方，以便新的实例命名功能可正常工作。</span><span class="sxs-lookup"><span data-stu-id="e4568-136">After you update the `ProcessNameFormat` registry key setting, you must restart Perfmon.exe or any other consumers of performance counters so that the new instance naming feature works correctly.</span></span>  
  
 <span data-ttu-id="e4568-137">下面的示例演示如何以编程方式更改 `ProcessNameFormat` 值。</span><span class="sxs-lookup"><span data-stu-id="e4568-137">The following example shows how to change the `ProcessNameFormat` value programmatically.</span></span>  
  
 [!code-csharp[Conceptual.PerfCounters.InProSxS#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.perfcounters.inprosxs/cs/regsetting1.cs#1)]
 [!code-vb[Conceptual.PerfCounters.InProSxS#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.perfcounters.inprosxs/vb/regsetting1.vb#1)]  
  
 <span data-ttu-id="e4568-138">当你进行此注册表更改时，如果安装了 .NET Framework 4 或更高版本，则 Perfmon.exe 会将应用程序的名称显示为 *应用* 程序 _ `p` *processID*，其中 *应用* 程序为应用程序的名称， *processID* 为应用程序的进程标识符。</span><span class="sxs-lookup"><span data-stu-id="e4568-138">When you make this registry change, and if .NET Framework 4 or later is installed, Perfmon.exe displays the names of applications as *application* _`p`*processID*, where *application* is the name of the application, and *processID* is the application's process identifier.</span></span> <span data-ttu-id="e4568-139">例如，如果一个名为 myapp.exe 的应用程序加载公共语言运行时的两个实例，则 Perfmon.exe 可以将一个实例标识为 myapp_1416，将第二个实例标识为 myapp_3160。</span><span class="sxs-lookup"><span data-stu-id="e4568-139">For example, if an application named myapp.exe loads two instances of the common language runtime, Perfmon.exe may identify one instance as myapp_1416 and the second as myapp_3160.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e4568-140">进程标识符可消除在解析名称相同且使用运行时早期版本的两个应用程序时存在的歧义性。</span><span class="sxs-lookup"><span data-stu-id="e4568-140">The process identifier eliminates the ambiguity of resolving two applications with the same name that use earlier versions of the runtime.</span></span> <span data-ttu-id="e4568-141">因为旧版公共语言运行时不支持并行方案，所以它们不需要运行时标识符。</span><span class="sxs-lookup"><span data-stu-id="e4568-141">A runtime identifier is not required for previous versions, because previous versions of the common language runtime do not support side-by-side scenarios.</span></span>  
  
 <span data-ttu-id="e4568-142">如果 .NET Framework 4 或更高版本不存在或已卸载，则设置注册表项不起作用。</span><span class="sxs-lookup"><span data-stu-id="e4568-142">If the .NET Framework 4 or a later version is not present or was uninstalled, setting the registry key has no effect.</span></span> <span data-ttu-id="e4568-143">这意味着名称相同的两个应用程序在 Perfmon.exe 中将继续显示为 application 和 application#1（例如，myapp 和 myapp#1）。</span><span class="sxs-lookup"><span data-stu-id="e4568-143">This means that two applications with the same name will continue to appear in Perfmon.exe as *application* and *application#1* (for example, as **myapp** and **myapp#1**).</span></span>
