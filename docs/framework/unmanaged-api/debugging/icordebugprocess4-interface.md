---
description: 了解详细信息： ICorDebugProcess4 接口
title: ICorDebugProcess4 接口
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4
helpviewer_keywords:
- ICorDebugProcess4 interface [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 16c7f3fbd1a79b1406fe0c19a9d922964667a2a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649983"
---
# <a name="icordebugprocess4-interface"></a><span data-ttu-id="bcb63-103">ICorDebugProcess4 接口</span><span class="sxs-lookup"><span data-stu-id="bcb63-103">ICorDebugProcess4 Interface</span></span>

<span data-ttu-id="bcb63-104">为进程外执行控制提供支持。</span><span class="sxs-lookup"><span data-stu-id="bcb63-104">Provides support for out of process execution control.</span></span>

## <a name="methods"></a><span data-ttu-id="bcb63-105">方法</span><span class="sxs-lookup"><span data-stu-id="bcb63-105">Methods</span></span>

| <span data-ttu-id="bcb63-106">方法</span><span class="sxs-lookup"><span data-stu-id="bcb63-106">Method</span></span>                                                                 | <span data-ttu-id="bcb63-107">说明</span><span class="sxs-lookup"><span data-stu-id="bcb63-107">Description</span></span>                                                                                             |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="bcb63-108">ProcessStateChanged</span><span class="sxs-lookup"><span data-stu-id="bcb63-108">ProcessStateChanged</span></span>](icordebugprocess4-processstatechanged-method.md) | <span data-ttu-id="bcb63-109">通知 ICorDebug 管道进程外调试器正在继续执行调试对象的执行。</span><span class="sxs-lookup"><span data-stu-id="bcb63-109">Notifies the ICorDebug pipeline that the out of process debugger is continuing the debugee's execution.</span></span> |

## <a name="remarks"></a><span data-ttu-id="bcb63-110">备注</span><span class="sxs-lookup"><span data-stu-id="bcb63-110">Remarks</span></span>

<span data-ttu-id="bcb63-111">此接口在运行时中存在，不会通过任何标头或库文件公开。</span><span class="sxs-lookup"><span data-stu-id="bcb63-111">This interface lives inside the runtime and isn't exposed through any headers or library files.</span></span> <span data-ttu-id="bcb63-112">但是，它是从使用 GUID 派生的 COM 接口， `IUnknown` `E930C679-78AF-4953-8AB7-B0AABF0F9F80` 该接口可通过常用的 COM 机制获得。</span><span class="sxs-lookup"><span data-stu-id="bcb63-112">However, it's a COM interface that derives from `IUnknown` with GUID `E930C679-78AF-4953-8AB7-B0AABF0F9F80` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb63-113">要求</span><span class="sxs-lookup"><span data-stu-id="bcb63-113">Requirements</span></span>

<span data-ttu-id="bcb63-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bcb63-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="bcb63-115">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="bcb63-115">**Header:** None</span></span>

<span data-ttu-id="bcb63-116">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="bcb63-116">**Library:** None</span></span>

<span data-ttu-id="bcb63-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcb63-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="bcb63-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="bcb63-118">See also</span></span>

- [<span data-ttu-id="bcb63-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="bcb63-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="bcb63-120">调试</span><span class="sxs-lookup"><span data-stu-id="bcb63-120">Debugging</span></span>](index.md)
