---
description: 了解详细信息： ISymUnmanagedSymbolSearchInfo：： GetSearchPathLength 方法
title: ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetSearchPathLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength
helpviewer_keywords:
- GetSearchPathLength method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength method [.NET Framework debugging]
ms.assetid: 274e73cf-8333-47ba-ac12-70214e2b0112
topic_type:
- apiref
ms.openlocfilehash: 3d5faf9d972881ff9c1eaf71bcaa6f68da46dae6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763015"
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpathlength-method"></a><span data-ttu-id="c3d93-103">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法</span><span class="sxs-lookup"><span data-stu-id="c3d93-103">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength Method</span></span>

<span data-ttu-id="c3d93-104">获取搜索路径长度。</span><span class="sxs-lookup"><span data-stu-id="c3d93-104">Gets the search path length.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3d93-105">语法</span><span class="sxs-lookup"><span data-stu-id="c3d93-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c3d93-106">参数</span><span class="sxs-lookup"><span data-stu-id="c3d93-106">Parameters</span></span>  

 `pcchPath`  
 <span data-ttu-id="c3d93-107">弄指向的指针， `ULONG32` 该指针接收包含搜索路径长度所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="c3d93-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path length.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c3d93-108">返回值</span><span class="sxs-lookup"><span data-stu-id="c3d93-108">Return Value</span></span>  

 <span data-ttu-id="c3d93-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c3d93-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3d93-110">要求</span><span class="sxs-lookup"><span data-stu-id="c3d93-110">Requirements</span></span>  

 <span data-ttu-id="c3d93-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c3d93-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3d93-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3d93-112">See also</span></span>

- [<span data-ttu-id="c3d93-113">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="c3d93-113">ISymUnmanagedSymbolSearchInfo Interface</span></span>](isymunmanagedsymbolsearchinfo-interface.md)
