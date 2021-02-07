---
description: 了解详细信息： ICLRDataTarget：： GetTLSValue 方法
title: ICLRDataTarget::GetTLSValue 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetTLSValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetTLSValue
helpviewer_keywords:
- GetTLSValue method [.NET Framework debugging]
- ICLRDataTarget::GetTLSValue method [.NET Framework debugging]
ms.assetid: 0d8a7730-edc9-4728-898f-41b219cf5a28
topic_type:
- apiref
ms.openlocfilehash: 5c0c4a462d89c2eceada4180ea532f36fc9e48b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718039"
---
# <a name="iclrdatatargetgettlsvalue-method"></a><span data-ttu-id="5aa97-103">ICLRDataTarget::GetTLSValue 方法</span><span class="sxs-lookup"><span data-stu-id="5aa97-103">ICLRDataTarget::GetTLSValue Method</span></span>

<span data-ttu-id="5aa97-104">从线程本地存储区中获取一个值，该值在目标进程中指定线程 (TLS) 。</span><span class="sxs-lookup"><span data-stu-id="5aa97-104">Gets a value from the thread local storage (TLS) of the specified thread in the target process.</span></span> <span data-ttu-id="5aa97-105">此方法由公共语言运行时 (CLR) 数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="5aa97-105">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5aa97-106">语法</span><span class="sxs-lookup"><span data-stu-id="5aa97-106">Syntax</span></span>  
  
```cpp  
HRESULT GetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [out] CLRDATA_ADDRESS   *value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5aa97-107">参数</span><span class="sxs-lookup"><span data-stu-id="5aa97-107">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="5aa97-108">中目标进程中的线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="5aa97-108">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `index`  
 <span data-ttu-id="5aa97-109">中位置的索引。</span><span class="sxs-lookup"><span data-stu-id="5aa97-109">[in] The index of the location.</span></span> <span data-ttu-id="5aa97-110">此值必须是指定线程的本地存储区中的有效索引。</span><span class="sxs-lookup"><span data-stu-id="5aa97-110">This value must be a valid index in the local store of the specified thread.</span></span>  
  
 `value`  
 <span data-ttu-id="5aa97-111">弄一个指向 `CLRDATA_ADDRESS` 值的指针，该值指定从给定的 TLS 位置返回的值。</span><span class="sxs-lookup"><span data-stu-id="5aa97-111">[out] A pointer to a `CLRDATA_ADDRESS` value that specifies the value returned from the given TLS location.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5aa97-112">备注</span><span class="sxs-lookup"><span data-stu-id="5aa97-112">Remarks</span></span>  

 <span data-ttu-id="5aa97-113">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="5aa97-113">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5aa97-114">要求</span><span class="sxs-lookup"><span data-stu-id="5aa97-114">Requirements</span></span>  

 <span data-ttu-id="5aa97-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5aa97-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5aa97-116">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="5aa97-116">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="5aa97-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5aa97-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5aa97-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5aa97-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5aa97-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="5aa97-119">See also</span></span>

- [<span data-ttu-id="5aa97-120">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="5aa97-120">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
