---
description: 了解详细信息： IMetaDataImport：： GetScopeProps 方法
title: IMetaDataImport::GetScopeProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetScopeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetScopeProps
helpviewer_keywords:
- IMetaDataImport::GetScopeProps method [.NET Framework metadata]
- GetScopeProps method [.NET Framework metadata]
ms.assetid: c8ba42d2-d9fa-43cb-bbc0-f33e1e592cb6
topic_type:
- apiref
ms.openlocfilehash: 2ed7c08cc876f467a46fe38c7c27719e5608e623
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789146"
---
# <a name="imetadataimportgetscopeprops-method"></a><span data-ttu-id="941b4-103">IMetaDataImport::GetScopeProps 方法</span><span class="sxs-lookup"><span data-stu-id="941b4-103">IMetaDataImport::GetScopeProps Method</span></span>

<span data-ttu-id="941b4-104">获取当前元数据范围内的程序集或模块的名称和版本标识符（可选）。</span><span class="sxs-lookup"><span data-stu-id="941b4-104">Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="941b4-105">语法</span><span class="sxs-lookup"><span data-stu-id="941b4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetScopeProps (  
   [out] LPWSTR           szName,  
   [in]  ULONG            cchName,  
   [out] ULONG            *pchName,  
   [out, optional] GUID   *pmvid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="941b4-106">参数</span><span class="sxs-lookup"><span data-stu-id="941b4-106">Parameters</span></span>  

 `szName`  
 <span data-ttu-id="941b4-107">弄程序集或模块名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="941b4-107">[out] A buffer for the assembly or module name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="941b4-108">中的大小（以宽字符为大小） `szName` 。</span><span class="sxs-lookup"><span data-stu-id="941b4-108">[in] The size in wide characters of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="941b4-109">弄返回的宽字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="941b4-109">[out] The number of wide characters returned in `szName`.</span></span>  
  
 `pmvid`  
 <span data-ttu-id="941b4-110">[out，optional]一个指向 GUID 的指针，该 GUID 用于唯一标识程序集或模块的版本。</span><span class="sxs-lookup"><span data-stu-id="941b4-110">[out, optional] A pointer to a GUID that uniquely identifies the version of the assembly or module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="941b4-111">备注</span><span class="sxs-lookup"><span data-stu-id="941b4-111">Remarks</span></span>  

 <span data-ttu-id="941b4-112">使用 [IMetaDataEmit：： SetModuleProps](imetadataemit-setmoduleprops-method.md) 方法设置这些属性。</span><span class="sxs-lookup"><span data-stu-id="941b4-112">The [IMetaDataEmit::SetModuleProps](imetadataemit-setmoduleprops-method.md) method is used to set these properties.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="941b4-113">要求</span><span class="sxs-lookup"><span data-stu-id="941b4-113">Requirements</span></span>  

 <span data-ttu-id="941b4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="941b4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="941b4-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="941b4-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="941b4-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="941b4-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="941b4-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="941b4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="941b4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="941b4-118">See also</span></span>

- [<span data-ttu-id="941b4-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="941b4-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="941b4-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="941b4-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
