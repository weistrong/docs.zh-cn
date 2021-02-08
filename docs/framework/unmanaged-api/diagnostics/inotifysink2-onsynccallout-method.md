---
description: 了解详细信息： INotifySink2：： OnSyncCallOut 方法
title: INotifySink2::OnSyncCallOut 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallOut
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallOut
helpviewer_keywords:
- INotifySink2::OnSyncCallOut method [.NET Framework debugging]
- OnSyncCallOut method [.NET Framework debugging]
ms.assetid: 97f15656-8677-4079-8553-a1d8603355d6
topic_type:
- apiref
ms.openlocfilehash: 03028b138a7d95c618ae20530f66aa692d314cab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800235"
---
# <a name="inotifysink2onsynccallout-method"></a><span data-ttu-id="61fe8-103">INotifySink2::OnSyncCallOut 方法</span><span class="sxs-lookup"><span data-stu-id="61fe8-103">INotifySink2::OnSyncCallOut Method</span></span>

<span data-ttu-id="61fe8-104">在调用时调用。</span><span class="sxs-lookup"><span data-stu-id="61fe8-104">Gets invoked when a call is out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61fe8-105">语法</span><span class="sxs-lookup"><span data-stu-id="61fe8-105">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallOut  
(  
    [in]  CALL_ID  in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*   out_pBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61fe8-106">参数</span><span class="sxs-lookup"><span data-stu-id="61fe8-106">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="61fe8-107">中传出的调用的 ID。请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="61fe8-107">[in] ID of the call that is out. See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="61fe8-108">弄调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="61fe8-108">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="61fe8-109">弄调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="61fe8-109">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="61fe8-110">返回值</span><span class="sxs-lookup"><span data-stu-id="61fe8-110">Return Value</span></span>  

 <span data-ttu-id="61fe8-111">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="61fe8-111">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61fe8-112">要求</span><span class="sxs-lookup"><span data-stu-id="61fe8-112">Requirements</span></span>  

 <span data-ttu-id="61fe8-113">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="61fe8-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61fe8-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="61fe8-114">See also</span></span>

- [<span data-ttu-id="61fe8-115">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="61fe8-115">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="61fe8-116">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="61fe8-116">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="61fe8-117">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="61fe8-117">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
