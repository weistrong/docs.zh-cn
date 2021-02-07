---
description: 了解详细信息： ICorDebugAppDomain：： EnumerateAssemblies 方法
title: ICorDebugAppDomain::EnumerateAssemblies 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateAssemblies
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateAssemblies
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateAssemblies method [.NET Framework debugging]
- EnumerateAssemblies method [.NET Framework debugging]
ms.assetid: 7add64f9-19a8-46a9-be62-905d5e7d1bd8
topic_type:
- apiref
ms.openlocfilehash: 3ffa3180b80eac46e2d61019e4e4aa992f7c0e72
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754259"
---
# <a name="icordebugappdomainenumerateassemblies-method"></a><span data-ttu-id="53581-103">ICorDebugAppDomain::EnumerateAssemblies 方法</span><span class="sxs-lookup"><span data-stu-id="53581-103">ICorDebugAppDomain::EnumerateAssemblies Method</span></span>

<span data-ttu-id="53581-104">获取应用程序域中的程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="53581-104">Gets an enumerator for the assemblies in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53581-105">语法</span><span class="sxs-lookup"><span data-stu-id="53581-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateAssemblies (  
    [out] ICorDebugAssemblyEnum  **ppAssemblies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="53581-106">参数</span><span class="sxs-lookup"><span data-stu-id="53581-106">Parameters</span></span>  

 `ppAssemblies`  
 <span data-ttu-id="53581-107">弄指向 ICorDebugAssemblyEnum 对象地址的指针，该对象是应用程序域中的程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="53581-107">[out] A pointer to the address of an ICorDebugAssemblyEnum object that is the enumerator for the assemblies in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53581-108">要求</span><span class="sxs-lookup"><span data-stu-id="53581-108">Requirements</span></span>  

 <span data-ttu-id="53581-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="53581-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53581-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="53581-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="53581-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="53581-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="53581-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53581-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
