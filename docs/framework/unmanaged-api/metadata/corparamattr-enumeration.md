---
description: 了解详细信息： CorParamAttr 枚举
title: CorParamAttr 枚举
ms.date: 03/30/2017
api_name:
- CorParamAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorParamAttr
helpviewer_keywords:
- CorParamAttr enumeration [.NET Framework metadata]
ms.assetid: a7ff90ad-dad8-48e8-917d-4aa9a118cbc8
topic_type:
- apiref
ms.openlocfilehash: c07569d3fb92b20a7985dbfeb2205af727866051
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784283"
---
# <a name="corparamattr-enumeration"></a><span data-ttu-id="be806-103">CorParamAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="be806-103">CorParamAttr Enumeration</span></span>

<span data-ttu-id="be806-104">包含一些值，用于描述方法参数的元数据。</span><span class="sxs-lookup"><span data-stu-id="be806-104">Contains values that describe the metadata of a method parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be806-105">语法</span><span class="sxs-lookup"><span data-stu-id="be806-105">Syntax</span></span>  
  
```cpp  
typedef enum CorParamAttr {  
  
    pdIn                        =   0x0001,  
    pdOut                       =   0x0002,  
    pdOptional                  =   0x0010,  
  
    pdReservedMask              =   0xf000,  
    pdHasDefault                =   0x1000,  
    pdHasFieldMarshal           =   0x2000,  
  
    pdUnused                    =   0xcfe0  
  
} CorParamAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="be806-106">成员</span><span class="sxs-lookup"><span data-stu-id="be806-106">Members</span></span>  
  
|<span data-ttu-id="be806-107">成员</span><span class="sxs-lookup"><span data-stu-id="be806-107">Member</span></span>|<span data-ttu-id="be806-108">说明</span><span class="sxs-lookup"><span data-stu-id="be806-108">Description</span></span>|  
|------------|-----------------|  
|`pdIn`|<span data-ttu-id="be806-109">指定将参数传递给方法调用。</span><span class="sxs-lookup"><span data-stu-id="be806-109">Specifies that the parameter is passed into the method call.</span></span>|  
|`pdOut`|<span data-ttu-id="be806-110">指定从方法返回传递参数。</span><span class="sxs-lookup"><span data-stu-id="be806-110">Specifies that the parameter is passed from the method return.</span></span>|  
|`pdOptional`|<span data-ttu-id="be806-111">指定参数为可选。</span><span class="sxs-lookup"><span data-stu-id="be806-111">Specifies that the parameter is optional.</span></span>|  
|`pdReservedMask`|<span data-ttu-id="be806-112">保留供公共语言运行时内部使用。</span><span class="sxs-lookup"><span data-stu-id="be806-112">Reserved for internal use by the common language runtime.</span></span>|  
|`pdHasDefault`|<span data-ttu-id="be806-113">指定参数具有默认值。</span><span class="sxs-lookup"><span data-stu-id="be806-113">Specifies that the parameter has a default value.</span></span>|  
|`pdHasFieldMarshal`|<span data-ttu-id="be806-114">指定参数具有封送处理信息。</span><span class="sxs-lookup"><span data-stu-id="be806-114">Specifies that the parameter has marshaling information.</span></span>|  
|`pdUnused`|<span data-ttu-id="be806-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="be806-115">Unused.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="be806-116">要求</span><span class="sxs-lookup"><span data-stu-id="be806-116">Requirements</span></span>  

 <span data-ttu-id="be806-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be806-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be806-118">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="be806-118">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="be806-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be806-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be806-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="be806-120">See also</span></span>

- [<span data-ttu-id="be806-121">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="be806-121">Metadata Enumerations</span></span>](metadata-enumerations.md)
