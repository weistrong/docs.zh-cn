---
description: 了解详细信息： CeeSectionRelocType 枚举
title: CeeSectionRelocType 枚举
ms.date: 03/30/2017
api_name:
- CeeSectionRelocType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionRelocType
helpviewer_keywords:
- CeeSectionRelocType enumeration [.NET Framework metadata]
ms.assetid: 124656f6-0dad-4ceb-9043-d3869ab65cde
topic_type:
- apiref
ms.openlocfilehash: 49f7b39b3cc4c2e71dd3e4e426d0ca787e9ac0b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678830"
---
# <a name="ceesectionreloctype-enumeration"></a><span data-ttu-id="77c7e-103">CeeSectionRelocType 枚举</span><span class="sxs-lookup"><span data-stu-id="77c7e-103">CeeSectionRelocType Enumeration</span></span>

<span data-ttu-id="77c7e-104">提供一些值，以影响对 `reloc` [ICeeGen：： AddSectionReloc](iceegen-addsectionreloc-method.md)的调用中发出的指令的类型。</span><span class="sxs-lookup"><span data-stu-id="77c7e-104">Provides values to influence the type of `reloc` instruction emitted in a call to [ICeeGen::AddSectionReloc](iceegen-addsectionreloc-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77c7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="77c7e-105">Syntax</span></span>  
  
```cpp  
typedef enum  {  
    srRelocAbsolute,  
    srRelocHighLow          = 3,  
    srRelocHighAdj,
    srRelocMapToken,  
    srRelocRelative,  
    srRelocFilePos,  
    srRelocCodeRelative,  
    srRelocIA64Imm64,  
    srRelocDir64,  
    srRelocIA64PcRel25,  
    srRelocIA64PcRel64,    srRelocAbsoluteTagged,    srRelocSentinel,    srNoBaseReloc       = 0x4000,  
    srRelocPtr          = 0x8000,  
    srRelocAbsolutePtr      = srRelocPtr + srRelocAbsolute,  
    srRelocHighLowPtr       = srRelocPtr + srRelocHighLow,  
    srRelocRelativePtr      = srRelocPtr + srRelocRelative,  
    srRelocIA64Imm64Ptr     = srRelocPtr + srRelocIA64Imm64,  
    srRelocDir64Ptr         = srRelocPtr + srRelocDir64  
    } CeeSectionRelocType;  
```  
  
## <a name="members"></a><span data-ttu-id="77c7e-106">成员</span><span class="sxs-lookup"><span data-stu-id="77c7e-106">Members</span></span>  
  
|<span data-ttu-id="77c7e-107">成员</span><span class="sxs-lookup"><span data-stu-id="77c7e-107">Member</span></span>|<span data-ttu-id="77c7e-108">说明</span><span class="sxs-lookup"><span data-stu-id="77c7e-108">Description</span></span>|  
|------------|-----------------|  
|`srRelocAbsolute`|<span data-ttu-id="77c7e-109">仅生成一个相对节 `reloc` ，不向 .reloc 节发送任何内容。</span><span class="sxs-lookup"><span data-stu-id="77c7e-109">Generates only a section-relative `reloc`, sending nothing into a .reloc section.</span></span>|  
|`srRelocHighLow`|<span data-ttu-id="77c7e-110">`reloc`为指针大小的位置生成。</span><span class="sxs-lookup"><span data-stu-id="77c7e-110">Generates a `reloc` for a pointer-sized location.</span></span> <span data-ttu-id="77c7e-111">这会根据平台转换为 BASED_HIGHLOW 或 BASED_DIR64。</span><span class="sxs-lookup"><span data-stu-id="77c7e-111">This is transformed into BASED_HIGHLOW or BASED_DIR64 depending on the platform.</span></span>|  
|`srRelocHighAdj`|<span data-ttu-id="77c7e-112">`reloc`为32位数字的前16位生成，其中后16位包含在 .reloc 表中的下一个单词中。</span><span class="sxs-lookup"><span data-stu-id="77c7e-112">Generates a `reloc` for the top 16 bits of a 32-bit number, where the bottom 16 bits are included in the next word in the .reloc table.</span></span>|  
|`srRelocMapToken`|<span data-ttu-id="77c7e-113">生成一个标记映射重定位，无需将其发送到 .reloc 部分。</span><span class="sxs-lookup"><span data-stu-id="77c7e-113">Generates a token map relocation, sending nothing into a .reloc section.</span></span>|  
|`srRelocRelative`|<span data-ttu-id="77c7e-114">指示值是相对地址链接地址。</span><span class="sxs-lookup"><span data-stu-id="77c7e-114">Indicates that the value is a relative address fixup.</span></span>|  
|`srRelocFilePos`|<span data-ttu-id="77c7e-115">仅生成一个相对节 `reloc` ，不向 .reloc 节发送任何内容。</span><span class="sxs-lookup"><span data-stu-id="77c7e-115">Generates only a section-relative `reloc`, sending nothing into a .reloc section.</span></span> <span data-ttu-id="77c7e-116">这与 `reloc` 节的文件位置相关，而不是部分的虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="77c7e-116">This `reloc` is relative to the file position of the section, not the section's virtual address.</span></span>|  
|`srRelocCodeRelative`|<span data-ttu-id="77c7e-117">指定代码相对地址链接地址。</span><span class="sxs-lookup"><span data-stu-id="77c7e-117">Specifies a code-relative address fixup.</span></span>|  
|`srRelocIA64Imm64`|<span data-ttu-id="77c7e-118">`reloc`为 ia64 指令中的64位地址生成 `movl` 。</span><span class="sxs-lookup"><span data-stu-id="77c7e-118">Generates a `reloc` for a 64 bit address in an ia64 `movl` instruction.</span></span>|  
|`srRelocDir64`|<span data-ttu-id="77c7e-119">`reloc`为64位地址生成。</span><span class="sxs-lookup"><span data-stu-id="77c7e-119">Generates a `reloc` for a 64-bit address.</span></span>|  
|`srRelocIA64PcRel25`|<span data-ttu-id="77c7e-120">`reloc`为 ia64 指令中的25位 PC 相对地址生成 `br.call` 。</span><span class="sxs-lookup"><span data-stu-id="77c7e-120">Generate a `reloc` for a 25-bit PC-relative address in an ia64 `br.call` instruction.</span></span>|  
|`srRelocIA64PcRel64`|<span data-ttu-id="77c7e-121">`reloc`为 ia64 指令中的64位电脑相对地址生成 `brl.call` 。</span><span class="sxs-lookup"><span data-stu-id="77c7e-121">Generates a `reloc` for a 64-bit PC-relative address in an ia64 `brl.call` instruction.</span></span>|  
|`srRelocAbsoluteTagged`|<span data-ttu-id="77c7e-122">生成一个与标记的指针值相对应的30位部分 `reloc` 。</span><span class="sxs-lookup"><span data-stu-id="77c7e-122">Generates a 30-bit section-relative `reloc`, used for tagged pointer values.</span></span>|  
|`srRelocSentinel`|<span data-ttu-id="77c7e-123">一个 sentinel 值，用于帮助确保对此枚举的任何添加都反映到内部 `reloc` 名称数组中。</span><span class="sxs-lookup"><span data-stu-id="77c7e-123">A sentinel value to help ensure any additions to this enum are reflected to the internal `reloc` name array.</span></span>|  
|`srNoBaseReloc`|<span data-ttu-id="77c7e-124">指定不发出 base `reloc` 。</span><span class="sxs-lookup"><span data-stu-id="77c7e-124">Specifies not to emit a base `reloc`.</span></span>|  
|`srRelocPtr`|<span data-ttu-id="77c7e-125">一个值，该值指示内存的修正内容是指针而不是节偏移量。</span><span class="sxs-lookup"><span data-stu-id="77c7e-125">A value indicating that the pre-fixup contents of memory are a pointer rather than a section offset.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="77c7e-126">要求</span><span class="sxs-lookup"><span data-stu-id="77c7e-126">Requirements</span></span>  

 <span data-ttu-id="77c7e-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="77c7e-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77c7e-128">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="77c7e-128">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="77c7e-129">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="77c7e-129">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="77c7e-130">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77c7e-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77c7e-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="77c7e-131">See also</span></span>

- [<span data-ttu-id="77c7e-132">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="77c7e-132">Metadata Enumerations</span></span>](metadata-enumerations.md)
- [<span data-ttu-id="77c7e-133">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="77c7e-133">ICeeGen Interface</span></span>](iceegen-interface.md)
- [<span data-ttu-id="77c7e-134">AddSectionReloc 方法</span><span class="sxs-lookup"><span data-stu-id="77c7e-134">AddSectionReloc Method</span></span>](iceegen-addsectionreloc-method.md)
