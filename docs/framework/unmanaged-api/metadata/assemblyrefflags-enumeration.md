---
description: 了解详细信息： AssemblyRefFlags 枚举
title: AssemblyRefFlags 枚举
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
ms.openlocfilehash: 1b33faf816194c8b386f34a63d885ba37c4329a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678895"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="01c18-103">AssemblyRefFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="01c18-103">AssemblyRefFlags Enumeration</span></span>

<span data-ttu-id="01c18-104">包含用于描述程序集引用的功能的值。</span><span class="sxs-lookup"><span data-stu-id="01c18-104">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01c18-105">语法</span><span class="sxs-lookup"><span data-stu-id="01c18-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="01c18-106">成员</span><span class="sxs-lookup"><span data-stu-id="01c18-106">Members</span></span>  
  
|<span data-ttu-id="01c18-107">成员</span><span class="sxs-lookup"><span data-stu-id="01c18-107">Member</span></span>|<span data-ttu-id="01c18-108">说明</span><span class="sxs-lookup"><span data-stu-id="01c18-108">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="01c18-109">指定程序集引用包含有关程序集的发布服务器的完整的未哈哈希信息。</span><span class="sxs-lookup"><span data-stu-id="01c18-109">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="01c18-110">要求</span><span class="sxs-lookup"><span data-stu-id="01c18-110">Requirements</span></span>  

 <span data-ttu-id="01c18-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="01c18-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01c18-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="01c18-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="01c18-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01c18-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01c18-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="01c18-114">See also</span></span>

- [<span data-ttu-id="01c18-115">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="01c18-115">Metadata Enumerations</span></span>](metadata-enumerations.md)
- [<span data-ttu-id="01c18-116">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="01c18-116">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
- [<span data-ttu-id="01c18-117">DefineAssemblyRef 方法</span><span class="sxs-lookup"><span data-stu-id="01c18-117">DefineAssemblyRef Method</span></span>](imetadataassemblyemit-defineassemblyref-method.md)
