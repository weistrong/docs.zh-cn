---
description: 了解详细信息： ICorDebugAssembly：： EnumerateModules 方法
title: ICorDebugAssembly::EnumerateModules 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.EnumerateModules
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::EnumerateModules
helpviewer_keywords:
- ICorDebugAssembly::EnumerateModules method [.NET Framework debugging]
- EnumerateModules method [.NET Framework debugging]
ms.assetid: c7ba51a1-0dd5-4452-b471-232febe0f897
topic_type:
- apiref
ms.openlocfilehash: 5d34fb1762e8f953007d6fcb59ab1147028f06a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722849"
---
# <a name="icordebugassemblyenumeratemodules-method"></a><span data-ttu-id="7de8b-103">ICorDebugAssembly::EnumerateModules 方法</span><span class="sxs-lookup"><span data-stu-id="7de8b-103">ICorDebugAssembly::EnumerateModules Method</span></span>

<span data-ttu-id="7de8b-104">获取中包含的模块的枚举器 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="7de8b-104">Gets an enumerator for the modules contained in the `ICorDebugAssembly`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7de8b-105">语法</span><span class="sxs-lookup"><span data-stu-id="7de8b-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateModules (  
    [out] ICorDebugModuleEnum **ppModules  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7de8b-106">参数</span><span class="sxs-lookup"><span data-stu-id="7de8b-106">Parameters</span></span>  

 `ppModules`  
 <span data-ttu-id="7de8b-107">弄一个指针，指向作为枚举器的 ICorDebugModuleEnum 接口的地址。</span><span class="sxs-lookup"><span data-stu-id="7de8b-107">[out] A pointer to the address of the ICorDebugModuleEnum interface that is the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7de8b-108">要求</span><span class="sxs-lookup"><span data-stu-id="7de8b-108">Requirements</span></span>  

 <span data-ttu-id="7de8b-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7de8b-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7de8b-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7de8b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7de8b-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7de8b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7de8b-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7de8b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
