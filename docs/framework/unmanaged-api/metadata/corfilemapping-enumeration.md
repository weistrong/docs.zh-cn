---
description: 了解详细信息： CorFileMapping 枚举
title: CorFileMapping 枚举
ms.date: 03/30/2017
api_name:
- CorFileMapping
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileMapping
helpviewer_keywords:
- CorFileMapping enumeration [.NET Framework metadata]
ms.assetid: 3ca41592-b8da-475a-8032-a15627730003
topic_type:
- apiref
ms.openlocfilehash: 0fc3916e75c576a6b133ba8a49c00eec6c9bac19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784465"
---
# <a name="corfilemapping-enumeration"></a><span data-ttu-id="cf25d-103">CorFileMapping 枚举</span><span class="sxs-lookup"><span data-stu-id="cf25d-103">CorFileMapping Enumeration</span></span>

<span data-ttu-id="cf25d-104">包含一些值，这些值描述从对 [IMetaDataInfo：： GetFileMapping](imetadatainfo-getfilemapping-method.md) 方法的调用返回的文件映射的类型。</span><span class="sxs-lookup"><span data-stu-id="cf25d-104">Contains values that describe the type of file mapping that is returned from a call to the [IMetaDataInfo::GetFileMapping](imetadatainfo-getfilemapping-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf25d-105">语法</span><span class="sxs-lookup"><span data-stu-id="cf25d-105">Syntax</span></span>  
  
```cpp  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="cf25d-106">成员</span><span class="sxs-lookup"><span data-stu-id="cf25d-106">Members</span></span>  
  
|<span data-ttu-id="cf25d-107">成员</span><span class="sxs-lookup"><span data-stu-id="cf25d-107">Member</span></span>|<span data-ttu-id="cf25d-108">说明</span><span class="sxs-lookup"><span data-stu-id="cf25d-108">Description</span></span>|  
|------------|-----------------|  
|`fmFlat`|<span data-ttu-id="cf25d-109">文件映射为数据文件。</span><span class="sxs-lookup"><span data-stu-id="cf25d-109">The file is mapped as a data file.</span></span> <span data-ttu-id="cf25d-110">也就是说， `SEC_IMAGE` 标志未传递到 Microsoft Win32 `CreateFileMapping` 函数。</span><span class="sxs-lookup"><span data-stu-id="cf25d-110">That is, the `SEC_IMAGE` flag was not passed to the Microsoft Win32 `CreateFileMapping` function.</span></span>|  
|`fmExecutableImage`|<span data-ttu-id="cf25d-111">使用 `LoadLibrary` 函数或带有标志的函数为执行映射文件 `CreateFileMapping` `SEC_IMAGE` 。</span><span class="sxs-lookup"><span data-stu-id="cf25d-111">The file is mapped for execution, by using either the `LoadLibrary` function or the `CreateFileMapping` function with the `SEC_IMAGE` flag.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cf25d-112">要求</span><span class="sxs-lookup"><span data-stu-id="cf25d-112">Requirements</span></span>  

 <span data-ttu-id="cf25d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cf25d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf25d-114">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="cf25d-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="cf25d-115">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf25d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf25d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="cf25d-116">See also</span></span>

- [<span data-ttu-id="cf25d-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="cf25d-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
- [<span data-ttu-id="cf25d-118">GetFileMapping 方法</span><span class="sxs-lookup"><span data-stu-id="cf25d-118">GetFileMapping Method</span></span>](imetadatainfo-getfilemapping-method.md)
