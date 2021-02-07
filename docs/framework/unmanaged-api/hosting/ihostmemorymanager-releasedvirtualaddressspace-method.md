---
description: 了解详细信息： IHostMemoryManager：： ReleasedVirtualAddressSpace 方法
title: IHostMemoryManager::ReleasedVirtualAddressSpace 方法
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.ReleasedVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::ReleasedVirtualAddressSpace
helpviewer_keywords:
- ReleasedVirtualAddressSpace method [.NET Framework hosting]
- IHostMemoryManager::ReleasedVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: d1876601-6ab9-48e1-8ebd-184af1d0cd76
topic_type:
- apiref
ms.openlocfilehash: e67e80018b5002bdf2a50530af9ab057696fff4c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707763"
---
# <a name="ihostmemorymanagerreleasedvirtualaddressspace-method"></a><span data-ttu-id="49d19-103">IHostMemoryManager::ReleasedVirtualAddressSpace 方法</span><span class="sxs-lookup"><span data-stu-id="49d19-103">IHostMemoryManager::ReleasedVirtualAddressSpace Method</span></span>

<span data-ttu-id="49d19-104">向宿主通知公共语言运行时 (CLR) 已使用指定内存完成。</span><span class="sxs-lookup"><span data-stu-id="49d19-104">Notifies the host that the common language runtime (CLR) has finished using the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49d19-105">语法</span><span class="sxs-lookup"><span data-stu-id="49d19-105">Syntax</span></span>  
  
```cpp  
HRESULT ReleasedVirtualAddressSpace(  
    [in] LPVOID startAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="49d19-106">参数</span><span class="sxs-lookup"><span data-stu-id="49d19-106">Parameters</span></span>  

 `startAddress`  
 <span data-ttu-id="49d19-107">中指向要释放的内存的起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="49d19-107">[in] Pointer to the starting address of the memory to be released.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="49d19-108">备注</span><span class="sxs-lookup"><span data-stu-id="49d19-108">Remarks</span></span>  

 <span data-ttu-id="49d19-109">`ReleasedVirtualAddressSpace`方法是一个回调方法，必须由宿主应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="49d19-109">The `ReleasedVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="49d19-110">它由 CLR 调用。</span><span class="sxs-lookup"><span data-stu-id="49d19-110">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49d19-111">要求</span><span class="sxs-lookup"><span data-stu-id="49d19-111">Requirements</span></span>  

 <span data-ttu-id="49d19-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49d19-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49d19-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="49d19-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="49d19-114">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="49d19-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="49d19-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49d19-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49d19-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="49d19-116">See also</span></span>

- [<span data-ttu-id="49d19-117">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="49d19-117">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)
