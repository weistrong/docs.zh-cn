---
description: 了解详细信息： WAITORTIMERCALLBACK 函数指针
title: WAITORTIMERCALLBACK 函数指针
ms.date: 03/30/2017
api_name:
- WAITORTIMERCALLBACK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- WAITORTIMERCALLBACK
helpviewer_keywords:
- WAITORTIMERCALLBACK function pointer [.NET Framework hosting]
ms.assetid: 1fec4aef-0a06-4df0-bae7-d31a9ef9603d
topic_type:
- apiref
ms.openlocfilehash: 6fd9e7eab56e48086eefcb26fc48cbf5f45d4a0e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679051"
---
# <a name="waitortimercallback-function-pointer"></a><span data-ttu-id="a14e0-103">WAITORTIMERCALLBACK 函数指针</span><span class="sxs-lookup"><span data-stu-id="a14e0-103">WAITORTIMERCALLBACK Function Pointer</span></span>

<span data-ttu-id="a14e0-104">指向一个函数，该函数向宿主通知等待句柄 (<xref:System.Threading.WaitHandle>) 已发出信号或超时。</span><span class="sxs-lookup"><span data-stu-id="a14e0-104">Points to a function that notifies the host that a wait handle (<xref:System.Threading.WaitHandle>) has either been signaled or timed out.</span></span>  
  
 <span data-ttu-id="a14e0-105">此函数指针在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="a14e0-105">This function pointer has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a14e0-106">语法</span><span class="sxs-lookup"><span data-stu-id="a14e0-106">Syntax</span></span>  
  
```cpp  
typedef VOID (__stdcall *WAITORTIMERCALLBACK) (  
    [in] PVOID lpParameter,  
    [in] BOOL  TimerOrWaitFired  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a14e0-107">参数</span><span class="sxs-lookup"><span data-stu-id="a14e0-107">Parameters</span></span>  

 `lpParameter`  
 <span data-ttu-id="a14e0-108">中指向对象的指针，该对象包含由宿主定义的信息。</span><span class="sxs-lookup"><span data-stu-id="a14e0-108">[in] A pointer to an object that contains information defined by the host.</span></span>  
  
 `TimerOrWaitFired`  
 <span data-ttu-id="a14e0-109">[in] `true` 如果等待句柄超时，则为; 如果等待句柄已终止，则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="a14e0-109">[in] `true` if the wait handle timed out, or `false` if it was signaled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a14e0-110">备注</span><span class="sxs-lookup"><span data-stu-id="a14e0-110">Remarks</span></span>  

 <span data-ttu-id="a14e0-111">指向该函数的 `WAITORTIMERCALLBACK` 点是回调函数，并且必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="a14e0-111">The function to which `WAITORTIMERCALLBACK` points is a callback function and must be implemented by the writer of the hosting application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a14e0-112">要求</span><span class="sxs-lookup"><span data-stu-id="a14e0-112">Requirements</span></span>  

 <span data-ttu-id="a14e0-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a14e0-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a14e0-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a14e0-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a14e0-115">**库：** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="a14e0-115">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="a14e0-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a14e0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a14e0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a14e0-117">See also</span></span>

- [<span data-ttu-id="a14e0-118">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="a14e0-118">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
