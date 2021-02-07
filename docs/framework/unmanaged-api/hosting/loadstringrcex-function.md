---
description: 了解详细信息： LoadStringRCEx 函数
title: LoadStringRCEx 函数
ms.date: 03/30/2017
api_name:
- LoadStringRCEx
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRCEx
helpviewer_keywords:
- LoadStringRCEx function [.NET Framework hosting]
ms.assetid: bc789636-ca14-4f07-8f77-9305874d7495
topic_type:
- apiref
ms.openlocfilehash: d3fe4b97014e5093dd8d209a5e27bac4ed7b879f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679871"
---
# <a name="loadstringrcex-function"></a><span data-ttu-id="8fc84-103">LoadStringRCEx 函数</span><span class="sxs-lookup"><span data-stu-id="8fc84-103">LoadStringRCEx Function</span></span>

<span data-ttu-id="8fc84-104">将 HRESULT 值转换为指定区域性的适当错误消息。</span><span class="sxs-lookup"><span data-stu-id="8fc84-104">Translates an HRESULT value to an appropriate error message for the specified culture.</span></span>  
  
 <span data-ttu-id="8fc84-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="8fc84-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fc84-106">语法</span><span class="sxs-lookup"><span data-stu-id="8fc84-106">Syntax</span></span>  
  
```cpp  
HRESULT LoadStringRCEx (  
    [in]  LCID    lcid,
    [in]  UINT    iResouceID,
    [out] LPWSTR  szBuffer,
    [in]  int     iMax,
    [in]  int     bQuiet,
    [out] int    *pcwchUsed  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fc84-107">参数</span><span class="sxs-lookup"><span data-stu-id="8fc84-107">Parameters</span></span>  

 `lcid`  
 <span data-ttu-id="8fc84-108">中区域性标识符。</span><span class="sxs-lookup"><span data-stu-id="8fc84-108">[in] A culture identifier.</span></span> <span data-ttu-id="8fc84-109">为传递-1 `lcid` 以使用默认区域性。</span><span class="sxs-lookup"><span data-stu-id="8fc84-109">Pass -1 for `lcid` to use the default culture.</span></span>  
  
 `iResourceID`  
 <span data-ttu-id="8fc84-110">中HRESULT。</span><span class="sxs-lookup"><span data-stu-id="8fc84-110">[in] An HRESULT.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="8fc84-111">弄一个缓冲区，其中包含成功完成后的错误消息。</span><span class="sxs-lookup"><span data-stu-id="8fc84-111">[out] A buffer that contains the error message upon successful completion.</span></span>  
  
 `iMax`  
 <span data-ttu-id="8fc84-112">中错误消息缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="8fc84-112">[in] The size of the error message buffer.</span></span>  
  
 `bQuiet`  
 <span data-ttu-id="8fc84-113">中掉.</span><span class="sxs-lookup"><span data-stu-id="8fc84-113">[in] Ignored.</span></span>  
  
 `pcwchUsed`  
 <span data-ttu-id="8fc84-114">弄指向错误消息长度的指针。</span><span class="sxs-lookup"><span data-stu-id="8fc84-114">[out] A pointer to the length of the error message.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8fc84-115">返回值</span><span class="sxs-lookup"><span data-stu-id="8fc84-115">Return Value</span></span>  

 <span data-ttu-id="8fc84-116">除以下值外，此方法还返回 Winerror.h 中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="8fc84-116">This method returns standard COM error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="8fc84-117">返回代码</span><span class="sxs-lookup"><span data-stu-id="8fc84-117">Return code</span></span>|<span data-ttu-id="8fc84-118">说明</span><span class="sxs-lookup"><span data-stu-id="8fc84-118">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="8fc84-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fc84-119">S_OK</span></span>|<span data-ttu-id="8fc84-120">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8fc84-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="8fc84-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8fc84-121">E_INVALIDARG</span></span>|<span data-ttu-id="8fc84-122">`szBuffer` 为 null，或者 `iMax` 为零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8fc84-122">`szBuffer` is null, or `iMax` is zero (0).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8fc84-123">备注</span><span class="sxs-lookup"><span data-stu-id="8fc84-123">Remarks</span></span>  

 <span data-ttu-id="8fc84-124">如果该方法未成功完成，则 `szBuffer` 包含一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="8fc84-124">If the method does not complete successfully, `szBuffer` contains an empty string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fc84-125">要求</span><span class="sxs-lookup"><span data-stu-id="8fc84-125">Requirements</span></span>  

 <span data-ttu-id="8fc84-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8fc84-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fc84-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8fc84-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8fc84-128">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8fc84-128">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8fc84-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fc84-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fc84-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="8fc84-130">See also</span></span>

- <xref:System.Globalization.CultureInfo.LCID%2A?displayProperty=nameWithType>
- [<span data-ttu-id="8fc84-131">LoadStringRC 函数</span><span class="sxs-lookup"><span data-stu-id="8fc84-131">LoadStringRC Function</span></span>](loadstringrc-function.md)
- [<span data-ttu-id="8fc84-132">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="8fc84-132">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
