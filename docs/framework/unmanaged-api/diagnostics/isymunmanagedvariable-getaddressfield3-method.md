---
description: 了解详细信息： ISymUnmanagedVariable：： GetAddressField3 方法
title: ISymUnmanagedVariable::GetAddressField3 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField3
helpviewer_keywords:
- ISymUnmanagedVariable::GetAddressField3 method [.NET Framework debugging]
- GetAddressField3 method [.NET Framework debugging]
ms.assetid: 4d834721-ad8d-439d-b356-c6b4aef022fc
topic_type:
- apiref
ms.openlocfilehash: 286d8382857e941173c22a7aebe65adc22ab779b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762911"
---
# <a name="isymunmanagedvariablegetaddressfield3-method"></a><span data-ttu-id="9d3a6-103">ISymUnmanagedVariable::GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="9d3a6-103">ISymUnmanagedVariable::GetAddressField3 Method</span></span>

<span data-ttu-id="9d3a6-104">获取此变量的第三个地址字段。</span><span class="sxs-lookup"><span data-stu-id="9d3a6-104">Gets the third address field for this variable.</span></span> <span data-ttu-id="9d3a6-105">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="9d3a6-105">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d3a6-106">语法</span><span class="sxs-lookup"><span data-stu-id="9d3a6-106">Syntax</span></span>  
  
```cpp  
HRESULT GetAddressField3(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9d3a6-107">参数</span><span class="sxs-lookup"><span data-stu-id="9d3a6-107">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="9d3a6-108">弄指向的指针 `ULONG32` ，该指针接收第三个地址字段。</span><span class="sxs-lookup"><span data-stu-id="9d3a6-108">[out] A pointer to a `ULONG32` that receives the third address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9d3a6-109">返回值</span><span class="sxs-lookup"><span data-stu-id="9d3a6-109">Return Value</span></span>  

 <span data-ttu-id="9d3a6-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="9d3a6-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d3a6-111">要求</span><span class="sxs-lookup"><span data-stu-id="9d3a6-111">Requirements</span></span>  

 <span data-ttu-id="9d3a6-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="9d3a6-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d3a6-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d3a6-113">See also</span></span>

- [<span data-ttu-id="9d3a6-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="9d3a6-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="9d3a6-115">GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="9d3a6-115">GetAddressField1 Method</span></span>](isymunmanagedvariable-getaddressfield1-method.md)
- [<span data-ttu-id="9d3a6-116">GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="9d3a6-116">GetAddressField2 Method</span></span>](isymunmanagedvariable-getaddressfield2-method.md)
- [<span data-ttu-id="9d3a6-117">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="9d3a6-117">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)
