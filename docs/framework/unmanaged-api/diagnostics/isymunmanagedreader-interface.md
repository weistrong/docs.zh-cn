---
description: 了解详细信息： ISymUnmanagedReader 接口
title: ISymUnmanagedReader 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader
helpviewer_keywords:
- ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: aa3cc15d-058e-4e6f-b03e-39569646ba47
topic_type:
- apiref
ms.openlocfilehash: bad4fdbac3bf6f03fa0db79ce54a5b0ca897028f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763795"
---
# <a name="isymunmanagedreader-interface"></a><span data-ttu-id="47ec0-103">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="47ec0-103">ISymUnmanagedReader Interface</span></span>

<span data-ttu-id="47ec0-104">表示一个符号读取器，该读取器提供对符号存储区中文档、方法和变量的访问。</span><span class="sxs-lookup"><span data-stu-id="47ec0-104">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="47ec0-105">方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-105">Methods</span></span>  
  
|<span data-ttu-id="47ec0-106">方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-106">Method</span></span>|<span data-ttu-id="47ec0-107">说明</span><span class="sxs-lookup"><span data-stu-id="47ec0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="47ec0-108">GetDocument 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-108">GetDocument Method</span></span>](isymunmanagedreader-getdocument-method.md)|<span data-ttu-id="47ec0-109">查找文档。</span><span class="sxs-lookup"><span data-stu-id="47ec0-109">Finds a document.</span></span>|  
|[<span data-ttu-id="47ec0-110">GetDocuments 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-110">GetDocuments Method</span></span>](isymunmanagedreader-getdocuments-method.md)|<span data-ttu-id="47ec0-111">返回在符号存储区中定义的所有文档的数组。</span><span class="sxs-lookup"><span data-stu-id="47ec0-111">Returns an array of all the documents defined in the symbol store.</span></span>|  
|[<span data-ttu-id="47ec0-112">GetDocumentVersion 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-112">GetDocumentVersion Method</span></span>](isymunmanagedreader-getdocumentversion-method.md)|<span data-ttu-id="47ec0-113">获取指定文档的指定版本。</span><span class="sxs-lookup"><span data-stu-id="47ec0-113">Gets the specified version of the specified document.</span></span>|  
|[<span data-ttu-id="47ec0-114">GetGlobalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-114">GetGlobalVariables Method</span></span>](isymunmanagedreader-getglobalvariables-method.md)|<span data-ttu-id="47ec0-115">返回所有全局变量。</span><span class="sxs-lookup"><span data-stu-id="47ec0-115">Returns all global variables.</span></span>|  
|[<span data-ttu-id="47ec0-116">GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-116">GetMethod Method</span></span>](isymunmanagedreader-getmethod-method.md)|<span data-ttu-id="47ec0-117">在给定方法标记的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="47ec0-117">Gets a symbol reader method, given a method token.</span></span>|  
|[<span data-ttu-id="47ec0-118">GetMethodByVersion 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-118">GetMethodByVersion Method</span></span>](isymunmanagedreader-getmethodbyversion-method.md)|<span data-ttu-id="47ec0-119">在给定方法标记和编辑和复制版本号的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="47ec0-119">Gets a symbol reader method, given a method token and an edit-and-copy version number.</span></span>|  
|[<span data-ttu-id="47ec0-120">GetMethodFromDocumentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-120">GetMethodFromDocumentPosition Method</span></span>](isymunmanagedreader-getmethodfromdocumentposition-method.md)|<span data-ttu-id="47ec0-121">返回包含文档中给定位置处的断点的方法。</span><span class="sxs-lookup"><span data-stu-id="47ec0-121">Returns the method that contains the breakpoint at the given position in a document.</span></span>|  
|[<span data-ttu-id="47ec0-122">GetMethodsFromDocumentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-122">GetMethodsFromDocumentPosition Method</span></span>](isymunmanagedreader-getmethodsfromdocumentposition-method.md)|<span data-ttu-id="47ec0-123">返回一组方法，其中每个方法都包含文档中给定位置处的断点。</span><span class="sxs-lookup"><span data-stu-id="47ec0-123">Returns an array of methods, each of which contains the breakpoint at the given position in a document.</span></span>|  
|[<span data-ttu-id="47ec0-124">GetMethodVersion 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-124">GetMethodVersion Method</span></span>](isymunmanagedreader-getmethodversion-method.md)|<span data-ttu-id="47ec0-125">获取方法版本。</span><span class="sxs-lookup"><span data-stu-id="47ec0-125">Gets the method version.</span></span>|  
|[<span data-ttu-id="47ec0-126">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-126">GetNamespaces Method</span></span>](isymunmanagedreader-getnamespaces-method.md)|<span data-ttu-id="47ec0-127">获取在此符号存储区的全局范围内定义的命名空间。</span><span class="sxs-lookup"><span data-stu-id="47ec0-127">Gets the namespaces defined at global scope within this symbol store.</span></span>|  
|[<span data-ttu-id="47ec0-128">GetSymAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-128">GetSymAttribute Method</span></span>](isymunmanagedreader-getsymattribute-method.md)|<span data-ttu-id="47ec0-129">根据名称获取自定义属性。</span><span class="sxs-lookup"><span data-stu-id="47ec0-129">Gets a custom attribute based upon its name.</span></span>|  
|[<span data-ttu-id="47ec0-130">GetSymbolStoreFileName 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-130">GetSymbolStoreFileName Method</span></span>](isymunmanagedreader-getsymbolstorefilename-method.md)|<span data-ttu-id="47ec0-131">提供符号存储区的磁盘上的文件名。</span><span class="sxs-lookup"><span data-stu-id="47ec0-131">Provides the on-disk file name of the symbol store.</span></span>|  
|[<span data-ttu-id="47ec0-132">GetUserEntryPoint 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-132">GetUserEntryPoint Method</span></span>](isymunmanagedreader-getuserentrypoint-method.md)|<span data-ttu-id="47ec0-133">返回指定为模块的用户入口点的方法（如果有）。</span><span class="sxs-lookup"><span data-stu-id="47ec0-133">Returns the method that was specified as the user entry point for the module, if any.</span></span>|  
|[<span data-ttu-id="47ec0-134">GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-134">GetVariables Method</span></span>](isymunmanagedreader-getvariables-method.md)|<span data-ttu-id="47ec0-135">根据给定的父和名称返回非局部变量。</span><span class="sxs-lookup"><span data-stu-id="47ec0-135">Return a non-local variable, given its parent and name.</span></span>|  
|[<span data-ttu-id="47ec0-136">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-136">Initialize Method</span></span>](isymunmanagedreader-initialize-method.md)|<span data-ttu-id="47ec0-137">用此读取器将与之关联的元数据导入程序接口以及模块的文件名初始化符号读取器。</span><span class="sxs-lookup"><span data-stu-id="47ec0-137">Initializes the symbol reader with the metadata importer interface that this reader will be associated with, along with the file name of the module.</span></span>|  
|[<span data-ttu-id="47ec0-138">ReplaceSymbolStore 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-138">ReplaceSymbolStore Method</span></span>](isymunmanagedreader-replacesymbolstore-method.md)|<span data-ttu-id="47ec0-139">用增量符号存储区替换现有的符号存储区。</span><span class="sxs-lookup"><span data-stu-id="47ec0-139">Replaces the existing symbol store with a delta symbol store.</span></span>|  
|[<span data-ttu-id="47ec0-140">UpdateSymbolStore 方法</span><span class="sxs-lookup"><span data-stu-id="47ec0-140">UpdateSymbolStore Method</span></span>](isymunmanagedreader-updatesymbolstore-method.md)|<span data-ttu-id="47ec0-141">使用增量符号存储区更新现有的符号存储区。</span><span class="sxs-lookup"><span data-stu-id="47ec0-141">Updates the existing symbol store with a delta symbol store.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="47ec0-142">要求</span><span class="sxs-lookup"><span data-stu-id="47ec0-142">Requirements</span></span>  

 <span data-ttu-id="47ec0-143">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="47ec0-143">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47ec0-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="47ec0-144">See also</span></span>

- [<span data-ttu-id="47ec0-145">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="47ec0-145">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="47ec0-146">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="47ec0-146">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)
