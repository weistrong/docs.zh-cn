---
description: 了解详细信息： PreBindAssemblyEx 函数
title: PreBindAssemblyEx 函数
ms.date: 03/30/2017
api_name:
- PreBindAssemblyEx
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- PreBindAssemblyEx
helpviewer_keywords:
- PreBindAssemblyEx function [.NET Framework fusion]
ms.assetid: bd285233-a4a2-4b52-bbca-0025a60e4864
topic_type:
- apiref
ms.openlocfilehash: e94bd7c335555e8109df60a00cadc76f7e13434b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800001"
---
# <a name="prebindassemblyex-function"></a><span data-ttu-id="6ad4a-103">PreBindAssemblyEx 函数</span><span class="sxs-lookup"><span data-stu-id="6ad4a-103">PreBindAssemblyEx Function</span></span>

<span data-ttu-id="6ad4a-104">获取程序集的策略后显示名称。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-104">Gets the post-policy display name for an assembly.</span></span>  
  
 <span data-ttu-id="6ad4a-105">此函数支持 .NET Framework 基础结构，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-105">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ad4a-106">语法</span><span class="sxs-lookup"><span data-stu-id="6ad4a-106">Syntax</span></span>  
  
```cpp  
HRESULT PreBindAssemblyEx (  
    [in]  IApplicationContext *pAppCtx,  
    [in]  IAssemblyName       *pName,  
    [in]  IAssembly           *pAsmParent,  
    [in]  LPCWSTR             pwzRuntimeVersion,  
    [out] IAssemblyName       **ppNamePostPolicy,  
    [in]  LPVOID              pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="6ad4a-107">参数</span><span class="sxs-lookup"><span data-stu-id="6ad4a-107">Parameters</span></span>  

 `pAppCtx`  
 <span data-ttu-id="6ad4a-108">中标识应用程序上下文。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-108">[in] Identifies the application context.</span></span>  
  
 `pName`  
 <span data-ttu-id="6ad4a-109">中标识程序集名称。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-109">[in] Identifies the assembly name.</span></span>  
  
 `pAsmParent`  
 <span data-ttu-id="6ad4a-110">中标识父程序集。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-110">[in] Identifies the parent assembly.</span></span> <span data-ttu-id="6ad4a-111">忽略此参数。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-111">This parameter is ignored.</span></span>  
  
 `pwzRuntimeVersion`  
 <span data-ttu-id="6ad4a-112">中标识运行时版本。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-112">[in] Identifies the runtime version.</span></span>  
  
 `ppNamePostPolicy`  
 <span data-ttu-id="6ad4a-113">弄包含策略后显示名称。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-113">[out] Contains the post-policy display name.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="6ad4a-114">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-114">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="6ad4a-115">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-115">`pvReserved` must be a null reference.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6ad4a-116">备注</span><span class="sxs-lookup"><span data-stu-id="6ad4a-116">Remarks</span></span>  

 <span data-ttu-id="6ad4a-117">`ppNamePostPolicy`仅当函数返回 HRESULT FUSION_E_REF_DEF_MISMATCH 时才设置 output 参数。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-117">The `ppNamePostPolicy` output parameter is set only if the function returns HRESULT FUSION_E_REF_DEF_MISMATCH.</span></span> <span data-ttu-id="6ad4a-118">否则为 null。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-118">Otherwise, it is null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ad4a-119">要求</span><span class="sxs-lookup"><span data-stu-id="6ad4a-119">Requirements</span></span>  

 <span data-ttu-id="6ad4a-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6ad4a-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ad4a-121">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="6ad4a-121">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="6ad4a-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6ad4a-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6ad4a-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ad4a-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ad4a-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="6ad4a-124">See also</span></span>

- [<span data-ttu-id="6ad4a-125">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="6ad4a-125">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
