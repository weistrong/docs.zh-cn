---
description: 了解详细信息： IMetaDataImport：： GetUserString 方法
title: IMetaDataImport::GetUserString 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetUserString
helpviewer_keywords:
- IMetaDataImport::GetUserString method [.NET Framework metadata]
- GetUserString method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 0fd3bb47-58b5-4083-b241-b9719df7a285
topic_type:
- apiref
ms.openlocfilehash: 074d196c74be30f5879410ad44b9bb5c096eb153
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789094"
---
# <a name="imetadataimportgetuserstring-method"></a><span data-ttu-id="84f3a-103">IMetaDataImport::GetUserString 方法</span><span class="sxs-lookup"><span data-stu-id="84f3a-103">IMetaDataImport::GetUserString Method</span></span>

<span data-ttu-id="84f3a-104">获取指定元数据标记所表示的文字字符串。</span><span class="sxs-lookup"><span data-stu-id="84f3a-104">Gets the literal string represented by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84f3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="84f3a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetUserString (  
   [in]   mdString    stk,  
   [out]  LPWSTR      szString,  
   [in]   ULONG       cchString,  
   [out]  ULONG       *pchString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84f3a-106">参数</span><span class="sxs-lookup"><span data-stu-id="84f3a-106">Parameters</span></span>  

 `stk`  
 <span data-ttu-id="84f3a-107">中要为其返回关联字符串的字符串标记。</span><span class="sxs-lookup"><span data-stu-id="84f3a-107">[in] The String token to return the associated string for.</span></span>  
  
 `szString`  
 <span data-ttu-id="84f3a-108">弄请求的字符串的副本。</span><span class="sxs-lookup"><span data-stu-id="84f3a-108">[out] A copy of the requested string.</span></span>  
  
 `cchString`  
 <span data-ttu-id="84f3a-109">中请求的的最大大小（以宽字符为大小） `szString` 。</span><span class="sxs-lookup"><span data-stu-id="84f3a-109">[in] The maximum size in wide characters of the requested `szString`.</span></span>  
  
 `pchString`  
 <span data-ttu-id="84f3a-110">弄返回的的大小（以宽字符为大小） `szString` 。</span><span class="sxs-lookup"><span data-stu-id="84f3a-110">[out] The size in wide characters of the returned `szString`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84f3a-111">要求</span><span class="sxs-lookup"><span data-stu-id="84f3a-111">Requirements</span></span>  

 <span data-ttu-id="84f3a-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84f3a-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84f3a-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="84f3a-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="84f3a-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="84f3a-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="84f3a-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84f3a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84f3a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="84f3a-116">See also</span></span>

- [<span data-ttu-id="84f3a-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="84f3a-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="84f3a-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="84f3a-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
