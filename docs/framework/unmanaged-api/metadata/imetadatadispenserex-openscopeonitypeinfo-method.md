---
description: 了解详细信息： IMetaDataDispenserEx：： OpenScopeOnITypeInfo 方法
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.OpenScopeOnITypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::OpenScopeOnITypeInfo
helpviewer_keywords:
- OpenScopeOnITypeInfo method [.NET Framework metadata]
- IMetaDataDispenserEx::OpenScopeOnITypeInfo method [.NET Framework metadata]
ms.assetid: 3480bbdb-c442-44a0-b7c6-333354503c52
topic_type:
- apiref
ms.openlocfilehash: bc36bac9e7c63f56f442f1e25fd7a6a93f75924b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753518"
---
# <a name="imetadatadispenserexopenscopeonitypeinfo-method"></a><span data-ttu-id="7acfc-103">IMetaDataDispenserEx::OpenScopeOnITypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7acfc-103">IMetaDataDispenserEx::OpenScopeOnITypeInfo Method</span></span>

<span data-ttu-id="7acfc-104">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="7acfc-104">This method is not implemented.</span></span> <span data-ttu-id="7acfc-105">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="7acfc-105">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7acfc-106">语法</span><span class="sxs-lookup"><span data-stu-id="7acfc-106">Syntax</span></span>  
  
```cpp  
HRESULT OpenScopeOnITypeInfo (  
    [in]  ITypeInfo   *pITI,  
    [in]  DWORD       dwOpenFlags,  
    [in]  REFIID      riid,  
    [out] IUnknown    **ppIUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7acfc-107">参数</span><span class="sxs-lookup"><span data-stu-id="7acfc-107">Parameters</span></span>  

 `pITI`  
 <span data-ttu-id="7acfc-108">中指向 [ITypeInfo](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) 接口的指针，该接口提供要打开范围的类型信息。</span><span class="sxs-lookup"><span data-stu-id="7acfc-108">[in] Pointer to an [ITypeInfo](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) interface that provides the type information on which to open the scope.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="7acfc-109">中打开模式标志。</span><span class="sxs-lookup"><span data-stu-id="7acfc-109">[in] The open mode flags.</span></span>  
  
 `riid`  
 <span data-ttu-id="7acfc-110">中所需的接口。</span><span class="sxs-lookup"><span data-stu-id="7acfc-110">[in] The desired interface.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="7acfc-111">弄指向返回接口的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="7acfc-111">[out] Pointer to a pointer to the returned interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7acfc-112">要求</span><span class="sxs-lookup"><span data-stu-id="7acfc-112">Requirements</span></span>  

 <span data-ttu-id="7acfc-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7acfc-113">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7acfc-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="7acfc-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7acfc-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="7acfc-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7acfc-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7acfc-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7acfc-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="7acfc-117">See also</span></span>

- [<span data-ttu-id="7acfc-118">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="7acfc-118">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="7acfc-119">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="7acfc-119">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
