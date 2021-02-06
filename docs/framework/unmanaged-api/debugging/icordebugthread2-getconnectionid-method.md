---
description: 了解详细信息： ICorDebugThread2：： GetConnectionID 方法
title: ICorDebugThread2::GetConnectionID 方法
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetConnectionID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetConnectionID
helpviewer_keywords:
- ICorDebugThread2::GetConnectionID method [.NET Framework debugging]
- GetConnectionID method [.NET Framework debugging]
ms.assetid: 9c76b587-f941-4fa1-8b86-f3494fb10c8e
topic_type:
- apiref
ms.openlocfilehash: 0f8035e703d3638b11f4206d9c47e39fe487d71d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99658732"
---
# <a name="icordebugthread2getconnectionid-method"></a><span data-ttu-id="d741d-103">ICorDebugThread2::GetConnectionID 方法</span><span class="sxs-lookup"><span data-stu-id="d741d-103">ICorDebugThread2::GetConnectionID Method</span></span>

<span data-ttu-id="d741d-104">获取此 ICorDebugThread2 对象的连接标识符。</span><span class="sxs-lookup"><span data-stu-id="d741d-104">Gets the connection identifier for this ICorDebugThread2 object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d741d-105">语法</span><span class="sxs-lookup"><span data-stu-id="d741d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetConnectionID (  
    [out] CONNID *pdwConnectionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d741d-106">参数</span><span class="sxs-lookup"><span data-stu-id="d741d-106">Parameters</span></span>  

 `pdwConnectionId`  
 <span data-ttu-id="d741d-107">弄一个 `CONNID` 表示连接标识符的。</span><span class="sxs-lookup"><span data-stu-id="d741d-107">[out] A `CONNID` that represents the connection identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d741d-108">备注</span><span class="sxs-lookup"><span data-stu-id="d741d-108">Remarks</span></span>  

 <span data-ttu-id="d741d-109">`GetConnectionID` `pdwConnectionId` 如果此线程不是连接的一部分，则该方法将在参数中返回零。</span><span class="sxs-lookup"><span data-stu-id="d741d-109">The `GetConnectionID` method returns zero in the `pdwConnectionId` parameter, if this thread is not part of a connection.</span></span>  
  
 <span data-ttu-id="d741d-110">如果此线程连接到 (SSAS) Microsoft SQL Server 2005 Analysis Services 的实例，则 `CONNID` 映射到服务器进程标识符 (SPID) 。</span><span class="sxs-lookup"><span data-stu-id="d741d-110">If this thread is connected to an instance of Microsoft SQL Server 2005 Analysis Services (SSAS), the `CONNID` maps to a server process identifier (SPID).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d741d-111">要求</span><span class="sxs-lookup"><span data-stu-id="d741d-111">Requirements</span></span>  

 <span data-ttu-id="d741d-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d741d-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d741d-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d741d-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d741d-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d741d-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d741d-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d741d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
