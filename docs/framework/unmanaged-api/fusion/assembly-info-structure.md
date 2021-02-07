---
description: 了解详细信息： ASSEMBLY_INFO 结构
title: ASSEMBLY_INFO 结构
ms.date: 03/30/2017
api_name:
- ASSEMBLY_INFO
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- ASSEMBLY_INFO
helpviewer_keywords:
- ASSEMBLY_INFO structure [.NET Framework fusion]
ms.assetid: b3cbb47c-457f-4083-8895-49562ca99ab8
topic_type:
- apiref
ms.openlocfilehash: c28d9abf13769197b62705d51bbcf4f099616bbc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761274"
---
# <a name="assembly_info-structure"></a><span data-ttu-id="24a55-103">ASSEMBLY_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="24a55-103">ASSEMBLY_INFO Structure</span></span>

<span data-ttu-id="24a55-104">包含有关在全局程序集缓存中注册的程序集的信息。</span><span class="sxs-lookup"><span data-stu-id="24a55-104">Contains information about an assembly that is registered in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24a55-105">语法</span><span class="sxs-lookup"><span data-stu-id="24a55-105">Syntax</span></span>  
  
```cpp  
typedef struct _ASSEMBLY_INFO {  
    ULONG           cbAssemblyInfo;  
    DWORD           dwAssemblyFlags;  
    ULARGE_INTEGER  uliAssemblySizeInKB;  
    LPWSTR          pszCurrentAssemblyPathBuf;  
    ULONG           cchBuf;  
} ASSEMBLY_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="24a55-106">成员</span><span class="sxs-lookup"><span data-stu-id="24a55-106">Members</span></span>  
  
|<span data-ttu-id="24a55-107">成员</span><span class="sxs-lookup"><span data-stu-id="24a55-107">Member</span></span>|<span data-ttu-id="24a55-108">说明</span><span class="sxs-lookup"><span data-stu-id="24a55-108">Description</span></span>|  
|------------|-----------------|  
|`cbAssemblyInfo`|<span data-ttu-id="24a55-109">结构的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="24a55-109">The size, in bytes, of the structure.</span></span> <span data-ttu-id="24a55-110">此字段保留供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="24a55-110">This field is reserved for future extensibility.</span></span>|  
|`dwAssemblyFlags`|<span data-ttu-id="24a55-111">指示程序集的安装详细信息的标志。</span><span class="sxs-lookup"><span data-stu-id="24a55-111">Flags that indicate installation details about the assembly.</span></span> <span data-ttu-id="24a55-112">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="24a55-112">The following values are supported:</span></span><br /><br /> <span data-ttu-id="24a55-113">-ASSEMBLYINFO_FLAG_INSTALLED 值，该值指示已安装程序集。</span><span class="sxs-lookup"><span data-stu-id="24a55-113">-   The ASSEMBLYINFO_FLAG_INSTALLED value, which indicates that the assembly is installed.</span></span> <span data-ttu-id="24a55-114">.NET Framework 的当前版本始终设置 `dwAssemblyFlags` 为此值。</span><span class="sxs-lookup"><span data-stu-id="24a55-114">The current version of the .NET Framework always sets `dwAssemblyFlags` to this value.</span></span><br /><span data-ttu-id="24a55-115">-ASSEMBLYINFO_FLAG_PAYLOADRESIDENT 值，该值指示程序集是一个有效负载。</span><span class="sxs-lookup"><span data-stu-id="24a55-115">-   The ASSEMBLYINFO_FLAG_PAYLOADRESIDENT value, which indicates that the assembly is a payload resident.</span></span> <span data-ttu-id="24a55-116">.NET Framework 的当前版本决不会将设置 `dwAssemblyFlags` 为此值。</span><span class="sxs-lookup"><span data-stu-id="24a55-116">The current version of the .NET Framework never sets `dwAssemblyFlags` to this value.</span></span>|  
|`uliAssemblySizeInKB`|<span data-ttu-id="24a55-117">程序集包含的文件的总大小（kb）。</span><span class="sxs-lookup"><span data-stu-id="24a55-117">The total size, in kilobytes, of the files that the assembly contains.</span></span>|  
|`pszCurrentAssemblyPathBuf`|<span data-ttu-id="24a55-118">指向包含清单文件的当前路径的字符串缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="24a55-118">A pointer to a string buffer that holds the current path to the manifest file.</span></span> <span data-ttu-id="24a55-119">路径必须以 null 字符结尾。</span><span class="sxs-lookup"><span data-stu-id="24a55-119">The path must end with a null character.</span></span>|  
|`cchBuf`|<span data-ttu-id="24a55-120">包含的宽字符数，包括 null 结束符 `pszCurrentAssemblyPathBuf` 。</span><span class="sxs-lookup"><span data-stu-id="24a55-120">The number of wide characters, including the null terminator, that `pszCurrentAssemblyPathBuf` contains.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24a55-121">要求</span><span class="sxs-lookup"><span data-stu-id="24a55-121">Requirements</span></span>  

 <span data-ttu-id="24a55-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24a55-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24a55-123">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="24a55-123">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="24a55-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24a55-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24a55-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="24a55-125">See also</span></span>

- [<span data-ttu-id="24a55-126">合成结构</span><span class="sxs-lookup"><span data-stu-id="24a55-126">Fusion Structures</span></span>](fusion-structures.md)
- [<span data-ttu-id="24a55-127">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="24a55-127">Global Assembly Cache</span></span>](../../app-domains/gac.md)
