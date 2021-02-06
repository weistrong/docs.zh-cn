---
description: 了解详细信息： ICorDebugSymbolProvider：： GetObjectSize 方法
title: ICorDebugSymbolProvider::GetObjectSize 方法
ms.date: 03/30/2017
ms.assetid: 3c564396-ac64-4ef3-b4f6-df96f1d46fc7
ms.openlocfilehash: 72720a1af9958fd0ab91276b3967733cec77fee7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659696"
---
# <a name="icordebugsymbolprovidergetobjectsize-method"></a><span data-ttu-id="e50c2-103">ICorDebugSymbolProvider::GetObjectSize 方法</span><span class="sxs-lookup"><span data-stu-id="e50c2-103">ICorDebugSymbolProvider::GetObjectSize Method</span></span>

<span data-ttu-id="e50c2-104">基于对象的 TypeSpec 签名返回对象的大小。</span><span class="sxs-lookup"><span data-stu-id="e50c2-104">Returns the object size for an object based on its typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e50c2-105">语法</span><span class="sxs-lookup"><span data-stu-id="e50c2-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObjectSize(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [out] ULONG32 *pObjectSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e50c2-106">参数</span><span class="sxs-lookup"><span data-stu-id="e50c2-106">Parameters</span></span>  

 `cbSignature`  
 <span data-ttu-id="e50c2-107">[in] TypeSpec 签名中的字节数。</span><span class="sxs-lookup"><span data-stu-id="e50c2-107">[in] The number of bytes in the typespec signature.</span></span>  
  
 <span data-ttu-id="e50c2-108">typeSig</span><span class="sxs-lookup"><span data-stu-id="e50c2-108">typeSig</span></span>  
 <span data-ttu-id="e50c2-109">[in] TypeSpec 签名。</span><span class="sxs-lookup"><span data-stu-id="e50c2-109">[in] The typespec signature.</span></span>  
  
 `pObjectSize`  
 <span data-ttu-id="e50c2-110">[out] 指向对象大小的指针。</span><span class="sxs-lookup"><span data-stu-id="e50c2-110">[out] A pointer to the size of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e50c2-111">备注</span><span class="sxs-lookup"><span data-stu-id="e50c2-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e50c2-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="e50c2-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e50c2-113">要求</span><span class="sxs-lookup"><span data-stu-id="e50c2-113">Requirements</span></span>  

 <span data-ttu-id="e50c2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e50c2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e50c2-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e50c2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e50c2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e50c2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e50c2-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e50c2-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e50c2-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e50c2-118">See also</span></span>

- [<span data-ttu-id="e50c2-119">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="e50c2-119">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="e50c2-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="e50c2-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
