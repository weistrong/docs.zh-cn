---
description: 了解详细信息： ICorDebugEval2：： NewParameterizedObject 方法
title: ICorDebugEval2::NewParameterizedObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewParameterizedObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewParameterizedObject
helpviewer_keywords:
- NewParameterizedObject method [.NET Framework debugging]
- ICorDebugEval2::NewParameterizedObject method [.NET Framework debugging]
ms.assetid: 3d705463-e640-4249-8036-4e8206d03cfe
topic_type:
- apiref
ms.openlocfilehash: 2dc746fdada0e79044a1387bd4cb1c11b81d7777
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693676"
---
# <a name="icordebugeval2newparameterizedobject-method"></a><span data-ttu-id="f7381-103">ICorDebugEval2::NewParameterizedObject 方法</span><span class="sxs-lookup"><span data-stu-id="f7381-103">ICorDebugEval2::NewParameterizedObject Method</span></span>

<span data-ttu-id="f7381-104">实例化一个新的参数化类型对象，并调用该对象的构造函数方法。</span><span class="sxs-lookup"><span data-stu-id="f7381-104">Instantiates a new parameterized type object and calls the object's constructor method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7381-105">语法</span><span class="sxs-lookup"><span data-stu-id="f7381-105">Syntax</span></span>  
  
```cpp  
HRESULT NewParameterizedObject (  
    [in] ICorDebugFunction     *pConstructor,  
    [in] ULONG32               nTypeArgs,  
    [in, size_is(nTypeArgs)] ICorDebugType *ppTypeArgs[],  
    [in] ULONG32               nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f7381-106">参数</span><span class="sxs-lookup"><span data-stu-id="f7381-106">Parameters</span></span>  

 `pConstructor`  
 <span data-ttu-id="f7381-107">中指向 ICorDebugFunction 对象的指针，该对象表示要实例化的对象的构造函数。</span><span class="sxs-lookup"><span data-stu-id="f7381-107">[in] A pointer to an ICorDebugFunction object that represents the constructor of the object to be instantiated.</span></span>  
  
 `nTypeArgs`  
 <span data-ttu-id="f7381-108">中传递的类型参数的数目。</span><span class="sxs-lookup"><span data-stu-id="f7381-108">[in] The number of type arguments passed.</span></span>  
  
 `ppTypeArgs`  
 <span data-ttu-id="f7381-109">中指针的数组，其中每个都指向一个 ICorDebugType 对象，该对象表示要实例化的对象的类型参数。</span><span class="sxs-lookup"><span data-stu-id="f7381-109">[in] An array of pointers, each of which points to an ICorDebugType object that represents a type argument for the object that is being instantiated.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="f7381-110">中传递给构造函数的参数的数目。</span><span class="sxs-lookup"><span data-stu-id="f7381-110">[in] The number of arguments passed to the constructor.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="f7381-111">中指针的数组，其中每个都指向表示传递给构造函数的参数值的 ICorDebugValue 对象。</span><span class="sxs-lookup"><span data-stu-id="f7381-111">[in] An array of pointers, each of which points to an ICorDebugValue object that represents an argument value that is passed to the constructor.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f7381-112">备注</span><span class="sxs-lookup"><span data-stu-id="f7381-112">Remarks</span></span>  

 <span data-ttu-id="f7381-113">对象的构造函数可以接受 <xref:System.Type> 参数。</span><span class="sxs-lookup"><span data-stu-id="f7381-113">The object's constructor may take <xref:System.Type> parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7381-114">要求</span><span class="sxs-lookup"><span data-stu-id="f7381-114">Requirements</span></span>  

 <span data-ttu-id="f7381-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f7381-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7381-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f7381-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f7381-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f7381-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f7381-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7381-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
