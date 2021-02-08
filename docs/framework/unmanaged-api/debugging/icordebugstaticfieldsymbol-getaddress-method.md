---
description: 了解详细信息： ICorDebugStaticFieldSymbol：： GetAddress 方法
title: ICorDebugStaticFieldSymbol::GetAddress 方法
ms.date: 03/30/2017
ms.assetid: 5a6c9a5a-ec72-4c40-a9c3-cee7baa63687
ms.openlocfilehash: 1944839ff6afc31dc3667111397cbb088b95b412
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801002"
---
# <a name="icordebugstaticfieldsymbolgetaddress-method"></a><span data-ttu-id="abfcf-103">ICorDebugStaticFieldSymbol::GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="abfcf-103">ICorDebugStaticFieldSymbol::GetAddress Method</span></span>

<span data-ttu-id="abfcf-104">获取静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="abfcf-104">Gets the address of a static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abfcf-105">语法</span><span class="sxs-lookup"><span data-stu-id="abfcf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAddress(  
   [out] CORDB_ADDRESS *pRVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="abfcf-106">参数</span><span class="sxs-lookup"><span data-stu-id="abfcf-106">Parameters</span></span>  

 <span data-ttu-id="abfcf-107">pRVA</span><span class="sxs-lookup"><span data-stu-id="abfcf-107">pRVA</span></span>  
 <span data-ttu-id="abfcf-108">[out] 指向静态字段的相对虚拟地址 (RVA) 的指针。</span><span class="sxs-lookup"><span data-stu-id="abfcf-108">[out] A pointer to the relative virtual address (RVA) of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="abfcf-109">备注</span><span class="sxs-lookup"><span data-stu-id="abfcf-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="abfcf-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="abfcf-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abfcf-111">要求</span><span class="sxs-lookup"><span data-stu-id="abfcf-111">Requirements</span></span>  

 <span data-ttu-id="abfcf-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="abfcf-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abfcf-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="abfcf-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="abfcf-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="abfcf-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="abfcf-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abfcf-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abfcf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="abfcf-116">See also</span></span>

- [<span data-ttu-id="abfcf-117">ICorDebugStaticFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="abfcf-117">ICorDebugStaticFieldSymbol Interface</span></span>](icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="abfcf-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="abfcf-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
