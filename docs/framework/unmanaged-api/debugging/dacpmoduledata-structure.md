---
description: 了解详细信息： DacpModuleData 结构
title: DacpModuleData 结构
ms.date: 02/01/2019
api.name:
- DacpModuleData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpModuleData Structure
helpviewer.keywords:
- DacpModuleData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 376a49ab78db08e5906e8d33389cdc45fe76e81e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661566"
---
# <a name="dacpmoduledata-structure"></a><span data-ttu-id="db236-103">DacpModuleData 结构</span><span class="sxs-lookup"><span data-stu-id="db236-103">DacpModuleData Structure</span></span>

<span data-ttu-id="db236-104">定义模块的运行时信息的传输缓冲区。</span><span class="sxs-lookup"><span data-stu-id="db236-104">Defines a transport buffer for a module's runtime information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="db236-105">语法</span><span class="sxs-lookup"><span data-stu-id="db236-105">Syntax</span></span>

```cpp
struct DacpModuleData
{
    CLRDATA_ADDRESS Address;
    CLRDATA_ADDRESS File;
    CLRDATA_ADDRESS  ilBase;
    char payLoad[132];
};
```

## <a name="members"></a><span data-ttu-id="db236-106">成员</span><span class="sxs-lookup"><span data-stu-id="db236-106">Members</span></span>

| <span data-ttu-id="db236-107">成员</span><span class="sxs-lookup"><span data-stu-id="db236-107">Member</span></span>    | <span data-ttu-id="db236-108">说明</span><span class="sxs-lookup"><span data-stu-id="db236-108">Description</span></span>                                                             |
| --------- | ----------------------------------------------------------------------- |
| `Address` | <span data-ttu-id="db236-109">Module 对象的地址。</span><span class="sxs-lookup"><span data-stu-id="db236-109">Address of the module object.</span></span>                                           |
| `File`    | <span data-ttu-id="db236-110">指向可移植可执行文件 (PE) 文件的指针。</span><span class="sxs-lookup"><span data-stu-id="db236-110">A pointer to the portable executable (PE) file.</span></span>                       |
| `ilBase`  | <span data-ttu-id="db236-111">加载的映像的基址。</span><span class="sxs-lookup"><span data-stu-id="db236-111">The address of the loaded image's base.</span></span>                                 |
| `payLoad` | <span data-ttu-id="db236-112">运行时使用的其他模块信息的负载缓冲区。</span><span class="sxs-lookup"><span data-stu-id="db236-112">A payload buffer for additional module information used by the runtime.</span></span> |

## <a name="remarks"></a><span data-ttu-id="db236-113">备注</span><span class="sxs-lookup"><span data-stu-id="db236-113">Remarks</span></span>

<span data-ttu-id="db236-114">此结构存在于运行时中，并且不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="db236-114">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="db236-115">若要使用它，请定义上面指定的结构。</span><span class="sxs-lookup"><span data-stu-id="db236-115">To use it, define the structure as specified above.</span></span>

## <a name="requirements"></a><span data-ttu-id="db236-116">要求</span><span class="sxs-lookup"><span data-stu-id="db236-116">Requirements</span></span>

<span data-ttu-id="db236-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db236-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="db236-118">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="db236-118">**Header:** None</span></span>  
<span data-ttu-id="db236-119">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="db236-119">**Library:** None</span></span>  
<span data-ttu-id="db236-120">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="db236-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="db236-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="db236-121">See also</span></span>

- [<span data-ttu-id="db236-122">调试</span><span class="sxs-lookup"><span data-stu-id="db236-122">Debugging</span></span>](index.md)
- [<span data-ttu-id="db236-123">调试结构</span><span class="sxs-lookup"><span data-stu-id="db236-123">Debugging Structures</span></span>](debugging-structures.md)
