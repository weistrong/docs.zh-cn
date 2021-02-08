---
description: 了解详细信息： ICorDebugVariableSymbol：： GetSlotIndex 方法
title: ICorDebugVariableSymbol::GetSlotIndex 方法
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
ms.openlocfilehash: 3b5cba06a5e80ffa323d2e6521e9ec4666f6f5f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790550"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a><span data-ttu-id="e4604-103">ICorDebugVariableSymbol::GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="e4604-103">ICorDebugVariableSymbol::GetSlotIndex Method</span></span>

<span data-ttu-id="e4604-104">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="e4604-104">Gets the managed slot index of a local variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4604-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4604-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4604-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4604-106">Parameters</span></span>  

 `pSlotIndex`  
 <span data-ttu-id="e4604-107">[out] 指向本地变量的槽索引的指针。</span><span class="sxs-lookup"><span data-stu-id="e4604-107">[out] A pointer to the local variable's slot index.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4604-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e4604-108">Return Value</span></span>  

 <span data-ttu-id="e4604-109">`S_OK` 如果成功。</span><span class="sxs-lookup"><span data-stu-id="e4604-109">`S_OK` if successful.</span></span> <span data-ttu-id="e4604-110">如果变量是一个函数自变量，则为 `E_FAIL`。</span><span class="sxs-lookup"><span data-stu-id="e4604-110">`E_FAIL` if the variable is a function argument.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e4604-111">备注</span><span class="sxs-lookup"><span data-stu-id="e4604-111">Remarks</span></span>  

 <span data-ttu-id="e4604-112">本地变量的托管槽索引可用于检索变量的元数据信息</span><span class="sxs-lookup"><span data-stu-id="e4604-112">The managed slot index of a local variable can be used to retrieve the variable's metadata information</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e4604-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="e4604-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4604-114">要求</span><span class="sxs-lookup"><span data-stu-id="e4604-114">Requirements</span></span>  

 <span data-ttu-id="e4604-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e4604-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4604-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4604-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4604-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4604-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4604-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4604-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4604-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4604-119">See also</span></span>

- [<span data-ttu-id="e4604-120">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="e4604-120">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="e4604-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="e4604-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
