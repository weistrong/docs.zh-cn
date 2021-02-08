---
description: 了解详细信息： IMetaDataEmit：： GetSaveSize 方法
title: IMetaDataEmit::GetSaveSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetSaveSize
helpviewer_keywords:
- IMetaDataEmit::GetSaveSize method [.NET Framework metadata]
- GetSaveSize method [.NET Framework metadata]
ms.assetid: 8aea2e2c-23a3-4cda-9a06-e19f97383830
topic_type:
- apiref
ms.openlocfilehash: 871e9f911eaaf1b1a7259466402e492d75aa7fb8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783932"
---
# <a name="imetadataemitgetsavesize-method"></a><span data-ttu-id="9a494-103">IMetaDataEmit::GetSaveSize 方法</span><span class="sxs-lookup"><span data-stu-id="9a494-103">IMetaDataEmit::GetSaveSize Method</span></span>

<span data-ttu-id="9a494-104">获取当前范围内的程序集和它的元数据的预计二进制大小。</span><span class="sxs-lookup"><span data-stu-id="9a494-104">Gets the estimated binary size of the assembly and its metadata in the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a494-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a494-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSaveSize (  
    [in]  CorSaveSize fSave,  
    [out] DWORD       *pdwSaveSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a494-106">参数</span><span class="sxs-lookup"><span data-stu-id="9a494-106">Parameters</span></span>  

 `fSave`  
 <span data-ttu-id="9a494-107">中 [CorSaveSize](corsavesize-enumeration.md) 枚举的一个值，该值指定是获取准确大小还是近似大小。</span><span class="sxs-lookup"><span data-stu-id="9a494-107">[in] A value of the [CorSaveSize](corsavesize-enumeration.md) enumeration that specifies whether to get an accurate or approximate size.</span></span> <span data-ttu-id="9a494-108">只有三个值有效： cssAccurate、cssQuick 和 cssDiscardTransientCAs：</span><span class="sxs-lookup"><span data-stu-id="9a494-108">Only three values are valid: cssAccurate, cssQuick, and cssDiscardTransientCAs:</span></span>  
  
- <span data-ttu-id="9a494-109">cssAccurate 返回准确的保存大小，但需要更长的时间来计算。</span><span class="sxs-lookup"><span data-stu-id="9a494-109">cssAccurate returns the exact save size but takes longer to calculate.</span></span>  
  
- <span data-ttu-id="9a494-110">cssQuick 返回大小，为安全起见，但计算时间较少。</span><span class="sxs-lookup"><span data-stu-id="9a494-110">cssQuick returns a size, padded for safety, but takes less time to calculate.</span></span>  
  
- <span data-ttu-id="9a494-111">cssDiscardTransientCAs 告知 `GetSaveSize` 它可以丢弃可放弃的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="9a494-111">cssDiscardTransientCAs tells `GetSaveSize` that it can throw away discardable custom attributes.</span></span>  
  
 `pdwSaveSize`  
 <span data-ttu-id="9a494-112">弄一个指针，指向保存该文件所需的大小。</span><span class="sxs-lookup"><span data-stu-id="9a494-112">[out] A pointer to the size that is required to save the file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9a494-113">备注</span><span class="sxs-lookup"><span data-stu-id="9a494-113">Remarks</span></span>  

 <span data-ttu-id="9a494-114">`GetSaveSize` 计算在当前作用域中保存程序集及其所有元数据所需的空间（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9a494-114">`GetSaveSize` calculates the space required, in bytes, to save the assembly and all its metadata in the current scope.</span></span> <span data-ttu-id="9a494-115"> (对 [IMetaDataEmit：： SaveToStream](imetadataemit-savetostream-method.md) 方法的调用将发出此数目的字节。 ) </span><span class="sxs-lookup"><span data-stu-id="9a494-115">(A call to the [IMetaDataEmit::SaveToStream](imetadataemit-savetostream-method.md) method would emit this number of bytes.)</span></span>  
  
 <span data-ttu-id="9a494-116">如果调用方通过[IMetaDataEmit：： SetHandler](imetadataemit-sethandler-method.md)或[IMetaDataEmit：： Merge](imetadataemit-merge-method.md)) 实现了[IMapToken](imaptoken-interface.md) (接口， `GetSaveSize` 则将对元数据执行两次传递以对其进行优化和压缩。</span><span class="sxs-lookup"><span data-stu-id="9a494-116">If the caller implements the [IMapToken](imaptoken-interface.md) interface (through [IMetaDataEmit::SetHandler](imetadataemit-sethandler-method.md) or [IMetaDataEmit::Merge](imetadataemit-merge-method.md)), `GetSaveSize` will perform two passes over the metadata to optimize and compress it.</span></span> <span data-ttu-id="9a494-117">否则，不执行任何优化。</span><span class="sxs-lookup"><span data-stu-id="9a494-117">Otherwise, no optimizations are performed.</span></span>  
  
 <span data-ttu-id="9a494-118">如果执行了优化，则第一个传递将只对元数据结构进行排序，以优化导入时间搜索的性能。</span><span class="sxs-lookup"><span data-stu-id="9a494-118">If optimization is performed, the first pass simply sorts the metadata structures to tune the performance of import-time searches.</span></span> <span data-ttu-id="9a494-119">此步骤通常会导致四处移动记录，并产生副作用，由工具保留的标记将会失效。</span><span class="sxs-lookup"><span data-stu-id="9a494-119">This step typically results in moving records around, with the side effect that tokens retained by the tool for future reference are invalidated.</span></span> <span data-ttu-id="9a494-120">但是，在第二次传递后，元数据不会将这些令牌更改通知给调用方。</span><span class="sxs-lookup"><span data-stu-id="9a494-120">The metadata does not inform the caller of these token changes until after the second pass, however.</span></span> <span data-ttu-id="9a494-121">在第二次传递中，将执行各种优化，以减少元数据的总大小，例如在 `mdTypeRef` `mdMemberRef` 引用指向在当前元数据范围内声明的类型或成员时，将 (早期绑定) 和标记。</span><span class="sxs-lookup"><span data-stu-id="9a494-121">In the second pass, various optimizations are performed that are intended to reduce the overall size of the metadata, such as optimizing away (early binding) `mdTypeRef` and `mdMemberRef` tokens when the reference is to a type or member that is declared in the current metadata scope.</span></span> <span data-ttu-id="9a494-122">在此阶段中，会发生另一轮标记映射。</span><span class="sxs-lookup"><span data-stu-id="9a494-122">In this pass, another round of token mapping occurs.</span></span> <span data-ttu-id="9a494-123">此次传递后，元数据引擎通过其接口通知调用方 `IMapToken` 所有已更改的令牌值。</span><span class="sxs-lookup"><span data-stu-id="9a494-123">After this pass, the metadata engine notifies the caller, through its `IMapToken` interface, of any changed token values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a494-124">要求</span><span class="sxs-lookup"><span data-stu-id="9a494-124">Requirements</span></span>  

 <span data-ttu-id="9a494-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9a494-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a494-126">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9a494-126">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9a494-127">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9a494-127">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9a494-128">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9a494-128">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a494-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a494-129">See also</span></span>

- [<span data-ttu-id="9a494-130">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="9a494-130">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="9a494-131">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="9a494-131">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
