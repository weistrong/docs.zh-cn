---
description: 了解详细信息： ISymUnmanagedReaderSymbolSearchInfo：： GetSymbolSearchInfoCount 方法
title: ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo.GetSymbolSearchInfoCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount
helpviewer_keywords:
- GetSymbolSearchInfoCount method [.NET Framework debugging]
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount method [.NET Framework debugging]
ms.assetid: 4068b6ec-525f-4446-8818-0296178cbd19
topic_type:
- apiref
ms.openlocfilehash: b8bfa61397850c3f960fe30c0136e0a8b074cf1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763587"
---
# <a name="isymunmanagedreadersymbolsearchinfogetsymbolsearchinfocount-method"></a><span data-ttu-id="7792b-103">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="7792b-103">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount Method</span></span>

<span data-ttu-id="7792b-104">获取符号搜索信息的计数。</span><span class="sxs-lookup"><span data-stu-id="7792b-104">Gets a count of symbol search information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7792b-105">语法</span><span class="sxs-lookup"><span data-stu-id="7792b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolSearchInfoCount(  
    [out] ULONG32 *pcSearchInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7792b-106">参数</span><span class="sxs-lookup"><span data-stu-id="7792b-106">Parameters</span></span>  

 `pcSearchInfo`  
 <span data-ttu-id="7792b-107">] out] 指向的指针 `ULONG32` ，该指针接收包含搜索信息所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="7792b-107">]out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the search information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7792b-108">返回值</span><span class="sxs-lookup"><span data-stu-id="7792b-108">Return Value</span></span>  

 <span data-ttu-id="7792b-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="7792b-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7792b-110">要求</span><span class="sxs-lookup"><span data-stu-id="7792b-110">Requirements</span></span>  

 <span data-ttu-id="7792b-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="7792b-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7792b-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="7792b-112">See also</span></span>

- [<span data-ttu-id="7792b-113">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="7792b-113">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](isymunmanagedreadersymbolsearchinfo-interface.md)
