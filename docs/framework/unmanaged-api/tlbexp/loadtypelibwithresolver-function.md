---
description: 了解详细信息： LoadTypeLibWithResolver 函数
title: LoadTypeLibWithResolver 函数
ms.date: 03/30/2017
api_name:
- LoadTypeLibWithResolver
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- LoadTypeLibWithResolver
helpviewer_keywords:
- LoadTypeLibWithResolver function [.NET Framework]
ms.assetid: 7123a89b-eb9b-463a-a552-a081e33b0a3a
topic_type:
- apiref
ms.openlocfilehash: 6747199364a549d922ad73bfac3e93b329d1172a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646213"
---
# <a name="loadtypelibwithresolver-function"></a><span data-ttu-id="28029-103">LoadTypeLibWithResolver 函数</span><span class="sxs-lookup"><span data-stu-id="28029-103">LoadTypeLibWithResolver Function</span></span>

<span data-ttu-id="28029-104">加载类型库，并使用提供的 [ITypeLibResolver 接口](itypelibresolver-interface.md) 解析任何内部引用的类型库。</span><span class="sxs-lookup"><span data-stu-id="28029-104">Loads a type library and uses the supplied [ITypeLibResolver interface](itypelibresolver-interface.md) to resolve any internally referenced type libraries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28029-105">语法</span><span class="sxs-lookup"><span data-stu-id="28029-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadTypeLibWithResolver(  
    [in]  LPCOLESTR           szFile,  
    [in]  REGKIND             regkind,  
    [in]  ITypeLibResolver   *pTlbResolver,  
    [out] ITypeLib          **pptlib);  
