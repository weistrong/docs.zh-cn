---
description: 了解详细信息： ISymUnmanagedConstant：： GetName 方法
title: ISymUnmanagedConstant::GetName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetName
helpviewer_keywords:
- ISymUnmanagedConstant::GetName method [.NET Framework debugging]
- GetName method, ISymUnmanagedConstant interface [.NET Framework debugging]
ms.assetid: cbaca4e1-4473-459b-ba34-f1f59ce7c0ba
topic_type:
- apiref
ms.openlocfilehash: 57531711ed60c9e35e749a3cb1f1ba5d5c48ca66
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689815"
---
# <a name="isymunmanagedconstantgetname-method"></a><span data-ttu-id="c3d1a-103">ISymUnmanagedConstant::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="c3d1a-103">ISymUnmanagedConstant::GetName Method</span></span>

<span data-ttu-id="c3d1a-104">获取常数的名称。</span><span class="sxs-lookup"><span data-stu-id="c3d1a-104">Gets the name of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3d1a-105">语法</span><span class="sxs-lookup"><span data-stu-id="c3d1a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c3d1a-106">参数</span><span class="sxs-lookup"><span data-stu-id="c3d1a-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="c3d1a-107">中参数指向的缓冲区的长度 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="c3d1a-107">[in] The length of the buffer that the `szName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="c3d1a-108">弄指向的指针， `ULONG32` 该指针接收包含名称（包括 null 终止）所需的缓冲区的大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="c3d1a-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="c3d1a-109">弄存储名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="c3d1a-109">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c3d1a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="c3d1a-110">Return Value</span></span>  

 <span data-ttu-id="c3d1a-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c3d1a-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3d1a-112">要求</span><span class="sxs-lookup"><span data-stu-id="c3d1a-112">Requirements</span></span>  

 <span data-ttu-id="c3d1a-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c3d1a-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3d1a-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3d1a-114">See also</span></span>

- [<span data-ttu-id="c3d1a-115">ISymUnmanagedConstant 接口</span><span class="sxs-lookup"><span data-stu-id="c3d1a-115">ISymUnmanagedConstant Interface</span></span>](isymunmanagedconstant-interface.md)
- [<span data-ttu-id="c3d1a-116">GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="c3d1a-116">GetSignature Method</span></span>](isymunmanagedconstant-getsignature-method.md)
- [<span data-ttu-id="c3d1a-117">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="c3d1a-117">GetValue Method</span></span>](isymunmanagedconstant-getvalue-method.md)
