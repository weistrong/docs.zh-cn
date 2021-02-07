---
description: 了解详细信息： ICorDebugEval2：： NewStringWithLength 方法
title: ICorDebugEval2::NewStringWithLength 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewStringWithLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewStringWithLength
helpviewer_keywords:
- NewStringWithLength method [.NET Framework debugging]
- ICorDebugEval2::NewStringWithLength method [.NET Framework debugging]
ms.assetid: d5f54a34-6335-4708-b407-a756ec70fab4
topic_type:
- apiref
ms.openlocfilehash: 23864dabefcb4fc12f73c66bc2d19a6cca1aacf0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693520"
---
# <a name="icordebugeval2newstringwithlength-method"></a><span data-ttu-id="dcfc4-103">ICorDebugEval2::NewStringWithLength 方法</span><span class="sxs-lookup"><span data-stu-id="dcfc4-103">ICorDebugEval2::NewStringWithLength Method</span></span>

<span data-ttu-id="dcfc4-104">使用指定的内容创建指定长度的字符串。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-104">Creates a string of the specified length, with the specified contents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcfc4-105">语法</span><span class="sxs-lookup"><span data-stu-id="dcfc4-105">Syntax</span></span>  
  
```cpp  
HRESULT NewStringWithLength (  
    [in] LPCWSTR               string,  
    [in] UINT                  uiLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dcfc4-106">参数</span><span class="sxs-lookup"><span data-stu-id="dcfc4-106">Parameters</span></span>  

 `string`  
 <span data-ttu-id="dcfc4-107">中指向字符串值的指针。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-107">[in] A pointer to the string value.</span></span>  
  
 `uiLength`  
 <span data-ttu-id="dcfc4-108">中字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-108">[in] Length of the string.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dcfc4-109">备注</span><span class="sxs-lookup"><span data-stu-id="dcfc4-109">Remarks</span></span>  

 <span data-ttu-id="dcfc4-110">如果字符串的尾随空字符应在托管字符串中，则该方法的调用方 `NewStringWithLength` 必须确保字符串长度包含结尾的 null 字符。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-110">If the string's trailing null character is expected to be in the managed string, the caller of the `NewStringWithLength` method must ensure that the string length includes the trailing null character.</span></span>  
  
 <span data-ttu-id="dcfc4-111">始终在当前执行线程的应用程序域中创建字符串。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-111">The string is always created in the application domain in which the thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dcfc4-112">要求</span><span class="sxs-lookup"><span data-stu-id="dcfc4-112">Requirements</span></span>  

 <span data-ttu-id="dcfc4-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dcfc4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dcfc4-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dcfc4-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dcfc4-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dcfc4-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dcfc4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dcfc4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
