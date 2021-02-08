---
description: 了解详细信息： .NET Native 应用中的运行时异常
title: .NET 本机应用中的运行时异常
ms.date: 03/30/2017
ms.assetid: 5f050181-8fdd-4a4e-9d16-f84c22a88a97
ms.openlocfilehash: 11a85d36a95e74dac36cd45e080428fcba0c673e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801977"
---
# <a name="runtime-exceptions-in-net-native-apps"></a><span data-ttu-id="50fca-103">.NET 本机应用中的运行时异常</span><span class="sxs-lookup"><span data-stu-id="50fca-103">Runtime Exceptions in .NET Native Apps</span></span>

<span data-ttu-id="50fca-104">请务必在通用 Windows 平台应用程序的目标平台上测试它们的发布版本，因为调试和发布配置完全不同。</span><span class="sxs-lookup"><span data-stu-id="50fca-104">It is important to test the release builds of your Universal Windows Platform app on their target platforms because the debug and release configurations are completely different.</span></span> <span data-ttu-id="50fca-105">默认情况下，调试配置使用 .NET Core 运行时来编译应用程序，但发布配置使用 .NET 本机将应用程序编译为本机代码。</span><span class="sxs-lookup"><span data-stu-id="50fca-105">By default, the debug configuration uses the .NET Core runtime to compile your app, but the release configuration uses .NET Native to compile your app to native code.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="50fca-106">有关处理在测试应用的发布版本时可能会遇到的 [MissingMetadataException](missingmetadataexception-class-net-native.md)、 [MissingInteropDataException](missinginteropdataexception-class-net-native.md)和 [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) 异常的信息，请参阅 [入门](getting-started-with-net-native.md) 主题中的 "步骤4：手动解析缺少的元数据：" 和 " [反射和 .NET Native](reflection-and-net-native.md) " 和 " [运行时指令" ( # A0) 配置文件引用](runtime-directives-rd-xml-configuration-file-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="50fca-106">For information on dealing with the [MissingMetadataException](missingmetadataexception-class-net-native.md), [MissingInteropDataException](missinginteropdataexception-class-net-native.md), and [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) exceptions that you may encounter when testing the release versions of your app, see "Step 4: Manually resolve missing metadata: in the [Getting Started](getting-started-with-net-native.md) topic, as well as [Reflection and .NET Native](reflection-and-net-native.md) and [Runtime Directives (rd.xml) Configuration File Reference](runtime-directives-rd-xml-configuration-file-reference.md).</span></span>  
  
## <a name="debug-and-release-builds"></a><span data-ttu-id="50fca-107">调试和发布版本</span><span class="sxs-lookup"><span data-stu-id="50fca-107">Debug and release builds</span></span>  

 <span data-ttu-id="50fca-108">当调试版本针对 .NET Core 运行时执行时，它未编译为本机代码。</span><span class="sxs-lookup"><span data-stu-id="50fca-108">When the debug build executes against the .NET Core runtime, it has not been compiled to native code.</span></span> <span data-ttu-id="50fca-109">这使得你的应用可使用通常由运行时提供的所有服务。</span><span class="sxs-lookup"><span data-stu-id="50fca-109">This makes all of the services ordinarily provided by the runtime available to your app.</span></span>  
  
 <span data-ttu-id="50fca-110">另一方面，发布版本编译为其目标平台的本机代码，删除外部运行时和库的大多数依赖项，并很大程度优化代码以获得最佳性能。</span><span class="sxs-lookup"><span data-stu-id="50fca-110">On the other hand, the release build compiles to native code for its target platforms, removes most dependencies on external runtimes and libraries, and heavily optimizes code for maximum performance.</span></span>  
  
 <span data-ttu-id="50fca-111">对使用 .NET 本机编译的发布版本进行调试时：</span><span class="sxs-lookup"><span data-stu-id="50fca-111">When you debug release builds that are compiled by using .NET Native:</span></span>  
  
- <span data-ttu-id="50fca-112">请使用不同于普通的 .NET 调试工具的 .NET 本机调试引擎。</span><span class="sxs-lookup"><span data-stu-id="50fca-112">You use the .NET Native debug engine, which is different from the normal .NET debugging tools.</span></span>  
  
- <span data-ttu-id="50fca-113">尽可能减小了可执行文件的大小。</span><span class="sxs-lookup"><span data-stu-id="50fca-113">The size of your executable is reduced as much as possible.</span></span> <span data-ttu-id="50fca-114">.NET 本机减小可执行文件的大小的方法之一是大量清理运行时异常消息， [Runtime exception messages](#Messages) 部分中更详细地讨论了这一主题。</span><span class="sxs-lookup"><span data-stu-id="50fca-114">One of the ways that .NET Native reduces the size of an executable is by significantly trimming runtime exception messages, a topic discussed in greater detail in the [Runtime exception messages](#Messages) section.</span></span>  
  
- <span data-ttu-id="50fca-115">很大程度优化了你的代码。</span><span class="sxs-lookup"><span data-stu-id="50fca-115">Your code is heavily optimized.</span></span> <span data-ttu-id="50fca-116">这意味着只要有可能就会使用该内联。</span><span class="sxs-lookup"><span data-stu-id="50fca-116">This means that inlining is used whenever possible.</span></span> <span data-ttu-id="50fca-117"> (内联将外部例程中的代码移到调用例程中。 ) .NET Native 提供专用运行时并实现主动内联会影响在调试时显示的调用堆栈。</span><span class="sxs-lookup"><span data-stu-id="50fca-117">(Inlining moves code from external routines into the calling routine.)   The fact that .NET Native provides a specialized runtime and implements aggressive inlining  affects the call stack that is displayed when debugging.</span></span>  <span data-ttu-id="50fca-118">有关详细信息，请参阅 [Runtime call stack](#CallStack) 部分。</span><span class="sxs-lookup"><span data-stu-id="50fca-118">For more information, see the [Runtime call stack](#CallStack) section.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="50fca-119">通过选中或取消选中“使用 .NET 本机工具链进行编译”  框，可以控制是否使用 .NET 本机工具链编译调试和发布版本。</span><span class="sxs-lookup"><span data-stu-id="50fca-119">You can control whether the debug and release builds are compiled with the .NET Native tool chain by checking or unchecking the **Compile with .NET Native tool chain** box.</span></span>   <span data-ttu-id="50fca-120">但是，请注意 Windows 应用商店将始终使用 .NET 本机工具链编译你的应用程序的生产版本。</span><span class="sxs-lookup"><span data-stu-id="50fca-120">Note, however, that the Windows Store will always compile the production version of your app with the .NET Native tool chain.</span></span>  
  
<a name="Messages"></a>

## <a name="runtime-exception-messages"></a><span data-ttu-id="50fca-121">Runtime exception messages</span><span class="sxs-lookup"><span data-stu-id="50fca-121">Runtime exception messages</span></span>  

 <span data-ttu-id="50fca-122">为尽量减少应用程序可执行文件的大小，.NET 本机不包含异常消息的完整文本。</span><span class="sxs-lookup"><span data-stu-id="50fca-122">To minimize application executable size, .NET Native does not include the full text of exception messages.</span></span> <span data-ttu-id="50fca-123">因此，在发布版本中引发的运行时异常可能不显示异常消息的完整文本。</span><span class="sxs-lookup"><span data-stu-id="50fca-123">As a result, runtime exceptions thrown in release builds may not display the full text of exception messages.</span></span> <span data-ttu-id="50fca-124">相反，该文本可能由一个子字符串和一个链接构成，跟随该链接可获取详细信息。</span><span class="sxs-lookup"><span data-stu-id="50fca-124">Instead, the text may consist of a substring along with a link to follow for more information.</span></span> <span data-ttu-id="50fca-125">例如，异常信息可能显示为：</span><span class="sxs-lookup"><span data-stu-id="50fca-125">For example, the exception information may appear as:</span></span>  
  
```output
Exception thrown: '$16_System.AggregateException' in Unknown Module.  
  
Additional information: AggregateException_ctor_DefaultMessage  
  
If there is a handler for this exception, the program may be safely continued.  
```  
  
 <span data-ttu-id="50fca-126">如果需要完整的异常消息，请改为运行调试版本。</span><span class="sxs-lookup"><span data-stu-id="50fca-126">If you need the complete exception message,  run the debug build instead.</span></span> <span data-ttu-id="50fca-127">例如，发布版本中的上一个异常信息在调试版本中可能显示如下：</span><span class="sxs-lookup"><span data-stu-id="50fca-127">For example, the previous exception information  from the release build might appear as follows in the debug build:</span></span>  
  
```output
Exception thrown: 'System.AggregateException' in NativeApp.exe.  
  
Additional information: Value does not fall within the expected range.  
```  
  
<a name="CallStack"></a>

## <a name="runtime-call-stack"></a><span data-ttu-id="50fca-128">Runtime call stack</span><span class="sxs-lookup"><span data-stu-id="50fca-128">Runtime call stack</span></span>  

 <span data-ttu-id="50fca-129">由于内联和其他优化，由 .NET 本机工具链编译的应用显示的调用堆栈可能无益于清晰地标识运行时异常的路径。</span><span class="sxs-lookup"><span data-stu-id="50fca-129">Because of inlining and other optimizations, the call stack displayed by an app compiled by the .NET Native tool chain may not help you to  clearly identify the path to a runtime exception.</span></span>  
  
 <span data-ttu-id="50fca-130">若要获取完整的堆栈，请改为运行调试版本。</span><span class="sxs-lookup"><span data-stu-id="50fca-130">To get the full stack, run the debug build instead.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50fca-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="50fca-131">See also</span></span>

- [<span data-ttu-id="50fca-132">调试 .NET 本机 Windows 通用应用</span><span class="sxs-lookup"><span data-stu-id="50fca-132">Debugging .NET Native Windows Universal Apps</span></span>](https://devblogs.microsoft.com/devops/debugging-net-native-windows-universal-apps/)
- [<span data-ttu-id="50fca-133">入门</span><span class="sxs-lookup"><span data-stu-id="50fca-133">Getting Started</span></span>](getting-started-with-net-native.md)
