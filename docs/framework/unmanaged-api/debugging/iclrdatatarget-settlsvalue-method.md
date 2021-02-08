---
description: 了解详细信息： ICLRDataTarget：： SetTLSValue 方法
title: ICLRDataTarget::SetTLSValue 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetTLSValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetTLSValue
helpviewer_keywords:
- ICLRDataTarget::SetTLSValue method [.NET Framework debugging]
- SetTLSValue method [.NET Framework debugging]
ms.assetid: 4a2d6a24-749a-47ad-9f01-4517203d3f35
topic_type:
- apiref
ms.openlocfilehash: 2432cd66f604575e35f171c98a0fb313c5ccd94e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785674"
---
# <a name="iclrdatatargetsettlsvalue-method"></a><span data-ttu-id="6cac1-103">ICLRDataTarget::SetTLSValue 方法</span><span class="sxs-lookup"><span data-stu-id="6cac1-103">ICLRDataTarget::SetTLSValue Method</span></span>

<span data-ttu-id="6cac1-104">在目标进程中指定线程 (TLS) 中设置一个值。</span><span class="sxs-lookup"><span data-stu-id="6cac1-104">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span> <span data-ttu-id="6cac1-105">此方法由公共语言运行时 (CLR) 数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="6cac1-105">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cac1-106">语法</span><span class="sxs-lookup"><span data-stu-id="6cac1-106">Syntax</span></span>  
  
```cpp  
HRESULT SetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [in] CLRDATA_ADDRESS    value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6cac1-107">参数</span><span class="sxs-lookup"><span data-stu-id="6cac1-107">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="6cac1-108">中目标进程中的线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="6cac1-108">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `index`  
 <span data-ttu-id="6cac1-109">中位置的索引。</span><span class="sxs-lookup"><span data-stu-id="6cac1-109">[in] The index of the location.</span></span> <span data-ttu-id="6cac1-110">此值必须是指定线程的本地存储区中的有效索引。</span><span class="sxs-lookup"><span data-stu-id="6cac1-110">This value must be a valid index in the local store of the specified thread.</span></span>  
  
 `value`  
 <span data-ttu-id="6cac1-111">中一个 `CLRDATA_ADDRESS` 值，该值指定要置于给定 TLS 位置的值。</span><span class="sxs-lookup"><span data-stu-id="6cac1-111">[in] A `CLRDATA_ADDRESS` value that specifies the value to place in the given TLS location.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6cac1-112">备注</span><span class="sxs-lookup"><span data-stu-id="6cac1-112">Remarks</span></span>  

 <span data-ttu-id="6cac1-113">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="6cac1-113">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6cac1-114">要求</span><span class="sxs-lookup"><span data-stu-id="6cac1-114">Requirements</span></span>  

 <span data-ttu-id="6cac1-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6cac1-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6cac1-116">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="6cac1-116">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6cac1-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6cac1-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6cac1-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6cac1-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cac1-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="6cac1-119">See also</span></span>

- [<span data-ttu-id="6cac1-120">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="6cac1-120">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
