---
description: 了解详细信息： ICorDebugILFrame：： EnumerateLocalVariables 方法
title: ICorDebugILFrame::EnumerateLocalVariables 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.EnumerateLocalVariables
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::EnumerateLocalVariables
helpviewer_keywords:
- EnumerateLocalVariables method [.NET Framework debugging]
- ICorDebugILFrame::EnumerateLocalVariables method [.NET Framework debugging]
ms.assetid: 1a67fa1b-2419-4cd0-aad4-6f46a0719b4b
topic_type:
- apiref
ms.openlocfilehash: 275cf7fcad32c452e6e7ebdd0774d64708a2398c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791382"
---
# <a name="icordebugilframeenumeratelocalvariables-method"></a><span data-ttu-id="c9deb-103">ICorDebugILFrame::EnumerateLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="c9deb-103">ICorDebugILFrame::EnumerateLocalVariables Method</span></span>

<span data-ttu-id="c9deb-104">获取此帧中局部变量的枚举数。</span><span class="sxs-lookup"><span data-stu-id="c9deb-104">Gets an enumerator for the local variables in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9deb-105">语法</span><span class="sxs-lookup"><span data-stu-id="c9deb-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateLocalVariables(
    [out] ICorDebugValueEnum    **ppValueEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9deb-106">参数</span><span class="sxs-lookup"><span data-stu-id="c9deb-106">Parameters</span></span>  

 `ppValueEnum`  
 <span data-ttu-id="c9deb-107">[out] 一个指向 ICorDebugValueEnum 对象的地址的指针，该对象是此帧中局部变量的枚举器。</span><span class="sxs-lookup"><span data-stu-id="c9deb-107">[out] A pointer to the address of an ICorDebugValueEnum object that is the enumerator for the local variables in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9deb-108">备注</span><span class="sxs-lookup"><span data-stu-id="c9deb-108">Remarks</span></span>  

 <span data-ttu-id="c9deb-109">`EnumerateLocalVariables` 获取一个枚举器，该枚举数可以列出此 ICorDebugILFrame 对象所表示的调用帧中可用的局部变量。</span><span class="sxs-lookup"><span data-stu-id="c9deb-109">`EnumerateLocalVariables` gets an enumerator that can list the local variables available in the call frame that is represented by this ICorDebugILFrame object.</span></span> <span data-ttu-id="c9deb-110">此列表可能不包括正在运行的函数中的所有局部变量，因为其中一些局部变量可能不处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="c9deb-110">The list may not include all of the local variables in the running function, because some of them may not be active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9deb-111">要求</span><span class="sxs-lookup"><span data-stu-id="c9deb-111">Requirements</span></span>  

 <span data-ttu-id="c9deb-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9deb-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9deb-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c9deb-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c9deb-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9deb-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9deb-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9deb-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
