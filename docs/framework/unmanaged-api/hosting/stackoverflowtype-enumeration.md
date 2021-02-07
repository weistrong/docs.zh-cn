---
description: 了解详细信息： StackOverflowType 枚举
title: StackOverflowType 枚举
ms.date: 03/30/2017
api_name:
- StackOverflowType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowType
helpviewer_keywords:
- StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type:
- apiref
ms.openlocfilehash: d39ccd99331a3e839236f1ede21254edb92b2dfb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679350"
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="f22ce-103">StackOverflowType 枚举</span><span class="sxs-lookup"><span data-stu-id="f22ce-103">StackOverflowType Enumeration</span></span>

<span data-ttu-id="f22ce-104">包含指示堆栈溢出事件的根本原因的值。</span><span class="sxs-lookup"><span data-stu-id="f22ce-104">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f22ce-105">语法</span><span class="sxs-lookup"><span data-stu-id="f22ce-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="f22ce-106">成员</span><span class="sxs-lookup"><span data-stu-id="f22ce-106">Members</span></span>  
  
|<span data-ttu-id="f22ce-107">成员</span><span class="sxs-lookup"><span data-stu-id="f22ce-107">Member</span></span>|<span data-ttu-id="f22ce-108">说明</span><span class="sxs-lookup"><span data-stu-id="f22ce-108">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="f22ce-109">堆栈溢出由执行引擎引起。</span><span class="sxs-lookup"><span data-stu-id="f22ce-109">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="f22ce-110">堆栈溢出由托管代码引起。</span><span class="sxs-lookup"><span data-stu-id="f22ce-110">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="f22ce-111">堆栈溢出由非托管代码引起。</span><span class="sxs-lookup"><span data-stu-id="f22ce-111">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f22ce-112">备注</span><span class="sxs-lookup"><span data-stu-id="f22ce-112">Remarks</span></span>  

 <span data-ttu-id="f22ce-113">此信息通过调用 [IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md) 方法传递到主机。</span><span class="sxs-lookup"><span data-stu-id="f22ce-113">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f22ce-114">要求</span><span class="sxs-lookup"><span data-stu-id="f22ce-114">Requirements</span></span>  

 <span data-ttu-id="f22ce-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f22ce-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f22ce-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f22ce-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f22ce-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f22ce-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f22ce-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f22ce-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f22ce-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="f22ce-119">See also</span></span>

- [<span data-ttu-id="f22ce-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="f22ce-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
