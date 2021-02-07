---
description: 了解详细信息： CreateApplicationContext 函数
title: CreateApplicationContext 函数
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
ms.openlocfilehash: f192e1ccc371cb6d50e4a41a286c412825ee4181
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761174"
---
# <a name="createapplicationcontext-function"></a><span data-ttu-id="092fd-103">CreateApplicationContext 函数</span><span class="sxs-lookup"><span data-stu-id="092fd-103">CreateApplicationContext Function</span></span>

<span data-ttu-id="092fd-104">此函数支持 .NET Framework 基础结构，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="092fd-104">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="092fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="092fd-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="092fd-106">参数</span><span class="sxs-lookup"><span data-stu-id="092fd-106">Parameters</span></span>  

 `pName`  
 <span data-ttu-id="092fd-107">中指向友好名称的指针。</span><span class="sxs-lookup"><span data-stu-id="092fd-107">[in] A pointer to a friendly name.</span></span>  
  
 `ppCtx`  
 <span data-ttu-id="092fd-108">弄指向应用程序上下文的指针。</span><span class="sxs-lookup"><span data-stu-id="092fd-108">[out] A pointer to an application context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="092fd-109">要求</span><span class="sxs-lookup"><span data-stu-id="092fd-109">Requirements</span></span>  

 <span data-ttu-id="092fd-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="092fd-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="092fd-111">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="092fd-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="092fd-112">**库：** 作为中的资源包含 Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="092fd-112">**Library:** Included as a resource in Fusion.dll</span></span>  
  
 <span data-ttu-id="092fd-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="092fd-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="092fd-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="092fd-114">See also</span></span>

- [<span data-ttu-id="092fd-115">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="092fd-115">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
- [<span data-ttu-id="092fd-116">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="092fd-116">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
- [<span data-ttu-id="092fd-117">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="092fd-117">Global Assembly Cache</span></span>](../../app-domains/gac.md)
