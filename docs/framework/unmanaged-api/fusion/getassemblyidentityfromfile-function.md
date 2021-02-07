---
description: 了解详细信息： GetAssemblyIdentityFromFile 函数
title: GetAssemblyIdentityFromFile 函数
ms.date: 03/30/2017
api_name:
- GetAssemblyIdentityFromFile
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyIdentityFromFile
helpviewer_keywords:
- GetAssemblyIdentityFromFile function [.NET Framework fusion]
ms.assetid: 2c32da53-76c7-4048-84d0-d05207333004
topic_type:
- apiref
ms.openlocfilehash: 8832e03182a5652c938404c99115fa8059439d1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761027"
---
# <a name="getassemblyidentityfromfile-function"></a><span data-ttu-id="ffd5c-103">GetAssemblyIdentityFromFile 函数</span><span class="sxs-lookup"><span data-stu-id="ffd5c-103">GetAssemblyIdentityFromFile Function</span></span>

<span data-ttu-id="ffd5c-104">获取一个指针，该指针指向在 `IUnknown` `IID` 指定文件路径的程序集中具有指定的对象。</span><span class="sxs-lookup"><span data-stu-id="ffd5c-104">Gets a pointer to an `IUnknown` object with the specified `IID` in the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffd5c-105">语法</span><span class="sxs-lookup"><span data-stu-id="ffd5c-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyIdentityFromFile (  
    [in]  LPCWSTR   pwzFilePath,  
    [in]  REFIID    riid,  
    [out] IUnknown  **ppIdentity  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="ffd5c-106">参数</span><span class="sxs-lookup"><span data-stu-id="ffd5c-106">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="ffd5c-107">中请求的程序集的有效路径。</span><span class="sxs-lookup"><span data-stu-id="ffd5c-107">[in] A valid path to the requested assembly.</span></span>  
  
 `riid`  
 <span data-ttu-id="ffd5c-108">中 `IID` 要返回的接口的。</span><span class="sxs-lookup"><span data-stu-id="ffd5c-108">[in] The `IID` of the interface to return.</span></span>  
  
 `ppIdentity`  
 <span data-ttu-id="ffd5c-109">弄返回的接口指针。</span><span class="sxs-lookup"><span data-stu-id="ffd5c-109">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffd5c-110">要求</span><span class="sxs-lookup"><span data-stu-id="ffd5c-110">Requirements</span></span>  

 <span data-ttu-id="ffd5c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ffd5c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffd5c-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="ffd5c-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ffd5c-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffd5c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffd5c-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="ffd5c-114">See also</span></span>

- [<span data-ttu-id="ffd5c-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ffd5c-115">IUnknown</span></span>](/cpp/atl/iunknown)
- [<span data-ttu-id="ffd5c-116">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="ffd5c-116">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
