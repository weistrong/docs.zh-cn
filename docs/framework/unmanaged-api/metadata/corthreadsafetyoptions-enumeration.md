---
description: 了解详细信息： CorThreadSafetyOptions 枚举
title: CorThreadSafetyOptions 枚举
ms.date: 03/30/2017
api_name:
- CorThreadSafetyOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorThreadSafetyOptions
helpviewer_keywords:
- CorThreadSafetyOptions enumeration [.NET Framework metadata]
ms.assetid: dae07d9b-df51-488c-b17e-52d6e48217bd
topic_type:
- apiref
ms.openlocfilehash: 7915bcf5e7b71fa84ea83642467c1600cd38712d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707314"
---
# <a name="corthreadsafetyoptions-enumeration"></a><span data-ttu-id="614e4-103">CorThreadSafetyOptions 枚举</span><span class="sxs-lookup"><span data-stu-id="614e4-103">CorThreadSafetyOptions Enumeration</span></span>

<span data-ttu-id="614e4-104">指定用于选择线程安全性选项的标志。</span><span class="sxs-lookup"><span data-stu-id="614e4-104">Specifies flags to select options for thread safety.</span></span>

## <a name="syntax"></a><span data-ttu-id="614e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="614e4-105">Syntax</span></span>

```cpp
typedef enum CorThreadSafetyOptions {
    MDThreadSafetyDefault       = 0x00000000,
    MDThreadSafetyOff           = 0x00000000,
    MDThreadSafetyOn            = 0x00000001,
} CorThreadSafetyOptions;
```

## <a name="members"></a><span data-ttu-id="614e4-106">成员</span><span class="sxs-lookup"><span data-stu-id="614e4-106">Members</span></span>

|<span data-ttu-id="614e4-107">成员</span><span class="sxs-lookup"><span data-stu-id="614e4-107">Member</span></span>|<span data-ttu-id="614e4-108">说明</span><span class="sxs-lookup"><span data-stu-id="614e4-108">Description</span></span>|
|------------|-----------------|
|`MDThreadSafetyDefault`|<span data-ttu-id="614e4-109">默认值。</span><span class="sxs-lookup"><span data-stu-id="614e4-109">Default value.</span></span> <span data-ttu-id="614e4-110">与 `MDThreadSafetyOff` 相同。</span><span class="sxs-lookup"><span data-stu-id="614e4-110">Same as `MDThreadSafetyOff`.</span></span>|
|`MDThreadSafetyOff`|<span data-ttu-id="614e4-111">指示无法设置读取器/写入器锁。</span><span class="sxs-lookup"><span data-stu-id="614e4-111">Indicates that a reader/writer lock cannot be set.</span></span>|
|`MDThreadSafetyOn`|<span data-ttu-id="614e4-112">指示可以设置读取器/写入器锁。</span><span class="sxs-lookup"><span data-stu-id="614e4-112">Indicates that a reader/writer lock can be set.</span></span>|

## <a name="requirements"></a><span data-ttu-id="614e4-113">要求</span><span class="sxs-lookup"><span data-stu-id="614e4-113">Requirements</span></span>

<span data-ttu-id="614e4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="614e4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="614e4-115">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="614e4-115">**Header:** CorHdr.h</span></span>

<span data-ttu-id="614e4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="614e4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="614e4-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="614e4-117">See also</span></span>

- [<span data-ttu-id="614e4-118">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="614e4-118">Metadata Enumerations</span></span>](metadata-enumerations.md)
