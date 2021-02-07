---
description: 了解详细信息： IMetaDataTables：： GetUserStringHeapSize 方法
title: IMetaDataTables::GetUserStringHeapSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetUserStringHeapSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetUserStringHeapSize
helpviewer_keywords:
- IMetaDataTables::GetUserStringHeapSize method [.NET Framework metadata]
- GetUserStringHeapSize method [.NET Framework metadata]
ms.assetid: cba9e4d6-9461-4420-9614-96ff7039ec9c
topic_type:
- apiref
ms.openlocfilehash: 7e6f3eed7803f52e6bde888852c4971900f0868c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687618"
---
# <a name="imetadatatablesgetuserstringheapsize-method"></a><span data-ttu-id="d9db3-103">IMetaDataTables::GetUserStringHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="d9db3-103">IMetaDataTables::GetUserStringHeapSize Method</span></span>

<span data-ttu-id="d9db3-104">获取用户字符串堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="d9db3-104">Gets the size, in bytes, of the user string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9db3-105">语法</span><span class="sxs-lookup"><span data-stu-id="d9db3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetUserStringHeapSize (  
    [out] ULONG   *pcbBlobs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9db3-106">参数</span><span class="sxs-lookup"><span data-stu-id="d9db3-106">Parameters</span></span>  

 `pcbBlobs`  
 <span data-ttu-id="d9db3-107">弄一个指针，指向用户字符串堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="d9db3-107">[out] A pointer to the size, in bytes, of the user string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9db3-108">要求</span><span class="sxs-lookup"><span data-stu-id="d9db3-108">Requirements</span></span>  

 <span data-ttu-id="d9db3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9db3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9db3-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d9db3-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d9db3-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d9db3-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d9db3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9db3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9db3-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9db3-113">See also</span></span>

- [<span data-ttu-id="d9db3-114">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="d9db3-114">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="d9db3-115">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="d9db3-115">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
