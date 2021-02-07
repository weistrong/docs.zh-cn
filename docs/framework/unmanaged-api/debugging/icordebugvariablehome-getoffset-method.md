---
description: 了解详细信息： ICorDebugVariableHome：： GetOffset 方法
title: ICorDebugVariableHome：： GetOffset 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetOffset
helpviewer_keywords:
- ICorDebugVariableHome::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: f025c2e5-3f6c-4be8-9ffe-c8b214617dfe
topic_type:
- apiref
ms.openlocfilehash: 48b57856d2825dd2ea9328064a28783b4b36029b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728764"
---
# <a name="icordebugvariablehomegetoffset-method"></a><span data-ttu-id="72a40-103">ICorDebugVariableHome：： GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="72a40-103">ICorDebugVariableHome::GetOffset Method</span></span>

<span data-ttu-id="72a40-104">获取与基寄存器相对应的偏移量。</span><span class="sxs-lookup"><span data-stu-id="72a40-104">Gets the offset from the base register for a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72a40-105">语法</span><span class="sxs-lookup"><span data-stu-id="72a40-105">Syntax</span></span>  
  
```cpp  
HRESULT GetOffset(  
    [out] LONG *pOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72a40-106">参数</span><span class="sxs-lookup"><span data-stu-id="72a40-106">Parameters</span></span>  

 `pOffset`  
 <span data-ttu-id="72a40-107">弄基寄存器的偏移量。</span><span class="sxs-lookup"><span data-stu-id="72a40-107">[out] The offset from the base register.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="72a40-108">返回值</span><span class="sxs-lookup"><span data-stu-id="72a40-108">Return Value</span></span>  

 <span data-ttu-id="72a40-109">方法返回以下值：</span><span class="sxs-lookup"><span data-stu-id="72a40-109">The method returns the following values:</span></span>  
  
|<span data-ttu-id="72a40-110">值</span><span class="sxs-lookup"><span data-stu-id="72a40-110">Value</span></span>|<span data-ttu-id="72a40-111">说明</span><span class="sxs-lookup"><span data-stu-id="72a40-111">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="72a40-112">变量在寄存器相对内存位置。</span><span class="sxs-lookup"><span data-stu-id="72a40-112">The variable is in a register-relative memory location.</span></span>|  
|`E_FAIL`|<span data-ttu-id="72a40-113">变量不在寄存器相对内存位置中。</span><span class="sxs-lookup"><span data-stu-id="72a40-113">The variable is not in a register-relative memory location.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="72a40-114">要求</span><span class="sxs-lookup"><span data-stu-id="72a40-114">Requirements</span></span>  

 <span data-ttu-id="72a40-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="72a40-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72a40-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="72a40-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="72a40-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72a40-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72a40-118">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72a40-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72a40-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="72a40-119">See also</span></span>

- [<span data-ttu-id="72a40-120">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="72a40-120">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
