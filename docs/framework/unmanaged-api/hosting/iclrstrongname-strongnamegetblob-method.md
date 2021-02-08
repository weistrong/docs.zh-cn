---
description: 了解详细信息： ICLRStrongName：： StrongNameGetBlob 方法
title: ICLRStrongName::StrongNameGetBlob 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameGetBlob
- ICLRStrongName.StrongNameGetBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameGetBlob
helpviewer_keywords:
- ICLRStrongName::StrongNameGetBlob method [.NET Framework hosting]
- StrongNameGetBlob method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: a24218f8-7196-44be-b7a2-ee9cdd7a85c4
topic_type:
- apiref
ms.openlocfilehash: 2b63ebd9c48ad18eef60f83c68fe412a4bd0d94f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799624"
---
# <a name="iclrstrongnamestrongnamegetblob-method"></a><span data-ttu-id="8567c-103">ICLRStrongName::StrongNameGetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="8567c-103">ICLRStrongName::StrongNameGetBlob Method</span></span>

<span data-ttu-id="8567c-104">使用指定地址处可执行文件的二进制表示形式填充指定的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="8567c-104">Fills the specified buffer with the binary representation of the executable file at the specified address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8567c-105">语法</span><span class="sxs-lookup"><span data-stu-id="8567c-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameGetBlob (  
    [in]  LPCWSTR    wszFilePath,  
    [in]  BYTE       *pbBlob,  
    [in, out] DWORD  *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8567c-106">参数</span><span class="sxs-lookup"><span data-stu-id="8567c-106">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="8567c-107">中要加载的可执行文件的有效路径。</span><span class="sxs-lookup"><span data-stu-id="8567c-107">[in] A valid path to the executable file to be loaded.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="8567c-108">中要在其中加载可执行文件的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="8567c-108">[in] The buffer into which to load the executable file.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="8567c-109">[in，out]请求的最大大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="8567c-109">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="8567c-110">返回时，的实际大小（以字节为单位） `pbBlob` 。</span><span class="sxs-lookup"><span data-stu-id="8567c-110">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8567c-111">返回值</span><span class="sxs-lookup"><span data-stu-id="8567c-111">Return Value</span></span>  

 <span data-ttu-id="8567c-112">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="8567c-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8567c-113">要求</span><span class="sxs-lookup"><span data-stu-id="8567c-113">Requirements</span></span>  

 <span data-ttu-id="8567c-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8567c-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8567c-115">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="8567c-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8567c-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8567c-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8567c-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8567c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8567c-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="8567c-118">See also</span></span>

- [<span data-ttu-id="8567c-119">StrongNameGetBlobFromImage 方法</span><span class="sxs-lookup"><span data-stu-id="8567c-119">StrongNameGetBlobFromImage Method</span></span>](iclrstrongname-strongnamegetblobfromimage-method.md)
- [<span data-ttu-id="8567c-120">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="8567c-120">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
