---
description: 了解详细信息： ISymUnmanagedConstant：： GetValue 方法
title: ISymUnmanagedConstant::GetValue 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetValue
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetValue
helpviewer_keywords:
- GetValue method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetValue method [.NET Framework debugging]
ms.assetid: 0036fc10-e768-47a8-b9cf-bf47faf8d194
topic_type:
- apiref
ms.openlocfilehash: 05818028deb804bf2a2426285b5185b01776199d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689685"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="c10e5-103">ISymUnmanagedConstant::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="c10e5-103">ISymUnmanagedConstant::GetValue Method</span></span>

<span data-ttu-id="c10e5-104">获取常量的值。</span><span class="sxs-lookup"><span data-stu-id="c10e5-104">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c10e5-105">语法</span><span class="sxs-lookup"><span data-stu-id="c10e5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c10e5-106">参数</span><span class="sxs-lookup"><span data-stu-id="c10e5-106">Parameters</span></span>  

 `pValue`  
 <span data-ttu-id="c10e5-107">弄指向接收值的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="c10e5-107">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c10e5-108">返回值</span><span class="sxs-lookup"><span data-stu-id="c10e5-108">Return Value</span></span>  

 <span data-ttu-id="c10e5-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c10e5-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c10e5-110">要求</span><span class="sxs-lookup"><span data-stu-id="c10e5-110">Requirements</span></span>  

 <span data-ttu-id="c10e5-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c10e5-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c10e5-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="c10e5-112">See also</span></span>

- [<span data-ttu-id="c10e5-113">ISymUnmanagedConstant 接口</span><span class="sxs-lookup"><span data-stu-id="c10e5-113">ISymUnmanagedConstant Interface</span></span>](isymunmanagedconstant-interface.md)
- [<span data-ttu-id="c10e5-114">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="c10e5-114">GetName Method</span></span>](isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="c10e5-115">GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="c10e5-115">GetSignature Method</span></span>](isymunmanagedconstant-getsignature-method.md)
