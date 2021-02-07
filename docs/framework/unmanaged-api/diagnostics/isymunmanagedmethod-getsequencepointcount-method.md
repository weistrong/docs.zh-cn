---
description: 了解详细信息： ISymUnmanagedMethod：： GetSequencePointCount 方法
title: ISymUnmanagedMethod::GetSequencePointCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSequencePointCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSequencePointCount
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePointCount method [.NET Framework debugging]
- GetSequencePointCount method [.NET Framework debugging]
ms.assetid: 836133e8-6108-4b9b-b0a9-bce4e08dccda
topic_type:
- apiref
ms.openlocfilehash: 6e0341ddc151454de8764a47a92556ab1925bfa1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709993"
---
# <a name="isymunmanagedmethodgetsequencepointcount-method"></a><span data-ttu-id="f8a90-103">ISymUnmanagedMethod::GetSequencePointCount 方法</span><span class="sxs-lookup"><span data-stu-id="f8a90-103">ISymUnmanagedMethod::GetSequencePointCount Method</span></span>

<span data-ttu-id="f8a90-104">获取此方法中序列点的计数。</span><span class="sxs-lookup"><span data-stu-id="f8a90-104">Gets the count of sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8a90-105">语法</span><span class="sxs-lookup"><span data-stu-id="f8a90-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSequencePointCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f8a90-106">参数</span><span class="sxs-lookup"><span data-stu-id="f8a90-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="f8a90-107">弄指向的指针 `ULONG32` ，该指针接收包含序列点所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="f8a90-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the sequence points.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f8a90-108">返回值</span><span class="sxs-lookup"><span data-stu-id="f8a90-108">Return Value</span></span>  

 <span data-ttu-id="f8a90-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f8a90-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8a90-110">要求</span><span class="sxs-lookup"><span data-stu-id="f8a90-110">Requirements</span></span>  

 <span data-ttu-id="f8a90-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f8a90-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8a90-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8a90-112">See also</span></span>

- [<span data-ttu-id="f8a90-113">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="f8a90-113">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
