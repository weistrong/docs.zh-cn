---
description: 了解详细信息： ICorDebugSymbolProvider：： GetTypeProps 方法
title: ICorDebugSymbolProvider::GetTypeProps 方法
ms.date: 03/30/2017
ms.assetid: 35ac4140-91ea-4c77-b1c4-1daf41986ca5
ms.openlocfilehash: b6a4a5a68e1e377fa839940832dfc49574009641
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659655"
---
# <a name="icordebugsymbolprovidergettypeprops-method"></a><span data-ttu-id="dd489-103">ICorDebugSymbolProvider::GetTypeProps 方法</span><span class="sxs-lookup"><span data-stu-id="dd489-103">ICorDebugSymbolProvider::GetTypeProps Method</span></span>

<span data-ttu-id="dd489-104">给定 vtable 中的相对虚拟地址 (RVA)，返回类型的属性信息（例如其泛型参数的签名数量）。</span><span class="sxs-lookup"><span data-stu-id="dd489-104">Returns information about a type's properties, such as the number of signature of its generic parameters, given a relative virtual address (RVA) in a vtable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd489-105">语法</span><span class="sxs-lookup"><span data-stu-id="dd489-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeProps(  
   [in]  ULONG32 vtableRva,  
   [in]  ULONG32 cbSignature,  
   [out] ULONG32 *pcbSignature,  
   [out, size_is(cbSignature), length_is(*pcbSignature)] BYTE signature[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dd489-106">参数</span><span class="sxs-lookup"><span data-stu-id="dd489-106">Parameters</span></span>  

 `tableRva`  
 <span data-ttu-id="dd489-107">[in] vtable 中的相对虚拟地址 (RVA)。</span><span class="sxs-lookup"><span data-stu-id="dd489-107">[in] A relative virtual address (RVA) in a vtable.</span></span>  
  
 `cbSignature`  
 <span data-ttu-id="dd489-108">[in] `signature` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="dd489-108">[in] The size of the `signature` array.</span></span> <span data-ttu-id="dd489-109">请参阅“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="dd489-109">See the Remarks section.</span></span>  
  
 `pcbSignature`  
 <span data-ttu-id="dd489-110">[out] [out] 指向返回的 `signature` 数组的大小的指针。</span><span class="sxs-lookup"><span data-stu-id="dd489-110">[out] [out] A pointer to the size of the returned `signature` array.</span></span>  
  
 `signature`  
 <span data-ttu-id="dd489-111">[out] 保存所有泛型参数的 typespec 签名的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="dd489-111">[out] A buffer that holds the typespec signatures of all generic parameters.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd489-112">备注</span><span class="sxs-lookup"><span data-stu-id="dd489-112">Remarks</span></span>  

 <span data-ttu-id="dd489-113">若要获取类型的数组的所需大小 `signature` ，请将 `cbSignature` 参数设置为0，将设置 `signature` 为 **null**。</span><span class="sxs-lookup"><span data-stu-id="dd489-113">To get the required size of the type's `signature` array, set the `cbSignature` argument to 0 and `signature` to **null**.</span></span> <span data-ttu-id="dd489-114">当该方法返回时，`pcbSignature` 将包含 `signature` 数组所需的字节数。</span><span class="sxs-lookup"><span data-stu-id="dd489-114">When the method returns, `pcbSignature` will contain the number of bytes required for the `signature` array.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="dd489-115">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="dd489-115">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd489-116">要求</span><span class="sxs-lookup"><span data-stu-id="dd489-116">Requirements</span></span>  

 <span data-ttu-id="dd489-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dd489-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd489-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dd489-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dd489-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd489-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dd489-120">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd489-120">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd489-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd489-121">See also</span></span>

- [<span data-ttu-id="dd489-122">GetMethodProps 方法</span><span class="sxs-lookup"><span data-stu-id="dd489-122">GetMethodProps Method</span></span>](icordebugsymbolprovider-getmethodprops-method.md)
- [<span data-ttu-id="dd489-123">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="dd489-123">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="dd489-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="dd489-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
