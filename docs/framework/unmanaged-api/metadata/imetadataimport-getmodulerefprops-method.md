---
description: 了解详细信息： IMetaDataImport：： GetModuleRefProps 方法
title: IMetaDataImport::GetModuleRefProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetModuleRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetModuleRefProps
helpviewer_keywords:
- GetModuleRefProps method [.NET Framework metadata]
- IMetaDataImport::GetModuleRefProps method [.NET Framework metadata]
ms.assetid: b558e766-4c11-4628-ae47-b4e0a1800168
topic_type:
- apiref
ms.openlocfilehash: 3e6b212ddad5eefb06942c3fd4b89411b277f761
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753349"
---
# <a name="imetadataimportgetmodulerefprops-method"></a><span data-ttu-id="f6f67-103">IMetaDataImport::GetModuleRefProps 方法</span><span class="sxs-lookup"><span data-stu-id="f6f67-103">IMetaDataImport::GetModuleRefProps Method</span></span>

<span data-ttu-id="f6f67-104">获取指定元数据标记引用的模块的名称。</span><span class="sxs-lookup"><span data-stu-id="f6f67-104">Gets the name of the module referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6f67-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6f67-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleRefProps (  
   [in]  mdModuleRef         mur,  
   [out] LPWSTR              szName,
   [in]  ULONG               cchName,
   [out] ULONG               *pchName
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6f67-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6f67-106">Parameters</span></span>  

 `mur`  
 <span data-ttu-id="f6f67-107">中引用要获取其元数据信息的模块的 ModuleRef 元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f6f67-107">[in] The ModuleRef metadata token that references the module to get metadata information for.</span></span>  
  
 `szName`  
 <span data-ttu-id="f6f67-108">弄用于保存模块名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="f6f67-108">[out] A buffer to hold the module name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="f6f67-109">中请求的大小（ `szName` 以宽字符为大小）。</span><span class="sxs-lookup"><span data-stu-id="f6f67-109">[in] The requested size of `szName` in wide characters.</span></span>  
  
 `pchName`  
 <span data-ttu-id="f6f67-110">弄返回的 `szName` 宽字符大小。</span><span class="sxs-lookup"><span data-stu-id="f6f67-110">[out] The returned size of `szName` in wide characters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6f67-111">要求</span><span class="sxs-lookup"><span data-stu-id="f6f67-111">Requirements</span></span>  

 <span data-ttu-id="f6f67-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6f67-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6f67-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f6f67-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f6f67-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6f67-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f6f67-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6f67-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6f67-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6f67-116">See also</span></span>

- [<span data-ttu-id="f6f67-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f6f67-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f6f67-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f6f67-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
