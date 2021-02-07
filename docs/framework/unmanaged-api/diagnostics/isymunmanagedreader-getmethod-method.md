---
description: 了解详细信息： ISymUnmanagedReader：： GetMethod 方法
title: ISymUnmanagedReader::GetMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedReader interface [.NET Framework debugging]
- ISymUnmanagedReader::GetMethod method [.NET Framework debugging]
ms.assetid: ae6cfb29-bc2c-4606-af86-1d32ebd31020
topic_type:
- apiref
ms.openlocfilehash: 7c0bb65840a3bc1c9450ad29fa8438cdb0377a16
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689490"
---
# <a name="isymunmanagedreadergetmethod-method"></a><span data-ttu-id="ec9e0-103">ISymUnmanagedReader::GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="ec9e0-103">ISymUnmanagedReader::GetMethod Method</span></span>

<span data-ttu-id="ec9e0-104">在给定方法标记的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="ec9e0-104">Gets a symbol reader method, given a method token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec9e0-105">语法</span><span class="sxs-lookup"><span data-stu-id="ec9e0-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethod (  
    [in]  mdMethodDef  token,  
    [out, retval] ISymUnmanagedMethod**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec9e0-106">参数</span><span class="sxs-lookup"><span data-stu-id="ec9e0-106">Parameters</span></span>  

 `token`  
 <span data-ttu-id="ec9e0-107">中方法标记。</span><span class="sxs-lookup"><span data-stu-id="ec9e0-107">[in] The method token.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="ec9e0-108">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="ec9e0-108">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ec9e0-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ec9e0-109">Return Value</span></span>  

 <span data-ttu-id="ec9e0-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ec9e0-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec9e0-111">要求</span><span class="sxs-lookup"><span data-stu-id="ec9e0-111">Requirements</span></span>  

 <span data-ttu-id="ec9e0-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ec9e0-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec9e0-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="ec9e0-113">See also</span></span>

- [<span data-ttu-id="ec9e0-114">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="ec9e0-114">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
