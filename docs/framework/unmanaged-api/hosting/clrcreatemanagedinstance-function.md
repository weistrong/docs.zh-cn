---
description: 了解详细信息： ClrCreateManagedInstance 函数
title: ClrCreateManagedInstance 函数
ms.date: 03/30/2017
api_name:
- ClrCreateManagedInstance
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- ClrCreateManagedInstance
helpviewer_keywords:
- ClrCreateManagedInstance function [.NET Framework hosting]
ms.assetid: 58ba42c0-4857-43bf-a039-73a4dc6544c2
topic_type:
- apiref
ms.openlocfilehash: b6d3b014f54dd563e53cd8a4c48907d01945015f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799923"
---
# <a name="clrcreatemanagedinstance-function"></a><span data-ttu-id="196c0-103">ClrCreateManagedInstance 函数</span><span class="sxs-lookup"><span data-stu-id="196c0-103">ClrCreateManagedInstance Function</span></span>

<span data-ttu-id="196c0-104">创建指定托管类型的实例。</span><span class="sxs-lookup"><span data-stu-id="196c0-104">Creates an instance of the specified managed type.</span></span>  
  
 <span data-ttu-id="196c0-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="196c0-105">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="196c0-106">使用 COM 激活创建托管类型的实例，或使用宿主 (参阅 [.NET Framework 4 和 4.5) 中添加的 CLR 承载接口](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md) 。</span><span class="sxs-lookup"><span data-stu-id="196c0-106">Use COM activation to create an instance of the managed type, or use hosting (see [CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="196c0-107">语法</span><span class="sxs-lookup"><span data-stu-id="196c0-107">Syntax</span></span>  
  
```cpp  
STDAPI ClrCreateManagedInstance (  
    [in]  LPCWSTR  pTypeName,
    [in]  REFIID   riid,
    [out] void     **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="196c0-108">参数</span><span class="sxs-lookup"><span data-stu-id="196c0-108">Parameters</span></span>  

 `pTypeName`  
 <span data-ttu-id="196c0-109">中一个指针，指向所请求的实例类型的名称。</span><span class="sxs-lookup"><span data-stu-id="196c0-109">[in] A pointer to the name of the instance type being requested.</span></span>  
  
 `riid`  
 <span data-ttu-id="196c0-110">中 `IID` 请求的实例类型的。</span><span class="sxs-lookup"><span data-stu-id="196c0-110">[in] The `IID` of the instance type being requested.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="196c0-111">弄指向调用方请求的托管类型实例的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="196c0-111">[out] A pointer to a pointer to an instance of the managed type that was requested by the caller.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="196c0-112">备注</span><span class="sxs-lookup"><span data-stu-id="196c0-112">Remarks</span></span>  

 <span data-ttu-id="196c0-113">公共语言运行时应已加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="196c0-113">The common language runtime should already be loaded into a process.</span></span> <span data-ttu-id="196c0-114">例如，在调用函数之前，可以使用对 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 函数的调用来加载该 `ClrCreateManagedInstance` 函数。</span><span class="sxs-lookup"><span data-stu-id="196c0-114">For example, it can be loaded by using a call to the [CorBindToRuntimeEx](corbindtoruntimeex-function.md) function before the `ClrCreateManagedInstance` function is called.</span></span> <span data-ttu-id="196c0-115">如果未加载运行时，则 `ClrCreateManagedInstance` 首先尝试加载运行时的 v v1.0.3705。</span><span class="sxs-lookup"><span data-stu-id="196c0-115">If the runtime is not loaded, `ClrCreateManagedInstance` first tries to load v1.0.3705 of the runtime.</span></span> <span data-ttu-id="196c0-116">如果失败，它将尝试加载最新版本的运行时。</span><span class="sxs-lookup"><span data-stu-id="196c0-116">If that fails, it attempts to load the latest version of the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="196c0-117">要求</span><span class="sxs-lookup"><span data-stu-id="196c0-117">Requirements</span></span>  

 <span data-ttu-id="196c0-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="196c0-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="196c0-119">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="196c0-119">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="196c0-120">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="196c0-120">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="196c0-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="196c0-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="196c0-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="196c0-122">See also</span></span>

- [<span data-ttu-id="196c0-123">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="196c0-123">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
- [<span data-ttu-id="196c0-124">承载</span><span class="sxs-lookup"><span data-stu-id="196c0-124">Hosting</span></span>](index.md)
