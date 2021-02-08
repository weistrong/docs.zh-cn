---
description: 了解详细信息： IMetaDataImport：： GetPermissionSetProps 方法
title: IMetaDataImport::GetPermissionSetProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPermissionSetProps
helpviewer_keywords:
- GetPermissionSetProps method [.NET Framework metadata]
- IMetaDataImport::GetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 9855f0e4-12c0-4d3d-ab5d-d6bc52d25eae
topic_type:
- apiref
ms.openlocfilehash: 9dc10b7bf531b6eec389334d80cf6a1cece20ee9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789185"
---
# <a name="imetadataimportgetpermissionsetprops-method"></a><span data-ttu-id="61d5b-103">IMetaDataImport::GetPermissionSetProps 方法</span><span class="sxs-lookup"><span data-stu-id="61d5b-103">IMetaDataImport::GetPermissionSetProps Method</span></span>

<span data-ttu-id="61d5b-104">获取与指定的权限标记所表示的关联的元数据 <xref:System.Security.PermissionSet?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="61d5b-104">Gets the metadata associated with the <xref:System.Security.PermissionSet?displayProperty=nameWithType> represented by the specified Permission token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61d5b-105">语法</span><span class="sxs-lookup"><span data-stu-id="61d5b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPermissionSetProps (  
   [in]  mdPermission      pm,  
   [out] DWORD             *pdwAction,
   [out] void const        **ppvPermission,
   [out] ULONG             *pcbPermission  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61d5b-106">参数</span><span class="sxs-lookup"><span data-stu-id="61d5b-106">Parameters</span></span>  

 `pm`  
 <span data-ttu-id="61d5b-107">中权限元数据标记，它表示要获取其元数据属性的权限集。</span><span class="sxs-lookup"><span data-stu-id="61d5b-107">[in] The Permission metadata token that represents the permission set to get the metadata properties for.</span></span>  
  
 `pdwAction`  
 <span data-ttu-id="61d5b-108">弄指向权限集的指针。</span><span class="sxs-lookup"><span data-stu-id="61d5b-108">[out] A pointer to the permission set.</span></span>  
  
 `ppvPermission`  
 <span data-ttu-id="61d5b-109">弄指向权限集的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="61d5b-109">[out] A pointer to the binary metadata signature of the permission set.</span></span>  
  
 `pcbPermission`  
 <span data-ttu-id="61d5b-110">弄的大小（以字节为单位） `ppvPermission` 。</span><span class="sxs-lookup"><span data-stu-id="61d5b-110">[out] The size in bytes of `ppvPermission`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61d5b-111">要求</span><span class="sxs-lookup"><span data-stu-id="61d5b-111">Requirements</span></span>  

 <span data-ttu-id="61d5b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61d5b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61d5b-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="61d5b-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="61d5b-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="61d5b-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="61d5b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61d5b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61d5b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="61d5b-116">See also</span></span>

- <xref:System.Security.PermissionSet>
- [<span data-ttu-id="61d5b-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="61d5b-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="61d5b-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="61d5b-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
