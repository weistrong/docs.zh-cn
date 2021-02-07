---
description: 了解详细信息： CorRegFlags 枚举
title: CorRegFlags 枚举
ms.date: 03/30/2017
api_name:
- CorRegFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRegFlags
helpviewer_keywords:
- CorRegFlags enumeration [.NET Framework metadata]
ms.assetid: 8d3080ee-39fe-4c57-8950-51323632d045
topic_type:
- apiref
ms.openlocfilehash: 534b7b4b170d1f586e967807c4cc8a9c82648e8b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753649"
---
# <a name="corregflags-enumeration"></a><span data-ttu-id="46172-103">CorRegFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="46172-103">CorRegFlags Enumeration</span></span>

<span data-ttu-id="46172-104">提供安装模块或复合图像时用于注册的标志值。</span><span class="sxs-lookup"><span data-stu-id="46172-104">Provides flag values used for registration when installing a module or composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46172-105">语法</span><span class="sxs-lookup"><span data-stu-id="46172-105">Syntax</span></span>  
  
```cpp  
typedef enum
{  
    regNoCopy  = 0x00000001,  
    regConfig  = 0x00000002,  
    regHasRefs = 0x00000004  
} CorRegFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="46172-106">成员</span><span class="sxs-lookup"><span data-stu-id="46172-106">Members</span></span>  
  
|<span data-ttu-id="46172-107">成员</span><span class="sxs-lookup"><span data-stu-id="46172-107">Member</span></span>|<span data-ttu-id="46172-108">说明</span><span class="sxs-lookup"><span data-stu-id="46172-108">Description</span></span>|  
|------------|-----------------|  
|`regNoCopy`|<span data-ttu-id="46172-109">指定不应将文件复制到目标。</span><span class="sxs-lookup"><span data-stu-id="46172-109">Specifies that files should not be copied into the destination.</span></span>|  
|`regConfig`|<span data-ttu-id="46172-110">指定模块或复合为配置。</span><span class="sxs-lookup"><span data-stu-id="46172-110">Specifies that the module or composite is a configuration.</span></span>|  
|`regHasRefs`|<span data-ttu-id="46172-111">指定模块或复合具有类引用。</span><span class="sxs-lookup"><span data-stu-id="46172-111">Specifies that the module or composite has class references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="46172-112">要求</span><span class="sxs-lookup"><span data-stu-id="46172-112">Requirements</span></span>  

 <span data-ttu-id="46172-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46172-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46172-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="46172-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="46172-115">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="46172-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="46172-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46172-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46172-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="46172-117">See also</span></span>

- [<span data-ttu-id="46172-118">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="46172-118">Metadata Enumerations</span></span>](metadata-enumerations.md)
