---
description: 了解详细信息： ICeeGen：： GetSectionBlock 方法
title: ICeeGen::GetSectionBlock 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionBlock
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionBlock
helpviewer_keywords:
- GetSectionBlock method [.NET Framework metadata]
- ICeeGen::GetSectionBlock method [.NET Framework metadata]
ms.assetid: 05c78aaf-5bbd-497e-9ae2-55f4fae0c5fb
topic_type:
- apiref
ms.openlocfilehash: d1a9fdeb35507f9dd6528b581be877049d2a1478
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721094"
---
# <a name="iceegengetsectionblock-method"></a><span data-ttu-id="d368f-103">ICeeGen::GetSectionBlock 方法</span><span class="sxs-lookup"><span data-stu-id="d368f-103">ICeeGen::GetSectionBlock Method</span></span>

<span data-ttu-id="d368f-104">获取代码库的节块。</span><span class="sxs-lookup"><span data-stu-id="d368f-104">Gets a section block of the code base.</span></span>  
  
 <span data-ttu-id="d368f-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="d368f-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d368f-106">语法</span><span class="sxs-lookup"><span data-stu-id="d368f-106">Syntax</span></span>  
  
```cpp  
HRESULT GetSectionBlock (  
    [in]  HCEESECTION    section,
    [in]  ULONG          len,  
    [in]  ULONG          align     = 1,  
    [out] void           **ppBytes = 0  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="d368f-107">参数</span><span class="sxs-lookup"><span data-stu-id="d368f-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="d368f-108">中要从中检索基本代码块的部分。</span><span class="sxs-lookup"><span data-stu-id="d368f-108">[in] The section from which to retrieve a block of the code base.</span></span>  
  
 `len`  
 <span data-ttu-id="d368f-109">中要检索的块的长度。</span><span class="sxs-lookup"><span data-stu-id="d368f-109">[in] The length of the block to be retrieved.</span></span>  
  
 `align`  
 <span data-ttu-id="d368f-110">中相对于部分开头的字节，用于对齐块的第一个字节。</span><span class="sxs-lookup"><span data-stu-id="d368f-110">[in] The byte, relative to the beginning of the section, with which to align the first byte of the block.</span></span> <span data-ttu-id="d368f-111">这是块在节中的位置。</span><span class="sxs-lookup"><span data-stu-id="d368f-111">This is the position of the block within the section.</span></span>  
  
 `ppBytes`  
 <span data-ttu-id="d368f-112">弄一个指针，指向接收检索到的块的地址的位置。</span><span class="sxs-lookup"><span data-stu-id="d368f-112">[out] A pointer to a location that receives the address of the retrieved block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d368f-113">备注</span><span class="sxs-lookup"><span data-stu-id="d368f-113">Remarks</span></span>  

 <span data-ttu-id="d368f-114">`GetSectionBlock`仅当有特殊部分的要求不是由其他方法处理时才调用。</span><span class="sxs-lookup"><span data-stu-id="d368f-114">Call `GetSectionBlock` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d368f-115">要求</span><span class="sxs-lookup"><span data-stu-id="d368f-115">Requirements</span></span>  

 <span data-ttu-id="d368f-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d368f-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d368f-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d368f-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d368f-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d368f-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d368f-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d368f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d368f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d368f-120">See also</span></span>

- [<span data-ttu-id="d368f-121">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="d368f-121">ICeeGen Interface</span></span>](iceegen-interface.md)
