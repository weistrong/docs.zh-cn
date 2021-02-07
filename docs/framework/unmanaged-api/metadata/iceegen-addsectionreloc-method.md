---
description: 了解详细信息： ICeeGen：： AddSectionReloc 方法
title: ICeeGen::AddSectionReloc 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.AddSectionReloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::AddSectionReloc
helpviewer_keywords:
- AddSectionReloc method [.NET Framework metadata]
- ICeeGen::AddSectionReloc method [.NET Framework metadata]
ms.assetid: b500a260-1d57-4953-95e1-c27063f7c8da
topic_type:
- apiref
ms.openlocfilehash: 715c506f0bdcb3fcef33b3e9165d1f9ae47c6073
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707171"
---
# <a name="iceegenaddsectionreloc-method"></a><span data-ttu-id="9739e-103">ICeeGen::AddSectionReloc 方法</span><span class="sxs-lookup"><span data-stu-id="9739e-103">ICeeGen::AddSectionReloc Method</span></span>

<span data-ttu-id="9739e-104">将 .reloc 指令添加到基本代码。</span><span class="sxs-lookup"><span data-stu-id="9739e-104">Adds a .reloc instruction to the code base.</span></span>  
  
 <span data-ttu-id="9739e-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="9739e-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9739e-106">语法</span><span class="sxs-lookup"><span data-stu-id="9739e-106">Syntax</span></span>  
  
```cpp  
HRESULT AddSectionReloc (  
   [in] HCEESECTION            section,  
   [in] ULONG                  offset,  
   [in] HCEESECTION            relativeTo,
   [in] CeeSectionRelocType    relocType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9739e-107">参数</span><span class="sxs-lookup"><span data-stu-id="9739e-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="9739e-108">中要将 .reloc 指令添加到的内存中代码部分。</span><span class="sxs-lookup"><span data-stu-id="9739e-108">[in] The section of in-memory code to which to add a .reloc instruction.</span></span>  
  
 `offset`  
 <span data-ttu-id="9739e-109">中部分的偏移量。</span><span class="sxs-lookup"><span data-stu-id="9739e-109">[in] The offset of the section.</span></span>  
  
 `relativeTo`  
 <span data-ttu-id="9739e-110">中引用的部分 `offset` 。</span><span class="sxs-lookup"><span data-stu-id="9739e-110">[in] The section to which `offset` refers.</span></span>  
  
 `relocType`  
 <span data-ttu-id="9739e-111">中 [CeeSectionRelocType](ceesectionreloctype-enumeration.md) 值之一，指示要添加的 .reloc 指令的类型。</span><span class="sxs-lookup"><span data-stu-id="9739e-111">[in] One of the [CeeSectionRelocType](ceesectionreloctype-enumeration.md) values, indicating the kind of .reloc instruction to add.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9739e-112">要求</span><span class="sxs-lookup"><span data-stu-id="9739e-112">Requirements</span></span>  

 <span data-ttu-id="9739e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9739e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9739e-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9739e-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9739e-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9739e-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9739e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9739e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9739e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9739e-117">See also</span></span>

- [<span data-ttu-id="9739e-118">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="9739e-118">ICeeGen Interface</span></span>](iceegen-interface.md)
