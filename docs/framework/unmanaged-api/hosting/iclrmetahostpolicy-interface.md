---
description: 了解详细信息： ICLRMetaHostPolicy 接口
title: ICLRMetaHostPolicy 接口
ms.date: 03/30/2017
api_name:
- ICLRMetaHostPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHostPolicy
helpviewer_keywords:
- ICLRMetaHostPolicy interface [.NET Framework hosting]
ms.assetid: 1bdeccb6-0698-4c97-ad69-eae2b69e59f1
topic_type:
- apiref
ms.openlocfilehash: b14ad417617c32242f8a59844f7c1f1a8d05c78d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637412"
---
# <a name="iclrmetahostpolicy-interface"></a><span data-ttu-id="a3ba0-103">ICLRMetaHostPolicy 接口</span><span class="sxs-lookup"><span data-stu-id="a3ba0-103">ICLRMetaHostPolicy Interface</span></span>

<span data-ttu-id="a3ba0-104">提供 [GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) 方法，该方法根据策略条件、托管程序集、版本和配置文件，返回指向公共语言运行时 (CLR) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-104">Provides the [GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) method, which returns a pointer to a common language runtime (CLR) interface based on a policy criteria, managed assembly, version and configuration file.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a3ba0-105">方法</span><span class="sxs-lookup"><span data-stu-id="a3ba0-105">Methods</span></span>  
  
|<span data-ttu-id="a3ba0-106">方法</span><span class="sxs-lookup"><span data-stu-id="a3ba0-106">Method</span></span>|<span data-ttu-id="a3ba0-107">说明</span><span class="sxs-lookup"><span data-stu-id="a3ba0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a3ba0-108">GetRequestedRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="a3ba0-108">GetRequestedRuntime Method</span></span>](iclrmetahostpolicy-getrequestedruntime-method.md)|<span data-ttu-id="a3ba0-109">提供基于策略标准、托管程序集、版本和配置文件的首选 CLR 接口。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-109">Provides a preferred CLR interface based on a policy criteria, managed assembly, version, and configuration file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a3ba0-110">备注</span><span class="sxs-lookup"><span data-stu-id="a3ba0-110">Remarks</span></span>  

 <span data-ttu-id="a3ba0-111">可以通过调用 [CLRCreateInstance](clrcreateinstance-function.md) 函数获取对此接口的引用，如以下代码所示：</span><span class="sxs-lookup"><span data-stu-id="a3ba0-111">You can get a reference to this interface by calling the [CLRCreateInstance](clrcreateinstance-function.md) function as shown in the following code:</span></span>  
  
```cpp  
ICLRMetaHostPolicy *pMetaHostPolicy = NULL;  
HRESULT hr = CLRCreateInstance(CLSID_CLRMetaHostPolicy,  
                   IID_ICLRMetaHostPolicy, (LPVOID*)&pMetaHostPolicy);  
```  
  
> [!NOTE]
> <span data-ttu-id="a3ba0-112">此接口实际上不会加载或激活 CLR，只是根据安装或加载的可用版本返回首选 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-112">This interface does not actually load or activate the CLR, but simply returns the preferred CLR version based on the available versions that are installed or loaded.</span></span>  
  
 <span data-ttu-id="a3ba0-113">.NET Framework 4 托管 API 合并了策略，因此具有特定需求的主机可以使用基本功能，而不会产生意外的处罚。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-113">The .NET Framework 4 hosting API consolidates policies so that hosts with specific needs may use basic functionality without incurring unintended penalties.</span></span> <span data-ttu-id="a3ba0-114">例如，许多 MSCorEE.dll 导出将绑定到特定的 CLR，不过方法可能不会在逻辑上需要它。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-114">For example, many of the MSCorEE.dll exports will bind to a specific CLR, although a method might not logically require it.</span></span> <span data-ttu-id="a3ba0-115">[METAHOST_POLICY_FLAGS](metahost-policy-flags-enumeration.md)枚举提供大部分主机所共有的绑定策略。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-115">The [METAHOST_POLICY_FLAGS](metahost-policy-flags-enumeration.md) enumeration provides binding policies that are common to the majority of hosts.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3ba0-116">要求</span><span class="sxs-lookup"><span data-stu-id="a3ba0-116">Requirements</span></span>  

 <span data-ttu-id="a3ba0-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a3ba0-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3ba0-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="a3ba0-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a3ba0-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3ba0-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3ba0-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3ba0-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3ba0-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="a3ba0-121">See also</span></span>

- [<span data-ttu-id="a3ba0-122">.NET Framework 4 和 4.5 中添加的 CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="a3ba0-122">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="a3ba0-123">承载接口</span><span class="sxs-lookup"><span data-stu-id="a3ba0-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="a3ba0-124">承载</span><span class="sxs-lookup"><span data-stu-id="a3ba0-124">Hosting</span></span>](index.md)
