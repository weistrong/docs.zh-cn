---
description: 了解详细信息： ICorDebugSymbolProvider：： GetMethodLocalSymbols 方法
title: ICorDebugSymbolProvider::GetMethodLocalSymbols 方法
ms.date: 03/30/2017
ms.assetid: 8b989e38-e779-49d1-9e90-f1f920484b08
ms.openlocfilehash: f4eaac208d98b25ae4a53acfd977d354c6f6ac1b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659811"
---
# <a name="icordebugsymbolprovidergetmethodlocalsymbols-method"></a><span data-ttu-id="f6f40-103">ICorDebugSymbolProvider::GetMethodLocalSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="f6f40-103">ICorDebugSymbolProvider::GetMethodLocalSymbols Method</span></span>

<span data-ttu-id="f6f40-104">给定方法的相对虚拟地址 (RVA)，获取该方法的本地符号。</span><span class="sxs-lookup"><span data-stu-id="f6f40-104">Gets a method's local symbols given the relative virtual address (RVA) of that method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6f40-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6f40-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodLocalSymbols(  
   [in] ULONG32 nativeRVA,  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugVariableSymbol *pSymbols[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6f40-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6f40-106">Parameters</span></span>  

 `nativeRVA`  
 <span data-ttu-id="f6f40-107">[in] 方法的本机相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="f6f40-107">[in] The native relative virtual address of the method.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="f6f40-108">[in] 请求的本地符号数。</span><span class="sxs-lookup"><span data-stu-id="f6f40-108">[in] The number of local symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="f6f40-109">[out] 一个指针，指向由方法检索的符号的数量。</span><span class="sxs-lookup"><span data-stu-id="f6f40-109">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="f6f40-110">弄指向包含方法的本地符号的 [ICorDebugVariableSymbol](icordebugvariablesymbol-interface.md) 数组的指针。</span><span class="sxs-lookup"><span data-stu-id="f6f40-110">[out] A pointer to an [ICorDebugVariableSymbol](icordebugvariablesymbol-interface.md) array that contains the method's local symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f6f40-111">备注</span><span class="sxs-lookup"><span data-stu-id="f6f40-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f6f40-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="f6f40-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6f40-113">要求</span><span class="sxs-lookup"><span data-stu-id="f6f40-113">Requirements</span></span>  

 <span data-ttu-id="f6f40-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6f40-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6f40-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f6f40-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f6f40-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6f40-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6f40-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6f40-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6f40-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6f40-118">See also</span></span>

- [<span data-ttu-id="f6f40-119">GetMethodParameterSymbols 方法</span><span class="sxs-lookup"><span data-stu-id="f6f40-119">GetMethodParameterSymbols Method</span></span>](icordebugsymbolprovider-getmethodparametersymbols-method.md)
- [<span data-ttu-id="f6f40-120">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="f6f40-120">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="f6f40-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="f6f40-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
