---
description: 了解详细信息： ICorDebugModule：： GetClassFromToken 方法
title: ICorDebugModule::GetClassFromToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetClassFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetClassFromToken
helpviewer_keywords:
- GetClassFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetClassFromToken method [.NET Framework debugging]
ms.assetid: 622a4d3c-0425-4c54-a7e4-0735377cdad2
topic_type:
- apiref
ms.openlocfilehash: 8184c6c1920a4397c4037160276b5b86033baf71
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722604"
---
# <a name="icordebugmodulegetclassfromtoken-method"></a><span data-ttu-id="eda33-103">ICorDebugModule::GetClassFromToken 方法</span><span class="sxs-lookup"><span data-stu-id="eda33-103">ICorDebugModule::GetClassFromToken Method</span></span>

<span data-ttu-id="eda33-104">获取元数据标记指定的类。</span><span class="sxs-lookup"><span data-stu-id="eda33-104">Gets the class specified by the metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eda33-105">语法</span><span class="sxs-lookup"><span data-stu-id="eda33-105">Syntax</span></span>  
  
```cpp  
HRESULT GetClassFromToken(  
    [in]  mdTypeDef        typeDef,  
    [out] ICorDebugClass **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eda33-106">参数</span><span class="sxs-lookup"><span data-stu-id="eda33-106">Parameters</span></span>  

 `typedef`  
 <span data-ttu-id="eda33-107">中 `mdTypeDef` 引用类的元数据的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="eda33-107">[in] An `mdTypeDef` metadata token that references the metadata of a class.</span></span>  
  
 `ppClass`  
 <span data-ttu-id="eda33-108">弄指向表示类的 ICorDebugClass 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="eda33-108">[out] A pointer to the address of an ICorDebugClass object that represents the class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eda33-109">要求</span><span class="sxs-lookup"><span data-stu-id="eda33-109">Requirements</span></span>  

 <span data-ttu-id="eda33-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eda33-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eda33-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eda33-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eda33-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eda33-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eda33-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eda33-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
