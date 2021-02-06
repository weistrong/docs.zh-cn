---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetSimpleName 方法
title: ICorDebugMergedAssemblyRecord::GetSimpleName 方法
ms.date: 03/30/2017
ms.assetid: bc3410f6-ebca-4bca-9b45-fc38c74fa9cb
ms.openlocfilehash: e77a5cc7df009a5bc55a7eb952ead80e5f81f271
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650386"
---
# <a name="icordebugmergedassemblyrecordgetsimplename-method"></a><span data-ttu-id="eaa90-103">ICorDebugMergedAssemblyRecord::GetSimpleName 方法</span><span class="sxs-lookup"><span data-stu-id="eaa90-103">ICorDebugMergedAssemblyRecord::GetSimpleName Method</span></span>

<span data-ttu-id="eaa90-104">获取程序集的简单名。</span><span class="sxs-lookup"><span data-stu-id="eaa90-104">Gets the simple name of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eaa90-105">语法</span><span class="sxs-lookup"><span data-stu-id="eaa90-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSimpleName(  
   [in] ULONG32 cchName,
   [out] ULONG32 *pcchName,
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eaa90-106">参数</span><span class="sxs-lookup"><span data-stu-id="eaa90-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="eaa90-107">[in] `szName` 缓冲区中的字符数。</span><span class="sxs-lookup"><span data-stu-id="eaa90-107">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="eaa90-108">[out] 指向实际写入 `szName` 缓冲区的字符数。缓冲区的字符数的指针。</span><span class="sxs-lookup"><span data-stu-id="eaa90-108">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="eaa90-109">指向字符数组的指针。</span><span class="sxs-lookup"><span data-stu-id="eaa90-109">A pointer to a character array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eaa90-110">备注</span><span class="sxs-lookup"><span data-stu-id="eaa90-110">Remarks</span></span>  

 <span data-ttu-id="eaa90-111">此方法检索程序集的简单名（例如“System.Collections”），该名称不带文件扩展名、版本、区域性或公钥标记。</span><span class="sxs-lookup"><span data-stu-id="eaa90-111">This method retrieves the simple name of an assembly (such as "System.Collections"), without a file extension, version, culture, or public key token.</span></span> <span data-ttu-id="eaa90-112">它对应托管代码中的 <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="eaa90-112">It corresponds to the <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> property in managed code.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="eaa90-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="eaa90-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eaa90-114">要求</span><span class="sxs-lookup"><span data-stu-id="eaa90-114">Requirements</span></span>  

 <span data-ttu-id="eaa90-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eaa90-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eaa90-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eaa90-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eaa90-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eaa90-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eaa90-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eaa90-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eaa90-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="eaa90-119">See also</span></span>

- [<span data-ttu-id="eaa90-120">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="eaa90-120">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="eaa90-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="eaa90-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
