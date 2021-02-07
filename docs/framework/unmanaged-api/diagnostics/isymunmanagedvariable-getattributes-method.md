---
description: 了解详细信息： ISymUnmanagedVariable：： GetAttributes 方法
title: ISymUnmanagedVariable::GetAttributes 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAttributes
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAttributes
helpviewer_keywords:
- GetAttributes method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAttributes method [.NET Framework debugging]
ms.assetid: 80f168af-a6a6-4c8f-b9e6-8a82dc834ed5
topic_type:
- apiref
ms.openlocfilehash: 0adaeaf512f129f92b7f15cdba375395a0a81855
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762833"
---
# <a name="isymunmanagedvariablegetattributes-method"></a><span data-ttu-id="65987-103">ISymUnmanagedVariable::GetAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="65987-103">ISymUnmanagedVariable::GetAttributes Method</span></span>

<span data-ttu-id="65987-104">获取此变量的特性标志。</span><span class="sxs-lookup"><span data-stu-id="65987-104">Gets the attribute flags for this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65987-105">语法</span><span class="sxs-lookup"><span data-stu-id="65987-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAttributes(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="65987-106">参数</span><span class="sxs-lookup"><span data-stu-id="65987-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="65987-107">弄指向接收特性的的指针 `ULONG32` 。</span><span class="sxs-lookup"><span data-stu-id="65987-107">[out] A pointer to a `ULONG32` that receives the attributes.</span></span> <span data-ttu-id="65987-108">返回的值将是 [CorSymVarFlag](corsymvarflag-enumeration.md) 枚举中定义的值之一。</span><span class="sxs-lookup"><span data-stu-id="65987-108">The returned value will be one of the values defined in the [CorSymVarFlag](corsymvarflag-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="65987-109">返回值</span><span class="sxs-lookup"><span data-stu-id="65987-109">Return Value</span></span>  

 <span data-ttu-id="65987-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="65987-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65987-111">要求</span><span class="sxs-lookup"><span data-stu-id="65987-111">Requirements</span></span>  

 <span data-ttu-id="65987-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="65987-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65987-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="65987-113">See also</span></span>

- [<span data-ttu-id="65987-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="65987-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
