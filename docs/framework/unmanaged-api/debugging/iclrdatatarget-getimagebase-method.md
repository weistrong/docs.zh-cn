---
description: 了解详细信息： ICLRDataTarget：： GetImageBase 方法
title: ICLRDataTarget::GetImageBase 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetImageBase
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetImageBase
helpviewer_keywords:
- ICLRDataTarget::GetImageBase method [.NET Framework debugging]
- GetImageBase method [.NET Framework debugging]
ms.assetid: 091c5f32-c160-49e3-a75f-4692e084c8e4
topic_type:
- apiref
ms.openlocfilehash: 34e8341b219aaa184b4894c631f854e0a31921d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794866"
---
# <a name="iclrdatatargetgetimagebase-method"></a><span data-ttu-id="ee8ca-103">ICLRDataTarget::GetImageBase 方法</span><span class="sxs-lookup"><span data-stu-id="ee8ca-103">ICLRDataTarget::GetImageBase Method</span></span>

<span data-ttu-id="ee8ca-104">获取指定的图像的基本内存地址。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-104">Gets the base memory address of the specified image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee8ca-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee8ca-105">Syntax</span></span>  
  
```cpp  
HRESULT GetImageBase (  
    [in, string] LPCWSTR    imagePath,  
    [out] CLRDATA_ADDRESS   *baseAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ee8ca-106">参数</span><span class="sxs-lookup"><span data-stu-id="ee8ca-106">Parameters</span></span>  

 `imagePath`  
 <span data-ttu-id="ee8ca-107">中图像的文件名，包括其路径。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-107">[in] The file name of the image, including its path.</span></span>  
  
 `baseAddress`  
 <span data-ttu-id="ee8ca-108">弄指向存储图像基址的 CLRDATA_ADDRESS 的指针。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-108">[out] A pointer to a CLRDATA_ADDRESS that stores the base address of the image.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ee8ca-109">备注</span><span class="sxs-lookup"><span data-stu-id="ee8ca-109">Remarks</span></span>  

 <span data-ttu-id="ee8ca-110">图像文件名可以是也可以没有路径。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-110">The image file name may or may not have a path.</span></span> <span data-ttu-id="ee8ca-111">如果指定了路径，则在整个路径上完成匹配;否则，仅对文件名执行匹配。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-111">If a path is specified, matching is done on the whole path; otherwise, matching is done only on the file name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee8ca-112">要求</span><span class="sxs-lookup"><span data-stu-id="ee8ca-112">Requirements</span></span>  

 <span data-ttu-id="ee8ca-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee8ca-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee8ca-114">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="ee8ca-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="ee8ca-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee8ca-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee8ca-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee8ca-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee8ca-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee8ca-117">See also</span></span>

- [<span data-ttu-id="ee8ca-118">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="ee8ca-118">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
