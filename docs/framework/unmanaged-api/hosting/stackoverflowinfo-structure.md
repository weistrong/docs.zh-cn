---
description: 了解详细信息： StackOverflowInfo 结构
title: StackOverflowInfo 结构
ms.date: 03/30/2017
api_name:
- StackOverflowInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowInfo
helpviewer_keywords:
- StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type:
- apiref
ms.openlocfilehash: cca65e4293c05b89ebefc3c6dd36a6b8898eb15f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679389"
---
# <a name="stackoverflowinfo-structure"></a><span data-ttu-id="7f85e-103">StackOverflowInfo 结构</span><span class="sxs-lookup"><span data-stu-id="7f85e-103">StackOverflowInfo Structure</span></span>

<span data-ttu-id="7f85e-104">存储发生的溢出的类型以及因溢出而引发的异常的信息。</span><span class="sxs-lookup"><span data-stu-id="7f85e-104">Stores the type of overflow that occurred and information on the exception that was thrown due to the overflow.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f85e-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f85e-105">Syntax</span></span>  
  
```cpp  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="7f85e-106">成员</span><span class="sxs-lookup"><span data-stu-id="7f85e-106">Members</span></span>  
  
|<span data-ttu-id="7f85e-107">成员</span><span class="sxs-lookup"><span data-stu-id="7f85e-107">Member</span></span>|<span data-ttu-id="7f85e-108">说明</span><span class="sxs-lookup"><span data-stu-id="7f85e-108">Description</span></span>|  
|------------|-----------------|  
|`soType`|<span data-ttu-id="7f85e-109">指定溢出类型的 [StackOverflowType](stackoverflowtype-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="7f85e-109">A value of the [StackOverflowType](stackoverflowtype-enumeration.md) enumeration that specifies the type of overflow.</span></span>|  
|`pExceptionInfo`|<span data-ttu-id="7f85e-110">一个指向 Win32 对象的指针 `EXCEPTION_POINTERS` ，该对象包含一个异常记录，其中包含与计算机无关的异常说明和一个上下文记录，其中包含发生异常时的处理器上下文的依赖于计算机的说明。</span><span class="sxs-lookup"><span data-stu-id="7f85e-110">A pointer to a Win32 `EXCEPTION_POINTERS` object, which contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7f85e-111">备注</span><span class="sxs-lookup"><span data-stu-id="7f85e-111">Remarks</span></span>  

 <span data-ttu-id="7f85e-112">`StackOverflowInfo`对象将传递到事件的[IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md)方法 `Event_StackOverflow` 。</span><span class="sxs-lookup"><span data-stu-id="7f85e-112">A `StackOverflowInfo` object is passed to the [IActionOnCLREvent::OnEvent](iactiononclrevent-onevent-method.md) method for `Event_StackOverflow` events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f85e-113">要求</span><span class="sxs-lookup"><span data-stu-id="7f85e-113">Requirements</span></span>  

 <span data-ttu-id="7f85e-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f85e-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f85e-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7f85e-115">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="7f85e-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f85e-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7f85e-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f85e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f85e-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f85e-118">See also</span></span>

- [<span data-ttu-id="7f85e-119">承载结构</span><span class="sxs-lookup"><span data-stu-id="7f85e-119">Hosting Structures</span></span>](hosting-structures.md)
