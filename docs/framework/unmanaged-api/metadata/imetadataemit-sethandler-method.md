---
description: 了解详细信息： IMetaDataEmit：： SetHandler 方法
title: IMetaDataEmit::SetHandler 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetHandler
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetHandler
helpviewer_keywords:
- IMetaDataEmit::SetHandler method [.NET Framework metadata]
- SetHandler method [.NET Framework metadata]
ms.assetid: c6c1aaaf-e2cd-407c-b73e-fbe6ffd83bb3
topic_type:
- apiref
ms.openlocfilehash: 07ebf8eef816d373e92a82fc84adacfe5a8599fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657861"
---
# <a name="imetadataemitsethandler-method"></a><span data-ttu-id="789e2-103">IMetaDataEmit::SetHandler 方法</span><span class="sxs-lookup"><span data-stu-id="789e2-103">IMetaDataEmit::SetHandler Method</span></span>

<span data-ttu-id="789e2-104">将指定指针所引用的方法设置 `IUnknown` 为标记重新映射的通知回调。</span><span class="sxs-lookup"><span data-stu-id="789e2-104">Sets the method referenced by the specified `IUnknown` pointer as a notification callback for token remaps.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="789e2-105">语法</span><span class="sxs-lookup"><span data-stu-id="789e2-105">Syntax</span></span>  
  
```cpp  
HRESULT SetHandler (
    [in]  IUnknown    *pUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="789e2-106">参数</span><span class="sxs-lookup"><span data-stu-id="789e2-106">Parameters</span></span>  

 `pUnk`  
 <span data-ttu-id="789e2-107">中要注册的处理程序。</span><span class="sxs-lookup"><span data-stu-id="789e2-107">[in] The handler to register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="789e2-108">备注</span><span class="sxs-lookup"><span data-stu-id="789e2-108">Remarks</span></span>  

 <span data-ttu-id="789e2-109">元数据引擎使用由提供的方法将通知发送 `SetHandler` 到未以优化方式生成记录并且希望优化已保存记录的编译器。</span><span class="sxs-lookup"><span data-stu-id="789e2-109">The metadata engine sends notification by using the method that is provided by `SetHandler`, to compilers that do not generate records in an optimized way and that would like to optimize saved records.</span></span>  
  
 <span data-ttu-id="789e2-110">如果未通过提供回调方法，则 `SetHandler` 不会对保存执行任何优化，只是在 `IMapToken` 每个作用域的合并上使用合并了若干导入范围。</span><span class="sxs-lookup"><span data-stu-id="789e2-110">If the callback method is not provided through `SetHandler`, no optimization will be performed on save except where several import scopes have been merged using `IMapToken` on merge for each scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="789e2-111">要求</span><span class="sxs-lookup"><span data-stu-id="789e2-111">Requirements</span></span>  

 <span data-ttu-id="789e2-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="789e2-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="789e2-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="789e2-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="789e2-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="789e2-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="789e2-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="789e2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="789e2-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="789e2-116">See also</span></span>

- [<span data-ttu-id="789e2-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="789e2-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="789e2-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="789e2-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
