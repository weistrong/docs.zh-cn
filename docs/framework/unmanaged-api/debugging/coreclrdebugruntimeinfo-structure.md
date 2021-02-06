---
description: 了解详细信息： CoreClrDebugRuntimeInfo 结构
title: CoreClrDebugRuntimeInfo 结构
ms.date: 03/30/2017
api_name:
- CoreClrDebugRuntimeInfo
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CoreClrDebugRuntimeInfo
helpviewer_keywords:
- remote debugging API [Silverlight]
- CoreDebugRuntimeInfo structure
- Silverlight, remote debugging
ms.assetid: bd01c30f-b7a8-4179-9497-622b6599b1a6
topic_type:
- apiref
ms.openlocfilehash: 588e8bd1598996d1676e2df5517bd9a52eb59df4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661709"
---
# <a name="coreclrdebugruntimeinfo-structure"></a><span data-ttu-id="ad9e4-103">CoreClrDebugRuntimeInfo 结构</span><span class="sxs-lookup"><span data-stu-id="ad9e4-103">CoreClrDebugRuntimeInfo Structure</span></span>

<span data-ttu-id="ad9e4-104">表示公共语言运行时 (CLR) 实例，该实例加载到远程计算机上的进程中。</span><span class="sxs-lookup"><span data-stu-id="ad9e4-104">Represents a common language runtime (CLR) instance that is loaded in a process on a remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad9e4-105">语法</span><span class="sxs-lookup"><span data-stu-id="ad9e4-105">Syntax</span></span>  
  
```cpp  
struct  CoreClrDebugRuntimeInfo {  
    DWORD m_dwInternalID;  
};  
```  
  
## <a name="members"></a><span data-ttu-id="ad9e4-106">成员</span><span class="sxs-lookup"><span data-stu-id="ad9e4-106">Members</span></span>  
  
|<span data-ttu-id="ad9e4-107">成员</span><span class="sxs-lookup"><span data-stu-id="ad9e4-107">Member</span></span>|<span data-ttu-id="ad9e4-108">说明</span><span class="sxs-lookup"><span data-stu-id="ad9e4-108">Description</span></span>|  
|------------|-----------------|  
|`m_dwInternalID`|<span data-ttu-id="ad9e4-109">由运行在目标计算机上的远程调试代理分配的运行时标识符。</span><span class="sxs-lookup"><span data-stu-id="ad9e4-109">Runtime identifier that is assigned by the remote debugging proxy running on the target machine.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ad9e4-110">要求</span><span class="sxs-lookup"><span data-stu-id="ad9e4-110">Requirements</span></span>  

 <span data-ttu-id="ad9e4-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ad9e4-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad9e4-112">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="ad9e4-112">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="ad9e4-113">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="ad9e4-113">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="ad9e4-114">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="ad9e4-114">**.NET Framework Versions:** 3.5 SP1</span></span>
