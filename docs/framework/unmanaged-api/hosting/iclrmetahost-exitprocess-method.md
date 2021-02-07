---
description: 了解详细信息： ICLRMetaHost：： ExitProcess 方法
title: ICLRMetaHost::ExitProcess 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.ExitProcess
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::ExitProcess
helpviewer_keywords:
- ICLRMetaHost::ExitProcess method [.NET Framework hosting]
- ExitProcess method, ICLRMetaHost interface [.NET Framework hosting]
ms.assetid: b4df98cc-4e4e-407b-b8f4-e0076afef3a4
topic_type:
- apiref
ms.openlocfilehash: 3bc832538a5ad2b457de758fc35a632b09c02974
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689152"
---
# <a name="iclrmetahostexitprocess-method"></a><span data-ttu-id="49792-103">ICLRMetaHost::ExitProcess 方法</span><span class="sxs-lookup"><span data-stu-id="49792-103">ICLRMetaHost::ExitProcess Method</span></span>

<span data-ttu-id="49792-104">尝试正常关闭所有加载的运行时，然后终止进程。</span><span class="sxs-lookup"><span data-stu-id="49792-104">Attempts to shut down all loaded runtimes gracefully and then terminates the process.</span></span> <span data-ttu-id="49792-105">取代 [CorExitProcess](corexitprocess-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="49792-105">Supersedes the [CorExitProcess](corexitprocess-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49792-106">语法</span><span class="sxs-lookup"><span data-stu-id="49792-106">Syntax</span></span>  
  
```cpp  
HRESULT ExitProcess (  
    [in] INT32 iExitCode);  
```  
  
## <a name="parameters"></a><span data-ttu-id="49792-107">参数</span><span class="sxs-lookup"><span data-stu-id="49792-107">Parameters</span></span>  

 `iExitCode`  
 <span data-ttu-id="49792-108">中进程的退出代码。</span><span class="sxs-lookup"><span data-stu-id="49792-108">[in] The exit code for the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="49792-109">返回值</span><span class="sxs-lookup"><span data-stu-id="49792-109">Return Value</span></span>  

 <span data-ttu-id="49792-110">此方法从不返回，因此其返回值未定义。</span><span class="sxs-lookup"><span data-stu-id="49792-110">This method never returns, so its return value is undefined.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="49792-111">备注</span><span class="sxs-lookup"><span data-stu-id="49792-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49792-112">要求</span><span class="sxs-lookup"><span data-stu-id="49792-112">Requirements</span></span>  

 <span data-ttu-id="49792-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49792-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49792-114">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="49792-114">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="49792-115">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="49792-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="49792-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49792-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49792-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="49792-117">See also</span></span>

- [<span data-ttu-id="49792-118">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="49792-118">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="49792-119">承载</span><span class="sxs-lookup"><span data-stu-id="49792-119">Hosting</span></span>](index.md)
