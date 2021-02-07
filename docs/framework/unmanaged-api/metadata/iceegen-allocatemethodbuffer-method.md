---
description: 了解详细信息： ICeeGen：： AllocateMethodBuffer 方法
title: ICeeGen::AllocateMethodBuffer 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.AllocateMethodBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::AllocateMethodBuffer
helpviewer_keywords:
- AllocateMethodBuffer method [.NET Framework metadata]
- ICeeGen::AllocateMethodBuffer method [.NET Framework metadata]
ms.assetid: 845ab77e-9639-47f5-99fb-f3b619e3e779
topic_type:
- apiref
ms.openlocfilehash: ced5ac8b4fdd89fc41c2c70b68c5b49843a519e2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707132"
---
# <a name="iceegenallocatemethodbuffer-method"></a><span data-ttu-id="c2a55-103">ICeeGen::AllocateMethodBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="c2a55-103">ICeeGen::AllocateMethodBuffer Method</span></span>

<span data-ttu-id="c2a55-104">为方法创建指定大小的缓冲区，并获取该方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="c2a55-104">Creates a buffer of the specified size for a method, and gets the relative virtual address of the method.</span></span>  
  
 <span data-ttu-id="c2a55-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="c2a55-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2a55-106">语法</span><span class="sxs-lookup"><span data-stu-id="c2a55-106">Syntax</span></span>  
  
```cpp  
HRESULT AllocateMethodBuffer (
    [in]  ULONG    cchBuffer,
    [out] UCHAR    **lpBuffer,  
    [out] ULONG    *RVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2a55-107">参数</span><span class="sxs-lookup"><span data-stu-id="c2a55-107">Parameters</span></span>  

 `cchBuffer`  
 <span data-ttu-id="c2a55-108">中要创建的缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="c2a55-108">[in] The length of the buffer to create.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="c2a55-109">弄返回的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="c2a55-109">[out] The returned buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="c2a55-110">弄方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="c2a55-110">[out] The relative virtual address of the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2a55-111">要求</span><span class="sxs-lookup"><span data-stu-id="c2a55-111">Requirements</span></span>  

 <span data-ttu-id="c2a55-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c2a55-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2a55-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c2a55-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c2a55-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c2a55-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c2a55-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2a55-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2a55-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2a55-116">See also</span></span>

- [<span data-ttu-id="c2a55-117">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="c2a55-117">ICeeGen Interface</span></span>](iceegen-interface.md)
