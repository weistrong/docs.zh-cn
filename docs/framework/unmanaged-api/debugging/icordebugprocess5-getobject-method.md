---
description: 了解详细信息： ICorDebugProcess5：： GetObject 方法
title: ICorDebugProcess5::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetObject method [.NET Framework debugging]
ms.assetid: c8111502-5a20-447f-9dc2-76e8acd7ed5a
topic_type:
- apiref
ms.openlocfilehash: 4e295e1afc19cc5b9ca763b04b05097d48f0302c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746355"
---
# <a name="icordebugprocess5getobject-method"></a><span data-ttu-id="2b64f-103">ICorDebugProcess5::GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="2b64f-103">ICorDebugProcess5::GetObject Method</span></span>

<span data-ttu-id="2b64f-104">将对象地址转换为 "ICorDebugObjectValue" 对象。</span><span class="sxs-lookup"><span data-stu-id="2b64f-104">Converts an object address to an "ICorDebugObjectValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b64f-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b64f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObject(  
    [in] CORDB_ADDRESS addr,
    [out] ICorDebugObjectValue **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b64f-106">参数</span><span class="sxs-lookup"><span data-stu-id="2b64f-106">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="2b64f-107">中对象地址。</span><span class="sxs-lookup"><span data-stu-id="2b64f-107">[in] The object address.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="2b64f-108">弄一个指向 "ICorDebugObjectValue" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="2b64f-108">[out] A pointer to the address of an  "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2b64f-109">备注</span><span class="sxs-lookup"><span data-stu-id="2b64f-109">Remarks</span></span>  

 <span data-ttu-id="2b64f-110">如果不 `addr` 指向有效的托管对象，该方法将 `GetObject` 返回 `E_FAIL` 。</span><span class="sxs-lookup"><span data-stu-id="2b64f-110">If `addr` does not point to a valid managed object, the `GetObject` method returns `E_FAIL`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b64f-111">要求</span><span class="sxs-lookup"><span data-stu-id="2b64f-111">Requirements</span></span>  

 <span data-ttu-id="2b64f-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2b64f-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b64f-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2b64f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2b64f-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2b64f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2b64f-115">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b64f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b64f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b64f-116">See also</span></span>

- [<span data-ttu-id="2b64f-117">ICorDebugProcess5 接口</span><span class="sxs-lookup"><span data-stu-id="2b64f-117">ICorDebugProcess5 Interface</span></span>](icordebugprocess5-interface.md)
- [<span data-ttu-id="2b64f-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="2b64f-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
