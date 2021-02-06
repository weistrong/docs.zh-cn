---
description: 了解详细信息： COR_PRF_CODE_INFO 结构
title: COR_PRF_CODE_INFO 结构
ms.date: 03/30/2017
api_name:
- COR_PRF_CODE_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CODE_INFO
helpviewer_keywords:
- COR_PRF_CODE_INFO structure [.NET Framework profiling]
ms.assetid: cf30e27c-1f7e-43a2-ba1e-01e4137301db
topic_type:
- apiref
ms.openlocfilehash: 11eae032424a039cac1136c08409b5b4712e6db1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649242"
---
# <a name="cor_prf_code_info-structure"></a><span data-ttu-id="6a19b-103">COR_PRF_CODE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="6a19b-103">COR_PRF_CODE_INFO Structure</span></span>

<span data-ttu-id="6a19b-104">表示存储在内存中的一个本机代码连续块。</span><span class="sxs-lookup"><span data-stu-id="6a19b-104">Represents one contiguous block of native code stored in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a19b-105">语法</span><span class="sxs-lookup"><span data-stu-id="6a19b-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_PRF_CODE_INFO {  
    UINT_PTR startAddress;  
    SIZE_T size;  
} COR_PRF_CODE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="6a19b-106">成员</span><span class="sxs-lookup"><span data-stu-id="6a19b-106">Members</span></span>  
  
|<span data-ttu-id="6a19b-107">成员</span><span class="sxs-lookup"><span data-stu-id="6a19b-107">Member</span></span>|<span data-ttu-id="6a19b-108">说明</span><span class="sxs-lookup"><span data-stu-id="6a19b-108">Description</span></span>|  
|------------|-----------------|  
|`startAddress`|<span data-ttu-id="6a19b-109">连续代码块的起始地址。</span><span class="sxs-lookup"><span data-stu-id="6a19b-109">The starting address of the contiguous block of code.</span></span>|  
|`size`|<span data-ttu-id="6a19b-110">块的大小。</span><span class="sxs-lookup"><span data-stu-id="6a19b-110">The size of the block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6a19b-111">要求</span><span class="sxs-lookup"><span data-stu-id="6a19b-111">Requirements</span></span>  

 <span data-ttu-id="6a19b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6a19b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a19b-113">**标头：** Corprof.idl .idl</span><span class="sxs-lookup"><span data-stu-id="6a19b-113">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="6a19b-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a19b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a19b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a19b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a19b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a19b-116">See also</span></span>

- [<span data-ttu-id="6a19b-117">分析结构</span><span class="sxs-lookup"><span data-stu-id="6a19b-117">Profiling Structures</span></span>](profiling-structures.md)
