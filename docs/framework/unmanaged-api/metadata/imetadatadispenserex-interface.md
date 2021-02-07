---
description: 了解详细信息： IMetaDataDispenserEx 接口
title: IMetaDataDispenserEx 接口
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx
helpviewer_keywords:
- IMetaDataDispenserEx interface [.NET Framework metadata]
ms.assetid: 78b3629e-77a2-4406-89c3-56b5cc2c4594
topic_type:
- apiref
ms.openlocfilehash: d940ac20eaad4b930ab17fb2d194d3b03bd4cf3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753531"
---
# <a name="imetadatadispenserex-interface"></a><span data-ttu-id="c98b2-103">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="c98b2-103">IMetaDataDispenserEx Interface</span></span>

<span data-ttu-id="c98b2-104">扩展 [IMetaDataDispenser 接口](imetadatadispenser-interface.md) 接口，以提供控制元数据 api 对当前元数据范围的操作方式的功能。</span><span class="sxs-lookup"><span data-stu-id="c98b2-104">Extends the [IMetaDataDispenser Interface](imetadatadispenser-interface.md) interface to provide the capability to control how the metadata APIs operate on the current metadata scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c98b2-105">方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-105">Methods</span></span>  
  
|<span data-ttu-id="c98b2-106">方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-106">Method</span></span>|<span data-ttu-id="c98b2-107">说明</span><span class="sxs-lookup"><span data-stu-id="c98b2-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c98b2-108">FindAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-108">FindAssembly Method</span></span>](imetadatadispenserex-findassembly-method.md)|<span data-ttu-id="c98b2-109">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="c98b2-109">This method is not implemented.</span></span> <span data-ttu-id="c98b2-110">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c98b2-110">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="c98b2-111">FindAssemblyModule 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-111">FindAssemblyModule Method</span></span>](imetadatadispenserex-findassemblymodule-method.md)|<span data-ttu-id="c98b2-112">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="c98b2-112">This method is not implemented.</span></span> <span data-ttu-id="c98b2-113">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c98b2-113">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="c98b2-114">GetCORSystemDirectory 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-114">GetCORSystemDirectory Method</span></span>](imetadatadispenserex-getcorsystemdirectory-method.md)|<span data-ttu-id="c98b2-115">获取 (CLR) 保存当前公共语言运行时的目录。</span><span class="sxs-lookup"><span data-stu-id="c98b2-115">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="c98b2-116">此方法仅支持在进程外调试器中使用。</span><span class="sxs-lookup"><span data-stu-id="c98b2-116">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="c98b2-117">如果从另一个组件调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c98b2-117">If called from another component, it will return E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="c98b2-118">GetOption 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-118">GetOption Method</span></span>](imetadatadispenserex-getoption-method.md)|<span data-ttu-id="c98b2-119">为当前元数据范围获取指定选项的值。</span><span class="sxs-lookup"><span data-stu-id="c98b2-119">Gets the value of the specified option for the current metadata scope.</span></span> <span data-ttu-id="c98b2-120">选项控制如何处理对当前元数据范围的调用。</span><span class="sxs-lookup"><span data-stu-id="c98b2-120">The option controls how calls to the current metadata scope are handled.</span></span>|  
|[<span data-ttu-id="c98b2-121">OpenScopeOnITypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-121">OpenScopeOnITypeInfo Method</span></span>](imetadatadispenserex-openscopeonitypeinfo-method.md)|<span data-ttu-id="c98b2-122">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="c98b2-122">This method is not implemented.</span></span> <span data-ttu-id="c98b2-123">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c98b2-123">If called, it returns E_NOTIMPL.</span></span>|  
|[<span data-ttu-id="c98b2-124">SetOption 方法</span><span class="sxs-lookup"><span data-stu-id="c98b2-124">SetOption Method</span></span>](imetadatadispenserex-setoption-method.md)|<span data-ttu-id="c98b2-125">为当前元数据范围将指定的选项设置为给定的值。</span><span class="sxs-lookup"><span data-stu-id="c98b2-125">Sets the specified option to a given value for the current metadata scope.</span></span> <span data-ttu-id="c98b2-126">选项控制如何处理对当前元数据范围的调用。</span><span class="sxs-lookup"><span data-stu-id="c98b2-126">The option controls how calls to the current metadata scope are handled.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c98b2-127">要求</span><span class="sxs-lookup"><span data-stu-id="c98b2-127">Requirements</span></span>  

 <span data-ttu-id="c98b2-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c98b2-128">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c98b2-129">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c98b2-129">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c98b2-130">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c98b2-130">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c98b2-131">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c98b2-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c98b2-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="c98b2-132">See also</span></span>

- [<span data-ttu-id="c98b2-133">元数据接口</span><span class="sxs-lookup"><span data-stu-id="c98b2-133">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="c98b2-134">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="c98b2-134">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
- [<span data-ttu-id="c98b2-135">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="c98b2-135">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="c98b2-136">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="c98b2-136">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
