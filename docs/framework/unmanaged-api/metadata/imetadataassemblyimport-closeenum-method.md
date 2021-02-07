---
description: 了解详细信息： IMetaDataAssemblyImport：： CloseEnum 方法
title: IMetaDataAssemblyImport::CloseEnum 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::CloseEnum
helpviewer_keywords:
- CloseEnum method, IMetaDataAssemblyImport interface [.NET Framework metadata]
- IMetaDataAssemblyImport::CloseEnum method [.NET Framework metadata]
ms.assetid: c9df4087-12b3-46d9-b075-9067dd7805df
topic_type:
- apiref
ms.openlocfilehash: 3ff234fac905a058ed832d58a0f996a2c7393ed0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678076"
---
# <a name="imetadataassemblyimportcloseenum-method"></a><span data-ttu-id="dbefc-103">IMetaDataAssemblyImport::CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="dbefc-103">IMetaDataAssemblyImport::CloseEnum Method</span></span>

<span data-ttu-id="dbefc-104">释放对指定枚举实例的引用。</span><span class="sxs-lookup"><span data-stu-id="dbefc-104">Releases a reference to the specified enumeration instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbefc-105">语法</span><span class="sxs-lookup"><span data-stu-id="dbefc-105">Syntax</span></span>  
  
```cpp  
void CloseEnum (  
    [in] HCORENUM     hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dbefc-106">参数</span><span class="sxs-lookup"><span data-stu-id="dbefc-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="dbefc-107">中要关闭的枚举实例。</span><span class="sxs-lookup"><span data-stu-id="dbefc-107">[in] The enumeration instance to be closed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dbefc-108">要求</span><span class="sxs-lookup"><span data-stu-id="dbefc-108">Requirements</span></span>  

 <span data-ttu-id="dbefc-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dbefc-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dbefc-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="dbefc-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dbefc-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="dbefc-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="dbefc-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dbefc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbefc-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="dbefc-113">See also</span></span>

- [<span data-ttu-id="dbefc-114">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="dbefc-114">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
