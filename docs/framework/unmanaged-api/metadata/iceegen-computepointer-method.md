---
description: 了解详细信息： ICeeGen：： ComputePointer 方法
title: ICeeGen::ComputePointer 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.ComputePointer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::ComputePointer
helpviewer_keywords:
- ICeeGen::ComputePointer method [.NET Framework metadata]
- ComputePointer method [.NET Framework metadata]
ms.assetid: b6b95c04-0f2c-4fcc-a8bc-3b1dcbdba731
topic_type:
- apiref
ms.openlocfilehash: 9319343cc93eae3e4c7b060239d23ad8aeb7d3e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721167"
---
# <a name="iceegencomputepointer-method"></a><span data-ttu-id="f363b-103">ICeeGen::ComputePointer 方法</span><span class="sxs-lookup"><span data-stu-id="f363b-103">ICeeGen::ComputePointer Method</span></span>

<span data-ttu-id="f363b-104">确定指定代码节的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="f363b-104">Determines the buffer for the specified code section.</span></span>  
  
 <span data-ttu-id="f363b-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="f363b-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f363b-106">语法</span><span class="sxs-lookup"><span data-stu-id="f363b-106">Syntax</span></span>  
  
```cpp  
HRESULT ComputePointer (  
    [in]  HCEESECTION  section,  
    [in]  ULONG        RVA,
    [out] UCHAR        **lpBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f363b-107">参数</span><span class="sxs-lookup"><span data-stu-id="f363b-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="f363b-108">中要为其返回缓冲区的代码部分。</span><span class="sxs-lookup"><span data-stu-id="f363b-108">[in] The code section for which to return a buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="f363b-109">中要为其获取指针的方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="f363b-109">[in] The relative virtual address of the method for which to get a pointer.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="f363b-110">弄指向返回的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="f363b-110">[out] A pointer to the returned buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f363b-111">要求</span><span class="sxs-lookup"><span data-stu-id="f363b-111">Requirements</span></span>  

 <span data-ttu-id="f363b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f363b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f363b-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f363b-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f363b-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f363b-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f363b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f363b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f363b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f363b-116">See also</span></span>

- [<span data-ttu-id="f363b-117">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="f363b-117">ICeeGen Interface</span></span>](iceegen-interface.md)
