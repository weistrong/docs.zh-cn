---
description: 了解详细信息： IXCLRDataModule 接口
title: IXCLRDataModule 接口
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 403d4dd3db64f2855347562da7217a3562985c7d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800742"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="6d9df-103">IXCLRDataModule 接口</span><span class="sxs-lookup"><span data-stu-id="6d9df-103">IXCLRDataModule Interface</span></span>

<span data-ttu-id="6d9df-104">提供用于查询有关已加载模块的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="6d9df-104">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="6d9df-105">方法</span><span class="sxs-lookup"><span data-stu-id="6d9df-105">Methods</span></span>

| <span data-ttu-id="6d9df-106">方法</span><span class="sxs-lookup"><span data-stu-id="6d9df-106">Method</span></span>                                                                                                                                | <span data-ttu-id="6d9df-107">说明</span><span class="sxs-lookup"><span data-stu-id="6d9df-107">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="6d9df-108">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="6d9df-108">GetMethodDefinitionByToken</span></span>](ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="6d9df-109">获取对应于给定元数据标记的方法定义。</span><span class="sxs-lookup"><span data-stu-id="6d9df-109">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="6d9df-110">请求</span><span class="sxs-lookup"><span data-stu-id="6d9df-110">Request</span></span>](ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="6d9df-111">请求填充模块数据所提供的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="6d9df-111">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="6d9df-112">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="6d9df-112">GetVersionId</span></span>](ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="6d9df-113">获取模块的版本 ID。</span><span class="sxs-lookup"><span data-stu-id="6d9df-113">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="6d9df-114">备注</span><span class="sxs-lookup"><span data-stu-id="6d9df-114">Remarks</span></span>

<span data-ttu-id="6d9df-115">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="6d9df-115">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="6d9df-116">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="6d9df-116">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9df-117">要求</span><span class="sxs-lookup"><span data-stu-id="6d9df-117">Requirements</span></span>

<span data-ttu-id="6d9df-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6d9df-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="6d9df-119">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="6d9df-119">**Header:** None</span></span>  
<span data-ttu-id="6d9df-120">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="6d9df-120">**Library:** None</span></span>  
<span data-ttu-id="6d9df-121">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6d9df-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d9df-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d9df-122">See also</span></span>

- [<span data-ttu-id="6d9df-123">调试</span><span class="sxs-lookup"><span data-stu-id="6d9df-123">Debugging</span></span>](index.md)
- [<span data-ttu-id="6d9df-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="6d9df-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
