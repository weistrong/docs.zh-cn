---
description: 了解详细信息： CorValidatorModuleType 枚举
title: CorValidatorModuleType 枚举
ms.date: 03/30/2017
api_name:
- CorValidatorModuleType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorValidatorModuleType
helpviewer_keywords:
- CorValidatorModuleType enumeration [.NET Framework metadata]
ms.assetid: 748f1ab2-fbcb-4f55-89ec-8d23d81ebc80
topic_type:
- apiref
ms.openlocfilehash: 13792c461660ddd8cfd530f5b34d642d806cdea4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707229"
---
# <a name="corvalidatormoduletype-enumeration"></a><span data-ttu-id="bdadc-103">CorValidatorModuleType 枚举</span><span class="sxs-lookup"><span data-stu-id="bdadc-103">CorValidatorModuleType Enumeration</span></span>

<span data-ttu-id="bdadc-104">指定模块的类型。</span><span class="sxs-lookup"><span data-stu-id="bdadc-104">Specifies the type of a module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdadc-105">语法</span><span class="sxs-lookup"><span data-stu-id="bdadc-105">Syntax</span></span>  
  
```cpp  
typedef enum  
{  
    ValidatorModuleTypeInvalid  = 0x0,  
    ValidatorModuleTypeMin      = 0x00000001,  
    ValidatorModuleTypePE       = 0x00000001,  
    ValidatorModuleTypeObj      = 0x00000002,  
    ValidatorModuleTypeEnc      = 0x00000003,  
    ValidatorModuleTypeIncr     = 0x00000004,  
    ValidatorModuleTypeMax      = 0x00000004  
} CorValidatorModuleType;  
```  
  
## <a name="members"></a><span data-ttu-id="bdadc-106">成员</span><span class="sxs-lookup"><span data-stu-id="bdadc-106">Members</span></span>  
  
|<span data-ttu-id="bdadc-107">成员</span><span class="sxs-lookup"><span data-stu-id="bdadc-107">Member</span></span>|<span data-ttu-id="bdadc-108">说明</span><span class="sxs-lookup"><span data-stu-id="bdadc-108">Description</span></span>|  
|------------|-----------------|  
|`ValidatorModuleTypeInvalid`|<span data-ttu-id="bdadc-109">模块是无效类型。</span><span class="sxs-lookup"><span data-stu-id="bdadc-109">The module is an invalid type.</span></span>|  
|`ValidatorModuleTypeMin`|<span data-ttu-id="bdadc-110">枚举的最小值 `CorValidatorModuleType` 。</span><span class="sxs-lookup"><span data-stu-id="bdadc-110">The minimum value of the `CorValidatorModuleType` enum.</span></span>|  
|`ValidatorModuleTypePE`|<span data-ttu-id="bdadc-111">模块是可移植的可执行文件 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="bdadc-111">The module is a portable executable (PE) file.</span></span>|  
|`ValidatorModuleTypeObj`|<span data-ttu-id="bdadc-112">模块是 .obj 文件。</span><span class="sxs-lookup"><span data-stu-id="bdadc-112">The module is a .obj file.</span></span>|  
|`ValidatorModuleTypeEnc`|<span data-ttu-id="bdadc-113">模块是 "编辑并继续" 调试器会话。</span><span class="sxs-lookup"><span data-stu-id="bdadc-113">The module is an edit-and-continue debugger session.</span></span>|  
|`ValidatorModuleTypeIncr`|<span data-ttu-id="bdadc-114">模块是增量生成的模块。</span><span class="sxs-lookup"><span data-stu-id="bdadc-114">The module is one that has been incrementally built.</span></span>|  
|`ValidatorModuleTypeMax`|<span data-ttu-id="bdadc-115">枚举的最大值 `CorValidatorModuleType` 。</span><span class="sxs-lookup"><span data-stu-id="bdadc-115">The maximum value of the `CorValidatorModuleType` enum.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bdadc-116">要求</span><span class="sxs-lookup"><span data-stu-id="bdadc-116">Requirements</span></span>  

 <span data-ttu-id="bdadc-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bdadc-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdadc-118">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="bdadc-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bdadc-119">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bdadc-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bdadc-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdadc-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdadc-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bdadc-121">See also</span></span>

- [<span data-ttu-id="bdadc-122">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="bdadc-122">Metadata Enumerations</span></span>](metadata-enumerations.md)
