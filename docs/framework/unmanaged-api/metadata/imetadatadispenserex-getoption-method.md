---
description: 了解详细信息： IMetaDataDispenserEx：： GetOption 方法
title: IMetaDataDispenserEx::GetOption 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetOption
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetOption
helpviewer_keywords:
- GetOption method [.NET Framework metadata]
- IMetaDataDispenserEx::GetOption method [.NET Framework metadata]
ms.assetid: d7f794e5-8e25-4d65-850a-7c34fbfce87d
topic_type:
- apiref
ms.openlocfilehash: cf52a251c3c0e0485558a150b727d58eeae81995
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753544"
---
# <a name="imetadatadispenserexgetoption-method"></a><span data-ttu-id="a9499-103">IMetaDataDispenserEx::GetOption 方法</span><span class="sxs-lookup"><span data-stu-id="a9499-103">IMetaDataDispenserEx::GetOption Method</span></span>

<span data-ttu-id="a9499-104">为当前元数据范围获取指定选项的值。</span><span class="sxs-lookup"><span data-stu-id="a9499-104">Gets the value of the specified option for the current metadata scope.</span></span> <span data-ttu-id="a9499-105">选项控制如何处理对当前元数据范围的调用。</span><span class="sxs-lookup"><span data-stu-id="a9499-105">The option controls how calls to the current metadata scope are handled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9499-106">语法</span><span class="sxs-lookup"><span data-stu-id="a9499-106">Syntax</span></span>  
  
```cpp  
HRESULT GetOption (  
    [in]  REFGUID         optionId,
    [out] const VARIANT   *pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9499-107">参数</span><span class="sxs-lookup"><span data-stu-id="a9499-107">Parameters</span></span>  

 `optionId`  
 <span data-ttu-id="a9499-108">中指向 GUID 的指针，该 GUID 指定要检索的选项。</span><span class="sxs-lookup"><span data-stu-id="a9499-108">[in] A pointer to a GUID that specifies the option to be retrieved.</span></span> <span data-ttu-id="a9499-109">有关支持的 Guid 的列表，请参阅 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="a9499-109">See the Remarks section for a list of supported GUIDs.</span></span>  
  
 `pValue`  
 <span data-ttu-id="a9499-110">弄返回的选项的值。</span><span class="sxs-lookup"><span data-stu-id="a9499-110">[out] The value of the returned option.</span></span> <span data-ttu-id="a9499-111">此值的类型将是指定选项的类型的变体。</span><span class="sxs-lookup"><span data-stu-id="a9499-111">The type of this value will be a variant of the specified option's type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9499-112">备注</span><span class="sxs-lookup"><span data-stu-id="a9499-112">Remarks</span></span>  

 <span data-ttu-id="a9499-113">以下列表显示了此方法支持的 Guid。</span><span class="sxs-lookup"><span data-stu-id="a9499-113">The following list shows the GUIDs that are supported for this method.</span></span> <span data-ttu-id="a9499-114">有关说明，请参阅 [IMetaDataDispenserEx：： SetOption](imetadatadispenserex-setoption-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a9499-114">For descriptions, see the [IMetaDataDispenserEx::SetOption](imetadatadispenserex-setoption-method.md) method.</span></span> <span data-ttu-id="a9499-115">如果不 `optionId` 在此列表中，则此方法返回 HRESULT `E_INVALIDARG` ，指示参数不正确。</span><span class="sxs-lookup"><span data-stu-id="a9499-115">If `optionId` is not in this list, this method returns HRESULT `E_INVALIDARG`, indicating an incorrect parameter.</span></span>  
  
- <span data-ttu-id="a9499-116">MetaDataCheckDuplicatesFor</span><span class="sxs-lookup"><span data-stu-id="a9499-116">MetaDataCheckDuplicatesFor</span></span>  
  
- <span data-ttu-id="a9499-117">MetaDataRefToDefCheck</span><span class="sxs-lookup"><span data-stu-id="a9499-117">MetaDataRefToDefCheck</span></span>  
  
- <span data-ttu-id="a9499-118">MetaDataNotificationForTokenMovement</span><span class="sxs-lookup"><span data-stu-id="a9499-118">MetaDataNotificationForTokenMovement</span></span>  
  
- <span data-ttu-id="a9499-119">MetaDataSetENC</span><span class="sxs-lookup"><span data-stu-id="a9499-119">MetaDataSetENC</span></span>  
  
- <span data-ttu-id="a9499-120">MetaDataErrorIfEmitOutOfOrder</span><span class="sxs-lookup"><span data-stu-id="a9499-120">MetaDataErrorIfEmitOutOfOrder</span></span>  
  
- <span data-ttu-id="a9499-121">MetaDataGenerateTCEAdapters</span><span class="sxs-lookup"><span data-stu-id="a9499-121">MetaDataGenerateTCEAdapters</span></span>  
  
- <span data-ttu-id="a9499-122">MetaDataLinkerOptions</span><span class="sxs-lookup"><span data-stu-id="a9499-122">MetaDataLinkerOptions</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9499-123">要求</span><span class="sxs-lookup"><span data-stu-id="a9499-123">Requirements</span></span>  

 <span data-ttu-id="a9499-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a9499-124">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9499-125">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a9499-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a9499-126">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a9499-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a9499-127">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9499-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9499-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9499-128">See also</span></span>

- [<span data-ttu-id="a9499-129">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="a9499-129">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="a9499-130">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="a9499-130">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
