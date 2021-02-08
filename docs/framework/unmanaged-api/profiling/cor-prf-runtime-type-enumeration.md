---
description: 了解详细信息： COR_PRF_RUNTIME_TYPE 枚举
title: COR_PRF_RUNTIME_TYPE 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_RUNTIME_TYPE Enumeration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_RUNTIME_TYPE
helpviewer_keywords:
- COR_PRF_RUNTIME_TYPE enumeration [.NET Framework profiling]
ms.assetid: 35449514-333f-4918-9c60-7aa198d655d2
topic_type:
- apiref
ms.openlocfilehash: 8f4b4a0c51c43b1db97b511387eaee1aee79f523
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789039"
---
# <a name="cor_prf_runtime_type-enumeration"></a><span data-ttu-id="3c7c4-103">COR_PRF_RUNTIME_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="3c7c4-103">COR_PRF_RUNTIME_TYPE Enumeration</span></span>

<span data-ttu-id="3c7c4-104">包含一些值，这些值指示公共语言运行时的版本 (CLR) ： desktop 或 CoreCLR，用于 Silverlight。</span><span class="sxs-lookup"><span data-stu-id="3c7c4-104">Contains values that indicate the version of the common language runtime (CLR): desktop or CoreCLR, which is used in Silverlight.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c7c4-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c7c4-105">Syntax</span></span>  
  
```cpp  
typedef enum  
{  
    COR_PRF_DESKTOP_CLR = 0x1,  
    COR_PRF_CORE_CLR    = 0x2,  
} COR_PRF_RUNTIME_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="3c7c4-106">成员</span><span class="sxs-lookup"><span data-stu-id="3c7c4-106">Members</span></span>  
  
|<span data-ttu-id="3c7c4-107">成员</span><span class="sxs-lookup"><span data-stu-id="3c7c4-107">Member</span></span>|<span data-ttu-id="3c7c4-108">说明</span><span class="sxs-lookup"><span data-stu-id="3c7c4-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_DESKTOP_CLR`|<span data-ttu-id="3c7c4-109">CLR 的桌面版本。</span><span class="sxs-lookup"><span data-stu-id="3c7c4-109">The desktop version of the CLR.</span></span>|  
|`COR_PRF_CORE_CLR`|<span data-ttu-id="3c7c4-110">Silverlight 中使用的 CLR 核心版本。</span><span class="sxs-lookup"><span data-stu-id="3c7c4-110">The core version of the CLR, used in Silverlight.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c7c4-111">备注</span><span class="sxs-lookup"><span data-stu-id="3c7c4-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c7c4-112">要求</span><span class="sxs-lookup"><span data-stu-id="3c7c4-112">Requirements</span></span>  

 <span data-ttu-id="3c7c4-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c7c4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c7c4-114">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3c7c4-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3c7c4-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c7c4-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c7c4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c7c4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c7c4-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c7c4-117">See also</span></span>

- [<span data-ttu-id="3c7c4-118">分析枚举</span><span class="sxs-lookup"><span data-stu-id="3c7c4-118">Profiling Enumerations</span></span>](profiling-enumerations.md)
