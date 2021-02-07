---
description: 了解详细信息： ICorDebugDataTarget2：： GetImageFromPointer 方法
title: ICorDebugDataTarget2::GetImageFromPointer 方法
ms.date: 03/30/2017
ms.assetid: 939cabe1-b647-4090-b662-eeec23c6c58d
ms.openlocfilehash: bcf73fa522072707a7b08d90965fcd38188c2bb5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764393"
---
# <a name="icordebugdatatarget2getimagefrompointer-method"></a><span data-ttu-id="b7efc-103">ICorDebugDataTarget2::GetImageFromPointer 方法</span><span class="sxs-lookup"><span data-stu-id="b7efc-103">ICorDebugDataTarget2::GetImageFromPointer Method</span></span>

<span data-ttu-id="b7efc-104">返回该模块地址中的模块基址和大小。</span><span class="sxs-lookup"><span data-stu-id="b7efc-104">Returns the module base address and size from an address in that module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7efc-105">语法</span><span class="sxs-lookup"><span data-stu-id="b7efc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetImageFromPointer(  
   [in] CORDB_ADDRESS addr,
   [out] CORDB_ADDRESS *pImageBase,
   [out] ULONG32 *pSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7efc-106">参数</span><span class="sxs-lookup"><span data-stu-id="b7efc-106">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="b7efc-107">一个 [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) 值，该值表示模块中的地址。</span><span class="sxs-lookup"><span data-stu-id="b7efc-107">A [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) value that represents an address in a module.</span></span>  
  
 `pImageBase`  
 <span data-ttu-id="b7efc-108">弄一个 [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) 值，该值表示模块的基址。</span><span class="sxs-lookup"><span data-stu-id="b7efc-108">[out] A [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `pSize`  
 <span data-ttu-id="b7efc-109">指针指向模块大小。</span><span class="sxs-lookup"><span data-stu-id="b7efc-109">A pointer to the module size.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7efc-110">备注</span><span class="sxs-lookup"><span data-stu-id="b7efc-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b7efc-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b7efc-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7efc-112">要求</span><span class="sxs-lookup"><span data-stu-id="b7efc-112">Requirements</span></span>  

 <span data-ttu-id="b7efc-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7efc-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7efc-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7efc-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7efc-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7efc-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7efc-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7efc-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7efc-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7efc-117">See also</span></span>

- [<span data-ttu-id="b7efc-118">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="b7efc-118">ICorDebugDataTarget2 Interface</span></span>](icordebugdatatarget2-interface.md)
- [<span data-ttu-id="b7efc-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="b7efc-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
