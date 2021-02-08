---
description: 了解详细信息： ICorDebugILFrame：： EnumerateArguments 方法
title: ICorDebugILFrame::EnumerateArguments 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.EnumerateArguments
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::EnumerateArguments
helpviewer_keywords:
- ICorDebugILFrame::EnumerateArguments method [.NET Framework debugging]
- EnumerateArguments method [.NET Framework debugging]
ms.assetid: 00ac81e2-a774-422a-bd88-54a4b3c99f73
topic_type:
- apiref
ms.openlocfilehash: 513f931e70a4e914b89f440545cf33ea1cce1fdf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791395"
---
# <a name="icordebugilframeenumeratearguments-method"></a><span data-ttu-id="58cd0-103">ICorDebugILFrame::EnumerateArguments 方法</span><span class="sxs-lookup"><span data-stu-id="58cd0-103">ICorDebugILFrame::EnumerateArguments Method</span></span>

<span data-ttu-id="58cd0-104">获取此帧中的参数的枚举数。</span><span class="sxs-lookup"><span data-stu-id="58cd0-104">Gets an enumerator for the arguments in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58cd0-105">语法</span><span class="sxs-lookup"><span data-stu-id="58cd0-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateArguments (  
    [out] ICorDebugValueEnum    **ppValueEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58cd0-106">参数</span><span class="sxs-lookup"><span data-stu-id="58cd0-106">Parameters</span></span>  

 `ppValueEnum`  
 <span data-ttu-id="58cd0-107">弄指向 ICorDebugValueEnum 对象地址的指针，该对象是此帧中自变量的枚举器。</span><span class="sxs-lookup"><span data-stu-id="58cd0-107">[out] A pointer to the address of an ICorDebugValueEnum object that is the enumerator for the arguments in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58cd0-108">备注</span><span class="sxs-lookup"><span data-stu-id="58cd0-108">Remarks</span></span>  

 <span data-ttu-id="58cd0-109">`EnumerateArguments` 获取一个枚举器，该枚举数可以列出此 ICorDebugILFrame 对象所表示的调用帧中可用的参数。</span><span class="sxs-lookup"><span data-stu-id="58cd0-109">`EnumerateArguments` gets an enumerator that can list the arguments available in the call frame that is represented by this ICorDebugILFrame object.</span></span> <span data-ttu-id="58cd0-110">此列表将包含 [vararg](/cpp/windows/vararg) 参数 (即，可变数量的参数) 以及不是的参数 `vararg` 。</span><span class="sxs-lookup"><span data-stu-id="58cd0-110">The list will include arguments that are [vararg](/cpp/windows/vararg) (that is, a variable number of arguments) as well as arguments that are not `vararg`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58cd0-111">要求</span><span class="sxs-lookup"><span data-stu-id="58cd0-111">Requirements</span></span>  

 <span data-ttu-id="58cd0-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58cd0-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58cd0-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58cd0-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58cd0-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58cd0-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58cd0-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58cd0-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
