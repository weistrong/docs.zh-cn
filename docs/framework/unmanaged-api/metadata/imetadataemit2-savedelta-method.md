---
description: 了解详细信息： IMetaDataEmit2：： SaveDelta 方法
title: IMetaDataEmit2::SaveDelta 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDelta
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDelta
helpviewer_keywords:
- IMetaDataEmit2::SaveDelta method [.NET Framework metadata]
- SaveDelta method [.NET Framework metadata]
ms.assetid: b95739fe-d2fa-4776-ae0d-31d9707ef799
topic_type:
- apiref
ms.openlocfilehash: 6e7a7527125869fea041f407da056db3eea88cbe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771764"
---
# <a name="imetadataemit2savedelta-method"></a><span data-ttu-id="8f9a6-103">IMetaDataEmit2::SaveDelta 方法</span><span class="sxs-lookup"><span data-stu-id="8f9a6-103">IMetaDataEmit2::SaveDelta Method</span></span>

<span data-ttu-id="8f9a6-104">将当前的 "编辑并继续" 会话中的更改保存到指定的文件。</span><span class="sxs-lookup"><span data-stu-id="8f9a6-104">Saves changes from the current edit-and-continue session to the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f9a6-105">语法</span><span class="sxs-lookup"><span data-stu-id="8f9a6-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveDelta (  
    [in] LPCWSTR     szFile,
    [in] DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f9a6-106">参数</span><span class="sxs-lookup"><span data-stu-id="8f9a6-106">Parameters</span></span>  

 `szFile`  
 <span data-ttu-id="8f9a6-107">中用于保存更改的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="8f9a6-107">[in] The file name under which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="8f9a6-108">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="8f9a6-108">[in] Reserved.</span></span> <span data-ttu-id="8f9a6-109">必须为零。</span><span class="sxs-lookup"><span data-stu-id="8f9a6-109">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f9a6-110">要求</span><span class="sxs-lookup"><span data-stu-id="8f9a6-110">Requirements</span></span>  

 <span data-ttu-id="8f9a6-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f9a6-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f9a6-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8f9a6-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8f9a6-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8f9a6-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8f9a6-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f9a6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f9a6-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f9a6-115">See also</span></span>

- [<span data-ttu-id="8f9a6-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8f9a6-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="8f9a6-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8f9a6-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
