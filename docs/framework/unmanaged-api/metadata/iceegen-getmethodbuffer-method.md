---
description: 了解详细信息： ICeeGen：： GetMethodBuffer 方法
title: ICeeGen::GetMethodBuffer 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetMethodBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetMethodBuffer
helpviewer_keywords:
- ICeeGen::GetMethodBuffer method [.NET Framework metadata]
- GetMethodBuffer method [.NET Framework metadata]
ms.assetid: c7c5b39a-d4ac-41f1-9d1e-44163f563a49
topic_type:
- apiref
ms.openlocfilehash: 24811f231b1db6d985753d4f4695f432aa12edc2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706924"
---
# <a name="iceegengetmethodbuffer-method"></a><span data-ttu-id="3e8ed-103">ICeeGen::GetMethodBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="3e8ed-103">ICeeGen::GetMethodBuffer Method</span></span>

<span data-ttu-id="3e8ed-104">获取指定的相对虚拟地址处的方法的适当大小的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="3e8ed-104">Gets a buffer of the appropriate size for the method at the specified relative virtual address.</span></span>  
  
 <span data-ttu-id="3e8ed-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="3e8ed-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e8ed-106">语法</span><span class="sxs-lookup"><span data-stu-id="3e8ed-106">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodBuffer (  
    [in]  ULONG       RVA,  
    [out] UCHAR       **lpBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e8ed-107">参数</span><span class="sxs-lookup"><span data-stu-id="3e8ed-107">Parameters</span></span>  

 `RVA`  
 <span data-ttu-id="3e8ed-108">中要为其返回缓冲区的方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="3e8ed-108">[in] The relative virtual address of the method for which to return a buffer.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="3e8ed-109">弄指向返回的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="3e8ed-109">[out] A pointer to the returned buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e8ed-110">要求</span><span class="sxs-lookup"><span data-stu-id="3e8ed-110">Requirements</span></span>  

 <span data-ttu-id="3e8ed-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3e8ed-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e8ed-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3e8ed-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3e8ed-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3e8ed-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3e8ed-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e8ed-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e8ed-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e8ed-115">See also</span></span>

- [<span data-ttu-id="3e8ed-116">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="3e8ed-116">ICeeGen Interface</span></span>](iceegen-interface.md)
