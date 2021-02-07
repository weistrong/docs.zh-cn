---
description: 了解详细信息： ICorDebugEval：： NewObjectNoConstructor 方法
title: ICorDebugEval::NewObjectNoConstructor 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewObjectNoConstructor
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewObjectNoConstructor
helpviewer_keywords:
- NewObjectNoConstructor method [.NET Framework debugging]
- ICorDebugEval::NewObjectNoConstructor method [.NET Framework debugging]
ms.assetid: 80d509ca-b5e3-4c46-9c14-800db73d9bf7
topic_type:
- apiref
ms.openlocfilehash: 4bc8f95da1a554091052dc7e7f49aef4f494578d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693806"
---
# <a name="icordebugevalnewobjectnoconstructor-method"></a><span data-ttu-id="9a9ef-103">ICorDebugEval::NewObjectNoConstructor 方法</span><span class="sxs-lookup"><span data-stu-id="9a9ef-103">ICorDebugEval::NewObjectNoConstructor Method</span></span>

<span data-ttu-id="9a9ef-104">分配指定类型的新对象实例，而不尝试调用构造函数方法。</span><span class="sxs-lookup"><span data-stu-id="9a9ef-104">Allocates a new object instance of the specified type, without attempting to call a constructor method.</span></span>  
  
 <span data-ttu-id="9a9ef-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="9a9ef-105">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="9a9ef-106">改 [为使用 ICorDebugEval2：： NewParameterizedObjectNoConstructor](icordebugeval2-newparameterizedobjectnoconstructor-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a9ef-106">Use [ICorDebugEval2::NewParameterizedObjectNoConstructor](icordebugeval2-newparameterizedobjectnoconstructor-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a9ef-107">语法</span><span class="sxs-lookup"><span data-stu-id="9a9ef-107">Syntax</span></span>  
  
```cpp  
HRESULT NewObjectNoConstructor (  
    [in] ICorDebugClass     *pClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a9ef-108">参数</span><span class="sxs-lookup"><span data-stu-id="9a9ef-108">Parameters</span></span>  

 `pClass`  
 <span data-ttu-id="9a9ef-109">中指向 ICorDebugClass 对象的指针，该对象表示要实例化的对象的类型。</span><span class="sxs-lookup"><span data-stu-id="9a9ef-109">[in] Pointer to an ICorDebugClass object that represents the type of object to be instantiated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a9ef-110">要求</span><span class="sxs-lookup"><span data-stu-id="9a9ef-110">Requirements</span></span>  

 <span data-ttu-id="9a9ef-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9a9ef-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a9ef-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9a9ef-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9a9ef-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9a9ef-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9a9ef-114">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="9a9ef-114">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a9ef-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a9ef-115">See also</span></span>

- [<span data-ttu-id="9a9ef-116">NewParameterizedObjectNoConstructor 方法</span><span class="sxs-lookup"><span data-stu-id="9a9ef-116">NewParameterizedObjectNoConstructor Method</span></span>](icordebugeval2-newparameterizedobjectnoconstructor-method.md)
