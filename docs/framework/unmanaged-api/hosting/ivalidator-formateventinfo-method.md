---
description: 了解详细信息： IValidator：： FormatEventInfo 方法
title: IValidator::FormatEventInfo 方法
ms.date: 03/30/2017
api_name:
- IValidator.FormatEventInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FormatEventInfo
helpviewer_keywords:
- IValidator::FormatEventInfo method [.NET Framework hosting]
- FormatEventInfo method, IValidator interface [.NET Framework hosting]
ms.assetid: 4c0c7477-05ba-461b-b21b-cbfba95f1db1
topic_type:
- apiref
ms.openlocfilehash: 28ecf9ab2b14cd2fdd178a4ad9d8e218f7038a9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680156"
---
# <a name="ivalidatorformateventinfo-method"></a><span data-ttu-id="9f6d4-103">IValidator::FormatEventInfo 方法</span><span class="sxs-lookup"><span data-stu-id="9f6d4-103">IValidator::FormatEventInfo Method</span></span>

<span data-ttu-id="9f6d4-104">获取与指定的验证错误相对应的错误消息。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-104">Gets the error message corresponding to the specified validation error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f6d4-105">语法</span><span class="sxs-lookup"><span data-stu-id="9f6d4-105">Syntax</span></span>  
  
```cpp  
HRESULT FormatEventInfo(  
    [in] HRESULT            hVECode,  
    [in] VEContext          Context,  
    [in, out] LPWSTR        msg,  
    [in] unsigned long      ulMaxLength,  
    [in] SAFEARRAY(VARIANT) psa  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9f6d4-106">参数</span><span class="sxs-lookup"><span data-stu-id="9f6d4-106">Parameters</span></span>  

 `hVECode`  
 <span data-ttu-id="9f6d4-107">中传递给验证错误处理程序的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-107">[in] The HRESULT value that was passed to the validation error handler.</span></span>  
  
 `Context`  
 <span data-ttu-id="9f6d4-108">中一个 `VEContext` 实例，其中包含有关验证错误的上下文信息。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-108">[in] A `VEContext` instance that contains context information about the validation error.</span></span>  
  
 `msg`  
 <span data-ttu-id="9f6d4-109">[in，out]包含返回的错误消息的字符串。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-109">[in, out] A string that contains the returned error message.</span></span>  
  
 `ulMaxLength`  
 <span data-ttu-id="9f6d4-110">中错误消息的最大长度。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-110">[in] The maximum length of the error message.</span></span>  
  
 `psa`  
 <span data-ttu-id="9f6d4-111">中一个安全数组，其中包含描述错误的其他参数。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-111">[in] A safe array that contains additional parameters describing the error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f6d4-112">要求</span><span class="sxs-lookup"><span data-stu-id="9f6d4-112">Requirements</span></span>  

 <span data-ttu-id="9f6d4-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6d4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f6d4-114">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="9f6d4-114">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="9f6d4-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f6d4-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9f6d4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f6d4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
