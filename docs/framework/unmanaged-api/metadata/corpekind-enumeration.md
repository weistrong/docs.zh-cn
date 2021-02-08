---
description: 了解详细信息： CorPEKind 枚举
title: CorPEKind 枚举
ms.date: 03/30/2017
api_name:
- CorPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPEKind
helpviewer_keywords:
- CorPEKind enumeration [.NET Framework metadata]
ms.assetid: 22dc6dea-b1b9-4982-a730-a022d586b117
topic_type:
- apiref
ms.openlocfilehash: 6d1f29a220ce9d4be4151d8eff6557fa8c693ed2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784270"
---
# <a name="corpekind-enumeration"></a><span data-ttu-id="86564-103">CorPEKind 枚举</span><span class="sxs-lookup"><span data-stu-id="86564-103">CorPEKind Enumeration</span></span>

<span data-ttu-id="86564-104">包含一些值，用于描述从 [IMetaDataImport2：： GetPEKind](imetadataimport2-getpekind-method.md)调用返回的可移植可执行文件 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="86564-104">Contains values that describe a portable executable (PE) file, as returned from a call to [IMetaDataImport2::GetPEKind](imetadataimport2-getpekind-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86564-105">语法</span><span class="sxs-lookup"><span data-stu-id="86564-105">Syntax</span></span>  
  
```cpp  
typedef enum CorPEKind {  
  
    peNot           = 0x00000000,  
    peILonly        = 0x00000001,  
    pe32BitRequired = 0x00000002,  
    pe32Plus        = 0x00000004,  
    pe32Unmanaged   = 0x00000008,  
    pe32BitPreferred= 0x00000010  
  
} CorPEKind;  
```  
  
## <a name="members"></a><span data-ttu-id="86564-106">成员</span><span class="sxs-lookup"><span data-stu-id="86564-106">Members</span></span>  
  
|<span data-ttu-id="86564-107">成员</span><span class="sxs-lookup"><span data-stu-id="86564-107">Member</span></span>|<span data-ttu-id="86564-108">说明</span><span class="sxs-lookup"><span data-stu-id="86564-108">Description</span></span>|  
|------------|-----------------|  
|`peNot`|<span data-ttu-id="86564-109">指示这不是 PE 文件。</span><span class="sxs-lookup"><span data-stu-id="86564-109">Indicates that this is not a PE file.</span></span>|  
|`peILOnly`|<span data-ttu-id="86564-110">指示此 PE 文件仅包含托管代码。</span><span class="sxs-lookup"><span data-stu-id="86564-110">Indicates that this PE file contains only managed code.</span></span>|  
|`pe32BitRequired`|<span data-ttu-id="86564-111">指示此 PE 文件进行 Win32 调用。</span><span class="sxs-lookup"><span data-stu-id="86564-111">Indicates that this PE file makes Win32 calls.</span></span>|  
|`pe32Plus`|<span data-ttu-id="86564-112">指示此 PE 文件在64位平台上运行。</span><span class="sxs-lookup"><span data-stu-id="86564-112">Indicates that this PE file runs on a 64-bit platform.</span></span>|  
|`pe32Unmanaged`|<span data-ttu-id="86564-113">指示此 PE 文件是本机代码。</span><span class="sxs-lookup"><span data-stu-id="86564-113">Indicates that this PE file is native code.</span></span>|  
|<span data-ttu-id="86564-114">pe32BitPreferred</span><span class="sxs-lookup"><span data-stu-id="86564-114">pe32BitPreferred</span></span>|<span data-ttu-id="86564-115">指示此 PE 文件与平台无关，并倾向于在32位环境中加载。</span><span class="sxs-lookup"><span data-stu-id="86564-115">Indicates that this PE file is platform-neutral and prefers to be loaded in a 32-bit environment.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="86564-116">备注</span><span class="sxs-lookup"><span data-stu-id="86564-116">Remarks</span></span>  

 <span data-ttu-id="86564-117">这些值可用于按位组合。</span><span class="sxs-lookup"><span data-stu-id="86564-117">These values can be used in bitwise combinations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86564-118">要求</span><span class="sxs-lookup"><span data-stu-id="86564-118">Requirements</span></span>  

 <span data-ttu-id="86564-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="86564-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86564-120">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="86564-120">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="86564-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86564-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86564-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="86564-122">See also</span></span>

- [<span data-ttu-id="86564-123">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="86564-123">Metadata Enumerations</span></span>](metadata-enumerations.md)
