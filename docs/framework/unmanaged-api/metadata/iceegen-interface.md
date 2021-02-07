---
description: 了解详细信息： ICeeGen 接口
title: ICeeGen 接口
ms.date: 03/30/2017
api_name:
- ICeeGen
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen
helpviewer_keywords:
- ICeeGen interface [.NET Framework metadata]
ms.assetid: 383d20b0-efe9-4e71-8fb8-1186b2e7d0c0
topic_type:
- apiref
ms.openlocfilehash: 43e9e0696523346ffbcf0b8823a48ed2c9c359e4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706807"
---
# <a name="iceegen-interface"></a><span data-ttu-id="3bfcb-103">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="3bfcb-103">ICeeGen Interface</span></span>

<span data-ttu-id="3bfcb-104">提供用于动态代码编译的方法。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-104">Provides methods for dynamic code compilation.</span></span>  
  
 <span data-ttu-id="3bfcb-105">此接口已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-105">This interface is obsolete and should not be used.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3bfcb-106">方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-106">Methods</span></span>  
  
|<span data-ttu-id="3bfcb-107">方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-107">Method</span></span>|<span data-ttu-id="3bfcb-108">说明</span><span class="sxs-lookup"><span data-stu-id="3bfcb-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3bfcb-109">AddSectionReloc 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-109">AddSectionReloc Method</span></span>](iceegen-addsectionreloc-method.md)|<span data-ttu-id="3bfcb-110">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-110">Obsolete.</span></span> <span data-ttu-id="3bfcb-111">将 .reloc 指令添加到基本代码。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-111">Adds a .reloc instruction to the code base.</span></span>|  
|[<span data-ttu-id="3bfcb-112">AllocateMethodBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-112">AllocateMethodBuffer Method</span></span>](iceegen-allocatemethodbuffer-method.md)|<span data-ttu-id="3bfcb-113">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-113">Obsolete.</span></span> <span data-ttu-id="3bfcb-114">为方法创建指定大小的缓冲区，并获取该方法的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-114">Creates a buffer of the specified size for a method, and gets the relative virtual address of the method.</span></span>|  
|[<span data-ttu-id="3bfcb-115">ComputePointer 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-115">ComputePointer Method</span></span>](iceegen-computepointer-method.md)|<span data-ttu-id="3bfcb-116">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-116">Obsolete.</span></span> <span data-ttu-id="3bfcb-117">确定指定代码节的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-117">Determines the buffer for the specified code section.</span></span>|  
|[<span data-ttu-id="3bfcb-118">EmitString 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-118">EmitString Method</span></span>](iceegen-emitstring-method.md)|<span data-ttu-id="3bfcb-119">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-119">Obsolete.</span></span> <span data-ttu-id="3bfcb-120">向基本代码发出指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-120">Emits the specified string into the code base.</span></span>|  
|[<span data-ttu-id="3bfcb-121">GenerateCeeFile 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-121">GenerateCeeFile Method</span></span>](iceegen-generateceefile-method.md)|<span data-ttu-id="3bfcb-122">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-122">Obsolete.</span></span> <span data-ttu-id="3bfcb-123">生成一个代码基文件，其中包含当前加载到此中的代码库 `ICeeGen` 。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-123">Generates a code-base file that contains the code base currently loaded into this `ICeeGen`.</span></span>|  
|[<span data-ttu-id="3bfcb-124">GenerateCeeMemoryImage 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-124">GenerateCeeMemoryImage Method</span></span>](iceegen-generateceememoryimage-method.md)|<span data-ttu-id="3bfcb-125">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-125">Obsolete.</span></span> <span data-ttu-id="3bfcb-126">为基本代码在内存中生成一个图像。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-126">Generates an image in memory for the code base.</span></span>|  
|[<span data-ttu-id="3bfcb-127">GetIlSection 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-127">GetIlSection Method</span></span>](iceegen-getilsection-method.md)|<span data-ttu-id="3bfcb-128">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-128">Obsolete.</span></span> <span data-ttu-id="3bfcb-129">获取由指定句柄引用的中间语言代码库的部分。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-129">Gets the section of the intermediate language code base referenced by the specified handle.</span></span>|  
|[<span data-ttu-id="3bfcb-130">GetIMapTokenIface 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-130">GetIMapTokenIface Method</span></span>](iceegen-getimaptokeniface-method.md)|<span data-ttu-id="3bfcb-131">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-131">Obsolete.</span></span> <span data-ttu-id="3bfcb-132">获取指定的标记所引用的接口。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-132">Gets the interface referenced by the specified token.</span></span>|  
|[<span data-ttu-id="3bfcb-133">GetMethodBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-133">GetMethodBuffer Method</span></span>](iceegen-getmethodbuffer-method.md)|<span data-ttu-id="3bfcb-134">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-134">Obsolete.</span></span> <span data-ttu-id="3bfcb-135">获取指定的相对虚拟地址处的方法的适当大小的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-135">Gets a buffer of the appropriate size for the method at the specified relative virtual address.</span></span>|  
|[<span data-ttu-id="3bfcb-136">GetSectionBlock 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-136">GetSectionBlock Method</span></span>](iceegen-getsectionblock-method.md)|<span data-ttu-id="3bfcb-137">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-137">Obsolete.</span></span> <span data-ttu-id="3bfcb-138">获取代码库的节块。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-138">Gets a section block of the code base.</span></span>|  
|[<span data-ttu-id="3bfcb-139">GetSectionCreate 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-139">GetSectionCreate Method</span></span>](iceegen-getsectioncreate-method.md)|<span data-ttu-id="3bfcb-140">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-140">Obsolete.</span></span> <span data-ttu-id="3bfcb-141">使用指定的名称和标志值生成并获取代码部分。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-141">Generates and gets a code section using the specified name and flag values.</span></span>|  
|[<span data-ttu-id="3bfcb-142">GetSectionDataLen 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-142">GetSectionDataLen Method</span></span>](iceegen-getsectiondatalen-method.md)|<span data-ttu-id="3bfcb-143">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-143">Obsolete.</span></span> <span data-ttu-id="3bfcb-144">获取指定节的长度。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-144">Gets the length of the specified section.</span></span>|  
|[<span data-ttu-id="3bfcb-145">GetString 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-145">GetString Method</span></span>](iceegen-getstring-method.md)|<span data-ttu-id="3bfcb-146">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-146">Obsolete.</span></span> <span data-ttu-id="3bfcb-147">获取存储在指定的相对虚拟地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-147">Gets the string stored at the specified relative virtual address.</span></span>|  
|[<span data-ttu-id="3bfcb-148">GetStringSection 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-148">GetStringSection Method</span></span>](iceegen-getstringsection-method.md)|<span data-ttu-id="3bfcb-149">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-149">Obsolete.</span></span> <span data-ttu-id="3bfcb-150">获取由指定句柄引用的代码段的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-150">Gets a string representation of the code section referenced by the specified handle.</span></span>|  
|[<span data-ttu-id="3bfcb-151">TruncateSection 方法</span><span class="sxs-lookup"><span data-stu-id="3bfcb-151">TruncateSection Method</span></span>](iceegen-truncatesection-method.md)|<span data-ttu-id="3bfcb-152">已过时。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-152">Obsolete.</span></span> <span data-ttu-id="3bfcb-153">按指定长度截断指定的代码段。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-153">Truncates the specified code section by the specified length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3bfcb-154">要求</span><span class="sxs-lookup"><span data-stu-id="3bfcb-154">Requirements</span></span>  

 <span data-ttu-id="3bfcb-155">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfcb-155">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3bfcb-156">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="3bfcb-156">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3bfcb-157">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3bfcb-157">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3bfcb-158">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3bfcb-158">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3bfcb-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="3bfcb-159">See also</span></span>

- [<span data-ttu-id="3bfcb-160">元数据接口</span><span class="sxs-lookup"><span data-stu-id="3bfcb-160">Metadata Interfaces</span></span>](metadata-interfaces.md)
