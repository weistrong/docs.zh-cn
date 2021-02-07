---
description: 了解详细信息： ISymUnmanagedWriter：： Initialize2 方法
title: ISymUnmanagedWriter::Initialize2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Initialize2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Initialize2
helpviewer_keywords:
- ISymUnmanagedWriter::Initialize2 method [.NET Framework debugging]
- Initialize2 method [.NET Framework debugging]
ms.assetid: 93de56b6-4ae8-4cca-acdc-25a434623509
topic_type:
- apiref
ms.openlocfilehash: 0d4c769c9f1b571296cbfe159057df083a6d5ca6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762274"
---
# <a name="isymunmanagedwriterinitialize2-method"></a><span data-ttu-id="1af29-103">ISymUnmanagedWriter::Initialize2 方法</span><span class="sxs-lookup"><span data-stu-id="1af29-103">ISymUnmanagedWriter::Initialize2 Method</span></span>

<span data-ttu-id="1af29-104">设置此编写器将与之关联的元数据发射器接口，并设置调试符号将写入的输出文件名。</span><span class="sxs-lookup"><span data-stu-id="1af29-104">Sets the metadata emitter interface with which this writer will be associated, and sets the output file name to which the debugging symbols will be written.</span></span> <span data-ttu-id="1af29-105">此方法还允许您设置程序数据库 (PDB) 文件的最终位置。</span><span class="sxs-lookup"><span data-stu-id="1af29-105">This method also lets you set the final location of the program database (PDB) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1af29-106">语法</span><span class="sxs-lookup"><span data-stu-id="1af29-106">Syntax</span></span>  
  
```cpp  
HRESULT Initialize2(  
    [in] IUnknown     *emitter,  
    [in] const WCHAR  *tempfilename,  
    [in] IStream      *pIStream,  
    [in] BOOL         fFullBuild,  
    [in] const WCHAR  *finalfilename);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1af29-107">参数</span><span class="sxs-lookup"><span data-stu-id="1af29-107">Parameters</span></span>  

 `emitter`  
 <span data-ttu-id="1af29-108">中指向元数据发射器接口的指针。</span><span class="sxs-lookup"><span data-stu-id="1af29-108">[in] A pointer to the metadata emitter interface.</span></span>  
  
 `tempfilename`  
 <span data-ttu-id="1af29-109">中指向的指针 `WCHAR` ，该指针包含向其中写入调试符号的文件名。</span><span class="sxs-lookup"><span data-stu-id="1af29-109">[in] A pointer to a `WCHAR` that contains the file name to which the debugging symbols are written.</span></span> <span data-ttu-id="1af29-110">如果为不使用文件名的编写器指定文件名，则忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="1af29-110">If a file name is specified for a writer that does not use file names, this parameter is ignored.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="1af29-111">中如果已指定，则符号编写器会将符号发送到给定的 <xref:System.Runtime.InteropServices.ComTypes.IStream> （而不是参数中指定的文件） `filename` 。</span><span class="sxs-lookup"><span data-stu-id="1af29-111">[in] If specified, the symbol writer emits the symbols into the given <xref:System.Runtime.InteropServices.ComTypes.IStream> rather than to the file specified in the `filename` parameter.</span></span> <span data-ttu-id="1af29-112">`pIStream` 参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="1af29-112">The `pIStream` parameter is optional.</span></span>  
  
 `fFullBuild`  
 <span data-ttu-id="1af29-113">[in] `true` 如果这是完全重新生成，则为; `false` 如果这是增量编译，则为。</span><span class="sxs-lookup"><span data-stu-id="1af29-113">[in] `true` if this is a full rebuild; `false` if this is an incremental compilation.</span></span>  
  
 `finalfilename`  
 <span data-ttu-id="1af29-114">中指向的指针 `WCHAR` ，它是 PDB 文件的最终位置的路径字符串。</span><span class="sxs-lookup"><span data-stu-id="1af29-114">[in] A pointer to a `WCHAR` that is the path string to the final location of the PDB file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1af29-115">返回值</span><span class="sxs-lookup"><span data-stu-id="1af29-115">Return Value</span></span>  

 <span data-ttu-id="1af29-116">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="1af29-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1af29-117">要求</span><span class="sxs-lookup"><span data-stu-id="1af29-117">Requirements</span></span>  

 <span data-ttu-id="1af29-118">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="1af29-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1af29-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="1af29-119">See also</span></span>

- [<span data-ttu-id="1af29-120">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="1af29-120">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="1af29-121">Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="1af29-121">Initialize Method</span></span>](isymunmanagedwriter-initialize-method.md)
