---
description: 了解详细信息： FExecuteInAppDomainCallback 函数指针
title: FExecuteInAppDomainCallback 函数指针
ms.date: 03/30/2017
api_name:
- FExecuteInAppDomainCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FExecuteInAppDomainCallback
helpviewer_keywords:
- FExecuteInAppDomainCallback function pointer [.NET Framework hosting]
ms.assetid: 2709f18f-3eee-497f-bc33-3ab7a485599b
topic_type:
- apiref
ms.openlocfilehash: 97c7fe14a3eafd6f4626d8729be3b45ad5502f1a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785388"
---
# <a name="fexecuteinappdomaincallback-function-pointer"></a><span data-ttu-id="83e38-103">FExecuteInAppDomainCallback 函数指针</span><span class="sxs-lookup"><span data-stu-id="83e38-103">FExecuteInAppDomainCallback Function Pointer</span></span>

<span data-ttu-id="83e38-104">指向由公共语言运行时 (CLR) 调用以执行托管代码的函数。</span><span class="sxs-lookup"><span data-stu-id="83e38-104">Points to a function that is called by the common language runtime (CLR) to execute managed code.</span></span>  
  
 <span data-ttu-id="83e38-105">此函数指针在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="83e38-105">This function pointer has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83e38-106">语法</span><span class="sxs-lookup"><span data-stu-id="83e38-106">Syntax</span></span>  
  
```cpp  
typedef HRESULT (__stdcall *FExecuteInAppDomainCallback) (  
    [in] void  *cookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83e38-107">参数</span><span class="sxs-lookup"><span data-stu-id="83e38-107">Parameters</span></span>  

 `cookie`  
 <span data-ttu-id="83e38-108">中指向包含要执行的托管代码的不透明调用方分配的内存的指针。</span><span class="sxs-lookup"><span data-stu-id="83e38-108">[in] A pointer to opaque caller-allocated memory that contains the managed code to be executed.</span></span>  
  
 <span data-ttu-id="83e38-109">此内存的分配和生存期由调用方 (即 CLR) 控制。</span><span class="sxs-lookup"><span data-stu-id="83e38-109">The allocation and lifetime of this memory are controlled by the caller (that is, the CLR).</span></span> <span data-ttu-id="83e38-110">这不是 CLR 托管堆内存。</span><span class="sxs-lookup"><span data-stu-id="83e38-110">This is not CLR managed-heap memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83e38-111">要求</span><span class="sxs-lookup"><span data-stu-id="83e38-111">Requirements</span></span>  

 <span data-ttu-id="83e38-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="83e38-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83e38-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="83e38-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83e38-114">**库：** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="83e38-114">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="83e38-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83e38-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83e38-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="83e38-116">See also</span></span>

- [<span data-ttu-id="83e38-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="83e38-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
