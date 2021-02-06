---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetVersion 方法
title: ICorDebugMergedAssemblyRecord::GetVersion 方法
ms.date: 03/30/2017
ms.assetid: c6858b06-ae26-4312-b325-ea6025016675
ms.openlocfilehash: 0e87e2bbb1207ebd1eb5775b7f52d5689b4e8727
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650334"
---
# <a name="icordebugmergedassemblyrecordgetversion-method"></a><span data-ttu-id="3debd-103">ICorDebugMergedAssemblyRecord::GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="3debd-103">ICorDebugMergedAssemblyRecord::GetVersion Method</span></span>

<span data-ttu-id="3debd-104">获取程序集的版本信息。</span><span class="sxs-lookup"><span data-stu-id="3debd-104">Gets the assembly's version information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3debd-105">语法</span><span class="sxs-lookup"><span data-stu-id="3debd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVersion(  
   [out] USHORT *pMajor,
   [out] USHORT *pMinor,
   [out] USHORT *pBuild,
   [out] USHORT *pRevision  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3debd-106">参数</span><span class="sxs-lookup"><span data-stu-id="3debd-106">Parameters</span></span>  

 `pMajor`  
 <span data-ttu-id="3debd-107">[out] 指向主版本号的指针。</span><span class="sxs-lookup"><span data-stu-id="3debd-107">[out] A pointer to the major version number.</span></span>  
  
 `pMinor`  
 <span data-ttu-id="3debd-108">[out] 指向次版本号的指针。</span><span class="sxs-lookup"><span data-stu-id="3debd-108">[out] A pointer to the minor version number.</span></span>  
  
 `pBuild`  
 <span data-ttu-id="3debd-109">[out] 指向内部版本号的指针。</span><span class="sxs-lookup"><span data-stu-id="3debd-109">[out] A pointer to the build number.</span></span>  
  
 `pRevision`  
 <span data-ttu-id="3debd-110">[out] 指向修订号的指针。</span><span class="sxs-lookup"><span data-stu-id="3debd-110">[out] A pointer to the revision number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3debd-111">备注</span><span class="sxs-lookup"><span data-stu-id="3debd-111">Remarks</span></span>  

 <span data-ttu-id="3debd-112">有关程序集版本号的信息，请参阅 <xref:System.Version> 类主题。</span><span class="sxs-lookup"><span data-stu-id="3debd-112">For information on assembly version numbers, see the <xref:System.Version> class topic.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3debd-113">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="3debd-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3debd-114">要求</span><span class="sxs-lookup"><span data-stu-id="3debd-114">Requirements</span></span>  

 <span data-ttu-id="3debd-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3debd-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3debd-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3debd-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3debd-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3debd-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3debd-118">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3debd-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3debd-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="3debd-119">See also</span></span>

- [<span data-ttu-id="3debd-120">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="3debd-120">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="3debd-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="3debd-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
