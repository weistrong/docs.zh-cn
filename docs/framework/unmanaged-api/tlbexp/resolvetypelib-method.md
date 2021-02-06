---
description: 了解详细信息： ResolveTypeLib 方法
title: ResolveTypeLib 方法
ms.date: 03/30/2017
api_name:
- ResolveTypeLib
api_location:
- tlbref.dll
f1_keywords:
- ResolveTypeLib
helpviewer_keywords:
- ITypeLibResolver::ResolveTypeLib method [.NET Framework]
- ResolveTypeLib method [.NET Framework]
ms.assetid: 95d2aa0d-8eeb-4a9f-a216-5249f7e2c167
topic_type:
- apiref
ms.openlocfilehash: ca7f94f630479d30bb9129497b38bcf04e759e5d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646278"
---
# <a name="resolvetypelib-method"></a><span data-ttu-id="e3a67-103">ResolveTypeLib 方法</span><span class="sxs-lookup"><span data-stu-id="e3a67-103">ResolveTypeLib Method</span></span>

<span data-ttu-id="e3a67-104">通过返回类型库的完全限定路径来解析该类型库的简单名称。</span><span class="sxs-lookup"><span data-stu-id="e3a67-104">Resolves the simple name of a type library by returning its fully qualified path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3a67-105">语法</span><span class="sxs-lookup"><span data-stu-id="e3a67-105">Syntax</span></span>  
  
```cpp  
HRESULT ResolveTypeLib(  
    [in]  BSTR      bstrSimpleName,  
    [in]  GUID      tlbid,  
    [in]  LCID      lcid,  
    [in]  USHORT    wMajorVersion,  
    [in]  USHORT    wMinorVersion,  
    [in]  SYSKIND   syskind,  
    [out] BSTR     *pbstrResolvedTlbName);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e3a67-106">参数</span><span class="sxs-lookup"><span data-stu-id="e3a67-106">Parameters</span></span>  

 `bstrSimpleName`  
 <span data-ttu-id="e3a67-107">中一个 [BSTR](/previous-versions/windows/desktop/automat/bstr) ，其中包含类型库的简单名称。</span><span class="sxs-lookup"><span data-stu-id="e3a67-107">[in] A [BSTR](/previous-versions/windows/desktop/automat/bstr) that contains the simple name of the type library.</span></span>  
  
 `tlbid`  
 <span data-ttu-id="e3a67-108">中分配给注册表中的类型库的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e3a67-108">[in] The GUID assigned to the type library in the registry.</span></span>  
  
 `lcid`  
 <span data-ttu-id="e3a67-109">中类型库的本地化 ID。</span><span class="sxs-lookup"><span data-stu-id="e3a67-109">[in] The localization ID of the type library.</span></span>  
  
 `wMajorVersion`  
 <span data-ttu-id="e3a67-110">中类型库的主版本号。</span><span class="sxs-lookup"><span data-stu-id="e3a67-110">[in] The major version number of the type library.</span></span> <span data-ttu-id="e3a67-111">例如，对于版本 *x. y*，主版本号是 *x*。</span><span class="sxs-lookup"><span data-stu-id="e3a67-111">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `wMinorVersion`  
 <span data-ttu-id="e3a67-112">中类型库的次版本号。</span><span class="sxs-lookup"><span data-stu-id="e3a67-112">[in] The minor version number of the type library.</span></span> <span data-ttu-id="e3a67-113">例如，对于版本 *x. y*，次版本号为 *y*。</span><span class="sxs-lookup"><span data-stu-id="e3a67-113">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
 `syskind`  
 <span data-ttu-id="e3a67-114">中标识操作环境的 [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) 标志。</span><span class="sxs-lookup"><span data-stu-id="e3a67-114">[in] A [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) flag that identifies the operating environment.</span></span> <span data-ttu-id="e3a67-115">常用值为 SYS_WIN32 和 SYS_WIN64。</span><span class="sxs-lookup"><span data-stu-id="e3a67-115">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pbstrResolvedTlbName`  
 <span data-ttu-id="e3a67-116">弄指向包含在参数中命名的类型库的完整路径的 [BSTR](/previous-versions/windows/desktop/automat/bstr) 的指针 `bstrSimpleName` 。</span><span class="sxs-lookup"><span data-stu-id="e3a67-116">[out] A pointer to a [BSTR](/previous-versions/windows/desktop/automat/bstr) that contains the full path of the type library named in the `bstrSimpleName` parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e3a67-117">备注</span><span class="sxs-lookup"><span data-stu-id="e3a67-117">Remarks</span></span>  

 <span data-ttu-id="e3a67-118">`ResolveTypeLib`方法由[LoadTypeLibWithResolver 函数](loadtypelibwithresolver-function.md)在[Tlbexp.exe (类型库导出程序) ](../../tools/tlbexp-exe-type-library-exporter.md)处理期间调用。</span><span class="sxs-lookup"><span data-stu-id="e3a67-118">The `ResolveTypeLib` method is called by the [LoadTypeLibWithResolver function](loadtypelibwithresolver-function.md) during [Tlbexp.exe (Type Library Exporter)](../../tools/tlbexp-exe-type-library-exporter.md) processing.</span></span>  
  
 <span data-ttu-id="e3a67-119">此接口的自定义实现必须返回[](/previous-versions/windows/desktop/automat/bstr)包含参数中名为的类型库的完整路径的 BSTR `bstrSimpleName` 。</span><span class="sxs-lookup"><span data-stu-id="e3a67-119">Custom implementations of this interface must return a [BSTR](/previous-versions/windows/desktop/automat/bstr) that contains the full path of the type library named in the `bstrSimpleName` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3a67-120">要求</span><span class="sxs-lookup"><span data-stu-id="e3a67-120">Requirements</span></span>  

 <span data-ttu-id="e3a67-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e3a67-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3a67-122">**标头：** TlbRef，TlbRef</span><span class="sxs-lookup"><span data-stu-id="e3a67-122">**Header:** TlbRef.idl, TlbRef.h</span></span>  
  
 <span data-ttu-id="e3a67-123">**库：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="e3a67-123">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="e3a67-124">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3a67-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3a67-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="e3a67-125">See also</span></span>

- [<span data-ttu-id="e3a67-126">Tlbexp Helper 函数</span><span class="sxs-lookup"><span data-stu-id="e3a67-126">Tlbexp Helper Functions</span></span>](index.md)
- [<span data-ttu-id="e3a67-127">LoadTypeLibEx</span><span class="sxs-lookup"><span data-stu-id="e3a67-127">LoadTypeLibEx</span></span>](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
