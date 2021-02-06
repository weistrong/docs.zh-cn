---
description: 了解详细信息： IMetaDataEmit：： SetMethodImplFlags 方法
title: IMetaDataEmit::SetMethodImplFlags 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetMethodImplFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetMethodImplFlags
helpviewer_keywords:
- IMetaDataEmit::SetMethodImplFlags method [.NET Framework metadata]
- SetMethodImpFlags method [.NET Framework metadata]
ms.assetid: 4bc82d9b-9544-4be3-ba51-a2d4d806158a
topic_type:
- apiref
ms.openlocfilehash: ea7f3122a21c8651014e60de3629db87eeaf6260
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657825"
---
# <a name="imetadataemitsetmethodimplflags-method"></a><span data-ttu-id="b7ec0-103">IMetaDataEmit::SetMethodImplFlags 方法</span><span class="sxs-lookup"><span data-stu-id="b7ec0-103">IMetaDataEmit::SetMethodImplFlags Method</span></span>

<span data-ttu-id="b7ec0-104">设置或更新指定的标记所引用的继承方法实现的元数据签名。</span><span class="sxs-lookup"><span data-stu-id="b7ec0-104">Sets or updates the metadata signature of the inherited method implementation that is referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7ec0-105">语法</span><span class="sxs-lookup"><span data-stu-id="b7ec0-105">Syntax</span></span>  
  
```cpp  
HRESULT SetMethodImplFlags (
    [in]  mdMethodDef   md,
    [in]  DWORD         dwImplFlags
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7ec0-106">参数</span><span class="sxs-lookup"><span data-stu-id="b7ec0-106">Parameters</span></span>  

 `md`  
 <span data-ttu-id="b7ec0-107">中要更改的方法的标记。</span><span class="sxs-lookup"><span data-stu-id="b7ec0-107">[in] The token for the method to be changed.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="b7ec0-108">中用于指定方法实现功能的 [CorMethodImpl](cormethodimpl-enumeration.md) 枚举值的组合。</span><span class="sxs-lookup"><span data-stu-id="b7ec0-108">[in] A combination of the values of the [CorMethodImpl](cormethodimpl-enumeration.md) enumeration that specifies the method implementation features.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7ec0-109">要求</span><span class="sxs-lookup"><span data-stu-id="b7ec0-109">Requirements</span></span>  

 <span data-ttu-id="b7ec0-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ec0-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7ec0-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b7ec0-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b7ec0-112">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b7ec0-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b7ec0-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7ec0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7ec0-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7ec0-114">See also</span></span>

- [<span data-ttu-id="b7ec0-115">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="b7ec0-115">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="b7ec0-116">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="b7ec0-116">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
