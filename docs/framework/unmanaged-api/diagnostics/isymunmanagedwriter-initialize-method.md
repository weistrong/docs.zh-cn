---
description: 了解详细信息： ISymUnmanagedWriter：： Initialize 方法
title: ISymUnmanagedWriter::Initialize 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Initialize
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Initialize
helpviewer_keywords:
- ISymUnmanagedWriter::Initialize method [.NET Framework debugging]
- Initialize method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: e0ebd793-3764-4df0-8f12-0e95f60b9eae
topic_type:
- apiref
ms.openlocfilehash: eab60e9539df3d43a1602268d704ac324f028915
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762287"
---
# <a name="isymunmanagedwriterinitialize-method"></a><span data-ttu-id="00620-103">ISymUnmanagedWriter::Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="00620-103">ISymUnmanagedWriter::Initialize Method</span></span>

<span data-ttu-id="00620-104">设置此编写器将与之关联的元数据发射器接口，并设置调试符号将写入的输出文件名。</span><span class="sxs-lookup"><span data-stu-id="00620-104">Sets the metadata emitter interface with which this writer will be associated, and sets the output file name to which the debugging symbols will be written.</span></span>  
  
 <span data-ttu-id="00620-105">此方法只能调用一次，并且必须在任何其他编写器方法之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="00620-105">This method can be called only once, and it must be called before any other writer methods.</span></span> <span data-ttu-id="00620-106">某些编写器可能需要文件名。</span><span class="sxs-lookup"><span data-stu-id="00620-106">Some writers may require a file name.</span></span> <span data-ttu-id="00620-107">但是，您始终可以将文件名传递给此方法，而不会对不使用文件名的编写器产生任何负面影响。</span><span class="sxs-lookup"><span data-stu-id="00620-107">However, you can always pass a file name to this method without any negative effect on writers that do not use the file name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00620-108">语法</span><span class="sxs-lookup"><span data-stu-id="00620-108">Syntax</span></span>  
  
```cpp  
HRESULT Initialize(  
    [in] IUnknown     *emitter,  
    [in] const WCHAR  *filename,  
    [in] IStream      *pIStream,  
    [in] BOOL         fFullBuild);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00620-109">参数</span><span class="sxs-lookup"><span data-stu-id="00620-109">Parameters</span></span>  

 `emitter`  
 <span data-ttu-id="00620-110">中指向元数据发射器接口的指针。</span><span class="sxs-lookup"><span data-stu-id="00620-110">[in] A pointer to the metadata emitter interface.</span></span>  
  
 `filename`  
 <span data-ttu-id="00620-111">中向其中写入调试符号的文件名。</span><span class="sxs-lookup"><span data-stu-id="00620-111">[in] The file name to which the debugging symbols are written.</span></span> <span data-ttu-id="00620-112">如果为不使用文件名的编写器指定文件名，则忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="00620-112">If a file name is specified for a writer that does not use file names, this parameter is ignored.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="00620-113">中如果已指定，则符号编写器会将符号发送到给定的 <xref:System.Runtime.InteropServices.ComTypes.IStream> （而不是参数中指定的文件） `filename` 。</span><span class="sxs-lookup"><span data-stu-id="00620-113">[in] If specified, the symbol writer will emit the symbols into the given <xref:System.Runtime.InteropServices.ComTypes.IStream> rather than to the file specified in the `filename` parameter.</span></span> <span data-ttu-id="00620-114">`pIStream` 参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="00620-114">The `pIStream` parameter is optional.</span></span>  
  
 `fFullBuild`  
 <span data-ttu-id="00620-115">[in] `true` 如果这是完全重新生成，则为; `false` 如果这是增量编译，则为。</span><span class="sxs-lookup"><span data-stu-id="00620-115">[in] `true` if this is a full rebuild; `false` if this is an incremental compilation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00620-116">返回值</span><span class="sxs-lookup"><span data-stu-id="00620-116">Return Value</span></span>  

 <span data-ttu-id="00620-117">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="00620-117">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00620-118">要求</span><span class="sxs-lookup"><span data-stu-id="00620-118">Requirements</span></span>  

 <span data-ttu-id="00620-119">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="00620-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00620-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="00620-120">See also</span></span>

- [<span data-ttu-id="00620-121">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="00620-121">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="00620-122">Initialize2 方法</span><span class="sxs-lookup"><span data-stu-id="00620-122">Initialize2 Method</span></span>](isymunmanagedwriter-initialize2-method.md)
