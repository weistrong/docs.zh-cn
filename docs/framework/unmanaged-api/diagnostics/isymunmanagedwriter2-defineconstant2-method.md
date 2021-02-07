---
description: 了解详细信息： ISymUnmanagedWriter2：:D efineConstant2 方法
title: ISymUnmanagedWriter2::DefineConstant2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineConstant2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineConstant2
helpviewer_keywords:
- DefineConstant2 method [.NET Framework debugging]
- ISymUnmanagedWriter2::DefineConstant2 method [.NET Framework debugging]
ms.assetid: dd2bc956-7dbe-49fc-a646-daa0d267f2df
topic_type:
- apiref
ms.openlocfilehash: 9a0c444909055e18bdcd0b54fefbc8534ff8681e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761923"
---
# <a name="isymunmanagedwriter2defineconstant2-method"></a><span data-ttu-id="ba982-103">ISymUnmanagedWriter2::DefineConstant2 方法</span><span class="sxs-lookup"><span data-stu-id="ba982-103">ISymUnmanagedWriter2::DefineConstant2 Method</span></span>

<span data-ttu-id="ba982-104">定义常数值的名称。</span><span class="sxs-lookup"><span data-stu-id="ba982-104">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba982-105">语法</span><span class="sxs-lookup"><span data-stu-id="ba982-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineConstant2(  
    [in] const WCHAR  *name,  
    [in] VARIANT      value,  
    [in] mdSignature  sigToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ba982-106">参数</span><span class="sxs-lookup"><span data-stu-id="ba982-106">Parameters</span></span>  

 `name`  
 <span data-ttu-id="ba982-107">中常量名称。</span><span class="sxs-lookup"><span data-stu-id="ba982-107">[in] The constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="ba982-108">中常量的值。</span><span class="sxs-lookup"><span data-stu-id="ba982-108">[in] The value of the constant.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="ba982-109">中常数的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ba982-109">[in] The metadata token of the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ba982-110">返回值</span><span class="sxs-lookup"><span data-stu-id="ba982-110">Return Value</span></span>  

 <span data-ttu-id="ba982-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ba982-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba982-112">要求</span><span class="sxs-lookup"><span data-stu-id="ba982-112">Requirements</span></span>  

 <span data-ttu-id="ba982-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ba982-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba982-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="ba982-114">See also</span></span>

- [<span data-ttu-id="ba982-115">ISymUnmanagedWriter2 接口</span><span class="sxs-lookup"><span data-stu-id="ba982-115">ISymUnmanagedWriter2 Interface</span></span>](isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="ba982-116">DefineConstant 方法</span><span class="sxs-lookup"><span data-stu-id="ba982-116">DefineConstant Method</span></span>](isymunmanagedwriter-defineconstant-method.md)
