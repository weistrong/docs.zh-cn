---
description: 了解详细信息： ICorDebugEval：： CallFunction 方法
title: ICorDebugEval::CallFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CallFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CallFunction
helpviewer_keywords:
- ICorDebugEval::CallFunction method [.NET Framework debugging]
- CallFunction method [.NET Framework debugging]
ms.assetid: 7f470c5c-e1c0-4d8d-aad8-830f113ae751
topic_type:
- apiref
ms.openlocfilehash: c0978ab3bdffc83e3eb5e3a6553e7f374ab6d5da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694183"
---
# <a name="icordebugevalcallfunction-method"></a><span data-ttu-id="3d6b7-103">ICorDebugEval::CallFunction 方法</span><span class="sxs-lookup"><span data-stu-id="3d6b7-103">ICorDebugEval::CallFunction Method</span></span>

<span data-ttu-id="3d6b7-104">设置对指定函数的调用。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-104">Sets up a call to the specified function.</span></span>

<span data-ttu-id="3d6b7-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-105">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="3d6b7-106">改 [为使用 ICorDebugEval2：： CallParameterizedFunction](icordebugeval2-callparameterizedfunction-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-106">Use [ICorDebugEval2::CallParameterizedFunction](icordebugeval2-callparameterizedfunction-method.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6b7-107">语法</span><span class="sxs-lookup"><span data-stu-id="3d6b7-107">Syntax</span></span>

```cpp
HRESULT CallFunction (
    [in] ICorDebugFunction  *pFunction,
    [in] ULONG32            nArgs,
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]
);
```

## <a name="parameters"></a><span data-ttu-id="3d6b7-108">参数</span><span class="sxs-lookup"><span data-stu-id="3d6b7-108">Parameters</span></span>

`pFunction`\
<span data-ttu-id="3d6b7-109">中指向 ICorDebugFunction 对象的指针，该对象指定要调用的函数。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-109">[in] Pointer to an ICorDebugFunction object that specifies the function to be called.</span></span>

`nArgs`\
<span data-ttu-id="3d6b7-110">中函数的参数数目。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-110">[in] The number of arguments for the function.</span></span>

`ppArgs`\
<span data-ttu-id="3d6b7-111">中指针的数组，其中每个都指向一个 ICorDebugValue 对象，该对象指定要传递给函数的参数。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-111">[in] An array of pointers, each of which points to an ICorDebugValue object that specifies an argument to be passed to the function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6b7-112">备注</span><span class="sxs-lookup"><span data-stu-id="3d6b7-112">Remarks</span></span>

<span data-ttu-id="3d6b7-113">如果该函数是虚拟的， `CallFunction` 将执行虚拟调度。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-113">If the function is virtual, `CallFunction` will perform virtual dispatch.</span></span> <span data-ttu-id="3d6b7-114">如果该函数在不同的应用程序域中，只要所有参数也在该应用程序域中，就会发生转换。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-114">If the function is in a different application domain, a transition will occur as long as all arguments are also in that application domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6b7-115">要求</span><span class="sxs-lookup"><span data-stu-id="3d6b7-115">Requirements</span></span>

<span data-ttu-id="3d6b7-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3d6b7-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="3d6b7-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3d6b7-117">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="3d6b7-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3d6b7-118">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="3d6b7-119">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="3d6b7-119">**.NET Framework Versions:** 1.1, 1.0</span></span>

## <a name="see-also"></a><span data-ttu-id="3d6b7-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="3d6b7-120">See also</span></span>

- [<span data-ttu-id="3d6b7-121">CallParameterizedFunction 方法</span><span class="sxs-lookup"><span data-stu-id="3d6b7-121">CallParameterizedFunction Method</span></span>](icordebugeval2-callparameterizedfunction-method.md)
