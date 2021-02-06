---
description: 了解详细信息： ICorDebugThread：： GetRegisterSet 方法
title: ICorDebugThread::GetRegisterSet 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetRegisterSet
helpviewer_keywords:
- ICorDebugThread::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 3b9b6260-98ac-4cfd-88e5-5d7614f94a0c
topic_type:
- apiref
ms.openlocfilehash: f61ccb34eabc1f4d8b8db8a0b78e3ddde9aa136d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658875"
---
# <a name="icordebugthreadgetregisterset-method"></a><span data-ttu-id="b1db2-103">ICorDebugThread::GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="b1db2-103">ICorDebugThread::GetRegisterSet Method</span></span>

<span data-ttu-id="b1db2-104">获取一个接口指针，该指针指向与此 ICorDebugThread 对象的活动部分关联的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="b1db2-104">Gets an interface pointer to the register set that is associated with the active part of this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1db2-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1db2-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1db2-106">参数</span><span class="sxs-lookup"><span data-stu-id="b1db2-106">Parameters</span></span>  

 `ppRegisters`  
 <span data-ttu-id="b1db2-107">弄指向 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 接口对象地址的指针，该对象表示此线程的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="b1db2-107">[out] A pointer to the address of an [ICorDebugRegisterSet](icordebugregisterset-interface.md) interface object that represents the register set for the active part of this thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1db2-108">要求</span><span class="sxs-lookup"><span data-stu-id="b1db2-108">Requirements</span></span>  

 <span data-ttu-id="b1db2-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1db2-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1db2-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b1db2-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b1db2-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1db2-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b1db2-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1db2-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
