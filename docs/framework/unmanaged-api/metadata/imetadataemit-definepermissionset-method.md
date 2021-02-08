---
description: 了解详细信息： IMetaDataEmit：:D efinePermissionSet 方法
title: IMetaDataEmit::DefinePermissionSet 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefinePermissionSet
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefinePermissionSet
helpviewer_keywords:
- DefinePermissionSet method [.NET Framework metadata]
- IMetaDataEmit::DefinePermissionSet method [.NET Framework metadata]
ms.assetid: 36cffbf7-82ca-4cf9-bf60-50ab491ac2d9
topic_type:
- apiref
ms.openlocfilehash: f5c3f1466217713cb3970c805079d8f65fd429c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784075"
---
# <a name="imetadataemitdefinepermissionset-method"></a><span data-ttu-id="8dfc5-103">IMetaDataEmit::DefinePermissionSet 方法</span><span class="sxs-lookup"><span data-stu-id="8dfc5-103">IMetaDataEmit::DefinePermissionSet Method</span></span>

<span data-ttu-id="8dfc5-104">使用指定的元数据签名创建权限集的定义，并获取该权限集定义的标记。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-104">Creates a definition for a permission set with the specified metadata signature, and gets a token to that permission set definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8dfc5-105">语法</span><span class="sxs-lookup"><span data-stu-id="8dfc5-105">Syntax</span></span>  
  
```cpp  
HRESULT DefinePermissionSet (  
    [in]  mdToken        tk,
    [in]  DWORD          dwAction,
    [in]  void const     *pvPermission,
    [in]  ULONG          cbPermission,
    [out] mdPermission   *ppm
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8dfc5-106">参数</span><span class="sxs-lookup"><span data-stu-id="8dfc5-106">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="8dfc5-107">中要修饰的对象。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-107">[in] The object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="8dfc5-108">中一个 [CorDeclSecurity](cordeclsecurity-enumeration.md) 值，指定要使用的声明性安全类型。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-108">[in] A [CorDeclSecurity](cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="8dfc5-109">中权限 BLOB。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-109">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="8dfc5-110">中的大小（以字节为单位） `pvPermission` 。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-110">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="8dfc5-111">弄返回的权限标记。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-111">[out] The returned permission token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dfc5-112">要求</span><span class="sxs-lookup"><span data-stu-id="8dfc5-112">Requirements</span></span>  

 <span data-ttu-id="8dfc5-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8dfc5-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dfc5-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="8dfc5-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8dfc5-115">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="8dfc5-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8dfc5-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8dfc5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8dfc5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="8dfc5-117">See also</span></span>

- [<span data-ttu-id="8dfc5-118">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="8dfc5-118">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="8dfc5-119">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="8dfc5-119">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
