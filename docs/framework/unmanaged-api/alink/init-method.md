---
description: 了解有关以下内容的详细信息： Init 方法
title: Init 方法
ms.date: 03/30/2017
api_name:
- IALink.Init
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- Init
helpviewer_keywords:
- Init method
ms.assetid: e48b5c64-049f-4f93-ad87-d07ae9cd5845
topic_type:
- apiref
ms.openlocfilehash: 531e05a09cbecbfb67c8c004d1e4ba1deb7e59a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662554"
---
# <a name="init-method"></a><span data-ttu-id="a7a3d-103">Init 方法</span><span class="sxs-lookup"><span data-stu-id="a7a3d-103">Init Method</span></span>

<span data-ttu-id="a7a3d-104">准备实现 [IALink 接口](ialink-interface.md) 以便使用的对象。</span><span class="sxs-lookup"><span data-stu-id="a7a3d-104">Prepares objects implementing the [IALink Interface](ialink-interface.md) for use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7a3d-105">语法</span><span class="sxs-lookup"><span data-stu-id="a7a3d-105">Syntax</span></span>  
  
```cpp  
HRESULT Init(  
    IMetaDataDispenserEx* pDispenser,  
    IMetaDataError* pErrorHandler  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a7a3d-106">参数</span><span class="sxs-lookup"><span data-stu-id="a7a3d-106">Parameters</span></span>  

 `pDispenser`  
 <span data-ttu-id="a7a3d-107">指向元数据分配器的[IMetaDataDispenserEx 接口](../metadata/imetadatadispenserex-interface.md)指针。</span><span class="sxs-lookup"><span data-stu-id="a7a3d-107">[IMetaDataDispenserEx Interface](../metadata/imetadatadispenserex-interface.md) pointer to the metadata dispenser.</span></span>  
  
 `pErrorHandler`  
 <span data-ttu-id="a7a3d-108">指向可选错误处理接口的[IMetaDataError 接口](../metadata/imetadataerror-interface.md)指针。</span><span class="sxs-lookup"><span data-stu-id="a7a3d-108">[IMetaDataError Interface](../metadata/imetadataerror-interface.md) pointer to an optional error handling interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a7a3d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a7a3d-109">Return Value</span></span>  

 <span data-ttu-id="a7a3d-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="a7a3d-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7a3d-111">要求</span><span class="sxs-lookup"><span data-stu-id="a7a3d-111">Requirements</span></span>  

 <span data-ttu-id="a7a3d-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="a7a3d-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7a3d-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a7a3d-113">See also</span></span>

- [<span data-ttu-id="a7a3d-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="a7a3d-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="a7a3d-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="a7a3d-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="a7a3d-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="a7a3d-116">ALink API</span></span>](index.md)
