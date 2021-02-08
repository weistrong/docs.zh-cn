---
description: 了解详细信息： GetFileVersion 函数
title: GetFileVersion 函数
ms.date: 03/30/2017
api_name:
- GetFileVersion
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetFileVersion
helpviewer_keywords:
- GetFileVersion function [.NET Framework hosting]
ms.assetid: b3222c85-da88-4485-97d7-3a6ee3e8d358
topic_type:
- apiref
ms.openlocfilehash: 7de19484f2f8123d61eb94e6a5ae09f56a3b5541
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785297"
---
# <a name="getfileversion-function"></a><span data-ttu-id="a1c28-103">GetFileVersion 函数</span><span class="sxs-lookup"><span data-stu-id="a1c28-103">GetFileVersion Function</span></span>

<span data-ttu-id="a1c28-104">使用指定的缓冲区获取公共语言运行时 (CLR) 指定文件的版本信息。</span><span class="sxs-lookup"><span data-stu-id="a1c28-104">Gets the common language runtime (CLR) version information of the specified file, using the specified buffer.</span></span>  
  
 <span data-ttu-id="a1c28-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="a1c28-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1c28-106">语法</span><span class="sxs-lookup"><span data-stu-id="a1c28-106">Syntax</span></span>  
  
```cpp  
HRESULT GetFileVersion (  
    [in]  LPCWSTR      szFilename,
    [in, out] LPWSTR   szBuffer,
    [in]  DWORD        cchBuffer,
    [out] DWORD        *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1c28-107">参数</span><span class="sxs-lookup"><span data-stu-id="a1c28-107">Parameters</span></span>  

 `szFilename`  
 <span data-ttu-id="a1c28-108">中要检查的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="a1c28-108">[in] The path of the file to be examined.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="a1c28-109">[in，out]为返回的版本信息分配的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="a1c28-109">[in, out] The buffer allocated for the version information that is returned.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="a1c28-110">中的大小（宽字符） `szBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="a1c28-110">[in] The size, in wide characters, of `szBuffer`.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="a1c28-111">弄返回的的大小（以字节为单位） `szBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="a1c28-111">[out] The size, in bytes, of the returned `szBuffer`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1c28-112">要求</span><span class="sxs-lookup"><span data-stu-id="a1c28-112">Requirements</span></span>  

 <span data-ttu-id="a1c28-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1c28-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1c28-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a1c28-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a1c28-115">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1c28-115">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1c28-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1c28-116">See also</span></span>

- [<span data-ttu-id="a1c28-117">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="a1c28-117">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
