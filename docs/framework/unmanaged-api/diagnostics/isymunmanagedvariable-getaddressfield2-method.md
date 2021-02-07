---
description: 了解详细信息： ISymUnmanagedVariable：： GetAddressField2 方法
title: ISymUnmanagedVariable::GetAddressField2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField2
helpviewer_keywords:
- GetAddressField2 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField2 method [.NET Framework debugging]
ms.assetid: 1f25b294-72b6-4882-a49b-6c9d364b6008
topic_type:
- apiref
ms.openlocfilehash: 5d9bc226bfc462157e66b1d8fb43762945cdc016
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762963"
---
# <a name="isymunmanagedvariablegetaddressfield2-method"></a><span data-ttu-id="9cbb1-103">ISymUnmanagedVariable::GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="9cbb1-103">ISymUnmanagedVariable::GetAddressField2 Method</span></span>

<span data-ttu-id="9cbb1-104">获取此变量的第二个地址字段。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-104">Gets the second address field for this variable.</span></span> <span data-ttu-id="9cbb1-105">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-105">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cbb1-106">语法</span><span class="sxs-lookup"><span data-stu-id="9cbb1-106">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressField2(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9cbb1-107">参数</span><span class="sxs-lookup"><span data-stu-id="9cbb1-107">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="9cbb1-108">弄指向的指针 `ULONG32` ，该指针接收第二个地址字段。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-108">[out] A pointer to a `ULONG32` that receives the second address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9cbb1-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9cbb1-109">Return Value</span></span>  

 <span data-ttu-id="9cbb1-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cbb1-111">要求</span><span class="sxs-lookup"><span data-stu-id="9cbb1-111">Requirements</span></span>  

 <span data-ttu-id="9cbb1-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="9cbb1-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cbb1-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="9cbb1-113">See also</span></span>

- [<span data-ttu-id="9cbb1-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="9cbb1-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="9cbb1-115">GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="9cbb1-115">GetAddressField1 Method</span></span>](isymunmanagedvariable-getaddressfield1-method.md)
- [<span data-ttu-id="9cbb1-116">GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="9cbb1-116">GetAddressField3 Method</span></span>](isymunmanagedvariable-getaddressfield3-method.md)
- [<span data-ttu-id="9cbb1-117">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="9cbb1-117">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)
