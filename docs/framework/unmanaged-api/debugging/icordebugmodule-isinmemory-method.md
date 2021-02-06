---
description: 了解详细信息： ICorDebugModule：： IsInMemory 方法
title: ICorDebugModule::IsInMemory 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsInMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsInMemory
helpviewer_keywords:
- IsInMemory method [.NET Framework debugging]
- ICorDebugModule::IsInMemory method [.NET Framework debugging]
ms.assetid: 89940711-98e7-4aa6-bffc-5e39e91e1b7d
topic_type:
- apiref
ms.openlocfilehash: 41454ede15e1d45775af8fb0ab7a6b571d9c0e41
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660084"
---
# <a name="icordebugmoduleisinmemory-method"></a><span data-ttu-id="460e4-103">ICorDebugModule::IsInMemory 方法</span><span class="sxs-lookup"><span data-stu-id="460e4-103">ICorDebugModule::IsInMemory Method</span></span>

<span data-ttu-id="460e4-104">获取一个值，该值指示此模块是否仅存在于内存中。</span><span class="sxs-lookup"><span data-stu-id="460e4-104">Gets a value that indicates whether this module exists only in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="460e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="460e4-105">Syntax</span></span>  
  
```cpp  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="460e4-106">参数</span><span class="sxs-lookup"><span data-stu-id="460e4-106">Parameters</span></span>  

 `pInMemory`  
 <span data-ttu-id="460e4-107">[out] `true` 如果此模块仅存在于内存中，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="460e4-107">[out] `true` if this module exists only in memory; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="460e4-108">备注</span><span class="sxs-lookup"><span data-stu-id="460e4-108">Remarks</span></span>  

 <span data-ttu-id="460e4-109">公共语言运行时 (CLR) 支持从原始字节流加载模块。</span><span class="sxs-lookup"><span data-stu-id="460e4-109">The common language runtime (CLR) supports the loading of modules from raw streams of bytes.</span></span> <span data-ttu-id="460e4-110">此类模块称为 *内存中模块* ，不存在于磁盘上。</span><span class="sxs-lookup"><span data-stu-id="460e4-110">Such modules are called *in-memory modules* and do not exist on disk.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="460e4-111">要求</span><span class="sxs-lookup"><span data-stu-id="460e4-111">Requirements</span></span>  

 <span data-ttu-id="460e4-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="460e4-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="460e4-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="460e4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="460e4-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="460e4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="460e4-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="460e4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="460e4-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="460e4-116">See also</span></span>
