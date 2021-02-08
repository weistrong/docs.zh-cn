---
description: 了解详细信息： ICorDebugInstanceFieldSymbol：： GetOffset 方法
title: ICorDebugInstanceFieldSymbol::GetName 方法
ms.date: 03/30/2017
ms.assetid: 7e470150-2b92-4425-989c-315f48964fd2
ms.openlocfilehash: 4a877b2f78adfac5c54694ab306fd7db60f266f0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791161"
---
# <a name="icordebuginstancefieldsymbolgetoffset-method"></a><span data-ttu-id="b195d-103">ICorDebugInstanceFieldSymbol::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="b195d-103">ICorDebugInstanceFieldSymbol::GetOffset Method</span></span>

<span data-ttu-id="b195d-104">获取父类中此示例字段的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b195d-104">Gets the offset in bytes of this instance field in its parent class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b195d-105">语法</span><span class="sxs-lookup"><span data-stu-id="b195d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetOffset(  
   [out] ULONG32 *pcbOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b195d-106">参数</span><span class="sxs-lookup"><span data-stu-id="b195d-106">Parameters</span></span>  

 `pcbOffset`  
 <span data-ttu-id="b195d-107">指向此示例字段在父类中偏移的字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="b195d-107">A pointer to the number of bytes that this instance field is offset in its parent class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b195d-108">备注</span><span class="sxs-lookup"><span data-stu-id="b195d-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b195d-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b195d-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b195d-110">要求</span><span class="sxs-lookup"><span data-stu-id="b195d-110">Requirements</span></span>  

 <span data-ttu-id="b195d-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b195d-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b195d-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b195d-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b195d-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b195d-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b195d-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b195d-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b195d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="b195d-115">See also</span></span>

- [<span data-ttu-id="b195d-116">ICorDebugInstanceFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="b195d-116">ICorDebugInstanceFieldSymbol Interface</span></span>](icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="b195d-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="b195d-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
