---
description: 了解详细信息： EClrUnhandledException 枚举
title: EClrUnhandledException 枚举
ms.date: 03/30/2017
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
ms.openlocfilehash: 088d448a92c4d9030208537b9c788477c85f9d37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785544"
---
# <a name="eclrunhandledexception-enumeration"></a><span data-ttu-id="b3d81-103">EClrUnhandledException 枚举</span><span class="sxs-lookup"><span data-stu-id="b3d81-103">EClrUnhandledException Enumeration</span></span>

<span data-ttu-id="b3d81-104">介绍用于管理用户代码中未经处理的异常的可用选项。</span><span class="sxs-lookup"><span data-stu-id="b3d81-104">Describes the available options for managing exceptions that are unhandled in user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3d81-105">语法</span><span class="sxs-lookup"><span data-stu-id="b3d81-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a><span data-ttu-id="b3d81-106">成员</span><span class="sxs-lookup"><span data-stu-id="b3d81-106">Members</span></span>  
  
|<span data-ttu-id="b3d81-107">成员</span><span class="sxs-lookup"><span data-stu-id="b3d81-107">Member</span></span>|<span data-ttu-id="b3d81-108">说明</span><span class="sxs-lookup"><span data-stu-id="b3d81-108">Description</span></span>|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|<span data-ttu-id="b3d81-109">指定发生默认行为。</span><span class="sxs-lookup"><span data-stu-id="b3d81-109">Specifies that the default behavior occurs.</span></span> <span data-ttu-id="b3d81-110">进程已被破坏。</span><span class="sxs-lookup"><span data-stu-id="b3d81-110">The process is torn down.</span></span>|  
|`eHostDeterminedPolicy`|<span data-ttu-id="b3d81-111">指定公共语言运行时 (CLR) 忽略未经处理的异常，并允许主机确定任何其他操作。</span><span class="sxs-lookup"><span data-stu-id="b3d81-111">Specifies that the common language runtime (CLR) ignores unhandled exceptions and lets the host determine any further action.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3d81-112">备注</span><span class="sxs-lookup"><span data-stu-id="b3d81-112">Remarks</span></span>  

 <span data-ttu-id="b3d81-113">若要指定 CLR 的行为类似于早期版本，请使用 `eHostDeterminedPolicy` 成员。</span><span class="sxs-lookup"><span data-stu-id="b3d81-113">To specify that the CLR behave like earlier versions, use the `eHostDeterminedPolicy` member.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3d81-114">要求</span><span class="sxs-lookup"><span data-stu-id="b3d81-114">Requirements</span></span>  

 <span data-ttu-id="b3d81-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d81-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3d81-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="b3d81-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b3d81-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b3d81-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b3d81-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3d81-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3d81-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3d81-119">See also</span></span>

- [<span data-ttu-id="b3d81-120">EClrFailure 枚举</span><span class="sxs-lookup"><span data-stu-id="b3d81-120">EClrFailure Enumeration</span></span>](eclrfailure-enumeration.md)
- [<span data-ttu-id="b3d81-121">EClrOperation 枚举</span><span class="sxs-lookup"><span data-stu-id="b3d81-121">EClrOperation Enumeration</span></span>](eclroperation-enumeration.md)
- [<span data-ttu-id="b3d81-122">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="b3d81-122">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)
- [<span data-ttu-id="b3d81-123">SetUnhandledExceptionPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="b3d81-123">SetUnhandledExceptionPolicy Method</span></span>](iclrpolicymanager-setunhandledexceptionpolicy-method.md)
- [<span data-ttu-id="b3d81-124">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="b3d81-124">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)
- [<span data-ttu-id="b3d81-125">承载枚举</span><span class="sxs-lookup"><span data-stu-id="b3d81-125">Hosting Enumerations</span></span>](hosting-enumerations.md)
