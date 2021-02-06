---
description: 了解详细信息： ICorDebugSymbolProvider：： GetStaticFieldSymbols 方法
title: ICorDebugSymbolProvider::GetStaticFieldSymbols 方法
ms.date: 03/30/2017
ms.assetid: b178367f-a6e4-413c-b06f-daf3804b456b
ms.openlocfilehash: e95f77be86ef88a73ca4c833b242617a0d405e21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659695"
---
# <a name="icordebugsymbolprovidergetstaticfieldsymbols-method"></a><span data-ttu-id="61519-103">ICorDebugSymbolProvider::GetStaticFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="61519-103">ICorDebugSymbolProvider::GetStaticFieldSymbols Method</span></span>

<span data-ttu-id="61519-104">获取与 Typespec 签名相对应的静态字段符号。</span><span class="sxs-lookup"><span data-stu-id="61519-104">Gets the static field symbols that correspond to a typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61519-105">语法</span><span class="sxs-lookup"><span data-stu-id="61519-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStaticFieldSymbols(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugStaticFieldSymbol *pSymbols[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61519-106">参数</span><span class="sxs-lookup"><span data-stu-id="61519-106">Parameters</span></span>  

 `cbSignature`  
 <span data-ttu-id="61519-107">[in] `typeSig` 数组中的字节数。</span><span class="sxs-lookup"><span data-stu-id="61519-107">[in] The number of bytes in the `typeSig` array.</span></span>  
  
 `typeSig`  
 <span data-ttu-id="61519-108">[in] 包含 `typespec` 签名的字节数组。</span><span class="sxs-lookup"><span data-stu-id="61519-108">[in] A byte array that contains the `typespec` signature.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="61519-109">[in] 请求的符号数。</span><span class="sxs-lookup"><span data-stu-id="61519-109">[in] The number of symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="61519-110">[out] 一个指针，指向由方法检索的符号的数量。</span><span class="sxs-lookup"><span data-stu-id="61519-110">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pSymbols`  
 <span data-ttu-id="61519-111">弄指向 [ICorDebugStaticFieldSymbol](icordebugstaticfieldsymbol-interface.md) 数组的指针，该数组包含请求的静态字段符号。</span><span class="sxs-lookup"><span data-stu-id="61519-111">[out] A pointer to an [ICorDebugStaticFieldSymbol](icordebugstaticfieldsymbol-interface.md) array that contains the requested static field symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="61519-112">备注</span><span class="sxs-lookup"><span data-stu-id="61519-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="61519-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="61519-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61519-114">要求</span><span class="sxs-lookup"><span data-stu-id="61519-114">Requirements</span></span>  

 <span data-ttu-id="61519-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61519-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61519-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="61519-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="61519-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="61519-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="61519-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61519-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61519-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="61519-119">See also</span></span>

- [<span data-ttu-id="61519-120">GetInstanceFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="61519-120">GetInstanceFieldSymbols Method</span></span>](icordebugsymbolprovider-getinstancefieldsymbols-method.md)
- [<span data-ttu-id="61519-121">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="61519-121">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="61519-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="61519-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
