---
description: 了解详细信息： IHostMemoryManager：： NeedsVirtualAddressSpace 方法
title: IHostMemoryManager::NeedsVirtualAddressSpace 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.NeedsVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::NeedsVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::NeedsVirtualAddressSpace method [.NET Framework hosting]
- NeedsVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: 71f0eab5-0170-46f8-9f88-1df5abdeb34a
topic_type:
- apiref
ms.openlocfilehash: 95d4128decffc82fdcb198155b48a31420f71220
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707782"
---
# <a name="ihostmemorymanagerneedsvirtualaddressspace-method"></a><span data-ttu-id="dcfec-103">IHostMemoryManager::NeedsVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="dcfec-103">IHostMemoryManager::NeedsVirtualAddressSpace Method</span></span>

<span data-ttu-id="dcfec-104">向宿主通知公共语言运行时 (CLR) 将要尝试使用指定的内存。</span><span class="sxs-lookup"><span data-stu-id="dcfec-104">Notifies the host that the common language runtime (CLR) is going to attempt to use the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcfec-105">语法</span><span class="sxs-lookup"><span data-stu-id="dcfec-105">Syntax</span></span>  
  
```cpp  
HRESULT NeedsVirtualAddressSpace (  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dcfec-106">参数</span><span class="sxs-lookup"><span data-stu-id="dcfec-106">Parameters</span></span>  

 `startAddress`  
 <span data-ttu-id="dcfec-107">中内存的起始地址。</span><span class="sxs-lookup"><span data-stu-id="dcfec-107">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="dcfec-108">中内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="dcfec-108">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dcfec-109">备注</span><span class="sxs-lookup"><span data-stu-id="dcfec-109">Remarks</span></span>  

 <span data-ttu-id="dcfec-110">`NeedsVirtualAddressSpace`方法是一个回调方法，必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="dcfec-110">The `NeedsVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="dcfec-111">它由 CLR 调用。</span><span class="sxs-lookup"><span data-stu-id="dcfec-111">It is called by the CLR.</span></span>  
  
 <span data-ttu-id="dcfec-112">如果主机不希望 CLR 使用指定的内存，则它可能会返回 E_OUTOFMEMORY HRESULT。</span><span class="sxs-lookup"><span data-stu-id="dcfec-112">If the host does not want the CLR to use the specified memory, it may return an E_OUTOFMEMORY HRESULT.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dcfec-113">要求</span><span class="sxs-lookup"><span data-stu-id="dcfec-113">Requirements</span></span>  

 <span data-ttu-id="dcfec-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dcfec-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dcfec-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="dcfec-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dcfec-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dcfec-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dcfec-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dcfec-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dcfec-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="dcfec-118">See also</span></span>

- [<span data-ttu-id="dcfec-119">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="dcfec-119">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
