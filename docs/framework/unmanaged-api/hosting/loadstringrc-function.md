---
description: 了解详细信息： LoadStringRC 函数
title: LoadStringRC 函数
ms.date: 03/30/2017
api_name:
- LoadStringRC
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRC
helpviewer_keywords:
- LoadStringRC function [.NET Framework hosting]
ms.assetid: 752e49b4-987c-4c28-a118-1a0c1ed510c5
topic_type:
- apiref
ms.openlocfilehash: 188597f9dc21b6a67fb84e91cd66b50ba5a514f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679880"
---
# <a name="loadstringrc-function"></a><span data-ttu-id="778b8-103">LoadStringRC 函数</span><span class="sxs-lookup"><span data-stu-id="778b8-103">LoadStringRC Function</span></span>

<span data-ttu-id="778b8-104">使用当前线程的默认区域性将 HRESULT 值转换为错误消息。</span><span class="sxs-lookup"><span data-stu-id="778b8-104">Translates an HRESULT value into an error message by using the default culture of the current thread.</span></span>  
  
 <span data-ttu-id="778b8-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="778b8-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="778b8-106">语法</span><span class="sxs-lookup"><span data-stu-id="778b8-106">Syntax</span></span>  
  
```cpp  
HRESULT LoadStringRC (  
    [in]  UINT    iResourceID,
    [out] LPWSTR  szBuffer,
    [in]  int     iMax,
    [in]  int     bQuiet  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="778b8-107">参数</span><span class="sxs-lookup"><span data-stu-id="778b8-107">Parameters</span></span>  

 `iResourceID`  
 <span data-ttu-id="778b8-108">中HRESULT。</span><span class="sxs-lookup"><span data-stu-id="778b8-108">[in] An HRESULT.</span></span>  
  
 `szBuffer`  
 <span data-ttu-id="778b8-109">弄一个缓冲区，其中包含成功完成后的错误消息。</span><span class="sxs-lookup"><span data-stu-id="778b8-109">[out] A buffer that contains the error message upon successful completion.</span></span>  
  
 `iMax`  
 <span data-ttu-id="778b8-110">中错误消息缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="778b8-110">[in] The size of the error message buffer.</span></span>  
  
 `bQuiet`  
 <span data-ttu-id="778b8-111">中掉.</span><span class="sxs-lookup"><span data-stu-id="778b8-111">[in] Ignored.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="778b8-112">返回值</span><span class="sxs-lookup"><span data-stu-id="778b8-112">Return Value</span></span>  

 <span data-ttu-id="778b8-113">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="778b8-113">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="778b8-114">返回代码</span><span class="sxs-lookup"><span data-stu-id="778b8-114">Return code</span></span>|<span data-ttu-id="778b8-115">说明</span><span class="sxs-lookup"><span data-stu-id="778b8-115">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="778b8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="778b8-116">S_OK</span></span>|<span data-ttu-id="778b8-117">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="778b8-117">The method completed successfully.</span></span>|  
|<span data-ttu-id="778b8-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="778b8-118">E_INVALIDARG</span></span>|<span data-ttu-id="778b8-119">`szBuffer` 为 null 或 `iMax` 为零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="778b8-119">`szBuffer` is null or `iMax` is zero (0).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="778b8-120">备注</span><span class="sxs-lookup"><span data-stu-id="778b8-120">Remarks</span></span>  

 <span data-ttu-id="778b8-121">如果该方法未成功完成，则 `szBuffer` 包含一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="778b8-121">If the method does not complete successfully, `szBuffer` contains an empty string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="778b8-122">要求</span><span class="sxs-lookup"><span data-stu-id="778b8-122">Requirements</span></span>  

 <span data-ttu-id="778b8-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="778b8-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="778b8-124">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="778b8-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="778b8-125">**库：** MSCorEE.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="778b8-125">**Library:** MSCorEE.dll and Mscorwks.dll.</span></span> <span data-ttu-id="778b8-126">使用 MSCorEE.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="778b8-126">Use MSCorEE.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="778b8-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="778b8-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="778b8-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="778b8-128">See also</span></span>

- [<span data-ttu-id="778b8-129">LoadStringRCEx 函数</span><span class="sxs-lookup"><span data-stu-id="778b8-129">LoadStringRCEx Function</span></span>](loadstringrcex-function.md)
- [<span data-ttu-id="778b8-130">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="778b8-130">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
