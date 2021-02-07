---
description: 了解详细信息： ICorDebugModule：： GetGlobalVariableValue 方法
title: ICorDebugModule::GetGlobalVariableValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetGlobalVariableValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetGlobalVariableValue
helpviewer_keywords:
- ICorDebugModule::GetGlobalVariableValue method [.NET Framework debugging]
- GetGlobalVariableValue method [.NET Framework debugging]
ms.assetid: bbc0881c-6a59-41a0-b5ee-2f3d1b71684c
topic_type:
- apiref
ms.openlocfilehash: a4efe2f56387be7351fd5bc16716bcd1f34f7d7a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691661"
---
# <a name="icordebugmodulegetglobalvariablevalue-method"></a><span data-ttu-id="1e032-103">ICorDebugModule::GetGlobalVariableValue 方法</span><span class="sxs-lookup"><span data-stu-id="1e032-103">ICorDebugModule::GetGlobalVariableValue Method</span></span>

<span data-ttu-id="1e032-104">获取指定全局变量的值。</span><span class="sxs-lookup"><span data-stu-id="1e032-104">Gets the value of the specified global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e032-105">语法</span><span class="sxs-lookup"><span data-stu-id="1e032-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGlobalVariableValue(  
    [in]  mdFieldDef      fieldDef,  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e032-106">参数</span><span class="sxs-lookup"><span data-stu-id="1e032-106">Parameters</span></span>  

 `fieldDef`  
 <span data-ttu-id="1e032-107">中 `mdFieldDef` 引用描述全局变量的元数据的令牌。</span><span class="sxs-lookup"><span data-stu-id="1e032-107">[in] An `mdFieldDef` token that references the metadata describing the global variable.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="1e032-108">弄指向 ICorDebugValue 对象的地址的指针，该对象表示指定的全局变量的值。</span><span class="sxs-lookup"><span data-stu-id="1e032-108">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified global variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e032-109">要求</span><span class="sxs-lookup"><span data-stu-id="1e032-109">Requirements</span></span>  

 <span data-ttu-id="1e032-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1e032-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e032-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1e032-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1e032-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1e032-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1e032-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e032-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
