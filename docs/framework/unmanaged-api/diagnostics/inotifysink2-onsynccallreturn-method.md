---
description: 了解详细信息： INotifySink2：： OnSyncCallReturn 方法
title: INotifySink2::OnSyncCallReturn 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallReturn
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallReturn
helpviewer_keywords:
- OnSyncCallReturn method [.NET Framework debugging]
- INotifySink2::OnSyncCallReturn method [.NET Framework debugging]
ms.assetid: c1bda761-6292-4750-a14b-7d5db8f33456
topic_type:
- apiref
ms.openlocfilehash: 01518de4e5a9e1374edddadb3c49f16e8fe679a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800248"
---
# <a name="inotifysink2onsynccallreturn-method"></a><span data-ttu-id="fd37c-103">INotifySink2::OnSyncCallReturn 方法</span><span class="sxs-lookup"><span data-stu-id="fd37c-103">INotifySink2::OnSyncCallReturn Method</span></span>

<span data-ttu-id="fd37c-104">当调用返回时调用。</span><span class="sxs-lookup"><span data-stu-id="fd37c-104">Gets invoked when a call returns.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd37c-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd37c-105">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallReturn  
(  
    [in]  CALL_ID   in_CallID,  
    [in, size_is(in_BufferSize)] BYTE*  in_pBuffer,  
    [in]  DWORD     in_BufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd37c-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd37c-106">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="fd37c-107">中从其返回的调用的 ID。</span><span class="sxs-lookup"><span data-stu-id="fd37c-107">[in] ID of the call being returned from.</span></span> <span data-ttu-id="fd37c-108">请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="fd37c-108">See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `in_pBuffer`  
 <span data-ttu-id="fd37c-109">中调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="fd37c-109">[in] Call buffer.</span></span>  
  
 `in_BufferSize`  
 <span data-ttu-id="fd37c-110">中调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="fd37c-110">[in] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd37c-111">返回值</span><span class="sxs-lookup"><span data-stu-id="fd37c-111">Return Value</span></span>  

 <span data-ttu-id="fd37c-112">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="fd37c-112">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd37c-113">要求</span><span class="sxs-lookup"><span data-stu-id="fd37c-113">Requirements</span></span>  

 <span data-ttu-id="fd37c-114">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="fd37c-114">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd37c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd37c-115">See also</span></span>

- [<span data-ttu-id="fd37c-116">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="fd37c-116">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="fd37c-117">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="fd37c-117">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="fd37c-118">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="fd37c-118">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
