---
description: 了解详细信息： CorFileFlags 枚举
title: CorFileFlags 枚举
ms.date: 03/30/2017
api_name:
- CorFileFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileFlags
helpviewer_keywords:
- CorFileFlags enumeration [.NET Framework metadata]
ms.assetid: d16703fd-518f-412e-92cb-74433d11032e
topic_type:
- apiref
ms.openlocfilehash: 8ffad9bad9c656a10c2c556f5e06f9d510ccb45a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784478"
---
# <a name="corfileflags-enumeration"></a><span data-ttu-id="057d0-103">CorFileFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="057d0-103">CorFileFlags Enumeration</span></span>

<span data-ttu-id="057d0-104">包含一些值，这些值描述在对 [IMetaDataAssemblyEmit：:D efinefile](imetadataassemblyemit-definefile-method.md)的调用中定义的文件类型。</span><span class="sxs-lookup"><span data-stu-id="057d0-104">Contains values that describe the type of file defined in a call to [IMetaDataAssemblyEmit::DefineFile](imetadataassemblyemit-definefile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="057d0-105">语法</span><span class="sxs-lookup"><span data-stu-id="057d0-105">Syntax</span></span>  
  
```cpp  
typedef enum CorFileFlags {  
  
    ffContainsMetaData      =   0x0000,  
    ffContainsNoMetaData    =   0x0001  
  
} CorFileFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="057d0-106">成员</span><span class="sxs-lookup"><span data-stu-id="057d0-106">Members</span></span>  
  
|<span data-ttu-id="057d0-107">成员</span><span class="sxs-lookup"><span data-stu-id="057d0-107">Member</span></span>|<span data-ttu-id="057d0-108">说明</span><span class="sxs-lookup"><span data-stu-id="057d0-108">Description</span></span>|  
|------------|-----------------|  
|`ffContainsMetaData`|<span data-ttu-id="057d0-109">指示该文件不是资源文件。</span><span class="sxs-lookup"><span data-stu-id="057d0-109">Indicates that the file is not a resource file.</span></span>|  
|`ffContainsNoMetaData`|<span data-ttu-id="057d0-110">指示文件可能不包含元数据，可能是资源文件。</span><span class="sxs-lookup"><span data-stu-id="057d0-110">Indicates that the file, possibly a resource file, does not contain metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="057d0-111">要求</span><span class="sxs-lookup"><span data-stu-id="057d0-111">Requirements</span></span>  

 <span data-ttu-id="057d0-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="057d0-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="057d0-113">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="057d0-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="057d0-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="057d0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="057d0-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="057d0-115">See also</span></span>

- [<span data-ttu-id="057d0-116">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="057d0-116">Metadata Enumerations</span></span>](metadata-enumerations.md)
