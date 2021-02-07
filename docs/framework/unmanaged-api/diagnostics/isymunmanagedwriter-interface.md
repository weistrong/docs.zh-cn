---
description: 了解详细信息： ISymUnmanagedWriter 接口
title: ISymUnmanagedWriter 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter
helpviewer_keywords:
- ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: 7d6733ec-f081-4166-bc17-de09e16dc304
topic_type:
- apiref
ms.openlocfilehash: 20fc0fd9b76b1aae4090582fe48a8a8e77d77c9f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762235"
---
# <a name="isymunmanagedwriter-interface"></a><span data-ttu-id="0c61c-103">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="0c61c-103">ISymUnmanagedWriter Interface</span></span>

<span data-ttu-id="0c61c-104">表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。</span><span class="sxs-lookup"><span data-stu-id="0c61c-104">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0c61c-105">方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-105">Methods</span></span>  
  
|<span data-ttu-id="0c61c-106">方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-106">Method</span></span>|<span data-ttu-id="0c61c-107">说明</span><span class="sxs-lookup"><span data-stu-id="0c61c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0c61c-108">Abort 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-108">Abort Method</span></span>](isymunmanagedwriter-abort-method.md)|<span data-ttu-id="0c61c-109">关闭符号编写器，而不将符号提交到符号存储区。</span><span class="sxs-lookup"><span data-stu-id="0c61c-109">Closes the symbol writer without committing the symbols to the symbol store.</span></span>|  
|[<span data-ttu-id="0c61c-110">Close 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-110">Close Method</span></span>](isymunmanagedwriter-close-method.md)|<span data-ttu-id="0c61c-111">将符号提交到符号存储区后关闭符号编写器。</span><span class="sxs-lookup"><span data-stu-id="0c61c-111">Closes the symbol writer after committing the symbols to the symbol store.</span></span>|  
|[<span data-ttu-id="0c61c-112">CloseMethod 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-112">CloseMethod Method</span></span>](isymunmanagedwriter-closemethod-method.md)|<span data-ttu-id="0c61c-113">关闭当前方法。</span><span class="sxs-lookup"><span data-stu-id="0c61c-113">Closes the current method.</span></span> <span data-ttu-id="0c61c-114">方法关闭后，不能在其中定义更多符号。</span><span class="sxs-lookup"><span data-stu-id="0c61c-114">Once a method is closed, no more symbols can be defined within it.</span></span>|  
|[<span data-ttu-id="0c61c-115">CloseNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-115">CloseNamespace Method</span></span>](isymunmanagedwriter-closenamespace-method.md)|<span data-ttu-id="0c61c-116">关闭最近打开的命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c61c-116">Closes the most recently opened namespace.</span></span>|  
|[<span data-ttu-id="0c61c-117">CloseScope 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-117">CloseScope Method</span></span>](isymunmanagedwriter-closescope-method.md)|<span data-ttu-id="0c61c-118">关闭当前词法范围。</span><span class="sxs-lookup"><span data-stu-id="0c61c-118">Closes the current lexical scope.</span></span>|  
|[<span data-ttu-id="0c61c-119">DefineConstant 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-119">DefineConstant Method</span></span>](isymunmanagedwriter-defineconstant-method.md)|<span data-ttu-id="0c61c-120">定义常数值的名称。</span><span class="sxs-lookup"><span data-stu-id="0c61c-120">Defines a name for a constant value.</span></span>|  
|[<span data-ttu-id="0c61c-121">DefineDocument 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-121">DefineDocument Method</span></span>](isymunmanagedwriter-definedocument-method.md)|<span data-ttu-id="0c61c-122">定义源文档。</span><span class="sxs-lookup"><span data-stu-id="0c61c-122">Defines a source document.</span></span>|  
|[<span data-ttu-id="0c61c-123">DefineField 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-123">DefineField Method</span></span>](isymunmanagedwriter-definefield-method.md)|<span data-ttu-id="0c61c-124">定义不在方法中的单个变量。</span><span class="sxs-lookup"><span data-stu-id="0c61c-124">Defines a single variable that is not within a method.</span></span>|  
|[<span data-ttu-id="0c61c-125">DefineGlobalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-125">DefineGlobalVariable Method</span></span>](isymunmanagedwriter-defineglobalvariable-method.md)|<span data-ttu-id="0c61c-126">定义单个全局变量。</span><span class="sxs-lookup"><span data-stu-id="0c61c-126">Defines a single global variable.</span></span>|  
|[<span data-ttu-id="0c61c-127">DefineLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-127">DefineLocalVariable Method</span></span>](isymunmanagedwriter-definelocalvariable-method.md)|<span data-ttu-id="0c61c-128">在当前词法范围内定义单个变量。</span><span class="sxs-lookup"><span data-stu-id="0c61c-128">Defines a single variable in the current lexical scope.</span></span>|  
|[<span data-ttu-id="0c61c-129">DefineParameter 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-129">DefineParameter Method</span></span>](isymunmanagedwriter-defineparameter-method.md)|<span data-ttu-id="0c61c-130">在当前方法中定义单个参数。</span><span class="sxs-lookup"><span data-stu-id="0c61c-130">Defines a single parameter in the current method.</span></span>|  
|[<span data-ttu-id="0c61c-131">DefineSequencePoints 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-131">DefineSequencePoints Method</span></span>](isymunmanagedwriter-definesequencepoints-method.md)|<span data-ttu-id="0c61c-132">在当前方法内定义一组序列点。</span><span class="sxs-lookup"><span data-stu-id="0c61c-132">Defines a group of sequence points within the current method.</span></span>|  
|[<span data-ttu-id="0c61c-133">GetDebugInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-133">GetDebugInfo Method</span></span>](isymunmanagedwriter-getdebuginfo-method.md)|<span data-ttu-id="0c61c-134">返回编译器将 (PE 中的调试目录项写入) 文件头所需的信息。</span><span class="sxs-lookup"><span data-stu-id="0c61c-134">Returns the information necessary for a compiler to write the debug directory entry in the portable executable (PE) file header.</span></span>|  
|[<span data-ttu-id="0c61c-135">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-135">Initialize Method</span></span>](isymunmanagedwriter-initialize-method.md)|<span data-ttu-id="0c61c-136">设置此编写器将与之关联的元数据发射器接口，并设置调试符号将写入的输出文件名。</span><span class="sxs-lookup"><span data-stu-id="0c61c-136">Sets the metadata emitter interface with which this writer will be associated, and sets the output file name to which the debugging symbols will be written.</span></span>|  
|[<span data-ttu-id="0c61c-137">Initialize2 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-137">Initialize2 Method</span></span>](isymunmanagedwriter-initialize2-method.md)|<span data-ttu-id="0c61c-138">设置此编写器将与之关联的元数据发射器接口，设置调试符号将写入到的输出文件名，并将程序数据库 (PDB) 文件的最终位置设置为。</span><span class="sxs-lookup"><span data-stu-id="0c61c-138">Sets the metadata emitter interface with which this writer will be associated, sets the output file name to which the debugging symbols will be written, and sets the final location of the program database (PDB) file.</span></span>|  
|[<span data-ttu-id="0c61c-139">OpenMethod 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-139">OpenMethod Method</span></span>](isymunmanagedwriter-openmethod-method.md)|<span data-ttu-id="0c61c-140">打开要在其中发出符号信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0c61c-140">Opens a method into which symbol information is emitted.</span></span>|  
|[<span data-ttu-id="0c61c-141">OpenNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-141">OpenNamespace Method</span></span>](isymunmanagedwriter-opennamespace-method.md)|<span data-ttu-id="0c61c-142">打开一个新的命名空间。</span><span class="sxs-lookup"><span data-stu-id="0c61c-142">Opens a new namespace.</span></span>|  
|[<span data-ttu-id="0c61c-143">OpenScope 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-143">OpenScope Method</span></span>](isymunmanagedwriter-openscope-method.md)|<span data-ttu-id="0c61c-144">在当前方法中打开新的词法范围。</span><span class="sxs-lookup"><span data-stu-id="0c61c-144">Opens a new lexical scope in the current method.</span></span>|  
|[<span data-ttu-id="0c61c-145">RemapToken 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-145">RemapToken Method</span></span>](isymunmanagedwriter-remaptoken-method.md)|<span data-ttu-id="0c61c-146">通知符号编写器在发出元数据时已重新映射元数据标记。</span><span class="sxs-lookup"><span data-stu-id="0c61c-146">Notifies the symbol writer that a metadata token has been remapped as the metadata was emitted.</span></span>|  
|[<span data-ttu-id="0c61c-147">SetMethodSourceRange 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-147">SetMethodSourceRange Method</span></span>](isymunmanagedwriter-setmethodsourcerange-method.md)|<span data-ttu-id="0c61c-148">指定源文件内方法的真正开始和结尾。</span><span class="sxs-lookup"><span data-stu-id="0c61c-148">Specifies the true start and end of a method within a source file.</span></span>|  
|[<span data-ttu-id="0c61c-149">SetScopeRange 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-149">SetScopeRange Method</span></span>](isymunmanagedwriter-setscoperange-method.md)|<span data-ttu-id="0c61c-150">定义指定词法范围的偏移量范围。</span><span class="sxs-lookup"><span data-stu-id="0c61c-150">Defines the offset range for the specified lexical scope.</span></span>|  
|[<span data-ttu-id="0c61c-151">SetSymAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-151">SetSymAttribute Method</span></span>](isymunmanagedwriter-setsymattribute-method.md)|<span data-ttu-id="0c61c-152">基于名称定义自定义属性。</span><span class="sxs-lookup"><span data-stu-id="0c61c-152">Defines a custom attribute based upon its name.</span></span>|  
|[<span data-ttu-id="0c61c-153">SetUserEntryPoint 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-153">SetUserEntryPoint Method</span></span>](isymunmanagedwriter-setuserentrypoint-method.md)|<span data-ttu-id="0c61c-154">指定用户定义的方法，该方法是此模块的入口点。</span><span class="sxs-lookup"><span data-stu-id="0c61c-154">Specifies the user-defined method that is the entry point for this module.</span></span>|  
|[<span data-ttu-id="0c61c-155">UsingNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="0c61c-155">UsingNamespace Method</span></span>](isymunmanagedwriter-usingnamespace-method.md)|<span data-ttu-id="0c61c-156">指定在当前打开的词法范围内使用给定的完全限定的命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="0c61c-156">Specifies that the given fully qualified namespace name is being used within the currently open lexical scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0c61c-157">要求</span><span class="sxs-lookup"><span data-stu-id="0c61c-157">Requirements</span></span>  

 <span data-ttu-id="0c61c-158">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0c61c-158">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c61c-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c61c-159">See also</span></span>

- [<span data-ttu-id="0c61c-160">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="0c61c-160">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="0c61c-161">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="0c61c-161">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="0c61c-162">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="0c61c-162">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)
