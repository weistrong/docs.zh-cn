---
description: 了解详细信息： ICorDebugEval：： NewObject 方法
title: ICorDebugEval::NewObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewObject
helpviewer_keywords:
- NewObject method [.NET Framework debugging]
- ICorDebugEval::NewObject method [.NET Framework debugging]
ms.assetid: ce3025e8-defa-4c5e-8298-f49d71fa5736
topic_type:
- apiref
ms.openlocfilehash: 0f7feb53d061e5dbc453015772b97f2a5a59bbb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693949"
---
# <a name="icordebugevalnewobject-method"></a><span data-ttu-id="094ce-103">ICorDebugEval::NewObject 方法</span><span class="sxs-lookup"><span data-stu-id="094ce-103">ICorDebugEval::NewObject Method</span></span>

<span data-ttu-id="094ce-104">分配一个新的对象实例，并调用指定的构造函数方法。</span><span class="sxs-lookup"><span data-stu-id="094ce-104">Allocates a new object instance and calls the specified constructor method.</span></span>  
  
 <span data-ttu-id="094ce-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="094ce-105">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="094ce-106">改 [为使用 ICorDebugEval2：： NewParameterizedObject](icordebugeval2-newparameterizedobject-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="094ce-106">Use [ICorDebugEval2::NewParameterizedObject](icordebugeval2-newparameterizedobject-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="094ce-107">语法</span><span class="sxs-lookup"><span data-stu-id="094ce-107">Syntax</span></span>  
  
```cpp  
HRESULT NewObject (  
    [in] ICorDebugFunction  *pConstructor,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="094ce-108">参数</span><span class="sxs-lookup"><span data-stu-id="094ce-108">Parameters</span></span>  

 `pConstructor`  
 <span data-ttu-id="094ce-109">中要调用的构造函数。</span><span class="sxs-lookup"><span data-stu-id="094ce-109">[in] The constructor to be called.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="094ce-110">[in] `ppArgs` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="094ce-110">[in] The size of the `ppArgs` array.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="094ce-111">中ICorDebugValue 对象的数组，其中每个对象都表示要传递给构造函数的参数。</span><span class="sxs-lookup"><span data-stu-id="094ce-111">[in] An array of ICorDebugValue objects, each of which represents an argument to be passed to the constructor.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="094ce-112">要求</span><span class="sxs-lookup"><span data-stu-id="094ce-112">Requirements</span></span>  

 <span data-ttu-id="094ce-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="094ce-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="094ce-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="094ce-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="094ce-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="094ce-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="094ce-116">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="094ce-116">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="094ce-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="094ce-117">See also</span></span>

- [<span data-ttu-id="094ce-118">NewParameterizedObject 方法</span><span class="sxs-lookup"><span data-stu-id="094ce-118">NewParameterizedObject Method</span></span>](icordebugeval2-newparameterizedobject-method.md)
