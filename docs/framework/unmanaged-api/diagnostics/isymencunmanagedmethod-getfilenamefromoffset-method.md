---
description: 了解详细信息： ISymENCUnmanagedMethod：： GetFileNameFromOffset 方法
title: ISymENCUnmanagedMethod::GetFileNameFromOffset 方法
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetFileNameFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetFileNameFromOffset
helpviewer_keywords:
- GetFileNameFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetFileNameFromOffset method [.NET Framework debugging]
ms.assetid: 00e2e194-12f5-436e-a997-2b9d3e844d4f
topic_type:
- apiref
ms.openlocfilehash: 1322e55f115958a2f4b2634dfa25eff127167d54
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737995"
---
# <a name="isymencunmanagedmethodgetfilenamefromoffset-method"></a><span data-ttu-id="1db26-103">ISymENCUnmanagedMethod::GetFileNameFromOffset 方法</span><span class="sxs-lookup"><span data-stu-id="1db26-103">ISymENCUnmanagedMethod::GetFileNameFromOffset Method</span></span>

<span data-ttu-id="1db26-104">获取与偏移量关联的行的文件名。</span><span class="sxs-lookup"><span data-stu-id="1db26-104">Gets the file name for the line associated with an offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1db26-105">语法</span><span class="sxs-lookup"><span data-stu-id="1db26-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFileNameFromOffset(  
    [in]  ULONG32  dwOffset,  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
       length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1db26-106">参数</span><span class="sxs-lookup"><span data-stu-id="1db26-106">Parameters</span></span>  

 `dwOffset`  
 <span data-ttu-id="1db26-107">中一个 `ULONG32` 包含偏移量的。</span><span class="sxs-lookup"><span data-stu-id="1db26-107">[in] A `ULONG32` that contains the offset.</span></span>  
  
 `cchName`  
 <span data-ttu-id="1db26-108">中 `ULONG32` 指示缓冲区大小的 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="1db26-108">[in] A `ULONG32` that indicates the size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="1db26-109">弄指向的指针， `ULONG32` 该指针接收包含文件名所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="1db26-109">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the file names.</span></span>  
  
 `szName`  
 <span data-ttu-id="1db26-110">弄包含文件名的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="1db26-110">[out] The buffer that contains the file names.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1db26-111">返回值</span><span class="sxs-lookup"><span data-stu-id="1db26-111">Return Value</span></span>  

 <span data-ttu-id="1db26-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="1db26-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1db26-113">要求</span><span class="sxs-lookup"><span data-stu-id="1db26-113">Requirements</span></span>  

 <span data-ttu-id="1db26-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="1db26-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1db26-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1db26-115">See also</span></span>

- [<span data-ttu-id="1db26-116">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="1db26-116">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)
