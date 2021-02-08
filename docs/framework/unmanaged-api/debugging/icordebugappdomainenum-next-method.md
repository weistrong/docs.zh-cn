---
description: 了解详细信息： ICorDebugAppDomainEnum：： Next 方法
title: ICorDebugAppDomainEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomainEnum::Next method
helpviewer_keywords:
- ICorDebugAppDomainEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugAppDomainEnum interface [.NET Framework debugging]
ms.assetid: b8d1def7-0ebc-4314-a3a2-fd36a75973e7
topic_type:
- apiref
ms.openlocfilehash: ac5397250e661b4ed380b3272744957f86e1a07b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791525"
---
# <a name="icordebugappdomainenumnext-method"></a><span data-ttu-id="08fcd-103">ICorDebugAppDomainEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="08fcd-103">ICorDebugAppDomainEnum::Next Method</span></span>

<span data-ttu-id="08fcd-104">从当前游标位置开始，获取集合中指定数量的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="08fcd-104">Gets the specified number of application domains from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08fcd-105">语法</span><span class="sxs-lookup"><span data-stu-id="08fcd-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
                           ICorDebugAppDomain *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08fcd-106">参数</span><span class="sxs-lookup"><span data-stu-id="08fcd-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="08fcd-107">中要检索的应用程序域的数量。</span><span class="sxs-lookup"><span data-stu-id="08fcd-107">[in] The number of application domains to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="08fcd-108">弄指针的数组，其中每个都指向表示应用程序域的 ICorDebugAppDomain 对象。</span><span class="sxs-lookup"><span data-stu-id="08fcd-108">[out] An array of pointers, each of which points to an ICorDebugAppDomain object that represents an application domain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="08fcd-109">弄一个指针，指向实际返回的应用程序域的数量。</span><span class="sxs-lookup"><span data-stu-id="08fcd-109">[out] A pointer to the number of application domains actually returned.</span></span> <span data-ttu-id="08fcd-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="08fcd-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08fcd-111">要求</span><span class="sxs-lookup"><span data-stu-id="08fcd-111">Requirements</span></span>  

 <span data-ttu-id="08fcd-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08fcd-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08fcd-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="08fcd-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="08fcd-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08fcd-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08fcd-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08fcd-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
