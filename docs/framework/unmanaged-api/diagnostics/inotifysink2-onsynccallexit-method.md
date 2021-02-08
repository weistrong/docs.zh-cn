---
description: 了解详细信息： INotifySink2：： OnSyncCallExit 方法
title: INotifySink2::OnSyncCallExit 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallExit
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallExit
helpviewer_keywords:
- INotifySink2::OnSyncCallExit method [.NET Framework debugging]
- OnSyncCallExit method [.NET Framework debugging]
ms.assetid: d9d7600e-a8f5-443a-96de-67d26e130f2d
topic_type:
- apiref
ms.openlocfilehash: 2de55c3b7956576049e4ad65b2cb6fbc69fa84af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800261"
---
# <a name="inotifysink2onsynccallexit-method"></a><span data-ttu-id="59ea2-103">INotifySink2::OnSyncCallExit 方法</span><span class="sxs-lookup"><span data-stu-id="59ea2-103">INotifySink2::OnSyncCallExit Method</span></span>

<span data-ttu-id="59ea2-104">在退出调用时调用。</span><span class="sxs-lookup"><span data-stu-id="59ea2-104">Gets invoked when exiting a call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59ea2-105">语法</span><span class="sxs-lookup"><span data-stu-id="59ea2-105">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallExit  
(  
    [in]  CALL_ID   in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*    out_pBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="59ea2-106">参数</span><span class="sxs-lookup"><span data-stu-id="59ea2-106">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="59ea2-107">中正在退出的调用的 ID。</span><span class="sxs-lookup"><span data-stu-id="59ea2-107">[in] ID of the call being exited.</span></span> <span data-ttu-id="59ea2-108">请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="59ea2-108">See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="59ea2-109">弄调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="59ea2-109">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="59ea2-110">弄调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="59ea2-110">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59ea2-111">返回值</span><span class="sxs-lookup"><span data-stu-id="59ea2-111">Return Value</span></span>  

 <span data-ttu-id="59ea2-112">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="59ea2-112">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59ea2-113">要求</span><span class="sxs-lookup"><span data-stu-id="59ea2-113">Requirements</span></span>  

 <span data-ttu-id="59ea2-114">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="59ea2-114">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59ea2-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="59ea2-115">See also</span></span>

- [<span data-ttu-id="59ea2-116">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="59ea2-116">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="59ea2-117">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="59ea2-117">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="59ea2-118">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="59ea2-118">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
