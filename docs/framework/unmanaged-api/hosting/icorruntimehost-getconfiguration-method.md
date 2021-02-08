---
description: 了解详细信息： ICorRuntimeHost：： GetConfiguration 方法
title: ICorRuntimeHost::GetConfiguration 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type:
- apiref
ms.openlocfilehash: d3e3f065c3957fb29daa11ed7c46858a53865c91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784829"
---
# <a name="icorruntimehostgetconfiguration-method"></a><span data-ttu-id="06809-103">ICorRuntimeHost::GetConfiguration 方法</span><span class="sxs-lookup"><span data-stu-id="06809-103">ICorRuntimeHost::GetConfiguration Method</span></span>

<span data-ttu-id="06809-104">获取一个对象，该对象允许主机指定 (CLR) 的公共语言运行时的回调配置。</span><span class="sxs-lookup"><span data-stu-id="06809-104">Gets an object that allows the host to specify the callback configuration of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06809-105">语法</span><span class="sxs-lookup"><span data-stu-id="06809-105">Syntax</span></span>  
  
```cpp  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="06809-106">参数</span><span class="sxs-lookup"><span data-stu-id="06809-106">Parameters</span></span>  

 `pConfiguration`  
 <span data-ttu-id="06809-107">弄指向可用于配置 CLR 的 [ICorConfiguration](icorconfiguration-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="06809-107">[out] A pointer to the address of an [ICorConfiguration](icorconfiguration-interface.md) object that can be used to configure the CLR.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="06809-108">备注</span><span class="sxs-lookup"><span data-stu-id="06809-108">Remarks</span></span>  

 <span data-ttu-id="06809-109">必须在初始化之前配置 CLR;否则，该 `GetConfiguration` 方法将返回一个 HRESULT，指示错误。</span><span class="sxs-lookup"><span data-stu-id="06809-109">The CLR must be configured prior to its initialization; otherwise, the `GetConfiguration` method returns an HRESULT indicating an error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06809-110">要求</span><span class="sxs-lookup"><span data-stu-id="06809-110">Requirements</span></span>  

 <span data-ttu-id="06809-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="06809-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06809-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="06809-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="06809-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="06809-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="06809-114">**.NET Framework 版本：** 1.0、1。1</span><span class="sxs-lookup"><span data-stu-id="06809-114">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06809-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="06809-115">See also</span></span>

- [<span data-ttu-id="06809-116">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="06809-116">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
