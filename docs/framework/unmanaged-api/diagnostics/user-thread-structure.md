---
description: 了解详细信息： USER_THREAD 结构
title: USER_THREAD 结构
ms.date: 03/30/2017
api_name:
- USER_THREAD
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- USER_THREAD
helpviewer_keywords:
- USER_THREAD structure [.NET Framework debugging]
ms.assetid: a57c7d71-c4b0-41f9-a964-0c5ee84a3124
topic_type:
- apiref
ms.openlocfilehash: a4bd22073b7610307e67107781bdb68a15ef795f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761263"
---
# <a name="user_thread-structure"></a><span data-ttu-id="ea27c-103">USER_THREAD 结构</span><span class="sxs-lookup"><span data-stu-id="ea27c-103">USER_THREAD Structure</span></span>

<span data-ttu-id="ea27c-104">向调试器提供有关线程的信息。</span><span class="sxs-lookup"><span data-stu-id="ea27c-104">Provides information to a debugger about a thread.</span></span> <span data-ttu-id="ea27c-105">有关详细信息，请参阅 [INotifySource2：： SetNotifyFilter](inotifysource2-setnotifyfilter-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ea27c-105">For more information, see the [INotifySource2::SetNotifyFilter](inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea27c-106">语法</span><span class="sxs-lookup"><span data-stu-id="ea27c-106">Syntax</span></span>  
  
```cpp  
typedef struct tagUSER_THREAD  
{  
    BYTE    *pSidBuffer;  
    DWORD   dwSidLen;  
    DWORD   dwTid;  
} USER_THREAD;  
```  
  
## <a name="members"></a><span data-ttu-id="ea27c-107">成员</span><span class="sxs-lookup"><span data-stu-id="ea27c-107">Members</span></span>  
  
|<span data-ttu-id="ea27c-108">成员</span><span class="sxs-lookup"><span data-stu-id="ea27c-108">Member</span></span>|<span data-ttu-id="ea27c-109">说明</span><span class="sxs-lookup"><span data-stu-id="ea27c-109">Description</span></span>|  
|------------|-----------------|  
|`pSidBuffer`|<span data-ttu-id="ea27c-110">线程缓冲区的地址。</span><span class="sxs-lookup"><span data-stu-id="ea27c-110">Address of thread buffer.</span></span>|  
|`dwSidLen`|<span data-ttu-id="ea27c-111">线程缓冲区的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="ea27c-111">Length of thread buffer, in bytes.</span></span>|  
|`dwTid`|<span data-ttu-id="ea27c-112">线程 ID。</span><span class="sxs-lookup"><span data-stu-id="ea27c-112">Thread ID.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ea27c-113">要求</span><span class="sxs-lookup"><span data-stu-id="ea27c-113">Requirements</span></span>  

 <span data-ttu-id="ea27c-114">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="ea27c-114">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea27c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="ea27c-115">See also</span></span>

- [<span data-ttu-id="ea27c-116">SetNotifyFilter 方法</span><span class="sxs-lookup"><span data-stu-id="ea27c-116">SetNotifyFilter Method</span></span>](inotifysource2-setnotifyfilter-method.md)
- [<span data-ttu-id="ea27c-117">诊断符号存储区结构</span><span class="sxs-lookup"><span data-stu-id="ea27c-117">Diagnostics Symbol Store Structures</span></span>](diagnostics-symbol-store-structures.md)
