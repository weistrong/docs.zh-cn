---
description: 了解详细信息： ISymUnmanagedVariable：： GetEndOffset 方法
title: ISymUnmanagedVariable::GetEndOffset 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedVariable::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedVariable interface [.NET Framework debugging]
ms.assetid: e5d777c5-d450-4c0f-999c-b3953ee22cfb
topic_type:
- apiref
ms.openlocfilehash: 302f19c0d9fce1864e94a79efe3a3d1515478c0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762794"
---
# <a name="isymunmanagedvariablegetendoffset-method"></a><span data-ttu-id="527bf-103">ISymUnmanagedVariable::GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="527bf-103">ISymUnmanagedVariable::GetEndOffset Method</span></span>

<span data-ttu-id="527bf-104">获取此变量在其父级内的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="527bf-104">Gets the end offset of this variable within its parent.</span></span> <span data-ttu-id="527bf-105">如果这是一个作用域内的本地变量，则结束偏移量将在为该作用域定义的偏移量内。</span><span class="sxs-lookup"><span data-stu-id="527bf-105">If this is a local variable within a scope, the end offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="527bf-106">语法</span><span class="sxs-lookup"><span data-stu-id="527bf-106">Syntax</span></span>  
  
```cpp  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="527bf-107">参数</span><span class="sxs-lookup"><span data-stu-id="527bf-107">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="527bf-108">弄指向的指针 `ULONG32` ，该指针接收结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="527bf-108">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="527bf-109">返回值</span><span class="sxs-lookup"><span data-stu-id="527bf-109">Return Value</span></span>  

 <span data-ttu-id="527bf-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="527bf-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="527bf-111">要求</span><span class="sxs-lookup"><span data-stu-id="527bf-111">Requirements</span></span>  

 <span data-ttu-id="527bf-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="527bf-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="527bf-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="527bf-113">See also</span></span>

- [<span data-ttu-id="527bf-114">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="527bf-114">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
- [<span data-ttu-id="527bf-115">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="527bf-115">GetStartOffset Method</span></span>](isymunmanagedvariable-getstartoffset-method.md)
