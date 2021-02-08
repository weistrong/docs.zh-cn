---
description: 了解详细信息： ICorDebugStaticFieldSymbol：： GetName 方法
title: ICorDebugStaticFieldSymbol::GetName 方法
ms.date: 03/30/2017
ms.assetid: e2be4af2-15d1-4e6a-8b68-1d78c93294a4
ms.openlocfilehash: c74de604f5880a69b77c89e56a82ae08517dd69c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794697"
---
# <a name="icordebugstaticfieldsymbolgetname-method"></a><span data-ttu-id="54dc2-103">ICorDebugStaticFieldSymbol::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="54dc2-103">ICorDebugStaticFieldSymbol::GetName Method</span></span>

<span data-ttu-id="54dc2-104">获取静态字段的名称。</span><span class="sxs-lookup"><span data-stu-id="54dc2-104">Gets the name of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54dc2-105">语法</span><span class="sxs-lookup"><span data-stu-id="54dc2-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
   [in] ULONG32 cchName,
   [out] ULONG32 *pcchName,
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54dc2-106">参数</span><span class="sxs-lookup"><span data-stu-id="54dc2-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="54dc2-107">[in] `szName` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="54dc2-107">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="54dc2-108">[out] 指向实际写入 `szName` 缓冲区的字符数。缓冲区的字符数的指针。</span><span class="sxs-lookup"><span data-stu-id="54dc2-108">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="54dc2-109">[out] 用于存储返回名称的字符数组。</span><span class="sxs-lookup"><span data-stu-id="54dc2-109">[out] A character array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54dc2-110">备注</span><span class="sxs-lookup"><span data-stu-id="54dc2-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="54dc2-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="54dc2-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54dc2-112">要求</span><span class="sxs-lookup"><span data-stu-id="54dc2-112">Requirements</span></span>  

 <span data-ttu-id="54dc2-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="54dc2-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54dc2-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="54dc2-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="54dc2-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="54dc2-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="54dc2-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54dc2-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54dc2-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="54dc2-117">See also</span></span>

- [<span data-ttu-id="54dc2-118">ICorDebugStaticFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="54dc2-118">ICorDebugStaticFieldSymbol Interface</span></span>](icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="54dc2-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="54dc2-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