```  
  
## <a name="parameters"></a><span data-ttu-id="28029-106">参数</span><span class="sxs-lookup"><span data-stu-id="28029-106">Parameters</span></span>  

 `szFile`  
 <span data-ttu-id="28029-107">中类型库的文件路径。</span><span class="sxs-lookup"><span data-stu-id="28029-107">[in] The file path of the type library.</span></span>  
  
 `regkind`  
 <span data-ttu-id="28029-108">中用于控制如何注册类型库的 [REGKIND 枚举](/windows/win32/api/oleauto/ne-oleauto-regkind) 标志。</span><span class="sxs-lookup"><span data-stu-id="28029-108">[in] A [REGKIND enumeration](/windows/win32/api/oleauto/ne-oleauto-regkind) flag that controls how the type library is registered.</span></span> <span data-ttu-id="28029-109">其可能的值为：</span><span class="sxs-lookup"><span data-stu-id="28029-109">Its possible values are:</span></span>  
  
- <span data-ttu-id="28029-110">`REGKIND_DEFAULT`：使用默认注册行为。</span><span class="sxs-lookup"><span data-stu-id="28029-110">`REGKIND_DEFAULT`: Use default registration behavior.</span></span>  
  
- <span data-ttu-id="28029-111">`REGKIND_REGISTER`：注册此类型库。</span><span class="sxs-lookup"><span data-stu-id="28029-111">`REGKIND_REGISTER`: Register this type library.</span></span>  
  
- <span data-ttu-id="28029-112">`REGKIND_NONE`：请勿注册此类型库。</span><span class="sxs-lookup"><span data-stu-id="28029-112">`REGKIND_NONE`: Do not register this type library.</span></span>  
  
 `pTlbResolver`  
 <span data-ttu-id="28029-113">中指向 [ITypeLibResolver 接口](itypelibresolver-interface.md)的实现的指针。</span><span class="sxs-lookup"><span data-stu-id="28029-113">[in] A pointer to the implementation of the [ITypeLibResolver interface](itypelibresolver-interface.md).</span></span>  
  
 `pptlib`  
 <span data-ttu-id="28029-114">弄对正在加载的类型库的引用。</span><span class="sxs-lookup"><span data-stu-id="28029-114">[out] A reference to the type library that is being loaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="28029-115">返回值</span><span class="sxs-lookup"><span data-stu-id="28029-115">Return Value</span></span>  

 <span data-ttu-id="28029-116">下表中列出的其中一个 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="28029-116">One of the HRESULT values listed in the following table.</span></span>  
  
|<span data-ttu-id="28029-117">返回值</span><span class="sxs-lookup"><span data-stu-id="28029-117">Return value</span></span>|<span data-ttu-id="28029-118">含义</span><span class="sxs-lookup"><span data-stu-id="28029-118">Meaning</span></span>|  
|------------------|-------------|  
|`S_OK`|<span data-ttu-id="28029-119">成功。</span><span class="sxs-lookup"><span data-stu-id="28029-119">Success.</span></span>|  
|`E_OUTOFMEMORY`|<span data-ttu-id="28029-120">内存不足。</span><span class="sxs-lookup"><span data-stu-id="28029-120">Out of memory.</span></span>|  
|`E_POINTER`|<span data-ttu-id="28029-121">一个或多个指针无效。</span><span class="sxs-lookup"><span data-stu-id="28029-121">One or more of the pointers are invalid.</span></span>|  
|`E_INVALIDARG`|<span data-ttu-id="28029-122">一个或多个参数无效。</span><span class="sxs-lookup"><span data-stu-id="28029-122">One or more of the arguments are invalid.</span></span>|  
|`TYPE_E_IOERROR`|<span data-ttu-id="28029-123">函数无法写入文件。</span><span class="sxs-lookup"><span data-stu-id="28029-123">The function could not write to the file.</span></span>|  
|`TYPE_E_REGISTRYACCESS`|<span data-ttu-id="28029-124">无法打开系统注册数据库。</span><span class="sxs-lookup"><span data-stu-id="28029-124">The system registration database could not be opened.</span></span>|  
|`TYPE_E_INVALIDSTATE`|<span data-ttu-id="28029-125">无法打开类型库。</span><span class="sxs-lookup"><span data-stu-id="28029-125">The type library could not be opened.</span></span>|  
|`TYPE_E_CANTLOADLIBRARY`|<span data-ttu-id="28029-126">未能加载类型库或 DLL。</span><span class="sxs-lookup"><span data-stu-id="28029-126">The type library or DLL could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28029-127">备注</span><span class="sxs-lookup"><span data-stu-id="28029-127">Remarks</span></span>  

 <span data-ttu-id="28029-128">[ (类型库导出程序)Tlbexp.exe](../../tools/tlbexp-exe-type-library-exporter.md)在 `LoadTypeLibWithResolver` 程序集到类型库转换过程中调用该函数。</span><span class="sxs-lookup"><span data-stu-id="28029-128">The [Tlbexp.exe (Type Library Exporter)](../../tools/tlbexp-exe-type-library-exporter.md) calls the `LoadTypeLibWithResolver` function during the assembly-to-type-library conversion process.</span></span>  
  
 <span data-ttu-id="28029-129">此函数加载指定的类型库，并对注册表的访问权限降至最低。</span><span class="sxs-lookup"><span data-stu-id="28029-129">This function loads the specified type library with minimal access to the registry.</span></span> <span data-ttu-id="28029-130">然后，该函数检查类型库以查找内部引用的类型库，其中每个库必须加载并添加到父类型库中。</span><span class="sxs-lookup"><span data-stu-id="28029-130">The function then examines the type library for internally referenced type libraries, each of which must be loaded and added to the parent type library.</span></span>  
  
 <span data-ttu-id="28029-131">在可以加载引用的类型库之前，必须将其引用文件路径解析为完整文件路径。</span><span class="sxs-lookup"><span data-stu-id="28029-131">Before a referenced type library can be loaded, its reference file path must be resolved to a full file path.</span></span> <span data-ttu-id="28029-132">这是通过[ITypeLibResolver 接口](itypelibresolver-interface.md)提供的[ResolveTypeLib 方法](resolvetypelib-method.md)实现的，该方法是在参数中传递的 `pTlbResolver` 。</span><span class="sxs-lookup"><span data-stu-id="28029-132">This is accomplished through the [ResolveTypeLib method](resolvetypelib-method.md) that is provided by the [ITypeLibResolver interface](itypelibresolver-interface.md), which is passed in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="28029-133">当所引用的类型库的完整文件路径已知时， `LoadTypeLibWithResolver` 函数将加载引用的类型库并将其添加到父类型库中，从而创建组合的主类型库。</span><span class="sxs-lookup"><span data-stu-id="28029-133">When the full file path of the referenced type library is known, the `LoadTypeLibWithResolver` function loads and adds the referenced type library to the parent type library, creating a combined master type library.</span></span>  
  
 <span data-ttu-id="28029-134">函数解析并加载所有内部引用的类型库后，将在参数中返回对主解析类型库的引用 `pptlib` 。</span><span class="sxs-lookup"><span data-stu-id="28029-134">After the function resolves and loads all internally referenced type libraries, it returns a reference to the master resolved type library in the `pptlib` parameter.</span></span>  
  
 <span data-ttu-id="28029-135">`LoadTypeLibWithResolver`函数通常由[Tlbexp.exe (类型库导出程序) ](../../tools/tlbexp-exe-type-library-exporter.md)，后者在参数中提供自己的内部[ITypeLibResolver 接口](itypelibresolver-interface.md)实现 `pTlbResolver` 。</span><span class="sxs-lookup"><span data-stu-id="28029-135">The `LoadTypeLibWithResolver` function is generally called by the [Tlbexp.exe (Type Library Exporter)](../../tools/tlbexp-exe-type-library-exporter.md), which supplies its own internal [ITypeLibResolver interface](itypelibresolver-interface.md) implementation in the `pTlbResolver` parameter.</span></span>  
  
 <span data-ttu-id="28029-136">如果直接调用 `LoadTypeLibWithResolver` ，则必须提供自己的 [ITypeLibResolver 接口](itypelibresolver-interface.md) 实现。</span><span class="sxs-lookup"><span data-stu-id="28029-136">If you call `LoadTypeLibWithResolver` directly, you must supply your own [ITypeLibResolver interface](itypelibresolver-interface.md) implementation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28029-137">要求</span><span class="sxs-lookup"><span data-stu-id="28029-137">Requirements</span></span>  

 <span data-ttu-id="28029-138">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28029-138">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28029-139">**标头：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="28029-139">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="28029-140">**库：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="28029-140">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="28029-141">**.NET Framework 版本：** 3.5、3.0、2。0</span><span class="sxs-lookup"><span data-stu-id="28029-141">**.NET Framework Version:** 3.5, 3.0, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28029-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="28029-142">See also</span></span>

- [<span data-ttu-id="28029-143">Tlbexp Helper 函数</span><span class="sxs-lookup"><span data-stu-id="28029-143">Tlbexp Helper Functions</span></span>](index.md)
- [<span data-ttu-id="28029-144">LoadTypeLibEx 函数</span><span class="sxs-lookup"><span data-stu-id="28029-144">LoadTypeLibEx Function</span></span>](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
