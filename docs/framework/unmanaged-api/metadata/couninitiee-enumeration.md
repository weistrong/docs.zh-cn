---
description: 了解详细信息： COUNINITIEE 枚举
title: COUNINITIEE 枚举
ms.date: 03/30/2017
api_name:
- COUNINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COUNINITIEE
helpviewer_keywords:
- COUNINITIEE enumeration [.NET Framework metadata]
ms.assetid: c42baa79-f469-4330-95a2-baf7f021c2fc
topic_type:
- apiref
ms.openlocfilehash: 893ab96851e9c762a888f3c4cac98b486a0b4614
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707223"
---
# <a name="couninitiee-enumeration"></a><span data-ttu-id="d6fad-103">COUNINITIEE 枚举</span><span class="sxs-lookup"><span data-stu-id="d6fad-103">COUNINITIEE Enumeration</span></span>

<span data-ttu-id="d6fad-104">指定初始化公共语言运行时 [CoUninitializeEE](../hosting/couninitializeee-function.md) 使用的常量。</span><span class="sxs-lookup"><span data-stu-id="d6fad-104">Specifies constants used by [CoUninitializeEE](../hosting/couninitializeee-function.md) when initializing the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6fad-105">语法</span><span class="sxs-lookup"><span data-stu-id="d6fad-105">Syntax</span></span>  
  
```cpp  
typedef enum tagCOUNINITEE  
{  
    COUNINITEE_DEFAULT  = 0x0,
    COUNINITEE_DLL      = 0x1  
} COUNINITIEE;  
```  
  
## <a name="members"></a><span data-ttu-id="d6fad-106">成员</span><span class="sxs-lookup"><span data-stu-id="d6fad-106">Members</span></span>  
  
|<span data-ttu-id="d6fad-107">成员</span><span class="sxs-lookup"><span data-stu-id="d6fad-107">Member</span></span>|<span data-ttu-id="d6fad-108">说明</span><span class="sxs-lookup"><span data-stu-id="d6fad-108">Description</span></span>|  
|------------|-----------------|  
|`COUNINITEE_DEFAULT`|<span data-ttu-id="d6fad-109">指示默认取消初始化模式。</span><span class="sxs-lookup"><span data-stu-id="d6fad-109">Indicates default uninitialization mode.</span></span>|  
|`COUNINITEE_DLL`|<span data-ttu-id="d6fad-110">指示用于卸载程序集的取消初始化模式。</span><span class="sxs-lookup"><span data-stu-id="d6fad-110">Indicates uninitialization mode for unloading an assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d6fad-111">要求</span><span class="sxs-lookup"><span data-stu-id="d6fad-111">Requirements</span></span>  

 <span data-ttu-id="d6fad-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d6fad-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6fad-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d6fad-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d6fad-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d6fad-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d6fad-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6fad-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6fad-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6fad-116">See also</span></span>

- [<span data-ttu-id="d6fad-117">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="d6fad-117">Metadata Enumerations</span></span>](metadata-enumerations.md)
