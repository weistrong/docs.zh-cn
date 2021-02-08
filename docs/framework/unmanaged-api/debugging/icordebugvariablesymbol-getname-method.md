---
description: 了解详细信息： ICorDebugVariableSymbol：： GetName 方法
title: ICorDebugVariableSymbol::GetName 方法
ms.date: 03/30/2017
ms.assetid: c922b7d4-44e5-45e4-aef3-cc9c35a0be80
ms.openlocfilehash: 4a3ba1dfebd256dcbb8374634a52f1feca5d9611
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790589"
---
# <a name="icordebugvariablesymbolgetname-method"></a><span data-ttu-id="8cdba-103">ICorDebugVariableSymbol::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="8cdba-103">ICorDebugVariableSymbol::GetName Method</span></span>

<span data-ttu-id="8cdba-104">获取变量名。</span><span class="sxs-lookup"><span data-stu-id="8cdba-104">Gets the name of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cdba-105">语法</span><span class="sxs-lookup"><span data-stu-id="8cdba-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
   [in] ULONG32 cchName,
   [out] ULONG32 *pcchName,
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8cdba-106">参数</span><span class="sxs-lookup"><span data-stu-id="8cdba-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="8cdba-107">[in] `szName` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="8cdba-107">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="8cdba-108">[out] 指向实际写入 `szName` 缓冲区的字符数。缓冲区的字符数的指针。</span><span class="sxs-lookup"><span data-stu-id="8cdba-108">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="8cdba-109">指向包含变量名的字符数组的指针。</span><span class="sxs-lookup"><span data-stu-id="8cdba-109">A pointer to a character array that contains the variable name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8cdba-110">备注</span><span class="sxs-lookup"><span data-stu-id="8cdba-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8cdba-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="8cdba-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8cdba-112">要求</span><span class="sxs-lookup"><span data-stu-id="8cdba-112">Requirements</span></span>  

 <span data-ttu-id="8cdba-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8cdba-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8cdba-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8cdba-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8cdba-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8cdba-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8cdba-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8cdba-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cdba-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cdba-117">See also</span></span>

- [<span data-ttu-id="8cdba-118">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="8cdba-118">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="8cdba-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="8cdba-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
