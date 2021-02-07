---
description: 了解详细信息： ISymUnmanagedSymbolSearchInfo：： GetHRESULT 方法
title: ISymUnmanagedSymbolSearchInfo::GetHRESULT 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetHRESULT
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT method [.NET Framework debugging]
- GetHRESULT method [.NET Framework debugging]
ms.assetid: 6999dc3d-65d7-4bf6-bb0a-6efc0fc72588
topic_type:
- apiref
ms.openlocfilehash: 5d351d84ba4e91ccb9acb531e77407a2d1caceec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763106"
---
# <a name="isymunmanagedsymbolsearchinfogethresult-method"></a><span data-ttu-id="6bc57-103">ISymUnmanagedSymbolSearchInfo::GetHRESULT 方法</span><span class="sxs-lookup"><span data-stu-id="6bc57-103">ISymUnmanagedSymbolSearchInfo::GetHRESULT Method</span></span>

<span data-ttu-id="6bc57-104">获取 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="6bc57-104">Gets the HRESULT.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bc57-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bc57-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHRESULT(  
    [out] HRESULT *phr);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6bc57-106">参数</span><span class="sxs-lookup"><span data-stu-id="6bc57-106">Parameters</span></span>  

 `phr`  
 <span data-ttu-id="6bc57-107">弄指向 HRESULT 的指针。</span><span class="sxs-lookup"><span data-stu-id="6bc57-107">[out] A pointer to the HRESULT.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6bc57-108">返回值</span><span class="sxs-lookup"><span data-stu-id="6bc57-108">Return Value</span></span>  

 <span data-ttu-id="6bc57-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="6bc57-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bc57-110">要求</span><span class="sxs-lookup"><span data-stu-id="6bc57-110">Requirements</span></span>  

 <span data-ttu-id="6bc57-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="6bc57-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bc57-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bc57-112">See also</span></span>

- [<span data-ttu-id="6bc57-113">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="6bc57-113">ISymUnmanagedSymbolSearchInfo Interface</span></span>](isymunmanagedsymbolsearchinfo-interface.md)
