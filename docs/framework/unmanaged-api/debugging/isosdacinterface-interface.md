---
description: 了解详细信息： ISOSDacInterface 接口
title: ISOSDacInterface 接口
ms.date: 02/01/2019
api.name:
- ISOSDacInterface Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface Interface
helpviewer.keywords:
- ISOSDacInterface Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ddb99b7c6fca6870024f04933861d01e4b31ea9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790394"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="fee8c-103">ISOSDacInterface 接口</span><span class="sxs-lookup"><span data-stu-id="fee8c-103">ISOSDacInterface Interface</span></span>

<span data-ttu-id="fee8c-104">提供用于访问中的数据的帮助器方法 `SOS` 。</span><span class="sxs-lookup"><span data-stu-id="fee8c-104">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="fee8c-105">方法</span><span class="sxs-lookup"><span data-stu-id="fee8c-105">Methods</span></span>

| <span data-ttu-id="fee8c-106">方法</span><span class="sxs-lookup"><span data-stu-id="fee8c-106">Method</span></span>                                                                                                               | <span data-ttu-id="fee8c-107">说明</span><span class="sxs-lookup"><span data-stu-id="fee8c-107">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="fee8c-108">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="fee8c-108">GetMethodDescData</span></span>](isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="fee8c-109">获取给定 MethodDesc 指针的数据。</span><span class="sxs-lookup"><span data-stu-id="fee8c-109">Gets the data for the given MethodDesc pointer.</span></span> |
| [<span data-ttu-id="fee8c-110">GetMethodDescPtrFromIP</span><span class="sxs-lookup"><span data-stu-id="fee8c-110">GetMethodDescPtrFromIP</span></span>](isosdacinterface-getmethoddescptrfromip-method.md) | <span data-ttu-id="fee8c-111">检索与包含给定本机指令地址的方法相对应的 MethodDesc 的指针。</span><span class="sxs-lookup"><span data-stu-id="fee8c-111">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span> |
| [<span data-ttu-id="fee8c-112">GetModuleData</span><span class="sxs-lookup"><span data-stu-id="fee8c-112">GetModuleData</span></span>](isosdacinterface-getmoduledata-method.md)| <span data-ttu-id="fee8c-113">提取与在给定地址加载的模块对应的数据。</span><span class="sxs-lookup"><span data-stu-id="fee8c-113">Fetches the data corresponding to the module loaded at a given address.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fee8c-114">备注</span><span class="sxs-lookup"><span data-stu-id="fee8c-114">Remarks</span></span>

<span data-ttu-id="fee8c-115">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="fee8c-115">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="fee8c-116">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `436f00f2-b42a-4b9f-870c-e73db66ae930` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="fee8c-116">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee8c-117">要求</span><span class="sxs-lookup"><span data-stu-id="fee8c-117">Requirements</span></span>

<span data-ttu-id="fee8c-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fee8c-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
<span data-ttu-id="fee8c-119">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="fee8c-119">**Header:** None</span></span>  
<span data-ttu-id="fee8c-120">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="fee8c-120">**Library:** None</span></span>  
<span data-ttu-id="fee8c-121">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="fee8c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="fee8c-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fee8c-122">See also</span></span>

- [<span data-ttu-id="fee8c-123">调试</span><span class="sxs-lookup"><span data-stu-id="fee8c-123">Debugging</span></span>](index.md)
- [<span data-ttu-id="fee8c-124">调试接口</span><span class="sxs-lookup"><span data-stu-id="fee8c-124">Debugging Interfaces</span></span>](debugging-interfaces.md)
