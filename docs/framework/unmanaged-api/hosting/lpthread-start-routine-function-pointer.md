---
description: 了解详细信息： LPTHREAD_START_ROUTINE 函数指针
title: LPTHREAD_START_ROUTINE 函数指针
ms.date: 03/30/2017
api_name:
- LPTHREAD_START_ROUTINE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- LPTHREAD_START_ROUTINE
helpviewer_keywords:
- LPTHREAD_START_ROUTINE function pointer [.NET Framework hosting]
ms.assetid: 7b9b93b0-fe92-42ba-8693-701168a29dde
topic_type:
- apiref
ms.openlocfilehash: 9f79cffb0b5290031915b453353dd47cb3959970
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679795"
---
# <a name="lpthread_start_routine-function-pointer"></a><span data-ttu-id="987af-103">LPTHREAD_START_ROUTINE 函数指针</span><span class="sxs-lookup"><span data-stu-id="987af-103">LPTHREAD_START_ROUTINE Function Pointer</span></span>

<span data-ttu-id="987af-104">指向一个函数，该函数通知宿主线程已开始执行。</span><span class="sxs-lookup"><span data-stu-id="987af-104">Points to a function that notifies the host that a thread has started to execute.</span></span>  
  
 <span data-ttu-id="987af-105">此函数指针在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="987af-105">This function pointer has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="987af-106">语法</span><span class="sxs-lookup"><span data-stu-id="987af-106">Syntax</span></span>  
  
```cpp  
typedef DWORD (__stdcall *LPTHREAD_START_ROUTINE) (  
    [in] LPVOID lpThreadParameter  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="987af-107">参数</span><span class="sxs-lookup"><span data-stu-id="987af-107">Parameters</span></span>  

 `lpThreadParameter`  
 <span data-ttu-id="987af-108">中指向已开始执行的代码的指针。</span><span class="sxs-lookup"><span data-stu-id="987af-108">[in] A pointer to the code that has started executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="987af-109">备注</span><span class="sxs-lookup"><span data-stu-id="987af-109">Remarks</span></span>  

 <span data-ttu-id="987af-110">指向该函数的 `LPTHREAD_START_ROUTINE` 点是回调函数，并且必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="987af-110">The function to which `LPTHREAD_START_ROUTINE` points is a callback function and must be implemented by the writer of the hosting application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="987af-111">要求</span><span class="sxs-lookup"><span data-stu-id="987af-111">Requirements</span></span>  

 <span data-ttu-id="987af-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="987af-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="987af-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="987af-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="987af-114">**库：** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="987af-114">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="987af-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="987af-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="987af-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="987af-116">See also</span></span>

- [<span data-ttu-id="987af-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="987af-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
