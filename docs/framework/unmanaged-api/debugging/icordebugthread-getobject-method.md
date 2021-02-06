---
description: 了解详细信息： ICorDebugThread：： GetObject 方法
title: ICorDebugThread::GetObject 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetObject method [.NET Framework debugging]
ms.assetid: 1590febe-96c2-4046-97db-d81d81d67e01
topic_type:
- apiref
ms.openlocfilehash: db5760be0ef4230b2dccec9d1836ea0eee56f231
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658931"
---
# <a name="icordebugthreadgetobject-method"></a><span data-ttu-id="0d001-103">ICorDebugThread::GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="0d001-103">ICorDebugThread::GetObject Method</span></span>

<span data-ttu-id="0d001-104"> (CLR) 线程获取公共语言运行时的接口指针。</span><span class="sxs-lookup"><span data-stu-id="0d001-104">Gets an interface pointer to the common language runtime (CLR) thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d001-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d001-105">Syntax</span></span>  
  
```cpp  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d001-106">参数</span><span class="sxs-lookup"><span data-stu-id="0d001-106">Parameters</span></span>  

 `ppObject`  
 <span data-ttu-id="0d001-107">弄指向表示 CLR 线程的 ICorDebugValue 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="0d001-107">[out] A pointer to the address of an ICorDebugValue interface object that represents the CLR thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d001-108">要求</span><span class="sxs-lookup"><span data-stu-id="0d001-108">Requirements</span></span>  

 <span data-ttu-id="0d001-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0d001-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d001-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0d001-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0d001-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0d001-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0d001-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d001-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d001-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="0d001-113">See also</span></span>

- <xref:System.Threading.Thread>
