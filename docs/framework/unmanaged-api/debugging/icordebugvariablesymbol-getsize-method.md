---
description: 了解详细信息： ICorDebugVariableSymbol：： GetSize 方法
title: ICorDebugVariableSymbol::GetSize 方法
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
ms.openlocfilehash: f4098bf5e053ab66dd7966d4b665cfad4dee01d5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790576"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="db51b-103">ICorDebugVariableSymbol::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="db51b-103">ICorDebugVariableSymbol::GetSize Method</span></span>

<span data-ttu-id="db51b-104">获取变量的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="db51b-104">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db51b-105">语法</span><span class="sxs-lookup"><span data-stu-id="db51b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db51b-106">参数</span><span class="sxs-lookup"><span data-stu-id="db51b-106">Parameters</span></span>  

 `pcbValue`  
 <span data-ttu-id="db51b-107">指向包含变量大小的 32 位无符号整数的指针。</span><span class="sxs-lookup"><span data-stu-id="db51b-107">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db51b-108">备注</span><span class="sxs-lookup"><span data-stu-id="db51b-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="db51b-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="db51b-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db51b-110">要求</span><span class="sxs-lookup"><span data-stu-id="db51b-110">Requirements</span></span>  

 <span data-ttu-id="db51b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db51b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db51b-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db51b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db51b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db51b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db51b-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db51b-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db51b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="db51b-115">See also</span></span>

- [<span data-ttu-id="db51b-116">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="db51b-116">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="db51b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="db51b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
