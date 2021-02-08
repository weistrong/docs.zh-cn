---
description: 了解详细信息： ICLRDataTarget3 接口
title: ICLRDataTarget3 接口
ms.date: 03/30/2017
api_name:
- ICLRDataTarget3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d2711bdf-64b3-404c-a0c3-01ba4907f703
topic_type:
- apiref
ms.openlocfilehash: deea609298563e60897f9bedab9fb1e175dc7b73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794784"
---
# <a name="iclrdatatarget3-interface"></a><span data-ttu-id="0ede8-103">ICLRDataTarget3 接口</span><span class="sxs-lookup"><span data-stu-id="0ede8-103">ICLRDataTarget3 Interface</span></span>

<span data-ttu-id="0ede8-104">提供对异常信息的访问的 [ICLRDataTarget2](iclrdatatarget2-interface.md) 的子类。</span><span class="sxs-lookup"><span data-stu-id="0ede8-104">A subclass of [ICLRDataTarget2](iclrdatatarget2-interface.md) that provides access to exception information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0ede8-105">方法</span><span class="sxs-lookup"><span data-stu-id="0ede8-105">Methods</span></span>  
  
|<span data-ttu-id="0ede8-106">方法</span><span class="sxs-lookup"><span data-stu-id="0ede8-106">Method</span></span>|<span data-ttu-id="0ede8-107">说明</span><span class="sxs-lookup"><span data-stu-id="0ede8-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0ede8-108">GetExceptionRecord 方法</span><span class="sxs-lookup"><span data-stu-id="0ede8-108">GetExceptionRecord Method</span></span>](iclrdatatarget3-getexceptionrecord-method.md)|<span data-ttu-id="0ede8-109">由公共语言运行时 (CLR) 数据访问服务调用，以检索与目标进程关联的异常记录。</span><span class="sxs-lookup"><span data-stu-id="0ede8-109">Called by the common language runtime (CLR) data access services to retrieve the exception record associated with the target process.</span></span>|  
|[<span data-ttu-id="0ede8-110">GetExceptionContextRecord 方法</span><span class="sxs-lookup"><span data-stu-id="0ede8-110">GetExceptionContextRecord Method</span></span>](iclrdatatarget3-getexceptioncontextrecord-method.md)|<span data-ttu-id="0ede8-111">由公共语言运行时 (CLR) 数据访问服务调用，以检索与目标进程关联的上下文记录。</span><span class="sxs-lookup"><span data-stu-id="0ede8-111">Called by the CLR data access services to retrieve the context record associated with the target process.</span></span>|  
|[<span data-ttu-id="0ede8-112">GetExceptionThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="0ede8-112">GetExceptionThreadID Method</span></span>](iclrdatatarget3-getexceptionthreadid-method.md)|<span data-ttu-id="0ede8-113">由 CLR 数据访问服务调用，从而获取引发异常的线程的 ID。</span><span class="sxs-lookup"><span data-stu-id="0ede8-113">Called by the CLR data access services to get the ID of the thread that threw the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ede8-114">备注</span><span class="sxs-lookup"><span data-stu-id="0ede8-114">Remarks</span></span>  

 <span data-ttu-id="0ede8-115">API 客户端（即调试器）必须针对特定的目标进程实现此接口。</span><span class="sxs-lookup"><span data-stu-id="0ede8-115">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="0ede8-116">例如，活动进程的实现将不同于内存转储的。</span><span class="sxs-lookup"><span data-stu-id="0ede8-116">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="0ede8-117">目标可能不支持对其内存区域的修改。</span><span class="sxs-lookup"><span data-stu-id="0ede8-117">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ede8-118">要求</span><span class="sxs-lookup"><span data-stu-id="0ede8-118">Requirements</span></span>  

 <span data-ttu-id="0ede8-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0ede8-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ede8-120">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="0ede8-120">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="0ede8-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ede8-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ede8-122">**.NET Framework 版本：**[!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0ede8-122">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ede8-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ede8-123">See also</span></span>

- [<span data-ttu-id="0ede8-124">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="0ede8-124">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
- [<span data-ttu-id="0ede8-125">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="0ede8-125">ICLRDataTarget2 Interface</span></span>](iclrdatatarget2-interface.md)
- [<span data-ttu-id="0ede8-126">调试接口</span><span class="sxs-lookup"><span data-stu-id="0ede8-126">Debugging Interfaces</span></span>](debugging-interfaces.md)
