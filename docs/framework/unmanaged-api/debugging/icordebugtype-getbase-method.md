---
description: 了解详细信息： ICorDebugType：： GetBase 方法
title: ICorDebugType::GetBase 方法
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetBase
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetBase
helpviewer_keywords:
- ICorDebugType::GetBase method [.NET Framework debugging]
- GetBase method [.NET Framework debugging]
ms.assetid: f24e1af9-c220-4f79-ae62-4153ec17ea81
topic_type:
- apiref
ms.openlocfilehash: 78cd540974b540b704e946f6c723214d72e89ab4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658381"
---
# <a name="icordebugtypegetbase-method"></a><span data-ttu-id="0dfe1-103">ICorDebugType::GetBase 方法</span><span class="sxs-lookup"><span data-stu-id="0dfe1-103">ICorDebugType::GetBase Method</span></span>

<span data-ttu-id="0dfe1-104">获取一个接口指针，该指针指向表示此所表示的类型的基类型（如果存在）的 ICorDebugType `ICorDebugType` 。</span><span class="sxs-lookup"><span data-stu-id="0dfe1-104">Gets an interface pointer to an ICorDebugType that represents the base type, if one exists, of the type represented by this `ICorDebugType`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0dfe1-105">语法</span><span class="sxs-lookup"><span data-stu-id="0dfe1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBase (  
    [out] ICorDebugType   **pBase  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0dfe1-106">参数</span><span class="sxs-lookup"><span data-stu-id="0dfe1-106">Parameters</span></span>  

 `pBase`  
 <span data-ttu-id="0dfe1-107">弄指向 `ICorDebugType` 表示基类型的对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="0dfe1-107">[out] A pointer to the address of an `ICorDebugType` object that represents the base type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0dfe1-108">备注</span><span class="sxs-lookup"><span data-stu-id="0dfe1-108">Remarks</span></span>  

 <span data-ttu-id="0dfe1-109">查找类型的基类型对于实现常见调试器功能非常有用，例如打印对象或其父类的所有字段。</span><span class="sxs-lookup"><span data-stu-id="0dfe1-109">Looking up the base type for a type is useful to implement common debugger functionality, such as printing out all the fields of an object or its parent classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0dfe1-110">要求</span><span class="sxs-lookup"><span data-stu-id="0dfe1-110">Requirements</span></span>  

 <span data-ttu-id="0dfe1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0dfe1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0dfe1-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0dfe1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0dfe1-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0dfe1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0dfe1-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0dfe1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
