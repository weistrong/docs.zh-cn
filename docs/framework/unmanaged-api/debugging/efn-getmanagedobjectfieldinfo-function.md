---
description: 了解详细信息： _EFN_GetManagedObjectFieldInfo 函数
title: _EFN_GetManagedObjectFieldInfo 函数
ms.date: 03/30/2017
api_name:
- _EFN_GetManagedObjectFieldInfo
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_GetManagedObjectFieldInfo
helpviewer_keywords:
- _EFN_GetManagedObjectFieldInfo function [.NET Framework debugging]
ms.assetid: 3b93bcff-62a4-47b2-babc-6bcf4216119a
topic_type:
- apiref
ms.openlocfilehash: 749ab286a86db07c1b66ff2b61ff073d15334800
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637880"
---
# <a name="_efn_getmanagedobjectfieldinfo-function"></a><span data-ttu-id="aca7f-103">\_EFN \_ GetManagedObjectFieldInfo 函数</span><span class="sxs-lookup"><span data-stu-id="aca7f-103">\_EFN\_GetManagedObjectFieldInfo Function</span></span>

<span data-ttu-id="aca7f-104">使用提供的对象指针和字段名，获取从对象的开头到字段和字段值的偏移量。</span><span class="sxs-lookup"><span data-stu-id="aca7f-104">Gets the offset from the start of an object to a field and the field's value, using the provided object pointer and field name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aca7f-105">语法</span><span class="sxs-lookup"><span data-stu-id="aca7f-105">Syntax</span></span>  
  
```cpp  
HRESULT _EFN_GetManagedObjectFieldInfo(  
    [in]  PDEBUG_CLIENT Client,  
    [in]  ULONG64       objAddr,  
    [in]  __out_ecount (mdNameLen) PSTR szFieldName,  
    [out] PULONG64      pValue,  
    [out] PULONG        pOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aca7f-106">参数</span><span class="sxs-lookup"><span data-stu-id="aca7f-106">Parameters</span></span>  

 `Client`  
 <span data-ttu-id="aca7f-107">中指向调试客户端的指针。</span><span class="sxs-lookup"><span data-stu-id="aca7f-107">[in] A pointer to the debug client.</span></span>  
  
 `objAddr`  
 <span data-ttu-id="aca7f-108">中托管对象指针。</span><span class="sxs-lookup"><span data-stu-id="aca7f-108">[in] A managed object pointer.</span></span>  
  
 <span data-ttu-id="aca7f-109">szFieldName</span><span class="sxs-lookup"><span data-stu-id="aca7f-109">szFieldName</span></span>  
 <span data-ttu-id="aca7f-110">中指向字段名称的托管对象指针。</span><span class="sxs-lookup"><span data-stu-id="aca7f-110">[in] A managed object pointer to the field name.</span></span>  
  
 `pValue`  
 <span data-ttu-id="aca7f-111">弄字段值。</span><span class="sxs-lookup"><span data-stu-id="aca7f-111">[out] The field value.</span></span> <span data-ttu-id="aca7f-112">此参数可以为 null。</span><span class="sxs-lookup"><span data-stu-id="aca7f-112">This parameter can be null.</span></span>  
  
 `pOffset`  
 <span data-ttu-id="aca7f-113">弄与字段的偏移量 `objAddr` 。</span><span class="sxs-lookup"><span data-stu-id="aca7f-113">[out] The offset from `objAddr` to the field.</span></span> <span data-ttu-id="aca7f-114">此参数可以为 null。</span><span class="sxs-lookup"><span data-stu-id="aca7f-114">This parameter can be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aca7f-115">备注</span><span class="sxs-lookup"><span data-stu-id="aca7f-115">Remarks</span></span>  

 <span data-ttu-id="aca7f-116">如果偏移量为0，则不写入偏移量。</span><span class="sxs-lookup"><span data-stu-id="aca7f-116">If the offset is 0, no offset is written.</span></span>  
  
 <span data-ttu-id="aca7f-117">如果当前上下文中的线程上没有托管代码，则该函数将返回具有0xa0 的工具值的 HRESULT SOS_E_NOMANAGEDCODE 和错误代码0x1000。</span><span class="sxs-lookup"><span data-stu-id="aca7f-117">If there is no managed code on the thread currently in context, the function returns HRESULT SOS_E_NOMANAGEDCODE with a facility value of 0xa0 and an error code of 0x1000.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aca7f-118">要求</span><span class="sxs-lookup"><span data-stu-id="aca7f-118">Requirements</span></span>  

 <span data-ttu-id="aca7f-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aca7f-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aca7f-120">**标头：** SOS_Stacktrace。h</span><span class="sxs-lookup"><span data-stu-id="aca7f-120">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="aca7f-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aca7f-121">**.NET Framework Version:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aca7f-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="aca7f-122">See also</span></span>

- [<span data-ttu-id="aca7f-123">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="aca7f-123">Debugging Global Static Functions</span></span>](debugging-global-static-functions.md)
