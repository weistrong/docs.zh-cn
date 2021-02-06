---
description: 了解详细信息： ICorDebugProcess2：： GetVersion 方法
title: ICorDebugProcess2::GetVersion 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.GetVersion
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::GetVersion
helpviewer_keywords:
- GetVersion method, ICorDebugProcess2 interface [.NET Framework debugging]
- ICorDebugProcess2::GetVersion method [.NET Framework debugging]
ms.assetid: e11d5a75-61d9-4548-aedf-79c26079bd17
topic_type:
- apiref
ms.openlocfilehash: 8472e811ea4df1f99fb4e27b55f3561fae0c8a21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650076"
---
# <a name="icordebugprocess2getversion-method"></a><span data-ttu-id="33555-103">ICorDebugProcess2::GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="33555-103">ICorDebugProcess2::GetVersion Method</span></span>

<span data-ttu-id="33555-104">获取在此进程中运行 (CLR) 的公共语言运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="33555-104">Gets the version number of the common language runtime (CLR) that is running in this process.</span></span>

## <a name="syntax"></a><span data-ttu-id="33555-105">语法</span><span class="sxs-lookup"><span data-stu-id="33555-105">Syntax</span></span>

```cpp
HRESULT GetVersion (
    [out] COR_VERSION     *version
);
```

## <a name="parameters"></a><span data-ttu-id="33555-106">参数</span><span class="sxs-lookup"><span data-stu-id="33555-106">Parameters</span></span>

`version`\
<span data-ttu-id="33555-107">弄指向存储运行时版本号的 COR_VERSION 结构的指针。</span><span class="sxs-lookup"><span data-stu-id="33555-107">[out] A pointer to a COR_VERSION structure that stores the version number of the runtime.</span></span>

## <a name="remarks"></a><span data-ttu-id="33555-108">备注</span><span class="sxs-lookup"><span data-stu-id="33555-108">Remarks</span></span>

<span data-ttu-id="33555-109">`GetVersion`如果进程中未加载运行时，则方法将返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="33555-109">The `GetVersion` method returns an error code if no runtime has been loaded in the process.</span></span>

## <a name="requirements"></a><span data-ttu-id="33555-110">要求</span><span class="sxs-lookup"><span data-stu-id="33555-110">Requirements</span></span>

<span data-ttu-id="33555-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="33555-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="33555-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="33555-112">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="33555-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="33555-113">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="33555-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33555-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
