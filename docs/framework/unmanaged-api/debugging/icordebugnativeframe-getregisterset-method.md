---
description: 了解详细信息： ICorDebugNativeFrame：： GetRegisterSet 方法
title: ICorDebugNativeFrame::GetRegisterSet 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetRegisterSet
helpviewer_keywords:
- ICorDebugNativeFrame::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 6f309b5f-5556-4f1e-b1dd-4fe97fc81d01
topic_type:
- apiref
ms.openlocfilehash: 8878c438ad76b1a87429e09b8a4a8bbffb90d00d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722407"
---
# <a name="icordebugnativeframegetregisterset-method"></a><span data-ttu-id="48d77-103">ICorDebugNativeFrame::GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="48d77-103">ICorDebugNativeFrame::GetRegisterSet Method</span></span>

<span data-ttu-id="48d77-104">获取此堆栈帧的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="48d77-104">Gets the register set for this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48d77-105">语法</span><span class="sxs-lookup"><span data-stu-id="48d77-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="48d77-106">参数</span><span class="sxs-lookup"><span data-stu-id="48d77-106">Parameters</span></span>  

 `ppRegisters`  
 <span data-ttu-id="48d77-107">弄一个指向 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 对象地址的指针，该对象表示此堆栈帧的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="48d77-107">[out] A pointer to the address of an [ICorDebugRegisterSet](icordebugregisterset-interface.md) object that represents the register set for this stack frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48d77-108">要求</span><span class="sxs-lookup"><span data-stu-id="48d77-108">Requirements</span></span>  

 <span data-ttu-id="48d77-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48d77-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48d77-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48d77-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="48d77-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48d77-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48d77-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48d77-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48d77-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="48d77-113">See also</span></span>
