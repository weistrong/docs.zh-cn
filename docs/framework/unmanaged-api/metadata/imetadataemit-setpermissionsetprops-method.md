---
description: 了解详细信息： IMetaDataEmit：： SetPermissionSetProps 方法
title: IMetaDataEmit::SetPermissionSetProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPermissionSetProps
helpviewer_keywords:
- SetPermissionSetProps method [.NET Framework metadata]
- IMetaDataEmit::SetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 8eaee971-40bf-45e2-a3d8-6e57674213b6
topic_type:
- apiref
ms.openlocfilehash: 1e2786a21a1024f32328e36878a1a2427af54f51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771881"
---
# <a name="imetadataemitsetpermissionsetprops-method"></a><span data-ttu-id="8293b-103">IMetaDataEmit::SetPermissionSetProps 方法</span><span class="sxs-lookup"><span data-stu-id="8293b-103">IMetaDataEmit::SetPermissionSetProps Method</span></span>

<span data-ttu-id="8293b-104">设置或更新通过之前调用 [IMetaDataEmit：:D efinepermissionset](imetadataemit-definepermissionset-method.md)定义的权限集的元数据签名的功能。</span><span class="sxs-lookup"><span data-stu-id="8293b-104">Sets or updates features of the metadata signature of a permission set defined by a prior call to [IMetaDataEmit::DefinePermissionSet](imetadataemit-definepermissionset-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8293b-105">语法</span><span class="sxs-lookup"><span data-stu-id="8293b-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPermissionSetProps (
    [in]  mdToken         tk,
    [in]  DWORD           dwAction,
    [in]  void const      *pvPermission,
    [in]  ULONG           cbPermission,
    [out] mdPermission    *ppm
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8293b-106">参数</span><span class="sxs-lookup"><span data-stu-id="8293b-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="8293b-107">中表示要修饰的对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="8293b-107">[in] A metadata token that represents the object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="8293b-108">中一个 [CorDeclSecurity](cordeclsecurity-enumeration.md) 值，指定要使用的声明性安全类型。</span><span class="sxs-lookup"><span data-stu-id="8293b-108">[in] A [CorDeclSecurity](cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="8293b-109">中权限 BLOB。</span><span class="sxs-lookup"><span data-stu-id="8293b-109">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="8293b-110">中的大小（以字节为单位） `pvPermission` 。</span><span class="sxs-lookup"><span data-stu-id="8293b-110">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="8293b-111">弄 `mdPermission` 表示更新的权限的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="8293b-111">[out] An `mdPermission` metadata token that represents the updated permissions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8293b-112">要求</span><span class="sxs-lookup"><span data-stu-id="8293b-112">Requirements</span></span>  

 <span data-ttu-id="8293b-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8293b-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8293b-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8293b-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8293b-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8293b-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8293b-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8293b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8293b-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8293b-117">See also</span></span>

- [<span data-ttu-id="8293b-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8293b-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8293b-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8293b-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
