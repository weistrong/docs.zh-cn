---
description: 了解详细信息： GetCORRequiredVersion 函数
title: GetCORRequiredVersion 函数
ms.date: 03/30/2017
api_name:
- GetCORRequiredVersion
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetCORRequiredVersion
helpviewer_keywords:
- GetCORRequiredVersion function [.NET Framework hosting]
ms.assetid: 1588fe7b-c378-4f4b-9c4b-48647f1119cc
topic_type:
- apiref
ms.openlocfilehash: ea1b928054e3ec6080b00e2a41228035f50c0f84
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785349"
---
# <a name="getcorrequiredversion-function"></a><span data-ttu-id="fb5c9-103">GetCORRequiredVersion 函数</span><span class="sxs-lookup"><span data-stu-id="fb5c9-103">GetCORRequiredVersion Function</span></span>

<span data-ttu-id="fb5c9-104">获取 CLR) 版本号 (所需的公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-104">Gets the required common language runtime (CLR) version number.</span></span>  
  
 <span data-ttu-id="fb5c9-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb5c9-106">语法</span><span class="sxs-lookup"><span data-stu-id="fb5c9-106">Syntax</span></span>  
  
```cpp  
HRESULT GetCORRequiredVersion (  
    [out] LPWSTR   pbuffer,  
    [in]  DWORD    cchBuffer,  
    [out] DWORD   *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb5c9-107">参数</span><span class="sxs-lookup"><span data-stu-id="fb5c9-107">Parameters</span></span>  

 `pbuffer`  
 <span data-ttu-id="fb5c9-108">弄包含指定版本号的字符串的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-108">[out] A buffer containing a string that specifies the version number.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="fb5c9-109">中缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-109">[in] The size, in bytes, of the buffer.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="fb5c9-110">弄缓冲区中返回的字节数。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-110">[out] The number of bytes returned in the buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb5c9-111">要求</span><span class="sxs-lookup"><span data-stu-id="fb5c9-111">Requirements</span></span>  

 <span data-ttu-id="fb5c9-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb5c9-113">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="fb5c9-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fb5c9-114">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fb5c9-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fb5c9-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fb5c9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb5c9-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="fb5c9-116">See also</span></span>

- [<span data-ttu-id="fb5c9-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="fb5c9-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
