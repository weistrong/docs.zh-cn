---
description: 了解详细信息： IMetaDataEmit2 接口
title: IMetaDataEmit2 接口
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2
helpviewer_keywords:
- IMetaDataEmit2 interface [.NET Framework metadata]
ms.assetid: 866dc96b-bbfc-4c0f-80c2-38ce93072106
topic_type:
- apiref
ms.openlocfilehash: db1880d64bf3b1e9084d6745251c174788a4afe7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99745666"
---
# <a name="imetadataemit2-interface"></a><span data-ttu-id="a0d51-103">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="a0d51-103">IMetaDataEmit2 Interface</span></span>

<span data-ttu-id="a0d51-104">扩展 [IMetaDataEmit](imetadataemit-interface.md) 接口，主要用于提供使用泛型类型的能力。</span><span class="sxs-lookup"><span data-stu-id="a0d51-104">Extends the [IMetaDataEmit](imetadataemit-interface.md) interface primarily to provide the ability to work with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a0d51-105">方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-105">Methods</span></span>  
  
|<span data-ttu-id="a0d51-106">方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-106">Method</span></span>|<span data-ttu-id="a0d51-107">说明</span><span class="sxs-lookup"><span data-stu-id="a0d51-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a0d51-108">DefineGenericParam 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-108">DefineGenericParam Method</span></span>](imetadataemit2-definegenericparam-method.md)|<span data-ttu-id="a0d51-109">创建泛型类型参数的定义，并获取该泛型类型参数的令牌。</span><span class="sxs-lookup"><span data-stu-id="a0d51-109">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>|  
|[<span data-ttu-id="a0d51-110">DefineMethodSpec 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-110">DefineMethodSpec Method</span></span>](imetadataemit2-definemethodspec-method.md)|<span data-ttu-id="a0d51-111">创建方法的泛型实例，并获取定义的标记。</span><span class="sxs-lookup"><span data-stu-id="a0d51-111">Creates a generic instance of a method, and gets a token to the definition.</span></span>|  
|[<span data-ttu-id="a0d51-112">GetDeltaSaveSize 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-112">GetDeltaSaveSize Method</span></span>](imetadataemit2-getdeltasavesize-method.md)|<span data-ttu-id="a0d51-113">获取一个值，该值指示为当前的 "编辑并继续" 会话表示更改所需的数据的大小差异。</span><span class="sxs-lookup"><span data-stu-id="a0d51-113">Gets a value indicating the difference in size of the data that is required to express the changes for the current edit-and-continue session.</span></span>|  
|[<span data-ttu-id="a0d51-114">ResetENCLog 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-114">ResetENCLog Method</span></span>](imetadataemit2-resetenclog-method.md)|<span data-ttu-id="a0d51-115">重置编辑并继续日志并启动新的会话。</span><span class="sxs-lookup"><span data-stu-id="a0d51-115">Resets the edit-and-continue log and starts a new session.</span></span>|  
|[<span data-ttu-id="a0d51-116">SaveDelta 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-116">SaveDelta Method</span></span>](imetadataemit2-savedelta-method.md)|<span data-ttu-id="a0d51-117">将当前的 "编辑并继续" 会话中的更改保存到指定的文件。</span><span class="sxs-lookup"><span data-stu-id="a0d51-117">Saves changes from the current edit-and-continue session to the specified file.</span></span>|  
|[<span data-ttu-id="a0d51-118">SaveDeltaToMemory 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-118">SaveDeltaToMemory Method</span></span>](imetadataemit2-savedeltatomemory-method.md)|<span data-ttu-id="a0d51-119">将当前的 "编辑并继续" 会话中的更改保存到内存。</span><span class="sxs-lookup"><span data-stu-id="a0d51-119">Saves changes from the current edit-and-continue session to memory.</span></span>|  
|[<span data-ttu-id="a0d51-120">SaveDeltaToStream 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-120">SaveDeltaToStream Method</span></span>](imetadataemit2-savedeltatostream-method.md)|<span data-ttu-id="a0d51-121">将当前的 "编辑并继续" 会话中的更改保存到指定的流。</span><span class="sxs-lookup"><span data-stu-id="a0d51-121">Saves changes from the current edit-and-continue session to the specified stream.</span></span>|  
|[<span data-ttu-id="a0d51-122">SetGenericParamProps 方法</span><span class="sxs-lookup"><span data-stu-id="a0d51-122">SetGenericParamProps Method</span></span>](imetadataemit2-setgenericparamprops-method.md)|<span data-ttu-id="a0d51-123">设置指定的标记所引用的泛型参数定义的属性值。</span><span class="sxs-lookup"><span data-stu-id="a0d51-123">Sets property values for the generic parameter definition referenced by the specified token.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a0d51-124">要求</span><span class="sxs-lookup"><span data-stu-id="a0d51-124">Requirements</span></span>  

 <span data-ttu-id="a0d51-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a0d51-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0d51-126">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a0d51-126">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a0d51-127">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a0d51-127">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a0d51-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0d51-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0d51-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0d51-129">See also</span></span>

- [<span data-ttu-id="a0d51-130">元数据接口</span><span class="sxs-lookup"><span data-stu-id="a0d51-130">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="a0d51-131">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="a0d51-131">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
