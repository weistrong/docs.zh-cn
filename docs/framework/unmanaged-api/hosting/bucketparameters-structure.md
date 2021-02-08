---
description: 了解详细信息： BucketParameters 结构
title: BucketParameters 结构
ms.date: 03/30/2017
api_name:
- BucketParameters
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- BucketParameters
helpviewer_keywords:
- BucketParameters structure [.NET Framework hosting]
ms.assetid: 9432487e-f276-45d6-9a13-9a68024dbd46
topic_type:
- apiref
ms.openlocfilehash: e2d701caa0e2374cb6b44d5fb5537f2ecc7e34fd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799962"
---
# <a name="bucketparameters-structure"></a><span data-ttu-id="88ace-103">BucketParameters 结构</span><span class="sxs-lookup"><span data-stu-id="88ace-103">BucketParameters Structure</span></span>

<span data-ttu-id="88ace-104">存储事件的类型名称和与事件关联的当前异常的参数。</span><span class="sxs-lookup"><span data-stu-id="88ace-104">Stores the type name of an event and the parameters for the current exception that is associated with the event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88ace-105">语法</span><span class="sxs-lookup"><span data-stu-id="88ace-105">Syntax</span></span>  
  
```cpp  
typedef struct _BucketParameters {  
    BOOL  fInited;
    WCHAR pszEventTypeName[255];
    WCHAR pszParams[10][255];
} BucketParameters;  
```  
  
## <a name="members"></a><span data-ttu-id="88ace-106">成员</span><span class="sxs-lookup"><span data-stu-id="88ace-106">Members</span></span>  
  
|<span data-ttu-id="88ace-107">成员</span><span class="sxs-lookup"><span data-stu-id="88ace-107">Member</span></span>|<span data-ttu-id="88ace-108">说明</span><span class="sxs-lookup"><span data-stu-id="88ace-108">Description</span></span>|  
|------------|-----------------|  
|`fInited`|<span data-ttu-id="88ace-109">`true`如果此结构的其余部分有效，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="88ace-109">`true`, if the rest of this structure is valid; otherwise, `false`.</span></span>|  
|`pszEventTypeName`|<span data-ttu-id="88ace-110">事件类型的名称。</span><span class="sxs-lookup"><span data-stu-id="88ace-110">Name of the event type.</span></span>|  
|`pszParams`|<span data-ttu-id="88ace-111">一个字符串数组，其中每个字符串都为与事件关联的当前异常指定一个参数。</span><span class="sxs-lookup"><span data-stu-id="88ace-111">An array of strings, each of which specifies a parameter for the current exception associated with the event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="88ace-112">要求</span><span class="sxs-lookup"><span data-stu-id="88ace-112">Requirements</span></span>  

 <span data-ttu-id="88ace-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="88ace-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88ace-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="88ace-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="88ace-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88ace-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88ace-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="88ace-116">See also</span></span>

- [<span data-ttu-id="88ace-117">承载结构</span><span class="sxs-lookup"><span data-stu-id="88ace-117">Hosting Structures</span></span>](hosting-structures.md)
