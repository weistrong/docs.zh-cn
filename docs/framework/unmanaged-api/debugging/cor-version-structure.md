---
description: 了解详细信息： COR_VERSION 结构
title: COR_VERSION 结构
ms.date: 03/30/2017
api_name:
- COR_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_VERSION
helpviewer_keywords:
- COR_VERSION structure [.NET Framework debugging]
ms.assetid: 5efaee1c-a001-4c73-9525-4160f4c71567
topic_type:
- apiref
ms.openlocfilehash: abdbe2a62d89db9dd673a429d81209fc42c34b73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801756"
---
# <a name="cor_version-structure"></a><span data-ttu-id="06f49-103">COR_VERSION 结构</span><span class="sxs-lookup"><span data-stu-id="06f49-103">COR_VERSION Structure</span></span>

<span data-ttu-id="06f49-104">存储由四个部分组成的公共语言运行时标准版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-104">Stores the standard four-part version number of the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06f49-105">语法</span><span class="sxs-lookup"><span data-stu-id="06f49-105">Syntax</span></span>  
  
```cpp  
typedef struct _COR_VERSION {  
    DWORD dwMajor;  
    DWORD dwMinor;  
    DWORD dwBuild;  
    DWORD dwSubBuild;  
} COR_VERSION;  
```  
  
## <a name="members"></a><span data-ttu-id="06f49-106">成员</span><span class="sxs-lookup"><span data-stu-id="06f49-106">Members</span></span>  
  
|<span data-ttu-id="06f49-107">成员</span><span class="sxs-lookup"><span data-stu-id="06f49-107">Member</span></span>|<span data-ttu-id="06f49-108">说明</span><span class="sxs-lookup"><span data-stu-id="06f49-108">Description</span></span>|  
|------------|-----------------|  
|`dwMajor`|<span data-ttu-id="06f49-109">主版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-109">The major version number.</span></span>|  
|`dwMinor`|<span data-ttu-id="06f49-110">次版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-110">The minor version number.</span></span>|  
|`dwBuild`|<span data-ttu-id="06f49-111">内部版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-111">The build number.</span></span>|  
|`dwSubBuild`|<span data-ttu-id="06f49-112">子内部版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-112">The sub-build number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06f49-113">备注</span><span class="sxs-lookup"><span data-stu-id="06f49-113">Remarks</span></span>  

 <span data-ttu-id="06f49-114">如果版本号为1.0.3705.288，1为主要版本号，0为次版本号，3705为内部版本号，288为子内部版本号。</span><span class="sxs-lookup"><span data-stu-id="06f49-114">If the version number is 1.0.3705.288, 1 is the major version number, 0 is the minor version number, 3705 is the build number, and 288 is the sub-build number.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06f49-115">要求</span><span class="sxs-lookup"><span data-stu-id="06f49-115">Requirements</span></span>  

 <span data-ttu-id="06f49-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06f49-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06f49-117">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="06f49-117">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="06f49-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="06f49-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="06f49-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06f49-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06f49-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="06f49-120">See also</span></span>

- [<span data-ttu-id="06f49-121">调试结构</span><span class="sxs-lookup"><span data-stu-id="06f49-121">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="06f49-122">调试</span><span class="sxs-lookup"><span data-stu-id="06f49-122">Debugging</span></span>](index.md)
