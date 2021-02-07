---
description: 了解详细信息： ICorDebugAssembly：： GetAppDomain 方法
title: ICorDebugAssembly::GetAppDomain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetAppDomain
helpviewer_keywords:
- ICorDebugAssembly::GetAppDomain method [.NET Framework debugging]
- GetAppDomain method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 14e18510-23ac-4cba-9f96-c86147a2df9d
topic_type:
- apiref
ms.openlocfilehash: f67b2a211b080843e2bd7b8820a5bf54dae638e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712098"
---
# <a name="icordebugassemblygetappdomain-method"></a><span data-ttu-id="9a128-103">ICorDebugAssembly::GetAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="9a128-103">ICorDebugAssembly::GetAppDomain Method</span></span>

<span data-ttu-id="9a128-104">获取一个接口指针，该指针指向包含此实例的应用程序域 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="9a128-104">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a128-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a128-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a128-106">参数</span><span class="sxs-lookup"><span data-stu-id="9a128-106">Parameters</span></span>  

 `ppAppDomain`  
 <span data-ttu-id="9a128-107">弄一个指针，指向表示应用程序域的 ICorDebugAppDomain 接口的地址。</span><span class="sxs-lookup"><span data-stu-id="9a128-107">[out] A pointer to the address of an ICorDebugAppDomain interface that represents the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9a128-108">备注</span><span class="sxs-lookup"><span data-stu-id="9a128-108">Remarks</span></span>  

 <span data-ttu-id="9a128-109">如果此程序集是系统程序集，则 `GetAppDomain` 返回 null。</span><span class="sxs-lookup"><span data-stu-id="9a128-109">If this assembly is the system assembly, `GetAppDomain` returns null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a128-110">要求</span><span class="sxs-lookup"><span data-stu-id="9a128-110">Requirements</span></span>  

 <span data-ttu-id="9a128-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9a128-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a128-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9a128-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9a128-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9a128-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9a128-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9a128-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
