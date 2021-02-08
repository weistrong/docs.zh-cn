---
description: 了解详细信息： ICorPublishProcess：： GetDisplayName 方法
title: ICorPublishProcess::GetDisplayName 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetDisplayName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetDisplayName
helpviewer_keywords:
- ICorPublishProcess::GetDisplayName method [.NET Framework debugging]
- GetDisplayName method, ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 7c0af9e9-a73f-41aa-a685-b21c439e059d
topic_type:
- apiref
ms.openlocfilehash: 7aef55a40c24953766377f21e8291bceb1594480
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794580"
---
# <a name="icorpublishprocessgetdisplayname-method"></a><span data-ttu-id="4fae6-103">ICorPublishProcess::GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="4fae6-103">ICorPublishProcess::GetDisplayName Method</span></span>

<span data-ttu-id="4fae6-104">获取此 [ICorPublishProcess](icorpublishprocess-interface.md)引用的进程的可执行文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="4fae6-104">Gets the full path of the executable for the process referenced by this [ICorPublishProcess](icorpublishprocess-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4fae6-105">语法</span><span class="sxs-lookup"><span data-stu-id="4fae6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDisplayName (  
    [in]  ULONG32                    cchName,
    [out] ULONG32                    *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]
        WCHAR                        *szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4fae6-106">参数</span><span class="sxs-lookup"><span data-stu-id="4fae6-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="4fae6-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="4fae6-107">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="4fae6-108">弄在数组中返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="4fae6-108">[out] The number of wide characters returned in the `szName` array.</span></span>  
  
 `szName`  
 <span data-ttu-id="4fae6-109">弄用于存储可执行文件的名称（包括完整路径）的数组。</span><span class="sxs-lookup"><span data-stu-id="4fae6-109">[out] An array to store the name, including the full path, of the executable.</span></span> <span data-ttu-id="4fae6-110">名称以 null 结尾。</span><span class="sxs-lookup"><span data-stu-id="4fae6-110">The name is null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4fae6-111">要求</span><span class="sxs-lookup"><span data-stu-id="4fae6-111">Requirements</span></span>  

 <span data-ttu-id="4fae6-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4fae6-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4fae6-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="4fae6-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="4fae6-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4fae6-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4fae6-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4fae6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fae6-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="4fae6-116">See also</span></span>

- [<span data-ttu-id="4fae6-117">ICorPublishProcess 接口</span><span class="sxs-lookup"><span data-stu-id="4fae6-117">ICorPublishProcess Interface</span></span>](icorpublishprocess-interface.md)
