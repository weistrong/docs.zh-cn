---
description: 了解详细信息： ICorDebugType：： GetStaticFieldValue 方法
title: ICorDebugType::GetStaticFieldValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetStaticFieldValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetStaticFieldValue
helpviewer_keywords:
- GetStaticFieldValue method, ICorDebugType interface [.NET Framework debugging]
- ICorDebugType::GetStaticFieldValue method [.NET Framework debugging]
ms.assetid: 62eb5d55-53ee-4fb3-8d47-7b6c96808f9e
topic_type:
- apiref
ms.openlocfilehash: 378c72f24fedd76f40704ff684781bed124055bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658225"
---
# <a name="icordebugtypegetstaticfieldvalue-method"></a><span data-ttu-id="9cca8-103">ICorDebugType::GetStaticFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="9cca8-103">ICorDebugType::GetStaticFieldValue Method</span></span>

<span data-ttu-id="9cca8-104">获取一个指向 ICorDebugValue 对象的接口指针，该对象包含指定的堆栈帧中指定字段标记所引用的静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="9cca8-104">Gets an interface pointer to an ICorDebugValue object that contains the value of the static field referenced by the specified field token in the specified stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cca8-105">语法</span><span class="sxs-lookup"><span data-stu-id="9cca8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStaticFieldValue (  
    [in]  mdFieldDef        fieldDef,  
    [in]  ICorDebugFrame    *pFrame,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9cca8-106">参数</span><span class="sxs-lookup"><span data-stu-id="9cca8-106">Parameters</span></span>  

 `fieldDef`  
 <span data-ttu-id="9cca8-107">中 `mdFieldDef` 指定静态字段的标记。</span><span class="sxs-lookup"><span data-stu-id="9cca8-107">[in] An `mdFieldDef` token that specifies the static field.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="9cca8-108">中指向表示堆栈帧的 ICorDebugFrame 的指针。</span><span class="sxs-lookup"><span data-stu-id="9cca8-108">[in] A pointer to an ICorDebugFrame that represents the stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="9cca8-109">弄指向的地址的指针 `ICorDebugValue` ，该地址包含静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="9cca8-109">[out] A pointer to the address of an `ICorDebugValue` that contains the value of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9cca8-110">备注</span><span class="sxs-lookup"><span data-stu-id="9cca8-110">Remarks</span></span>  

 <span data-ttu-id="9cca8-111">`GetStaticFieldValue`仅当类型是 ELEMENT_TYPE_CLASS 或 ELEMENT_TYPE_VALUETYPE 时，才可以使用方法，如[ICorDebugType：： GetType](icordebugtype-gettype-method.md)方法所示。</span><span class="sxs-lookup"><span data-stu-id="9cca8-111">The `GetStaticFieldValue` method may be used only if the type is ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE, as indicated by the [ICorDebugType::GetType](icordebugtype-gettype-method.md) method.</span></span>  
  
 <span data-ttu-id="9cca8-112">对于非泛型类型，执行的操作与 `GetStaticFieldValue` 对[ICorDebugType：： GetClass](icordebugtype-getclass-method.md)返回的 ICorDebugClass 对象调用[ICorDebugClass：： GetStaticFieldValue](icordebugclass-getstaticfieldvalue-method.md)相同。</span><span class="sxs-lookup"><span data-stu-id="9cca8-112">For non-generic types, the operation performed by `GetStaticFieldValue` is identical to calling [ICorDebugClass::GetStaticFieldValue](icordebugclass-getstaticfieldvalue-method.md) on the ICorDebugClass object that is returned by [ICorDebugType::GetClass](icordebugtype-getclass-method.md).</span></span>  
  
 <span data-ttu-id="9cca8-113">对于泛型类型，静态字段值将与特定实例化相关。</span><span class="sxs-lookup"><span data-stu-id="9cca8-113">For generic types, a static field value will be relative to a particular instantiation.</span></span> <span data-ttu-id="9cca8-114">此外，如果静态字段可能是相对于线程、上下文或应用程序域的，则堆栈帧将有助于调试器确定正确的值。</span><span class="sxs-lookup"><span data-stu-id="9cca8-114">Also, if the static field could possibly be relative to a thread, a context, or an application domain, then the stack frame will help the debugger determine the proper value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9cca8-115">备注</span><span class="sxs-lookup"><span data-stu-id="9cca8-115">Remarks</span></span>  

 <span data-ttu-id="9cca8-116">`GetStaticFieldValue` 仅当对的调用 `ICorDebugType::GetType` 返回 ELEMENT_TYPE_CLASS 或 ELEMENT_TYPE_VALUETYPE 的值时才可使用。</span><span class="sxs-lookup"><span data-stu-id="9cca8-116">`GetStaticFieldValue` can be used only when a call to `ICorDebugType::GetType` returns a value of ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cca8-117">要求</span><span class="sxs-lookup"><span data-stu-id="9cca8-117">Requirements</span></span>  

 <span data-ttu-id="9cca8-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9cca8-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cca8-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9cca8-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9cca8-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9cca8-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9cca8-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cca8-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
