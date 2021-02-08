---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetPublicKeyToken 方法
title: ICorDebugMergedAssemblyRecord::GetPublicKeyToken 方法
ms.date: 03/30/2017
ms.assetid: 72020b72-9611-4bc3-b1e7-5a16b023bfa3
ms.openlocfilehash: 5ff870355ddf521012e93ed01a63e32358ca95cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801061"
---
# <a name="icordebugmergedassemblyrecordgetpublickeytoken-method"></a><span data-ttu-id="f0554-103">ICorDebugMergedAssemblyRecord::GetPublicKeyToken 方法</span><span class="sxs-lookup"><span data-stu-id="f0554-103">ICorDebugMergedAssemblyRecord::GetPublicKeyToken Method</span></span>

<span data-ttu-id="f0554-104">获取程序集的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="f0554-104">Gets the assembly's public key token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0554-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0554-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPublicKeyToken(  
   [in] ULONG32 cbPublicKeyToken,
   [out] ULONG32 *pcbPublicKeyToken,
   [out, size_is(cbPublicKeyToken), length_is(*pcbPublicKeyToken)] BYTE pbPublicKeyToken[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0554-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0554-106">Parameters</span></span>  

 `cbPublicKeyToken`  
 <span data-ttu-id="f0554-107">[in] `pbPublicKeyToken` 数组中的最大字节数。</span><span class="sxs-lookup"><span data-stu-id="f0554-107">[in] The maximum number of bytes in the `pbPublicKeyToken` array.</span></span>  
  
 `pcbPublicKeyToken`  
 <span data-ttu-id="f0554-108">[out] 指向写入 `pbPublicKeyToken` 数组的实际字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="f0554-108">[out] A pointer to the actual number of bytes written to the `pbPublicKeyToken` array.</span></span>  
  
 `pbPublicKeyToken`  
 <span data-ttu-id="f0554-109">[out] 指向包含程序集公钥标记的字节数组的指针。</span><span class="sxs-lookup"><span data-stu-id="f0554-109">[out] A pointer to a byte array that contains the assembly's public key token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0554-110">备注</span><span class="sxs-lookup"><span data-stu-id="f0554-110">Remarks</span></span>  

 <span data-ttu-id="f0554-111">程序集的公钥标记是指其公钥中 SHA1 哈希的最后 8 个字节。</span><span class="sxs-lookup"><span data-stu-id="f0554-111">An assembly's public key token is the last eight bytes of a SHA1 hash of its public key.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f0554-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="f0554-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0554-113">要求</span><span class="sxs-lookup"><span data-stu-id="f0554-113">Requirements</span></span>  

 <span data-ttu-id="f0554-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0554-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0554-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0554-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0554-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0554-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0554-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0554-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0554-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0554-118">See also</span></span>

- [<span data-ttu-id="f0554-119">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="f0554-119">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="f0554-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="f0554-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
