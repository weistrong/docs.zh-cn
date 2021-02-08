---
description: 了解详细信息： IMetaDataEmit2：： SaveDeltaToStream 方法
title: IMetaDataEmit2::SaveDeltaToStream 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToStream
helpviewer_keywords:
- IMetaDataEmit2::SaveDeltaToStream method [.NET Framework metadata]
- SaveDeltaToStream method [.NET Framework metadata]
ms.assetid: ecd786e8-f9a4-4190-a6ef-af18e8c6d654
topic_type:
- apiref
ms.openlocfilehash: ce2e7822a5220a8ab1264a6e18337ba0f7828e3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771699"
---
# <a name="imetadataemit2savedeltatostream-method"></a><span data-ttu-id="05f1e-103">IMetaDataEmit2::SaveDeltaToStream 方法</span><span class="sxs-lookup"><span data-stu-id="05f1e-103">IMetaDataEmit2::SaveDeltaToStream Method</span></span>

<span data-ttu-id="05f1e-104">将当前的 "编辑并继续" 会话中的更改保存到指定的流。</span><span class="sxs-lookup"><span data-stu-id="05f1e-104">Saves changes from the current edit-and-continue session to the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05f1e-105">语法</span><span class="sxs-lookup"><span data-stu-id="05f1e-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveDeltaToStream (  
    [in] IStream     *pIStream,
    [in] DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05f1e-106">参数</span><span class="sxs-lookup"><span data-stu-id="05f1e-106">Parameters</span></span>  

 `pIStream`  
 <span data-ttu-id="05f1e-107">中一个接口指针，指向要将更改保存到的可写流。</span><span class="sxs-lookup"><span data-stu-id="05f1e-107">[in] An interface pointer to the writable stream to which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="05f1e-108">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="05f1e-108">[in] Reserved.</span></span> <span data-ttu-id="05f1e-109">此值必须为零。</span><span class="sxs-lookup"><span data-stu-id="05f1e-109">This value must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05f1e-110">要求</span><span class="sxs-lookup"><span data-stu-id="05f1e-110">Requirements</span></span>  

 <span data-ttu-id="05f1e-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="05f1e-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05f1e-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="05f1e-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="05f1e-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="05f1e-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="05f1e-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05f1e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05f1e-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="05f1e-115">See also</span></span>

- [<span data-ttu-id="05f1e-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="05f1e-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="05f1e-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="05f1e-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
