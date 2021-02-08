---
description: 了解详细信息： CALL_ID 结构
title: CALL_ID 结构
ms.date: 03/30/2017
api_name:
- CALL_ID
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- CALL_ID
helpviewer_keywords:
- CALL_ID structure [.NET Framework debugging]
ms.assetid: bfd46324-afec-4782-9c18-586d81fb4740
topic_type:
- apiref
ms.openlocfilehash: 4ef6023e382e8c5fead48494f428648a37f3bef4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800482"
---
# <a name="call_id-structure"></a><span data-ttu-id="cf8d1-103">CALL_ID 结构</span><span class="sxs-lookup"><span data-stu-id="cf8d1-103">CALL_ID Structure</span></span>

<span data-ttu-id="cf8d1-104">向调试器提供有关正在调用的函数的信息。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-104">Provides information to a debugger about a function that is being called.</span></span> <span data-ttu-id="cf8d1-105">有关详细信息，请参阅 [INotifySink2](inotifysink2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-105">See the [INotifySink2](inotifysink2-interface.md) interface for more information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf8d1-106">语法</span><span class="sxs-lookup"><span data-stu-id="cf8d1-106">Syntax</span></span>  
  
```cpp  
typedef struct tagCALL_ID  
{  
    LPCOLESTR       szMachine;  
    DWORD           dwPid;  
    USER_THREAD     *pUserThread;  
    STACK_ADDRESS   addrStackPointer;  
    LPCOLESTR       szEntryPoint;  
    LPCOLESTR       szDestinationMachine;  
} CALL_ID;  
```  
  
## <a name="members"></a><span data-ttu-id="cf8d1-107">成员</span><span class="sxs-lookup"><span data-stu-id="cf8d1-107">Members</span></span>  
  
|<span data-ttu-id="cf8d1-108">成员</span><span class="sxs-lookup"><span data-stu-id="cf8d1-108">Member</span></span>|<span data-ttu-id="cf8d1-109">说明</span><span class="sxs-lookup"><span data-stu-id="cf8d1-109">Description</span></span>|  
|------------|-----------------|  
|`szMachine`|<span data-ttu-id="cf8d1-110">标识正在进行调用的计算机。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-110">Identifies the machine that is making the call.</span></span>|  
|`dwPid`|<span data-ttu-id="cf8d1-111">标识计算机处理器。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-111">Identifies the machine processor.</span></span>|  
|`pUserThread`|<span data-ttu-id="cf8d1-112">标识正在执行调用的线程。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-112">Identifies the thread that is executing the call.</span></span>|  
|`addrStackPointer`|<span data-ttu-id="cf8d1-113">指定调用堆栈的地址。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-113">Specifies the address of the call stack.</span></span>|  
|`szEntryPoint`|<span data-ttu-id="cf8d1-114">指定调用的地址。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-114">Specifies the address of the call.</span></span>|  
|`szDestinationMachine`|<span data-ttu-id="cf8d1-115">标识要执行调用的计算机。</span><span class="sxs-lookup"><span data-stu-id="cf8d1-115">Identifies the machine that will execute the call.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cf8d1-116">要求</span><span class="sxs-lookup"><span data-stu-id="cf8d1-116">Requirements</span></span>  

 <span data-ttu-id="cf8d1-117">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="cf8d1-117">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf8d1-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="cf8d1-118">See also</span></span>

- [<span data-ttu-id="cf8d1-119">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="cf8d1-119">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="cf8d1-120">诊断符号存储区结构</span><span class="sxs-lookup"><span data-stu-id="cf8d1-120">Diagnostics Symbol Store Structures</span></span>](diagnostics-symbol-store-structures.md)
