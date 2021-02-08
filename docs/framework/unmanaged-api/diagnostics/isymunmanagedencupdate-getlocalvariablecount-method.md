---
description: 了解详细信息： ISymUnmanagedENCUpdate：： GetLocalVariableCount 方法
title: ISymUnmanagedENCUpdate::GetLocalVariableCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariableCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount method [.NET Framework debugging]
- GetLocalVariableCount method [.NET Framework debugging]
ms.assetid: 9777d8bb-4abc-4be8-aa7c-34f853eceb9c
topic_type:
- apiref
ms.openlocfilehash: ab75ba0b0dda5722aebdbdc8b9a242cc90b0ac11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790147"
---
# <a name="isymunmanagedencupdategetlocalvariablecount-method"></a><span data-ttu-id="f96cc-103">ISymUnmanagedENCUpdate::GetLocalVariableCount 方法</span><span class="sxs-lookup"><span data-stu-id="f96cc-103">ISymUnmanagedENCUpdate::GetLocalVariableCount Method</span></span>

<span data-ttu-id="f96cc-104">获取局部变量的数目。</span><span class="sxs-lookup"><span data-stu-id="f96cc-104">Gets the number of local variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f96cc-105">语法</span><span class="sxs-lookup"><span data-stu-id="f96cc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalVariableCount(  
    [in]  mdMethodDef  mdMethodToken,  
    [out] ULONG        *pcLocals);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f96cc-106">参数</span><span class="sxs-lookup"><span data-stu-id="f96cc-106">Parameters</span></span>  

 `mdMethodToken`  
 <span data-ttu-id="f96cc-107">中方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f96cc-107">[in] The metadata token of methods.</span></span>  
  
 `pcLocals`  
 <span data-ttu-id="f96cc-108">弄指向的指针， `ULONG32` 该指针接收包含局部变量数所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="f96cc-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the number of local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f96cc-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f96cc-109">Return Value</span></span>  

 <span data-ttu-id="f96cc-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f96cc-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f96cc-111">要求</span><span class="sxs-lookup"><span data-stu-id="f96cc-111">Requirements</span></span>  

 <span data-ttu-id="f96cc-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f96cc-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f96cc-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f96cc-113">See also</span></span>

- [<span data-ttu-id="f96cc-114">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="f96cc-114">ISymUnmanagedENCUpdate Interface</span></span>](isymunmanagedencupdate-interface.md)
