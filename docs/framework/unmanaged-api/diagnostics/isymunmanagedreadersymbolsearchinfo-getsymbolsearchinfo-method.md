---
description: 了解详细信息： ISymUnmanagedReaderSymbolSearchInfo：： GetSymbolSearchInfo 方法
title: ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo.GetSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo
helpviewer_keywords:
- GetSymbolSearchInfo method [.NET Framework debugging]
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo method [.NET Framework debugging]
ms.assetid: 40fcdbc5-3bb2-41e9-b995-40984c209a7f
topic_type:
- apiref
ms.openlocfilehash: e14f78d6736684205b3f86150ce1fbb44a8112b7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763600"
---
# <a name="isymunmanagedreadersymbolsearchinfogetsymbolsearchinfo-method"></a><span data-ttu-id="c559b-103">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo 方法</span><span class="sxs-lookup"><span data-stu-id="c559b-103">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo Method</span></span>

<span data-ttu-id="c559b-104">获取符号搜索信息。</span><span class="sxs-lookup"><span data-stu-id="c559b-104">Gets symbol search information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c559b-105">语法</span><span class="sxs-lookup"><span data-stu-id="c559b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolSearchInfo(  
    [in]  ULONG32  cSearchInfo,  
    [out] ULONG32  *pcSearchInfo,  
    [out, size_is(cSearchInfo), length_is(*pcSearchInfo)]  
        ISymUnmanagedSymbolSearchInfo **rgpSearchInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c559b-106">参数</span><span class="sxs-lookup"><span data-stu-id="c559b-106">Parameters</span></span>  

 `cSearchInfo`  
 <span data-ttu-id="c559b-107">中 `ULONG32` 指示的大小的 `rgpSearchInfo` 。</span><span class="sxs-lookup"><span data-stu-id="c559b-107">[in] A `ULONG32` that indicates the size of `rgpSearchInfo`.</span></span>  
  
 `pcSearchInfo`  
 <span data-ttu-id="c559b-108">弄指向的指针 `ULONG32` ，该指针接收包含搜索信息所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="c559b-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the search information.</span></span>  
  
 `rgpSearchInfo`  
 <span data-ttu-id="c559b-109">弄设置为返回的 [ISymUnmanagedSymbolSearchInfo](isymunmanagedsymbolsearchinfo-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="c559b-109">[out] A pointer that is set to the returned [ISymUnmanagedSymbolSearchInfo](isymunmanagedsymbolsearchinfo-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c559b-110">返回值</span><span class="sxs-lookup"><span data-stu-id="c559b-110">Return Value</span></span>  

 <span data-ttu-id="c559b-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c559b-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c559b-112">要求</span><span class="sxs-lookup"><span data-stu-id="c559b-112">Requirements</span></span>  

 <span data-ttu-id="c559b-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c559b-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c559b-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c559b-114">See also</span></span>

- [<span data-ttu-id="c559b-115">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="c559b-115">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](isymunmanagedreadersymbolsearchinfo-interface.md)
