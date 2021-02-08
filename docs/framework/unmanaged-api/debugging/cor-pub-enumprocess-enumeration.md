---
description: 了解详细信息： COR_PUB_ENUMPROCESS 枚举
title: COR_PUB_ENUMPROCESS 枚举
ms.date: 03/30/2017
api_name:
- COR_PUB_ENUMPROCESS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_PUB_ENUMPROCESS
helpviewer_keywords:
- COR_PUB_ENUMPROCESS enumeration [.NET Framework debugging]
ms.assetid: 5d3ada6e-feea-47da-a7ed-b664107c137f
topic_type:
- apiref
ms.openlocfilehash: 66bbd08aabb9d2c93e385ed098bae54754a85b85
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801782"
---
# <a name="cor_pub_enumprocess-enumeration"></a><span data-ttu-id="75fa5-103">COR_PUB_ENUMPROCESS 枚举</span><span class="sxs-lookup"><span data-stu-id="75fa5-103">COR_PUB_ENUMPROCESS Enumeration</span></span>

<span data-ttu-id="75fa5-104">标识要枚举的进程的类型。</span><span class="sxs-lookup"><span data-stu-id="75fa5-104">Identifies the type of process to be enumerated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75fa5-105">语法</span><span class="sxs-lookup"><span data-stu-id="75fa5-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PUB_MANAGEDONLY    = 0x00000001  
} COR_PUB_ENUMPROCESS;  
```  
  
## <a name="members"></a><span data-ttu-id="75fa5-106">成员</span><span class="sxs-lookup"><span data-stu-id="75fa5-106">Members</span></span>  
  
|<span data-ttu-id="75fa5-107">成员名称</span><span class="sxs-lookup"><span data-stu-id="75fa5-107">Member name</span></span>|<span data-ttu-id="75fa5-108">描述</span><span class="sxs-lookup"><span data-stu-id="75fa5-108">Description</span></span>|  
|-----------------|-----------------|  
|`COR_PUB_MANAGEDONLY`|<span data-ttu-id="75fa5-109">托管进程。</span><span class="sxs-lookup"><span data-stu-id="75fa5-109">A managed process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="75fa5-110">备注</span><span class="sxs-lookup"><span data-stu-id="75fa5-110">Remarks</span></span>  

 <span data-ttu-id="75fa5-111">非托管调试 API 的当前版本仅枚举托管进程。</span><span class="sxs-lookup"><span data-stu-id="75fa5-111">The current version of the unmanaged debugging API enumerates only managed processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75fa5-112">要求</span><span class="sxs-lookup"><span data-stu-id="75fa5-112">Requirements</span></span>  

 <span data-ttu-id="75fa5-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="75fa5-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75fa5-114">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="75fa5-114">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="75fa5-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="75fa5-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="75fa5-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75fa5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75fa5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="75fa5-117">See also</span></span>

- [<span data-ttu-id="75fa5-118">调试枚举</span><span class="sxs-lookup"><span data-stu-id="75fa5-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
