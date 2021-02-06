---
description: 了解详细信息： ICorDebugSymbolProvider：： GetInstanceFieldSymbols 方法
title: ICorDebugSymbolProvider::GetInstanceFieldSymbols 方法
ms.date: 03/30/2017
ms.assetid: a29b9233-ee67-4b53-b8bc-c00b281e7edb
ms.openlocfilehash: 379d943743bb1fe21edbcca2265b4d8613d4f4b8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659889"
---
# <a name="icordebugsymbolprovidergetinstancefieldsymbols-method"></a><span data-ttu-id="1cd0a-103">ICorDebugSymbolProvider::GetInstanceFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="1cd0a-103">ICorDebugSymbolProvider::GetInstanceFieldSymbols Method</span></span>

<span data-ttu-id="1cd0a-104">获取与 Typespec 签名相对应的实例字段符号。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-104">Gets the instance field symbols that correspond to a typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cd0a-105">语法</span><span class="sxs-lookup"><span data-stu-id="1cd0a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetInstanceFieldSymbols(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugInstanceFieldSymbol *pSymbols[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1cd0a-106">参数</span><span class="sxs-lookup"><span data-stu-id="1cd0a-106">Parameters</span></span>  

 `cbSignature`  
 <span data-ttu-id="1cd0a-107">[in] `typeSig` 数组中的字节数。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-107">[in] The number of bytes in the `typeSig` array.</span></span>  
  
 `typeSig`  
 <span data-ttu-id="1cd0a-108">[in] 包含 `typespec` 签名的字节数组。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-108">[in] A byte array that contains the `typespec` signature.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="1cd0a-109">[in] 请求的符号数。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-109">[in] The number of symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="1cd0a-110">[out] 一个指针，指向由方法检索的符号的数量。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-110">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pSymbols`  
 <span data-ttu-id="1cd0a-111">弄指向 [ICorDebugStaticFieldSymbol](icordebugstaticfieldsymbol-interface.md) 数组的指针，该数组包含请求的实例字段符号。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-111">[out] A pointer to an [ICorDebugStaticFieldSymbol](icordebugstaticfieldsymbol-interface.md) array that contains the requested instance field symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1cd0a-112">备注</span><span class="sxs-lookup"><span data-stu-id="1cd0a-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1cd0a-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cd0a-114">要求</span><span class="sxs-lookup"><span data-stu-id="1cd0a-114">Requirements</span></span>  

 <span data-ttu-id="1cd0a-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1cd0a-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1cd0a-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1cd0a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1cd0a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1cd0a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1cd0a-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1cd0a-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cd0a-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cd0a-119">See also</span></span>

- [<span data-ttu-id="1cd0a-120">GetStaticFieldSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="1cd0a-120">GetStaticFieldSymbols Method</span></span>](icordebugsymbolprovider-getstaticfieldsymbols-method.md)
- [<span data-ttu-id="1cd0a-121">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="1cd0a-121">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="1cd0a-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="1cd0a-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
