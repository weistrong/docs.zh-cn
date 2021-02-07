---
description: 了解详细信息： ISymUnmanagedWriter：： RemapToken 方法
title: ISymUnmanagedWriter::RemapToken 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.RemapToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::RemapToken
helpviewer_keywords:
- ISymUnmanagedWriter::RemapToken method [.NET Framework debugging]
- RemapToken method [.NET Framework debugging]
ms.assetid: bca92682-ee1e-467f-8fb0-d8d4617f82fe
topic_type:
- apiref
ms.openlocfilehash: c065d42c3d2749f0262fdd81a74de918274ba67d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762079"
---
# <a name="isymunmanagedwriterremaptoken-method"></a><span data-ttu-id="69abe-103">ISymUnmanagedWriter::RemapToken 方法</span><span class="sxs-lookup"><span data-stu-id="69abe-103">ISymUnmanagedWriter::RemapToken Method</span></span>

<span data-ttu-id="69abe-104">通知符号编写器在发出元数据时已重新映射元数据标记。</span><span class="sxs-lookup"><span data-stu-id="69abe-104">Notifies the symbol writer that a metadata token has been remapped as the metadata was emitted.</span></span> <span data-ttu-id="69abe-105">如果符号编写器已将旧标记存储在符号存储区中，则必须用新值更新已存储的标记，或者必须将相应符号读取器的映射保存到读取阶段中重新映射。</span><span class="sxs-lookup"><span data-stu-id="69abe-105">If the symbol writer has stored the old token within the symbol store, it must either update the stored token with the new value, or it must save the map for the corresponding symbol reader to remap during the read phase.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69abe-106">语法</span><span class="sxs-lookup"><span data-stu-id="69abe-106">Syntax</span></span>  
  
```cpp  
HRESULT RemapToken(  
    [in] mdToken  oldToken,  
    [in] mdToken  newToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="69abe-107">参数</span><span class="sxs-lookup"><span data-stu-id="69abe-107">Parameters</span></span>  

 `oldToken`  
 <span data-ttu-id="69abe-108">中重新映射的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="69abe-108">[in] The metadata token that was remapped.</span></span>  
  
 `newToken`  
 <span data-ttu-id="69abe-109">中重新映射到的新的元数据标记 `oldToken` 。</span><span class="sxs-lookup"><span data-stu-id="69abe-109">[in] The new metadata token to which `oldToken` was remapped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="69abe-110">返回值</span><span class="sxs-lookup"><span data-stu-id="69abe-110">Return Value</span></span>  

 <span data-ttu-id="69abe-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="69abe-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="69abe-112">要求</span><span class="sxs-lookup"><span data-stu-id="69abe-112">Requirements</span></span>  

 <span data-ttu-id="69abe-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="69abe-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69abe-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="69abe-114">See also</span></span>

- [<span data-ttu-id="69abe-115">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="69abe-115">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
