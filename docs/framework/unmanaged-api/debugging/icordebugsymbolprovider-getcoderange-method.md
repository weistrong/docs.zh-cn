---
description: 了解详细信息： ICorDebugSymbolProvider：： GetCodeRange 方法
title: ICorDebugSymbolProvider::GetCodeRange 方法
ms.date: 03/30/2017
ms.assetid: 49a2451f-d250-4e73-aa96-9ff49d9f11c6
ms.openlocfilehash: 98b228be7483e6365815f6b783167b20fb3bcc48
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659902"
---
# <a name="icordebugsymbolprovidergetcoderange-method"></a><span data-ttu-id="ed437-103">ICorDebugSymbolProvider::GetCodeRange 方法</span><span class="sxs-lookup"><span data-stu-id="ed437-103">ICorDebugSymbolProvider::GetCodeRange Method</span></span>

<span data-ttu-id="ed437-104">给定方法的相对虚拟地址 (RVA)，获取该方法的起始地址和大小。</span><span class="sxs-lookup"><span data-stu-id="ed437-104">Gets the method start address and size given a relative virtual address (RVA) in a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed437-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed437-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCodeRange(  
   [in] ULONG32 codeRva,
   [out] ULONG32* pCodeStartAddress,
   [out] ULONG32* pCodeSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ed437-106">参数</span><span class="sxs-lookup"><span data-stu-id="ed437-106">Parameters</span></span>  

 `codeRva`  
 <span data-ttu-id="ed437-107">[in] 方法中的相对虚拟地址 (RVA)。</span><span class="sxs-lookup"><span data-stu-id="ed437-107">[in] The relative virtual address (RVA) in a method.</span></span>  
  
 `pCodeStartAddress`  
 <span data-ttu-id="ed437-108">[out] 指向该方法的起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="ed437-108">[out] A pointer to the starting address of the method.</span></span>  
  
 `pCodeSize`  
 <span data-ttu-id="ed437-109">指向方法代码大小（该方法的代码的字节数）的指针。</span><span class="sxs-lookup"><span data-stu-id="ed437-109">A pointer to the method code size (the number of bytes of the method's code).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ed437-110">备注</span><span class="sxs-lookup"><span data-stu-id="ed437-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed437-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="ed437-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed437-112">要求</span><span class="sxs-lookup"><span data-stu-id="ed437-112">Requirements</span></span>  

 <span data-ttu-id="ed437-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed437-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed437-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ed437-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ed437-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed437-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed437-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed437-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed437-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed437-117">See also</span></span>

- [<span data-ttu-id="ed437-118">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="ed437-118">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="ed437-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="ed437-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
