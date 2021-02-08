---
description: 了解详细信息： ICLRDataTarget3：： GetExceptionThreadID 方法
title: ICLRDataTarget3::GetExceptionThreadID 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICLRDataTarget3.GetExceptionThreadID
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 307d6ac7-4a86-45f3-999d-6b47004a68f2
topic_type:
- apiref
ms.openlocfilehash: 8202b6d83d0c81853111c5da7cfb8deec4d4e222
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794814"
---
# <a name="iclrdatatarget3getexceptionthreadid-method"></a><span data-ttu-id="e5eaa-103">ICLRDataTarget3::GetExceptionThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="e5eaa-103">ICLRDataTarget3::GetExceptionThreadID Method</span></span>

<span data-ttu-id="e5eaa-104">由公共语言运行时 (CLR) 数据访问服务调用，从而获取引发异常的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-104">Called by the common language runtime (CLR) data access services to get the ID of the thread that threw the exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5eaa-105">语法</span><span class="sxs-lookup"><span data-stu-id="e5eaa-105">Syntax</span></span>  
  
```cpp  
HRESULT GetExceptionThreadID(  
    [out] ULONG32* threadID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5eaa-106">参数</span><span class="sxs-lookup"><span data-stu-id="e5eaa-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="e5eaa-107">[out] 引发异常的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-107">[out] The ID of the thread that threw the exception.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e5eaa-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e5eaa-108">Return Value</span></span>  

 <span data-ttu-id="e5eaa-109">如果成功，则返回值是 `S_OK`；如果失败，则返回失败 `HRESULT` 代码。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-109">The return value is `S_OK` on success, or a failure `HRESULT` code on failure.</span></span> <span data-ttu-id="e5eaa-110">`HRESULT` 代码可以包括但不限于以下代码：</span><span class="sxs-lookup"><span data-stu-id="e5eaa-110">The `HRESULT` codes can include but are not limited to the following:</span></span>  
  
|<span data-ttu-id="e5eaa-111">返回代码</span><span class="sxs-lookup"><span data-stu-id="e5eaa-111">Return code</span></span>|<span data-ttu-id="e5eaa-112">描述</span><span class="sxs-lookup"><span data-stu-id="e5eaa-112">Description</span></span>|  
|-----------------|-----------------|  
|`S_OK`|<span data-ttu-id="e5eaa-113">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-113">Method succeeded.</span></span>|  
|`HRESULT_FROM_WIN32(ERROR_NOT_FOUND)`|<span data-ttu-id="e5eaa-114">找不到该异常的有效线程 ID。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-114">Could not find a valid thread ID for the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5eaa-115">备注</span><span class="sxs-lookup"><span data-stu-id="e5eaa-115">Remarks</span></span>  

 <span data-ttu-id="e5eaa-116">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-116">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5eaa-117">要求</span><span class="sxs-lookup"><span data-stu-id="e5eaa-117">Requirements</span></span>  

 <span data-ttu-id="e5eaa-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e5eaa-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5eaa-119">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="e5eaa-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="e5eaa-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5eaa-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5eaa-121">**.NET Framework 版本：**[!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e5eaa-121">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5eaa-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5eaa-122">See also</span></span>

- [<span data-ttu-id="e5eaa-123">ICLRDataTarget3 接口</span><span class="sxs-lookup"><span data-stu-id="e5eaa-123">ICLRDataTarget3 Interface</span></span>](iclrdatatarget3-interface.md)
- [<span data-ttu-id="e5eaa-124">GetExceptionContextRecord 方法</span><span class="sxs-lookup"><span data-stu-id="e5eaa-124">GetExceptionContextRecord Method</span></span>](iclrdatatarget3-getexceptioncontextrecord-method.md)
- [<span data-ttu-id="e5eaa-125">GetExceptionRecord 方法</span><span class="sxs-lookup"><span data-stu-id="e5eaa-125">GetExceptionRecord Method</span></span>](iclrdatatarget3-getexceptionrecord-method.md)
