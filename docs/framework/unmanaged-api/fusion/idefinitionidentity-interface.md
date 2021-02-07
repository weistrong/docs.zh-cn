---
description: 了解详细信息： IDefinitionIdentity 接口
title: IDefinitionIdentity 接口
ms.date: 03/30/2017
api_name:
- IDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionIdentity
helpviewer_keywords:
- IDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: ce5ba888-5fbe-4efd-91cf-f0ff94d8428b
topic_type:
- apiref
ms.openlocfilehash: 3471879cc822b655b786dd9d8234950cb4b99c1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760649"
---
# <a name="idefinitionidentity-interface"></a><span data-ttu-id="a1d8d-103">IDefinitionIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="a1d8d-103">IDefinitionIdentity Interface</span></span>

<span data-ttu-id="a1d8d-104">表示定义当前作用域中的应用程序的代码的唯一签名。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-104">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a1d8d-105">方法</span><span class="sxs-lookup"><span data-stu-id="a1d8d-105">Methods</span></span>  
  
|<span data-ttu-id="a1d8d-106">方法</span><span class="sxs-lookup"><span data-stu-id="a1d8d-106">Method</span></span>|<span data-ttu-id="a1d8d-107">说明</span><span class="sxs-lookup"><span data-stu-id="a1d8d-107">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|<span data-ttu-id="a1d8d-108">获取一个接口指针，该指针指向与 `IDefinitionIdentity` 此相同的新对象 `IDefinitionIdentity` ，但指定的特性更改除外。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-108">Gets an interface pointer to a new `IDefinitionIdentity` object that is identical to this `IDefinitionIdentity`, except for the specified attribute changes.</span></span>|  
|`IDefinitionIdentity::EnumAttributes`|<span data-ttu-id="a1d8d-109">获取一个指向 [IEnumIDENTITY_ATTRIBUTE](ienumidentity-attribute-interface.md) 对象的接口指针，该对象包含与此关联的特性 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-109">Gets an interface pointer to an [IEnumIDENTITY_ATTRIBUTE](ienumidentity-attribute-interface.md) object that contains the attributes associated with this `IDefinitionIdentity`.</span></span>|  
|`IDefinitionIdentity::GetAttribute`|<span data-ttu-id="a1d8d-110">获取指定命名空间中具有指定名称的属性的值。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-110">Gets the value of the attribute with the specified name in the specified namespace.</span></span>|  
|`IDefinitionIdentity::SetAttribute`|<span data-ttu-id="a1d8d-111">将指定命名空间中具有指定名称的特性设置为指定值。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-111">Sets the attribute that has the specified name in the specified namespace to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a1d8d-112">要求</span><span class="sxs-lookup"><span data-stu-id="a1d8d-112">Requirements</span></span>  

 <span data-ttu-id="a1d8d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1d8d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1d8d-114">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="a1d8d-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="a1d8d-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1d8d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1d8d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1d8d-116">See also</span></span>

- [<span data-ttu-id="a1d8d-117">合成接口</span><span class="sxs-lookup"><span data-stu-id="a1d8d-117">Fusion Interfaces</span></span>](fusion-interfaces.md)
