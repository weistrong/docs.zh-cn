---
description: 了解详细信息： IHostMemoryManager：： AcquiredVirtualAddressSpace 方法
title: IHostMemoryManager::AcquiredVirtualAddressSpace 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.AcquiredVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::AcquiredVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::AcquiredVirtualAddressSpace method [.NET Framework hosting]
- AcquiredVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: ef2f83c2-127e-4c38-8385-306c03cd2167
topic_type:
- apiref
ms.openlocfilehash: 70424c5bf907cfc3fb2e8951464335323f9331f4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707899"
---
# <a name="ihostmemorymanageracquiredvirtualaddressspace-method"></a><span data-ttu-id="a3e17-103">IHostMemoryManager::AcquiredVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="a3e17-103">IHostMemoryManager::AcquiredVirtualAddressSpace Method</span></span>

<span data-ttu-id="a3e17-104">向宿主通知公共语言运行时 (CLR) 已从操作系统中获取指定内存。</span><span class="sxs-lookup"><span data-stu-id="a3e17-104">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3e17-105">语法</span><span class="sxs-lookup"><span data-stu-id="a3e17-105">Syntax</span></span>  
  
```cpp  
HRESULT AcquiredVirtualAddressSpace(  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a3e17-106">参数</span><span class="sxs-lookup"><span data-stu-id="a3e17-106">Parameters</span></span>  

 `startAddress`  
 <span data-ttu-id="a3e17-107">中内存的起始地址。</span><span class="sxs-lookup"><span data-stu-id="a3e17-107">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="a3e17-108">中内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a3e17-108">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a3e17-109">备注</span><span class="sxs-lookup"><span data-stu-id="a3e17-109">Remarks</span></span>  

 <span data-ttu-id="a3e17-110">`AcquiredVirtualAddressSpace`方法是一个回调方法，必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="a3e17-110">The `AcquiredVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="a3e17-111">它由 CLR 调用。</span><span class="sxs-lookup"><span data-stu-id="a3e17-111">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3e17-112">要求</span><span class="sxs-lookup"><span data-stu-id="a3e17-112">Requirements</span></span>  

 <span data-ttu-id="a3e17-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a3e17-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3e17-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a3e17-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a3e17-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3e17-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3e17-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3e17-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3e17-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a3e17-117">See also</span></span>

- [<span data-ttu-id="a3e17-118">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="a3e17-118">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
