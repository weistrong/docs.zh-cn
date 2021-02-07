---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetCulture 方法
title: ICorDebugMergedAssemblyRecord::GetCulture 方法
ms.date: 03/30/2017
ms.assetid: 030b2f8c-8c21-40b7-855d-3afa78975a17
ms.openlocfilehash: f530bb68a1e7e4c4bff53b8f3046f6ae9ca42aab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753999"
---
# <a name="icordebugmergedassemblyrecordgetculture-method"></a><span data-ttu-id="77a5b-103">ICorDebugMergedAssemblyRecord::GetCulture 方法</span><span class="sxs-lookup"><span data-stu-id="77a5b-103">ICorDebugMergedAssemblyRecord::GetCulture Method</span></span>

<span data-ttu-id="77a5b-104">获取程序集的区域性名称字符串。</span><span class="sxs-lookup"><span data-stu-id="77a5b-104">Gets the culture name string of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77a5b-105">语法</span><span class="sxs-lookup"><span data-stu-id="77a5b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCulture(  
   [in] ULONG32 cchCulture,
   [out] ULONG32 *pcchCulture,
   [out, size_is(cchCulture), length_is(*pcchCulture)] WCHAR szCulture[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="77a5b-106">参数</span><span class="sxs-lookup"><span data-stu-id="77a5b-106">Parameters</span></span>  

 `cchCulture`  
 <span data-ttu-id="77a5b-107">[in] `szCulture` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="77a5b-107">[in] The number of characters in the `szCulture` buffer.</span></span>  
  
 `pcchCulture`  
 <span data-ttu-id="77a5b-108">[out] 实际写入 `szCulture` 缓冲区的字符数。</span><span class="sxs-lookup"><span data-stu-id="77a5b-108">[out] The number of characters actually written to the `szCulture` buffer.</span></span>  
  
 `szCulture`  
 <span data-ttu-id="77a5b-109">[out] 包含区域性名称的字符数组。</span><span class="sxs-lookup"><span data-stu-id="77a5b-109">[out] A character array that contains the culture name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="77a5b-110">备注</span><span class="sxs-lookup"><span data-stu-id="77a5b-110">Remarks</span></span>  

 <span data-ttu-id="77a5b-111">区域性名称是用于标识区域性的唯一字符串，例如“EN-US”（针对美式英语区域性）或“neutral”（针对非特定区域性）。</span><span class="sxs-lookup"><span data-stu-id="77a5b-111">The culture name is a unique string that identifies a culture, such as "en-US" (for the English (United States) culture), or "neutral" (for a neutral culture).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="77a5b-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="77a5b-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77a5b-113">要求</span><span class="sxs-lookup"><span data-stu-id="77a5b-113">Requirements</span></span>  

 <span data-ttu-id="77a5b-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77a5b-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77a5b-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="77a5b-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="77a5b-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="77a5b-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="77a5b-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77a5b-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77a5b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="77a5b-118">See also</span></span>

- [<span data-ttu-id="77a5b-119">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="77a5b-119">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="77a5b-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="77a5b-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
