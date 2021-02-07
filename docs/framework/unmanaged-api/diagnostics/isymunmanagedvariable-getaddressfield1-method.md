---
description: 了解详细信息： ISymUnmanagedVariable：： GetAddressField1 方法
title: ISymUnmanagedVariable::GetAddressField1 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField1
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField1
helpviewer_keywords:
- GetAddressField1 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField1 method [.NET Framework debugging]
ms.assetid: 25788ed1-0ce3-4b97-96fc-88f8997812a3
topic_type:
- apiref
ms.openlocfilehash: 1ff6862cef52ef8fcb449563198c2df1de356530
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762989"
---
# <a name="isymunmanagedvariablegetaddressfield1-method"></a><span data-ttu-id="02942-103">ISymUnmanagedVariable::GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="02942-103">ISymUnmanagedVariable::GetAddressField1 Method</span></span>

<span data-ttu-id="02942-104">获取此变量的第一个地址字段。</span><span class="sxs-lookup"><span data-stu-id="02942-104">Gets the first address field for this variable.</span></span> <span data-ttu-id="02942-105">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="02942-105">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02942-106">语法</span><span class="sxs-lookup"><span data-stu-id="02942-106">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressField1(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="02942-107">参数</span><span class="sxs-lookup"><span data-stu-id="02942-107">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="02942-108">弄指向的指针 `ULONG32` ，该指针接收第一个地址字段。</span><span class="sxs-lookup"><span data-stu-id="02942-108">[out] A pointer to a `ULONG32` that receives the first address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="02942-109">返回值</span><span class="sxs-lookup"><span data-stu-id="02942-109">Return Value</span></span>  

 <span data-ttu-id="02942-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="02942-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02942-111">要求</span><span class="sxs-lookup"><span data-stu-id="02942-111">Requirements</span></span>  

 <span data-ttu-id="02942-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="02942-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02942-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="02942-113">See also</span></span>

- [<span data-ttu-id="02942-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="02942-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="02942-115">GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="02942-115">GetAddressField2 Method</span></span>](isymunmanagedvariable-getaddressfield2-method.md)
- [<span data-ttu-id="02942-116">GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="02942-116">GetAddressField3 Method</span></span>](isymunmanagedvariable-getaddressfield3-method.md)
- [<span data-ttu-id="02942-117">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="02942-117">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)
