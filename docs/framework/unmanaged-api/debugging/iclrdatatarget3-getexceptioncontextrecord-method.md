---
description: 了解详细信息： ICLRDataTarget3：： GetExceptionContextRecord 方法
title: ICLRDataTarget3::GetExceptionContextRecord 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICLRDataTarget3.GetContextRecord
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 66076ed5-f05c-4114-9788-94cb143abb8a
topic_type:
- apiref
ms.openlocfilehash: c722eaaf0f9935bc7adaa69a1792f934f631a728
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794827"
---
# <a name="iclrdatatarget3getexceptioncontextrecord-method"></a><span data-ttu-id="0ac4d-103">ICLRDataTarget3::GetExceptionContextRecord 方法</span><span class="sxs-lookup"><span data-stu-id="0ac4d-103">ICLRDataTarget3::GetExceptionContextRecord Method</span></span>

<span data-ttu-id="0ac4d-104">由公共语言运行时 (CLR) 数据访问服务调用，以检索与目标进程关联的上下文记录。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-104">Called by the common language runtime (CLR) data access services to retrieve the context record associated with the target process.</span></span> <span data-ttu-id="0ac4d-105">例如，对于转储目标，此操作等效于通过 `ExceptionParam` Windows 调试帮助库中的 [MiniDumpWriteDump](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函数的参数传入的上下文记录 (dbghelp.dll) 。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-105">For example, for a dump target, this would be equivalent to the context record passed in via the `ExceptionParam` argument to the [MiniDumpWriteDump](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function in the Windows Debug Help Library (DbgHelp).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ac4d-106">语法</span><span class="sxs-lookup"><span data-stu-id="0ac4d-106">Syntax</span></span>  
  
```cpp  
HRESULT GetExceptionContextRecord(  
    [in] ULONG32 bufferSize,  
    [out] ULONG32* bufferUsed,  
    [out, size_is(bufferSize)] BYTE* buffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0ac4d-107">参数</span><span class="sxs-lookup"><span data-stu-id="0ac4d-107">Parameters</span></span>  

 `bufferSize`  
 <span data-ttu-id="0ac4d-108">[in] 输入缓冲区大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-108">[in] The input buffer size, in bytes.</span></span> <span data-ttu-id="0ac4d-109">此大小必须大到足以容纳上下文记录。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-109">This must be large enough to accommodate the context record.</span></span>  
  
 `bufferUsed`  
 <span data-ttu-id="0ac4d-110">[out] 指向接收实际写入缓冲区的字节数的 `ULONG32` 类型的指针。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-110">[out] A pointer to a `ULONG32` type that receives the number of bytes actually written to the buffer.</span></span>  
  
 `buffer`  
 <span data-ttu-id="0ac4d-111">[out] 指向接收上下文记录副本的内存缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-111">[out] A pointer to a memory buffer that receives a copy of the context record.</span></span> <span data-ttu-id="0ac4d-112">异常记录作为 [上下文](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) 类型返回。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-112">The exception record is returned as a [CONTEXT](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0ac4d-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0ac4d-113">Return Value</span></span>  

 <span data-ttu-id="0ac4d-114">如果成功，则返回值是 `S_OK`；如果失败，则返回失败 `HRESULT` 代码。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-114">The return value is `S_OK` on success, or a failure `HRESULT` code on failure.</span></span> <span data-ttu-id="0ac4d-115">`HRESULT` 代码可以包括但不限于以下代码：</span><span class="sxs-lookup"><span data-stu-id="0ac4d-115">The `HRESULT` codes can include but are not limited to the following:</span></span>  
  
|<span data-ttu-id="0ac4d-116">返回代码</span><span class="sxs-lookup"><span data-stu-id="0ac4d-116">Return code</span></span>|<span data-ttu-id="0ac4d-117">描述</span><span class="sxs-lookup"><span data-stu-id="0ac4d-117">Description</span></span>|  
|-----------------|-----------------|  
|`S_OK`|<span data-ttu-id="0ac4d-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-118">Method succeeded.</span></span> <span data-ttu-id="0ac4d-119">已将上下文记录复制到输出缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-119">The context record has been copied to the output buffer.</span></span>|  
|`HRESULT_FROM_WIN32(ERROR_NOT_FOUND)`|<span data-ttu-id="0ac4d-120">没有与目标关联的上下文记录。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-120">No context record is associated with the target.</span></span>|  
|`HRESULT_FROM_WIN32(ERROR_BAD_LENGTH)`|<span data-ttu-id="0ac4d-121">输入缓冲区大小不足以容纳上下文记录。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-121">The input buffer size is not large enough to accommodate the context record.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ac4d-122">备注</span><span class="sxs-lookup"><span data-stu-id="0ac4d-122">Remarks</span></span>  

 <span data-ttu-id="0ac4d-123">[上下文](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) 是在 Windows SDK 提供的标头中定义的特定于平台的结构。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-123">[CONTEXT](/windows/win32/api/winnt/ns-winnt-arm64_nt_context) is a platform-specific structure defined in headers provided by the Windows SDK.</span></span>  
  
 <span data-ttu-id="0ac4d-124">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-124">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ac4d-125">要求</span><span class="sxs-lookup"><span data-stu-id="0ac4d-125">Requirements</span></span>  

 <span data-ttu-id="0ac4d-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0ac4d-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ac4d-127">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="0ac4d-127">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="0ac4d-128">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ac4d-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ac4d-129">**.NET Framework 版本：**[!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0ac4d-129">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ac4d-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ac4d-130">See also</span></span>

- [<span data-ttu-id="0ac4d-131">ICLRDataTarget3 接口</span><span class="sxs-lookup"><span data-stu-id="0ac4d-131">ICLRDataTarget3 Interface</span></span>](iclrdatatarget3-interface.md)
- [<span data-ttu-id="0ac4d-132">GetExceptionRecord 方法</span><span class="sxs-lookup"><span data-stu-id="0ac4d-132">GetExceptionRecord Method</span></span>](iclrdatatarget3-getexceptionrecord-method.md)
- [<span data-ttu-id="0ac4d-133">GetExceptionThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="0ac4d-133">GetExceptionThreadID Method</span></span>](iclrdatatarget3-getexceptionthreadid-method.md)
