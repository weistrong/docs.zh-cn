---
description: 了解详细信息： GetRealProcAddress 函数
title: GetRealProcAddress 函数
ms.date: 03/30/2017
api_name:
- GetRealProcAddress
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetRealProcAddress
helpviewer_keywords:
- GetRealProcAddress function [.NET Framework hosting]
ms.assetid: f1f2fab1-400b-488f-95f2-d49c4fca3556
topic_type:
- apiref
ms.openlocfilehash: b8b3db77d6aef7fae3045a7aa2310c1fadc70e91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785310"
---
# <a name="getrealprocaddress-function"></a><span data-ttu-id="30b4e-103">GetRealProcAddress 函数</span><span class="sxs-lookup"><span data-stu-id="30b4e-103">GetRealProcAddress Function</span></span>

<span data-ttu-id="30b4e-104">获取从 (CLR) 的公共语言运行时的最新安装版本导出的指定函数的地址。</span><span class="sxs-lookup"><span data-stu-id="30b4e-104">Gets the address of the specified function that is exported from the latest installed version of the common language runtime (CLR).</span></span>  
  
 <span data-ttu-id="30b4e-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="30b4e-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30b4e-106">语法</span><span class="sxs-lookup"><span data-stu-id="30b4e-106">Syntax</span></span>  
  
```cpp  
HRESULT GetRealProcAddress (  
    [in]  LPCSTR  pwszProcName,
    [out] VOID  **ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30b4e-107">参数</span><span class="sxs-lookup"><span data-stu-id="30b4e-107">Parameters</span></span>  

 `pwszProcName`  
 <span data-ttu-id="30b4e-108">中函数的名称。</span><span class="sxs-lookup"><span data-stu-id="30b4e-108">[in] The name of the function.</span></span>  
  
 `ppv`  
 <span data-ttu-id="30b4e-109">弄接收指向函数地址的指针的位置。</span><span class="sxs-lookup"><span data-stu-id="30b4e-109">[out] The location that receives a pointer to the address of the function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="30b4e-110">返回值</span><span class="sxs-lookup"><span data-stu-id="30b4e-110">Return Value</span></span>  

 <span data-ttu-id="30b4e-111">除了在 CorError 中定义的以下值外，此方法还会返回 (COM) 错误代码的标准组件对象模型，如 Winerror.h 中所定义。</span><span class="sxs-lookup"><span data-stu-id="30b4e-111">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values defined in CorError.h.</span></span>  
  
|<span data-ttu-id="30b4e-112">返回代码</span><span class="sxs-lookup"><span data-stu-id="30b4e-112">Return code</span></span>|<span data-ttu-id="30b4e-113">说明</span><span class="sxs-lookup"><span data-stu-id="30b4e-113">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="30b4e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="30b4e-114">S_OK</span></span>|<span data-ttu-id="30b4e-115">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="30b4e-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="30b4e-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="30b4e-116">E_POINTER</span></span>|<span data-ttu-id="30b4e-117">`ppv` 无效。</span><span class="sxs-lookup"><span data-stu-id="30b4e-117">`ppv` is not valid.</span></span>|  
|<span data-ttu-id="30b4e-118">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="30b4e-118">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="30b4e-119">不从运行时导出函数。</span><span class="sxs-lookup"><span data-stu-id="30b4e-119">The function is not exported from the runtime.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="30b4e-120">要求</span><span class="sxs-lookup"><span data-stu-id="30b4e-120">Requirements</span></span>  

 <span data-ttu-id="30b4e-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30b4e-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30b4e-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="30b4e-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="30b4e-123">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="30b4e-123">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="30b4e-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30b4e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30b4e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="30b4e-125">See also</span></span>

- [<span data-ttu-id="30b4e-126">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="30b4e-126">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
