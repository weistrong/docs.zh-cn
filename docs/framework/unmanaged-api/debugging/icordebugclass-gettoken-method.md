---
description: 了解详细信息： ICorDebugClass：： GetToken 方法
title: ICorDebugClass::GetToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetToken
helpviewer_keywords:
- GetToken method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetToken method [.NET Framework debugging]
ms.assetid: ee5c848a-eac4-4462-b07a-07ccd76a75df
topic_type:
- apiref
ms.openlocfilehash: f87b71800410fc3a95790e6d35cf4bd10a5ce747
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711517"
---
# <a name="icordebugclassgettoken-method"></a><span data-ttu-id="24bfa-103">ICorDebugClass::GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="24bfa-103">ICorDebugClass::GetToken Method</span></span>

<span data-ttu-id="24bfa-104">获取 `TypeDef` 引用此类的定义的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="24bfa-104">Gets the `TypeDef` metadata token that references the definition of this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24bfa-105">语法</span><span class="sxs-lookup"><span data-stu-id="24bfa-105">Syntax</span></span>  
  
```cpp  
HRESULT GetToken (  
    [out] mdTypeDef          *pTypeDef  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="24bfa-106">参数</span><span class="sxs-lookup"><span data-stu-id="24bfa-106">Parameters</span></span>  

 `pTypeDef`  
 <span data-ttu-id="24bfa-107">弄指向 `mdTypeDef` 引用此类的定义的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="24bfa-107">[out] A pointer to an `mdTypeDef` token that references the definition of this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24bfa-108">要求</span><span class="sxs-lookup"><span data-stu-id="24bfa-108">Requirements</span></span>  

 <span data-ttu-id="24bfa-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24bfa-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24bfa-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24bfa-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24bfa-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24bfa-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="24bfa-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24bfa-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24bfa-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="24bfa-113">See also</span></span>

- [<span data-ttu-id="24bfa-114">元数据接口</span><span class="sxs-lookup"><span data-stu-id="24bfa-114">Metadata Interfaces</span></span>](../metadata/metadata-interfaces.md)
