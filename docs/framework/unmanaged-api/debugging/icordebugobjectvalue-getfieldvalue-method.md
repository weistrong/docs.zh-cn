---
description: 了解详细信息： ICorDebugObjectValue：： GetFieldValue 方法
title: ICorDebugObjectValue::GetFieldValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue.GetFieldValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue::GetFieldValue
helpviewer_keywords:
- ICorDebugObjectValue::GetFieldValue method [.NET Framework debugging]
- GetFieldValue method [.NET Framework debugging]
ms.assetid: c96770b0-3e09-47bb-bd29-20353b043459
topic_type:
- apiref
ms.openlocfilehash: 38dac36747b286ab16ae3310b6b59695480a6ff1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722186"
---
# <a name="icordebugobjectvaluegetfieldvalue-method"></a><span data-ttu-id="eee60-103">ICorDebugObjectValue::GetFieldValue 方法</span><span class="sxs-lookup"><span data-stu-id="eee60-103">ICorDebugObjectValue::GetFieldValue Method</span></span>

<span data-ttu-id="eee60-104">获取此对象值的指定类的指定字段的值。</span><span class="sxs-lookup"><span data-stu-id="eee60-104">Gets the value of the specified field of the specified class for this object value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eee60-105">语法</span><span class="sxs-lookup"><span data-stu-id="eee60-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFieldValue (  
    [in]  ICorDebugClass     *pClass,  
    [in]  mdFieldDef         fieldDef,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eee60-106">参数</span><span class="sxs-lookup"><span data-stu-id="eee60-106">Parameters</span></span>  

 `pClass`  
 <span data-ttu-id="eee60-107">中一个指向 "ICorDebugClass" 对象的指针，该对象表示要获取其字段值的类。</span><span class="sxs-lookup"><span data-stu-id="eee60-107">[in] A pointer to an "ICorDebugClass" object that represents the class for which to get the field value.</span></span>  
  
 `fieldDef`  
 <span data-ttu-id="eee60-108">中 `mdFieldDef` 引用描述字段的元数据的令牌。</span><span class="sxs-lookup"><span data-stu-id="eee60-108">[in] An `mdFieldDef` token that references the metadata describing the field.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="eee60-109">弄一个指向 "ICorDebugValue" 对象的指针，该对象表示指定字段的值。</span><span class="sxs-lookup"><span data-stu-id="eee60-109">[out] A pointer to an "ICorDebugValue" object that represents the value of the specified field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eee60-110">备注</span><span class="sxs-lookup"><span data-stu-id="eee60-110">Remarks</span></span>  

 <span data-ttu-id="eee60-111">参数中指定的类 `pClass` 必须位于对象值的类的层次结构中，并且字段必须是该类的字段。</span><span class="sxs-lookup"><span data-stu-id="eee60-111">The class, specified in the `pClass` parameter, must be in the hierarchy of the object value's class, and the field must be a field of that class.</span></span>  
  
 <span data-ttu-id="eee60-112">`GetFieldValue`对于泛型对象和泛型类，该方法仍将成功。</span><span class="sxs-lookup"><span data-stu-id="eee60-112">The `GetFieldValue` method will still succeed for generic objects and generic classes.</span></span> <span data-ttu-id="eee60-113">例如，如果 MyDictionary \<V> 从字典继承 \<string,V> ，并且对象值的类型为 MyDictionary，则 \<int32> 传递字典的 `ICorDebugClass` 对象 \<K,V> 将成功获取字典的字段 \<string,int32> 。</span><span class="sxs-lookup"><span data-stu-id="eee60-113">For example, if MyDictionary\<V> inherits from Dictionary\<string,V>, and the object value is of type MyDictionary\<int32>, passing the `ICorDebugClass` object for Dictionary\<K,V> will successfully get a field of Dictionary\<string,int32>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eee60-114">要求</span><span class="sxs-lookup"><span data-stu-id="eee60-114">Requirements</span></span>  

 <span data-ttu-id="eee60-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eee60-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eee60-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eee60-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eee60-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eee60-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eee60-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eee60-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eee60-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="eee60-119">See also</span></span>
