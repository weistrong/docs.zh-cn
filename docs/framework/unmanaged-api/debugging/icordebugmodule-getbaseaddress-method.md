---
description: 了解详细信息： ICorDebugModule：： GetBaseAddress 方法
title: ICorDebugModule::GetBaseAddress 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetBaseAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetBaseAddress
helpviewer_keywords:
- GetBaseAddress method [.NET Framework debugging]
- ICorDebugModule::GetBaseAddress method [.NET Framework debugging]
ms.assetid: 26a82815-1982-4eb7-92d1-5c3d318d5be4
topic_type:
- apiref
ms.openlocfilehash: bdfa4aeac3a9c06f666d56f1ee08ec503626ce7d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790810"
---
# <a name="icordebugmodulegetbaseaddress-method"></a><span data-ttu-id="b81fc-103">ICorDebugModule::GetBaseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="b81fc-103">ICorDebugModule::GetBaseAddress Method</span></span>

<span data-ttu-id="b81fc-104">获取模块的基址。</span><span class="sxs-lookup"><span data-stu-id="b81fc-104">Gets the base address of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b81fc-105">语法</span><span class="sxs-lookup"><span data-stu-id="b81fc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBaseAddress(  
    [out] CORDB_ADDRESS *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b81fc-106">参数</span><span class="sxs-lookup"><span data-stu-id="b81fc-106">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="b81fc-107">弄一个 `CORDB_ADDRESS` ，它指定模块的基址。</span><span class="sxs-lookup"><span data-stu-id="b81fc-107">[out] A `CORDB_ADDRESS` that specifies the base address of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b81fc-108">备注</span><span class="sxs-lookup"><span data-stu-id="b81fc-108">Remarks</span></span>  

 <span data-ttu-id="b81fc-109">如果该模块是本机映像 (也就是说，如果该模块是由本机映像生成器生成的，则 NGen.exe) ，其基址将为零。</span><span class="sxs-lookup"><span data-stu-id="b81fc-109">If the module is a native image (that is, if the module was produced by the native image generator, NGen.exe), its base address will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b81fc-110">要求</span><span class="sxs-lookup"><span data-stu-id="b81fc-110">Requirements</span></span>  

 <span data-ttu-id="b81fc-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b81fc-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b81fc-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b81fc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b81fc-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b81fc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b81fc-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b81fc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b81fc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="b81fc-115">See also</span></span>
