---
description: 了解详细信息： ISymUnmanagedMethod：： GetSequencePoints 方法
title: ISymUnmanagedMethod::GetSequencePoints 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSequencePoints
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSequencePoints
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePoints method [.NET Framework debugging]
- GetSequencePoints method [.NET Framework debugging]
ms.assetid: f909ac48-3d8f-49fb-a369-e3d9959151cd
topic_type:
- apiref
ms.openlocfilehash: acdfcb014648593065bd1ae252ef936898a1e8b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721289"
---
# <a name="isymunmanagedmethodgetsequencepoints-method"></a><span data-ttu-id="94a9c-103">ISymUnmanagedMethod::GetSequencePoints 方法</span><span class="sxs-lookup"><span data-stu-id="94a9c-103">ISymUnmanagedMethod::GetSequencePoints Method</span></span>

<span data-ttu-id="94a9c-104">获取此方法中的所有序列点。</span><span class="sxs-lookup"><span data-stu-id="94a9c-104">Gets all the sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94a9c-105">语法</span><span class="sxs-lookup"><span data-stu-id="94a9c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSequencePoints(  
    [in]  ULONG32  cPoints,  
    [out] ULONG32  *pcPoints,  
    [in, size_is(cPoints)] ULONG32  offsets[],  
    [in, size_is(cPoints)] ISymUnmanagedDocument* documents[],  
    [in, size_is(cPoints)] ULONG32  lines[],  
    [in, size_is(cPoints)] ULONG32  columns[],  
    [in, size_is(cPoints)] ULONG32  endLines[],  
    [in, size_is(cPoints)] ULONG32  endColumns[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94a9c-106">参数</span><span class="sxs-lookup"><span data-stu-id="94a9c-106">Parameters</span></span>  

 `cPoints`  
 <span data-ttu-id="94a9c-107">中 `ULONG32` 接收、、、 `offsets` `documents` `lines` `columns` 、 `endLines` 和 `endColumns` 数组的大小的。</span><span class="sxs-lookup"><span data-stu-id="94a9c-107">[in] A `ULONG32` that receives the size of the `offsets`, `documents`, `lines`, `columns`, `endLines`, and `endColumns` arrays.</span></span>  
  
 `pcPoints`  
 <span data-ttu-id="94a9c-108">弄指向的指针 `ULONG32` ，该指针接收包含序列点所需的缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="94a9c-108">[out] A pointer to a `ULONG32` that receives the length of the buffer required to contain the sequence points.</span></span>  
  
 `offsets`  
 <span data-ttu-id="94a9c-109">中用于存储 Microsoft 中间语言 (MSIL 的数组，用于序列点从方法开头开始) 偏移量。</span><span class="sxs-lookup"><span data-stu-id="94a9c-109">[in] An array in which to store the Microsoft intermediate language (MSIL) offsets from the beginning of the method for the sequence points.</span></span>  
  
 `documents`  
 <span data-ttu-id="94a9c-110">中要在其中存储序列点所在的文档的数组。</span><span class="sxs-lookup"><span data-stu-id="94a9c-110">[in] An array in which to store the documents in which the sequence points are located.</span></span>  
  
 `lines`  
 <span data-ttu-id="94a9c-111">中要在其中存储序列点所在的文档中的行的数组。</span><span class="sxs-lookup"><span data-stu-id="94a9c-111">[in] An array in which to store the lines in the documents at which the sequence points are located.</span></span>  
  
 `columns`  
 <span data-ttu-id="94a9c-112">中要在其中存储序列点所在的文档中的列的数组。</span><span class="sxs-lookup"><span data-stu-id="94a9c-112">[in] An array in which to store the columns in the documents at which the sequence points are located.</span></span>  
  
 `endLines`  
 <span data-ttu-id="94a9c-113">中序列点结束的文档中的行的数组。</span><span class="sxs-lookup"><span data-stu-id="94a9c-113">[in] The array of lines in the documents at which the sequence points end.</span></span>  
  
 `endColumns`  
 <span data-ttu-id="94a9c-114">中序列点结束的文档中的列的数组。</span><span class="sxs-lookup"><span data-stu-id="94a9c-114">[in] The array of columns in the documents at which the sequence points end.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="94a9c-115">返回值</span><span class="sxs-lookup"><span data-stu-id="94a9c-115">Return Value</span></span>  

 <span data-ttu-id="94a9c-116">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="94a9c-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94a9c-117">要求</span><span class="sxs-lookup"><span data-stu-id="94a9c-117">Requirements</span></span>  

 <span data-ttu-id="94a9c-118">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="94a9c-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94a9c-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="94a9c-119">See also</span></span>

- [<span data-ttu-id="94a9c-120">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="94a9c-120">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
