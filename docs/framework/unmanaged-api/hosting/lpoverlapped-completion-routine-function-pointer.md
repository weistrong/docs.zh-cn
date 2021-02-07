---
description: 了解详细信息： LPOVERLAPPED_COMPLETION_ROUTINE 函数指针
title: LPOVERLAPPED_COMPLETION_ROUTINE 函数指针
ms.date: 03/30/2017
api_name:
- LPOVERLAPPED_COMPLETION_ROUTINE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- LPOVERLAPPED_COMPLETION_ROUTINE
helpviewer_keywords:
- LPOVERLAPPED_COMPLETION_ROUTINE function pointer [.NET Framework hosting]
ms.assetid: 5fb645d9-b818-401c-8c2c-c30d86de58ba
topic_type:
- apiref
ms.openlocfilehash: 6645e6a9746404a4ae355a22cf16e6d164c63bed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679818"
---
# <a name="lpoverlapped_completion_routine-function-pointer"></a><span data-ttu-id="24c4c-103">LPOVERLAPPED_COMPLETION_ROUTINE 函数指针</span><span class="sxs-lookup"><span data-stu-id="24c4c-103">LPOVERLAPPED_COMPLETION_ROUTINE Function Pointer</span></span>

<span data-ttu-id="24c4c-104">指向一个函数，该函数在重叠 (即设备的异步) i/o 完成时通知宿主。</span><span class="sxs-lookup"><span data-stu-id="24c4c-104">Points to a function that notifies the host when an overlapped (that is, asynchronous) I/O to a device has completed.</span></span>  
  
 <span data-ttu-id="24c4c-105">此函数指针在 .NET Framework 4 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="24c4c-105">This function pointer has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24c4c-106">语法</span><span class="sxs-lookup"><span data-stu-id="24c4c-106">Syntax</span></span>  
  
```cpp  
typedef VOID (*LPOVERLAPPED_COMPLETION_ROUTINE) (  
    [in] DWORD  dwErrorCode,  
    [in] DWORD  dwNumberOfBytesTransfered,  
    [in] LPVOID lpOverlapped  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="24c4c-107">参数</span><span class="sxs-lookup"><span data-stu-id="24c4c-107">Parameters</span></span>  

 `dwErrorCode`  
 <span data-ttu-id="24c4c-108">中如果设备已关闭，则为错误代码的值;否则，此值为零。</span><span class="sxs-lookup"><span data-stu-id="24c4c-108">[in] A value that is an error code if the device has been closed; otherwise, this value is zero.</span></span>  
  
 <span data-ttu-id="24c4c-109">关闭设备会导致设备的所有挂起的 i/o 立即完成。</span><span class="sxs-lookup"><span data-stu-id="24c4c-109">Closing a device causes all pending I/O to the device to be completed immediately.</span></span>  
  
 `dwNumberOfBytesTransfered`  
 <span data-ttu-id="24c4c-110">中I/o 操作传输的字节数。</span><span class="sxs-lookup"><span data-stu-id="24c4c-110">[in] The number of bytes transferred by the I/O operation.</span></span>  
  
 `lpOverlapped`  
 <span data-ttu-id="24c4c-111">中指向结构的指针，该结构包含用于完成 i/o 请求的信息。</span><span class="sxs-lookup"><span data-stu-id="24c4c-111">[in] A pointer to a structure that contains information to be used to complete the I/O request.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="24c4c-112">备注</span><span class="sxs-lookup"><span data-stu-id="24c4c-112">Remarks</span></span>  

 <span data-ttu-id="24c4c-113">指向该函数的 `LPOVERLAPPED_COMPLETION_ROUTINE` 点是回调函数，并且必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="24c4c-113">The function to which `LPOVERLAPPED_COMPLETION_ROUTINE` points is a callback function and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="24c4c-114">回调函数允许主机处理已完成的 i/o 请求。</span><span class="sxs-lookup"><span data-stu-id="24c4c-114">The callback function allows the host to process the completed I/O request.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24c4c-115">要求</span><span class="sxs-lookup"><span data-stu-id="24c4c-115">Requirements</span></span>  

 <span data-ttu-id="24c4c-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24c4c-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24c4c-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="24c4c-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="24c4c-118">**库：** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="24c4c-118">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="24c4c-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24c4c-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24c4c-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="24c4c-120">See also</span></span>

- [<span data-ttu-id="24c4c-121">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="24c4c-121">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
