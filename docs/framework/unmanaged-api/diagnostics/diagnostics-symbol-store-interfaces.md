---
description: 了解详细信息：诊断符号存储区接口
title: 诊断符号存储区接口
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged interfaces [.NET Framework], debugging
- diagnostics symbol store interfaces [.NET Framework]
- interfaces [.NET Framework], diagnostics symbol store
- unmanaged interfaces [.NET Framework], diagnostics symbol store
- debugging interfaces [.NET Framework]
- interfaces [.NET Framework debugging]
ms.assetid: f96987d5-e6a5-478b-ac5e-302e16545cce
ms.openlocfilehash: 253a6e5eaa97c91332bca62f8fc47ad2945bf741
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800430"
---
# <a name="diagnostics-symbol-store-interfaces"></a><span data-ttu-id="2871b-103">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="2871b-103">Diagnostics Symbol Store Interfaces</span></span>

<span data-ttu-id="2871b-104">本主题介绍了一些非托管接口，这些接口允许编译器生成符号信息以供调试器使用。</span><span class="sxs-lookup"><span data-stu-id="2871b-104">This topic describes the unmanaged interfaces that enable a compiler to generate symbol information for use by a debugger.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2871b-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="2871b-105">In This Section</span></span>  

 [<span data-ttu-id="2871b-106">IBindingDisplay 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-106">IBindingDisplay Interface</span></span>](ibindingdisplay-interface.md)  
 <span data-ttu-id="2871b-107">提供显示有关正在运行的应用程序的当前绑定信息的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-107">Provides methods that display current binding information about the running application.</span></span>  
  
 [<span data-ttu-id="2871b-108">IDebugAutoAttach 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-108">IDebugAutoAttach Interface</span></span>](idebugautoattach-interface.md)  
 <span data-ttu-id="2871b-109">定义服务器调用的调试器自动附加的接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-109">Defines the interface for a server-invoked debugger auto attach.</span></span>  
  
 [<span data-ttu-id="2871b-110">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-110">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)  
 <span data-ttu-id="2871b-111">声明用于注册和注销连接通知源的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-111">Declares methods for registering and unregistering a connection notification source.</span></span>  
  
 [<span data-ttu-id="2871b-112">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-112">INotifySink2 Interface</span></span>](inotifysink2-interface.md)  
 <span data-ttu-id="2871b-113">声明接收器通知的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-113">Declares methods for sink notification.</span></span>  
  
 [<span data-ttu-id="2871b-114">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-114">INotifySource2 Interface</span></span>](inotifysource2-interface.md)  
 <span data-ttu-id="2871b-115">声明用于设置通知筛选器的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-115">Declares a method for setting notification filters.</span></span>  
  
 [<span data-ttu-id="2871b-116">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-116">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)  
 <span data-ttu-id="2871b-117">提供 "编辑并继续" 功能的信息。</span><span class="sxs-lookup"><span data-stu-id="2871b-117">Provides information for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="2871b-118">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-118">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)  
 <span data-ttu-id="2871b-119">此接口是 [ISymUnmanagedAsyncMethodPropertiesWriter 接口](isymunmanagedasyncmethodpropertieswriter-interface.md)的读取补充。</span><span class="sxs-lookup"><span data-stu-id="2871b-119">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
 [<span data-ttu-id="2871b-120">ISymUnmanagedAsyncMethodPropertiesWriter 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-120">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](isymunmanagedasyncmethodpropertieswriter-interface.md)  
 <span data-ttu-id="2871b-121">允许为每个方法符号定义可选的异步方法信息。</span><span class="sxs-lookup"><span data-stu-id="2871b-121">Allows definition of optional async method information per method symbol.</span></span> <span data-ttu-id="2871b-122">必须将与已打开的方法一起使用 (即，在对 [OpenMethod 方法](isymunmanagedwriter-openmethod-method.md)的调用与 [CloseMethod 方法](isymunmanagedwriter-closemethod-method.md) 的调用之间) 。</span><span class="sxs-lookup"><span data-stu-id="2871b-122">Must use with an opened method (that is, between calls to the [OpenMethod Method](isymunmanagedwriter-openmethod-method.md)and the [CloseMethod Method](isymunmanagedwriter-closemethod-method.md)).</span></span>  
  
 [<span data-ttu-id="2871b-123">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-123">ISymUnmanagedBinder Interface</span></span>](isymunmanagedbinder-interface.md)  
 <span data-ttu-id="2871b-124">表示非托管代码的符号绑定器。</span><span class="sxs-lookup"><span data-stu-id="2871b-124">Represents a symbol binder for unmanaged code.</span></span>  
  
 [<span data-ttu-id="2871b-125">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-125">ISymUnmanagedBinder2 Interface</span></span>](isymunmanagedbinder2-interface.md)  
 <span data-ttu-id="2871b-126">表示非托管代码的符号联编程序，并扩展 `ISymUnmanagedBinder` 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-126">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="2871b-127">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-127">ISymUnmanagedBinder3 Interface</span></span>](isymunmanagedbinder3-interface.md)  
 <span data-ttu-id="2871b-128">表示非托管代码的符号联编程序，并扩展 `ISymUnmanagedBinder` 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-128">Represents a symbol binder for unmanaged code, and extends the `ISymUnmanagedBinder` interface.</span></span>  
  
 [<span data-ttu-id="2871b-129">ISymUnmanagedConstant 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-129">ISymUnmanagedConstant Interface</span></span>](isymunmanagedconstant-interface.md)  
 <span data-ttu-id="2871b-130">提供对非托管常数的访问。</span><span class="sxs-lookup"><span data-stu-id="2871b-130">Provides access to unmanaged constants.</span></span>  
  
 [<span data-ttu-id="2871b-131">ISymUnmanagedDispose 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-131">ISymUnmanagedDispose Interface</span></span>](isymunmanageddispose-interface.md)  
 <span data-ttu-id="2871b-132">释放非托管资源。</span><span class="sxs-lookup"><span data-stu-id="2871b-132">Disposes of unmanaged resources.</span></span>  
  
 [<span data-ttu-id="2871b-133">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-133">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)  
 <span data-ttu-id="2871b-134">表示由符号存储引用的文档。</span><span class="sxs-lookup"><span data-stu-id="2871b-134">Represents a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="2871b-135">ISymUnmanagedDocumentWriter 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-135">ISymUnmanagedDocumentWriter Interface</span></span>](isymunmanageddocumentwriter-interface.md)  
 <span data-ttu-id="2871b-136">提供用于写入到符号存储区引用的文档的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-136">Provides methods for writing to a document referenced by a symbol store.</span></span>  
  
 [<span data-ttu-id="2871b-137">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-137">ISymUnmanagedENCUpdate Interface</span></span>](isymunmanagedencupdate-interface.md)  
 <span data-ttu-id="2871b-138">提供 "编辑并继续" 功能的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-138">Provides methods for the Edit and Continue feature.</span></span>  
  
 [<span data-ttu-id="2871b-139">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-139">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)  
 <span data-ttu-id="2871b-140">表示符号存储区中的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-140">Represents a method within the symbol store.</span></span>  
  
 [<span data-ttu-id="2871b-141">ISymUnmanagedNamespace 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-141">ISymUnmanagedNamespace Interface</span></span>](isymunmanagednamespace-interface.md)  
 <span data-ttu-id="2871b-142">表示命名空间。</span><span class="sxs-lookup"><span data-stu-id="2871b-142">Represents a namespace.</span></span>  
  
 [<span data-ttu-id="2871b-143">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-143">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)  
 <span data-ttu-id="2871b-144">表示一个符号读取器，该读取器提供对符号存储区中文档、方法和变量的访问。</span><span class="sxs-lookup"><span data-stu-id="2871b-144">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span>  
  
 [<span data-ttu-id="2871b-145">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-145">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)  
 <span data-ttu-id="2871b-146">给定方法标记和编辑和复制版本号，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-146">Gets a symbol reader method given a method token and an edit-and-copy version number.</span></span>  
  
 [<span data-ttu-id="2871b-147">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-147">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](isymunmanagedreadersymbolsearchinfo-interface.md)  
 <span data-ttu-id="2871b-148">提供用于获取符号搜索信息的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-148">Provides methods that get symbol search information.</span></span>  
  
 [<span data-ttu-id="2871b-149">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-149">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)  
 <span data-ttu-id="2871b-150">表示方法中的词法范围。</span><span class="sxs-lookup"><span data-stu-id="2871b-150">Represents a lexical scope within a method.</span></span>  
  
 [<span data-ttu-id="2871b-151">ISymUnmanagedScope2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-151">ISymUnmanagedScope2 Interface</span></span>](isymunmanagedscope2-interface.md)  
 <span data-ttu-id="2871b-152">表示方法内的词法范围，并 `ISymUnmanagedScope` 使用获取有关范围中定义的常量的信息的方法扩展接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-152">Represents a lexical scope within a method, and extends the `ISymUnmanagedScope` interface with methods that get information about constants defined within the scope..</span></span>  
  
 [<span data-ttu-id="2871b-153">ISymUnmanagedSourceServerModule 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-153">ISymUnmanagedSourceServerModule Interface</span></span>](isymunmanagedsourceservermodule-interface.md)  
 <span data-ttu-id="2871b-154">提供模块的源服务器数据。</span><span class="sxs-lookup"><span data-stu-id="2871b-154">Provides source server data for a module.</span></span>  
  
 [<span data-ttu-id="2871b-155">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-155">ISymUnmanagedSymbolSearchInfo Interface</span></span>](isymunmanagedsymbolsearchinfo-interface.md)  
 <span data-ttu-id="2871b-156">提供获取有关搜索路径的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-156">Provides methods that get information about the search path.</span></span>  
  
 [<span data-ttu-id="2871b-157">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-157">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)  
 <span data-ttu-id="2871b-158">表示变量，如参数、局部变量或字段。</span><span class="sxs-lookup"><span data-stu-id="2871b-158">Represents a variable, such as a parameter, a local variable, or a field.</span></span>  
  
 [<span data-ttu-id="2871b-159">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-159">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)  
 <span data-ttu-id="2871b-160">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-160">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span>  
  
 [<span data-ttu-id="2871b-161">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-161">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)  
 <span data-ttu-id="2871b-162">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-162">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="2871b-163">扩展 `ISymUnmanagedWriter` 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-163">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="2871b-164">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-164">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)  
 <span data-ttu-id="2871b-165">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="2871b-165">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="2871b-166">扩展 `ISymUnmanagedWriter` 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-166">Extends the `ISymUnmanagedWriter` interface.</span></span>  
  
 [<span data-ttu-id="2871b-167">ISymUnmanagedWriter4 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-167">ISymUnmanagedWriter4 Interface</span></span>](isymunmanagedwriter4-interface.md)  
 <span data-ttu-id="2871b-168">ISymUnmanagedWriter4 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-168">ISymUnmanagedWriter4 interface.</span></span>  
  
 [<span data-ttu-id="2871b-169">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="2871b-169">ISymUnmanagedWriter5 Interface</span></span>](isymunmanagedwriter5-interface.md)  
 <span data-ttu-id="2871b-170">ISymUnmanagedWriter5 接口。</span><span class="sxs-lookup"><span data-stu-id="2871b-170">ISymUnmanagedWriter5 interface.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="2871b-171">相关章节</span><span class="sxs-lookup"><span data-stu-id="2871b-171">Related Sections</span></span>  

 [<span data-ttu-id="2871b-172">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="2871b-172">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)  
  
 [<span data-ttu-id="2871b-173">诊断符号存储区结构</span><span class="sxs-lookup"><span data-stu-id="2871b-173">Diagnostics Symbol Store Structures</span></span>](diagnostics-symbol-store-structures.md)  
  
 [<span data-ttu-id="2871b-174">调试</span><span class="sxs-lookup"><span data-stu-id="2871b-174">Debugging</span></span>](../debugging/index.md)
