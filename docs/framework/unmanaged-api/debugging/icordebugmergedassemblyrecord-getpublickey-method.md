---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetPublicKey 方法
title: ICorDebugMergedAssemblyRecord::GetPublicKey 方法
ms.date: 03/30/2017
ms.assetid: 6f4e78ba-082b-489d-8b58-4c35fbcc7a5b
ms.openlocfilehash: 15175b0d02773bcbce46bfaec9ce1de3021b7dde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801093"
---
# <a name="icordebugmergedassemblyrecordgetpublickey-method"></a><span data-ttu-id="b5809-103">ICorDebugMergedAssemblyRecord::GetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="b5809-103">ICorDebugMergedAssemblyRecord::GetPublicKey Method</span></span>

<span data-ttu-id="b5809-104">获取程序集的公钥。</span><span class="sxs-lookup"><span data-stu-id="b5809-104">Gets the assembly's public key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5809-105">语法</span><span class="sxs-lookup"><span data-stu-id="b5809-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPublicKey(  
   [in] ULONG32 cbPublicKey,
   [out] ULONG32 *pcbPublicKey,
   [out, size_is(cbPublicKey), length_is(*pcbPublicKey)] BYTE pbPublicKey[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b5809-106">参数</span><span class="sxs-lookup"><span data-stu-id="b5809-106">Parameters</span></span>  

 `cbPublicKey`  
 <span data-ttu-id="b5809-107">[in] `pbPublicKey` 数组中的最大字节数。</span><span class="sxs-lookup"><span data-stu-id="b5809-107">[in] The maximum number of bytes in the `pbPublicKey` array.</span></span>  
  
 `pcbPublicKey`  
 <span data-ttu-id="b5809-108">[out] 指向写入 `pbPublicKey` 数组的实际字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="b5809-108">[out] A pointer to the actual number of bytes written to the `pbPublicKey` array.</span></span>  
  
 `pbPublicKey`  
 <span data-ttu-id="b5809-109">[out] 指向包含程序集公钥的字节数组的指针。</span><span class="sxs-lookup"><span data-stu-id="b5809-109">[out] A pointer to a byte array that contains the assembly's public key.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b5809-110">备注</span><span class="sxs-lookup"><span data-stu-id="b5809-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b5809-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b5809-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5809-112">要求</span><span class="sxs-lookup"><span data-stu-id="b5809-112">Requirements</span></span>  

 <span data-ttu-id="b5809-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b5809-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5809-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b5809-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5809-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5809-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5809-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5809-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5809-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5809-117">See also</span></span>

- [<span data-ttu-id="b5809-118">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="b5809-118">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="b5809-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="b5809-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
