---
description: 了解详细信息： ICLRStrongName：： StrongNameGetBlobFromImage 方法
title: ICLRStrongName::StrongNameGetBlobFromImage 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameGetBlobFromImage method [.NET Framework hosting]
ms.assetid: 0f5a2ec8-e776-4fd8-bda6-937b6834575a
topic_type:
- apiref
ms.openlocfilehash: 32f04e21f1f08f3872ccdd27a64f39ea29d7e060
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799611"
---
# <a name="iclrstrongnamestrongnamegetblobfromimage-method"></a><span data-ttu-id="08b2d-103">ICLRStrongName::StrongNameGetBlobFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="08b2d-103">ICLRStrongName::StrongNameGetBlobFromImage Method</span></span>

<span data-ttu-id="08b2d-104">获取指定内存地址处程序集映像的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="08b2d-104">Gets a binary representation of the assembly image at the specified memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08b2d-105">语法</span><span class="sxs-lookup"><span data-stu-id="08b2d-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08b2d-106">参数</span><span class="sxs-lookup"><span data-stu-id="08b2d-106">Parameters</span></span>  

 `pbBase`  
 <span data-ttu-id="08b2d-107">中映射的程序集清单的内存地址。</span><span class="sxs-lookup"><span data-stu-id="08b2d-107">[in] The memory address of the mapped assembly manifest.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="08b2d-108">中中图像的大小（以字节为单位） `pbBase` 。</span><span class="sxs-lookup"><span data-stu-id="08b2d-108">[in] The size, in bytes, of the image at `pbBase`.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="08b2d-109">中包含图像的二进制表示形式的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="08b2d-109">[in] A buffer to contain the binary representation of the image.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="08b2d-110">[in，out]请求的最大大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="08b2d-110">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="08b2d-111">返回时，的实际大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="08b2d-111">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08b2d-112">返回值</span><span class="sxs-lookup"><span data-stu-id="08b2d-112">Return Value</span></span>  

 <span data-ttu-id="08b2d-113">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="08b2d-113">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08b2d-114">要求</span><span class="sxs-lookup"><span data-stu-id="08b2d-114">Requirements</span></span>  

 <span data-ttu-id="08b2d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08b2d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08b2d-116">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="08b2d-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="08b2d-117">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="08b2d-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="08b2d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08b2d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08b2d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="08b2d-119">See also</span></span>

- [<span data-ttu-id="08b2d-120">StrongNameGetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="08b2d-120">StrongNameGetBlob Method</span></span>](iclrstrongname-strongnamegetblob-method.md)
- [<span data-ttu-id="08b2d-121">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="08b2d-121">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
