---
description: 了解详细信息： ISymUnmanagedVariable：： GetAddressKind 方法
title: ISymUnmanagedVariable::GetAddressKind 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressKind
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressKind
helpviewer_keywords:
- GetAddressKind method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressKind method [.NET Framework debugging]
ms.assetid: a71563c0-62f2-4eb4-970c-825d61827613
topic_type:
- apiref
ms.openlocfilehash: 4b090560335432ad39157fee987ce15728fece63
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762846"
---
# <a name="isymunmanagedvariablegetaddresskind-method"></a><span data-ttu-id="19f3a-103">ISymUnmanagedVariable::GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="19f3a-103">ISymUnmanagedVariable::GetAddressKind Method</span></span>

<span data-ttu-id="19f3a-104">获取此变量的地址类型。</span><span class="sxs-lookup"><span data-stu-id="19f3a-104">Gets the kind of address of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19f3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="19f3a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressKind(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="19f3a-106">参数</span><span class="sxs-lookup"><span data-stu-id="19f3a-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="19f3a-107">弄指向接收值的的指针 `ULONG32` 。</span><span class="sxs-lookup"><span data-stu-id="19f3a-107">[out] A pointer to a `ULONG32` that receives the value.</span></span> <span data-ttu-id="19f3a-108">可能的值是在 [CorSymAddrKind](corsymaddrkind-enumeration.md) 枚举中定义的。</span><span class="sxs-lookup"><span data-stu-id="19f3a-108">The possible values are defined in the [CorSymAddrKind](corsymaddrkind-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="19f3a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="19f3a-109">Return Value</span></span>  

 <span data-ttu-id="19f3a-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="19f3a-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19f3a-111">要求</span><span class="sxs-lookup"><span data-stu-id="19f3a-111">Requirements</span></span>  

 <span data-ttu-id="19f3a-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="19f3a-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19f3a-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="19f3a-113">See also</span></span>

- [<span data-ttu-id="19f3a-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="19f3a-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
