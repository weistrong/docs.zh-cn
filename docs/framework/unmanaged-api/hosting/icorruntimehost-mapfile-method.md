---
description: 了解详细信息： ICorRuntimeHost：：映射映射方法
title: ICorRuntimeHost::MapFile 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.MapFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::MapFile
helpviewer_keywords:
- ICorRuntimeHost::MapFile method [.NET Framework hosting]
- MapFile method [.NET Framework hosting]
ms.assetid: 45ae0502-0a31-4342-b7e3-f36e1cf738f3
topic_type:
- apiref
ms.openlocfilehash: 80c01a036de83b32b9d0de745d76bb97825c980b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789627"
---
# <a name="icorruntimehostmapfile-method"></a><span data-ttu-id="5104c-103">ICorRuntimeHost::MapFile 方法</span><span class="sxs-lookup"><span data-stu-id="5104c-103">ICorRuntimeHost::MapFile Method</span></span>

<span data-ttu-id="5104c-104">将指定的文件映射到内存。</span><span class="sxs-lookup"><span data-stu-id="5104c-104">Maps the specified file into memory.</span></span> <span data-ttu-id="5104c-105">此方法已过时。</span><span class="sxs-lookup"><span data-stu-id="5104c-105">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5104c-106">语法</span><span class="sxs-lookup"><span data-stu-id="5104c-106">Syntax</span></span>  
  
```cpp  
HRESULT MapFile(  
    [in]  HANDLE    hFile,  
    [out] HMODULE*  hMapAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5104c-107">参数</span><span class="sxs-lookup"><span data-stu-id="5104c-107">Parameters</span></span>  

 `hFile`  
 <span data-ttu-id="5104c-108">中要映射的文件的句柄。</span><span class="sxs-lookup"><span data-stu-id="5104c-108">[in] The handle of the file to be mapped.</span></span>  
  
 `hMapAddress`  
 <span data-ttu-id="5104c-109">弄开始映射文件的起始内存地址。</span><span class="sxs-lookup"><span data-stu-id="5104c-109">[out] The starting memory address at which to begin mapping the file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5104c-110">要求</span><span class="sxs-lookup"><span data-stu-id="5104c-110">Requirements</span></span>  

 <span data-ttu-id="5104c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5104c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5104c-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5104c-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5104c-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5104c-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5104c-114">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="5104c-114">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5104c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="5104c-115">See also</span></span>

- [<span data-ttu-id="5104c-116">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="5104c-116">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
