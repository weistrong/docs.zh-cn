---
description: 了解详细信息： ICorDebugClass：： GetStaticFieldValue 方法
title: ICorDebugClass::GetStaticFieldValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetStaticFieldValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetStaticFieldValue
helpviewer_keywords:
- GetStaticFieldValue method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetStaticFieldValue method [.NET Framework debugging]
ms.assetid: 56e718b4-fabd-418b-a5b3-3cc33c745683
topic_type:
- apiref
ms.openlocfilehash: a5406e44491ce89030731c35752066e4943cebfc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711513"
---
# <a name="icordebugclassgetstaticfieldvalue-method"></a><span data-ttu-id="9ece5-103">ICorDebugClass::GetStaticFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="9ece5-103">ICorDebugClass::GetStaticFieldValue Method</span></span>

<span data-ttu-id="9ece5-104">获取指定的静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="9ece5-104">Gets the value of the specified static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ece5-105">语法</span><span class="sxs-lookup"><span data-stu-id="9ece5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStaticFieldValue (  
    [in]  mdFieldDef         fieldDef,  
    [in]  ICorDebugFrame     *pFrame,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ece5-106">参数</span><span class="sxs-lookup"><span data-stu-id="9ece5-106">Parameters</span></span>  

 `fieldDef`  
 <span data-ttu-id="9ece5-107">中 `Def` 引用要检索的字段的字段标记。</span><span class="sxs-lookup"><span data-stu-id="9ece5-107">[in] A field `Def` token that references the field to be retrieved.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="9ece5-108">中指向 ICorDebugFrame 对象的指针，该对象表示要用于区分线程、上下文或应用程序域静态对象的帧。</span><span class="sxs-lookup"><span data-stu-id="9ece5-108">[in] A pointer to an ICorDebugFrame object that represents the frame to be used to disambiguate among thread, context, or application domain statics.</span></span>  
  
 <span data-ttu-id="9ece5-109">如果静态字段相对于线程、上下文或应用程序域，则该框架将确定正确的值。</span><span class="sxs-lookup"><span data-stu-id="9ece5-109">If the static field is relative to a thread, a context, or an application domain, the frame will determine the proper value.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="9ece5-110">弄指向 ICorDebugValue 对象的地址的指针，该对象表示静态字段的值。</span><span class="sxs-lookup"><span data-stu-id="9ece5-110">[out] A pointer to the address of an ICorDebugValue object that represents the value of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9ece5-111">备注</span><span class="sxs-lookup"><span data-stu-id="9ece5-111">Remarks</span></span>  

 <span data-ttu-id="9ece5-112">对于参数化类型，静态字段的值是相对于特定实例化的。</span><span class="sxs-lookup"><span data-stu-id="9ece5-112">For parameterized types, the value of a static field is relative to the particular instantiation.</span></span> <span data-ttu-id="9ece5-113">因此，如果类构造函数采用类型的参数 <xref:System.Type> ，请调用 [ICorDebugType：： GetStaticFieldValue](icordebugtype-getstaticfieldvalue-method.md) 而不是 `ICorDebugClass::GetStaticFieldValue` 。</span><span class="sxs-lookup"><span data-stu-id="9ece5-113">Therefore, if the class constructor takes parameters of type <xref:System.Type>, call [ICorDebugType::GetStaticFieldValue](icordebugtype-getstaticfieldvalue-method.md) instead of `ICorDebugClass::GetStaticFieldValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ece5-114">要求</span><span class="sxs-lookup"><span data-stu-id="9ece5-114">Requirements</span></span>  

 <span data-ttu-id="9ece5-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ece5-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ece5-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ece5-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ece5-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ece5-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ece5-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ece5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
