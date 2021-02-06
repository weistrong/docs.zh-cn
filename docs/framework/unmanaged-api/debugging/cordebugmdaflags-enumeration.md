---
description: 了解详细信息： CorDebugMDAFlags 枚举
title: CorDebugMDAFlags 枚举
ms.date: 03/30/2017
api_name:
- CorDebugMDAFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugMDAFlags
helpviewer_keywords:
- CorDebugMDAFlags enumeration [.NET Framework debugging]
ms.assetid: 7c0c92fe-8bd2-477f-b307-aca0143732ca
topic_type:
- apiref
ms.openlocfilehash: d7e9178d76286b112035729e997b1f68e2a93fb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661930"
---
# <a name="cordebugmdaflags-enumeration"></a><span data-ttu-id="b4037-103">CorDebugMDAFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="b4037-103">CorDebugMDAFlags Enumeration</span></span>

<span data-ttu-id="b4037-104">指定在其上激发托管调试助手 (MDA) 的线程的状态。</span><span class="sxs-lookup"><span data-stu-id="b4037-104">Specifies the status of the thread on which the managed debugging assistant (MDA) is fired.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4037-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4037-105">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugMDAFlags {  
    MDA_FLAG_SLIP = 0x2  
} CorDebugMDAFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="b4037-106">成员</span><span class="sxs-lookup"><span data-stu-id="b4037-106">Members</span></span>  
  
|<span data-ttu-id="b4037-107">成员</span><span class="sxs-lookup"><span data-stu-id="b4037-107">Member</span></span>|<span data-ttu-id="b4037-108">说明</span><span class="sxs-lookup"><span data-stu-id="b4037-108">Description</span></span>|  
|------------|-----------------|  
|`MDA_FLAG_SLIP`|<span data-ttu-id="b4037-109">触发 mda 后，触发 MDA 的线程发生了。</span><span class="sxs-lookup"><span data-stu-id="b4037-109">The thread on which the MDA was fired has slipped since the MDA was fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b4037-110">备注</span><span class="sxs-lookup"><span data-stu-id="b4037-110">Remarks</span></span>  

 <span data-ttu-id="b4037-111">当调用堆栈不再描述最初引发 MDA 的位置时，线程被视为已 *落后*。</span><span class="sxs-lookup"><span data-stu-id="b4037-111">When the call stack no longer describes where the MDA was originally raised, the thread is considered to have *slipped*.</span></span> <span data-ttu-id="b4037-112">这是一个不寻常的情况，导致在退出时线程执行无效操作的情况。</span><span class="sxs-lookup"><span data-stu-id="b4037-112">This is an unusual circumstance brought about by the thread's execution of an invalid operation upon exiting.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4037-113">要求</span><span class="sxs-lookup"><span data-stu-id="b4037-113">Requirements</span></span>  

 <span data-ttu-id="b4037-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b4037-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4037-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b4037-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b4037-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4037-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4037-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4037-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4037-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="b4037-118">See also</span></span>

- [<span data-ttu-id="b4037-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="b4037-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
