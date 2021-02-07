---
description: 了解详细信息： ICLRDataTarget：： Request 方法
title: ICLRDataTarget::Request 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.Request
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::Request
helpviewer_keywords:
- ICLRDataTarget::Request method [.NET Framework debugging]
- Request method [.NET Framework debugging]
ms.assetid: 4723bd1c-eddb-4ed2-897a-010024a47e01
topic_type:
- apiref
ms.openlocfilehash: 75c400a51a2fdaf0044d85b5f483d783fae4628b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712150"
---
# <a name="iclrdatatargetrequest-method"></a><span data-ttu-id="8d59b-103">ICLRDataTarget::Request 方法</span><span class="sxs-lookup"><span data-stu-id="8d59b-103">ICLRDataTarget::Request Method</span></span>

<span data-ttu-id="8d59b-104">由公共语言运行时调用 (CLR) 数据访问服务请求操作，如实现所定义。</span><span class="sxs-lookup"><span data-stu-id="8d59b-104">Called by the common language runtime (CLR) data access services to request an operation, as defined by the implementation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d59b-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d59b-105">Syntax</span></span>  
  
```cpp  
HRESULT Request (  
    [in] ULONG32            reqCode,  
    [in] ULONG32            inBufferSize,  
    [in, size_is(inBufferSize)]
        BYTE                *inBuffer,  
    [in] ULONG32            outBufferSize,  
    [out, size_is(outBufferSize)]
        BYTE                *outBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8d59b-106">参数</span><span class="sxs-lookup"><span data-stu-id="8d59b-106">Parameters</span></span>  

 `reqCode`  
 <span data-ttu-id="8d59b-107">中用户定义的。</span><span class="sxs-lookup"><span data-stu-id="8d59b-107">[in] User-defined.</span></span>  
  
 `inBufferSize`  
 <span data-ttu-id="8d59b-108">中输入缓冲区的大小，该大小用于传入的请求。</span><span class="sxs-lookup"><span data-stu-id="8d59b-108">[in] The size of the input buffer, which is used for the incoming request.</span></span>  
  
 `inBuffer`  
 <span data-ttu-id="8d59b-109">中包含请求的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="8d59b-109">[in] A buffer containing the request.</span></span>  
  
 `outBufferSize`  
 <span data-ttu-id="8d59b-110">中用于响应的输出缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="8d59b-110">[in] The size of the output buffer, which is used for the response.</span></span>  
  
 `outBuffer`  
 <span data-ttu-id="8d59b-111">弄包含响应的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="8d59b-111">[out] A Buffer containing the response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d59b-112">备注</span><span class="sxs-lookup"><span data-stu-id="8d59b-112">Remarks</span></span>  

 <span data-ttu-id="8d59b-113">`Request`方法便于添加未指定的自定义操作。</span><span class="sxs-lookup"><span data-stu-id="8d59b-113">The `Request` method facilitates the addition of unspecified custom operations.</span></span> <span data-ttu-id="8d59b-114">也就是说，此方法提供了扩展性，无需版本的接口定义。</span><span class="sxs-lookup"><span data-stu-id="8d59b-114">That is, this method provides extensibility without requiring revision of the interface definition.</span></span>  
  
 <span data-ttu-id="8d59b-115">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="8d59b-115">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d59b-116">要求</span><span class="sxs-lookup"><span data-stu-id="8d59b-116">Requirements</span></span>  

 <span data-ttu-id="8d59b-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d59b-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d59b-118">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="8d59b-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="8d59b-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d59b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8d59b-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d59b-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d59b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d59b-121">See also</span></span>

- [<span data-ttu-id="8d59b-122">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="8d59b-122">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
