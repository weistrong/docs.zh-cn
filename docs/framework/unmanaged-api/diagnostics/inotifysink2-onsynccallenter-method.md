---
description: 了解详细信息： INotifySink2：： OnSyncCallEnter 方法
title: INotifySink2::OnSyncCallEnter 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallEnter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallEnter
helpviewer_keywords:
- INotifySink2::OnSyncCallEnter method [.NET Framework debugging]
- OnSyncCallEnter method [.NET Framework debugging]
ms.assetid: e33265be-c25d-4145-ad02-c3e89d6f26c1
topic_type:
- apiref
ms.openlocfilehash: e7537b16ec8ea8d92ad92498c1bfdac5a9de6475
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800274"
---
# <a name="inotifysink2onsynccallenter-method"></a><span data-ttu-id="6e1aa-103">INotifySink2::OnSyncCallEnter 方法</span><span class="sxs-lookup"><span data-stu-id="6e1aa-103">INotifySink2::OnSyncCallEnter Method</span></span>

<span data-ttu-id="6e1aa-104">在输入调用时调用。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-104">Gets invoked when entering a call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e1aa-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e1aa-105">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallEnter  
(  
    [in]  CALL_ID   in_CallID,  
    [in, size_is(in_BufferSize)] BYTE*  in_pBuffer,  
    [in]  DWORD     in_BufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e1aa-106">参数</span><span class="sxs-lookup"><span data-stu-id="6e1aa-106">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="6e1aa-107">中正在输入的调用的 ID。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-107">[in] ID of the call being entered.</span></span> <span data-ttu-id="6e1aa-108">请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-108">See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `in_pBuffer`  
 <span data-ttu-id="6e1aa-109">中调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-109">[in] Call buffer.</span></span>  
  
 `in_BufferSize`  
 <span data-ttu-id="6e1aa-110">中调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-110">[in] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6e1aa-111">返回值</span><span class="sxs-lookup"><span data-stu-id="6e1aa-111">Return Value</span></span>  

 <span data-ttu-id="6e1aa-112">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="6e1aa-112">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e1aa-113">要求</span><span class="sxs-lookup"><span data-stu-id="6e1aa-113">Requirements</span></span>  

 <span data-ttu-id="6e1aa-114">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="6e1aa-114">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e1aa-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e1aa-115">See also</span></span>

- [<span data-ttu-id="6e1aa-116">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="6e1aa-116">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="6e1aa-117">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="6e1aa-117">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="6e1aa-118">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="6e1aa-118">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
