---
description: 了解详细信息： CVStruct 结构
title: CVStruct 结构
ms.date: 03/30/2017
api_name:
- CVStruct
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CVStruct
helpviewer_keywords:
- CVStruct structure [.NET Framework metadata]
ms.assetid: e9e4e497-d5fb-464b-991c-3bdd824664fd
topic_type:
- apiref
ms.openlocfilehash: 25e8073f75620bca0737b11499d318cd57d6101c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707210"
---
# <a name="cvstruct-structure"></a><span data-ttu-id="6ef3a-103">CVStruct 结构</span><span class="sxs-lookup"><span data-stu-id="6ef3a-103">CVStruct Structure</span></span>

<span data-ttu-id="6ef3a-104">包含在安装模块或复合图像时所使用的信息。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-104">Contains information that is used when installing a module or a composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ef3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="6ef3a-105">Syntax</span></span>  
  
```cpp  
typedef struct {  
    short Major;  
    short Minor;  
    short Sub;  
    short Build;  
} CVStruct;  
```  
  
## <a name="members"></a><span data-ttu-id="6ef3a-106">成员</span><span class="sxs-lookup"><span data-stu-id="6ef3a-106">Members</span></span>  
  
|<span data-ttu-id="6ef3a-107">成员</span><span class="sxs-lookup"><span data-stu-id="6ef3a-107">Member</span></span>|<span data-ttu-id="6ef3a-108">说明</span><span class="sxs-lookup"><span data-stu-id="6ef3a-108">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="6ef3a-109">主要</span><span class="sxs-lookup"><span data-stu-id="6ef3a-109">Major</span></span>|<span data-ttu-id="6ef3a-110">主版本的内部版本号。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-110">Major version build number.</span></span>|  
|<span data-ttu-id="6ef3a-111">次要</span><span class="sxs-lookup"><span data-stu-id="6ef3a-111">Minor</span></span>|<span data-ttu-id="6ef3a-112">次版本号。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-112">Minor version build number.</span></span>|  
|<span data-ttu-id="6ef3a-113">Sub</span><span class="sxs-lookup"><span data-stu-id="6ef3a-113">Sub</span></span>|<span data-ttu-id="6ef3a-114">子生成号。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-114">Sub-build number.</span></span>|  
|<span data-ttu-id="6ef3a-115">构建</span><span class="sxs-lookup"><span data-stu-id="6ef3a-115">Build</span></span>|<span data-ttu-id="6ef3a-116">内部版本号。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-116">Build number.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6ef3a-117">要求</span><span class="sxs-lookup"><span data-stu-id="6ef3a-117">Requirements</span></span>  

 <span data-ttu-id="6ef3a-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef3a-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ef3a-119">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="6ef3a-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6ef3a-120">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="6ef3a-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6ef3a-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ef3a-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ef3a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6ef3a-122">See also</span></span>

- [<span data-ttu-id="6ef3a-123">元数据结构</span><span class="sxs-lookup"><span data-stu-id="6ef3a-123">Metadata Structures</span></span>](metadata-structures.md)
