---
description: 了解详细信息： CorLocalRefPreservation 枚举
title: CorLocalRefPreservation 枚举
ms.date: 03/30/2017
api_name:
- CorLocalRefPreservation
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLocalRefPreservation
helpviewer_keywords:
- CorLocalRefPreservation enumeration [.NET Framework metadata]
ms.assetid: 44757163-1228-4213-a4c4-d4de503cc75d
topic_type:
- apiref
ms.openlocfilehash: afcdf6ce22c5f786e8f728cc1e45ad3ca44e7ef5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784413"
---
# <a name="corlocalrefpreservation-enumeration"></a><span data-ttu-id="1fab8-103">CorLocalRefPreservation 枚举</span><span class="sxs-lookup"><span data-stu-id="1fab8-103">CorLocalRefPreservation Enumeration</span></span>

<span data-ttu-id="1fab8-104">包含用于处理本地引用的标志值。</span><span class="sxs-lookup"><span data-stu-id="1fab8-104">Contains flag values for the treatment of local references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fab8-105">语法</span><span class="sxs-lookup"><span data-stu-id="1fab8-105">Syntax</span></span>  
  
```cpp  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a><span data-ttu-id="1fab8-106">成员</span><span class="sxs-lookup"><span data-stu-id="1fab8-106">Members</span></span>  
  
|<span data-ttu-id="1fab8-107">成员</span><span class="sxs-lookup"><span data-stu-id="1fab8-107">Member</span></span>|<span data-ttu-id="1fab8-108">说明</span><span class="sxs-lookup"><span data-stu-id="1fab8-108">Description</span></span>|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|<span data-ttu-id="1fab8-109">不保留本地引用。</span><span class="sxs-lookup"><span data-stu-id="1fab8-109">Preserve no local references.</span></span>|  
|`MDPreserveLocalTypeRef`|<span data-ttu-id="1fab8-110">保留本地类型引用。</span><span class="sxs-lookup"><span data-stu-id="1fab8-110">Preserve local type references.</span></span>|  
|`MDPreserveLocalMemberRef`|<span data-ttu-id="1fab8-111">保留局部成员引用。</span><span class="sxs-lookup"><span data-stu-id="1fab8-111">Preserve local member references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1fab8-112">要求</span><span class="sxs-lookup"><span data-stu-id="1fab8-112">Requirements</span></span>  

 <span data-ttu-id="1fab8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fab8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fab8-114">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="1fab8-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="1fab8-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fab8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fab8-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fab8-116">See also</span></span>

- [<span data-ttu-id="1fab8-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="1fab8-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
