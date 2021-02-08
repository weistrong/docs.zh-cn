---
description: 了解详细信息： CoreClrDebugProcInfo 结构
title: CoreClrDebugProcInfo 结构
ms.date: 03/30/2017
api_name:
- CoreClrDebugProcInfo
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CoreClrDebugProcInfo
helpviewer_keywords:
- remote debugging API [Silverlight]
- CoreClrDebugProcInfo structure
- Silverlight, remote debugging
ms.assetid: 4ddc37da-5c94-4beb-b61c-b54071c0e749
topic_type:
- apiref
ms.openlocfilehash: 04befb057be689e68dd3571a13990da9af64551f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801483"
---
# <a name="coreclrdebugprocinfo-structure"></a><span data-ttu-id="6aa1c-103">CoreClrDebugProcInfo 结构</span><span class="sxs-lookup"><span data-stu-id="6aa1c-103">CoreClrDebugProcInfo Structure</span></span>

<span data-ttu-id="6aa1c-104">表示在远程计算机上运行的进程。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-104">Represents a process that is running on a remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6aa1c-105">语法</span><span class="sxs-lookup"><span data-stu-id="6aa1c-105">Syntax</span></span>  
  
```cpp  
struct  CoreClrDebugProcInfo {  
    DWORD m_dwPID;  
    DWORD m_dwInternalID;  
    WCHAR m_wszName[256];  
};  
```  
  
## <a name="members"></a><span data-ttu-id="6aa1c-106">成员</span><span class="sxs-lookup"><span data-stu-id="6aa1c-106">Members</span></span>  
  
|<span data-ttu-id="6aa1c-107">成员</span><span class="sxs-lookup"><span data-stu-id="6aa1c-107">Member</span></span>|<span data-ttu-id="6aa1c-108">说明</span><span class="sxs-lookup"><span data-stu-id="6aa1c-108">Description</span></span>|  
|------------|-----------------|  
|`m_dwPID`|<span data-ttu-id="6aa1c-109">操作系统分配的进程标识符。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-109">OS-assigned process identifier.</span></span>|  
|`m_dwInternalID`|<span data-ttu-id="6aa1c-110">由运行在目标计算机上的远程调试代理分配的进程标识符。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-110">Process identifier that is assigned by the remote debugging proxy running on the target machine.</span></span> <span data-ttu-id="6aa1c-111">此标识符的回收通常少于 OS 标识符。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-111">This identifier recycles less often than the OS identifier.</span></span>|  
|`m_wszName`|<span data-ttu-id="6aa1c-112">进程的命令行。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-112">Command-line of the process.</span></span> <span data-ttu-id="6aa1c-113">此成员可能会被截断。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-113">This member may be truncated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6aa1c-114">要求</span><span class="sxs-lookup"><span data-stu-id="6aa1c-114">Requirements</span></span>  

 <span data-ttu-id="6aa1c-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6aa1c-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6aa1c-116">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="6aa1c-116">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="6aa1c-117">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="6aa1c-117">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="6aa1c-118">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="6aa1c-118">**.NET Framework Versions:** 3.5 SP1</span></span>
