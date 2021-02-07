---
description: 了解详细信息： IDefinitionAppId 接口
title: IDefinitionAppId 接口
ms.date: 03/30/2017
api_name:
- IDefinitionAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionAppId
helpviewer_keywords:
- IDefinitionAppId interface [.NET Framework fusion]
ms.assetid: e72f2550-bdec-4a20-a2f4-2e14847266c1
topic_type:
- apiref
ms.openlocfilehash: 3c68044e7e747521e190fad404e89d6d0a994611
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760662"
---
# <a name="idefinitionappid-interface"></a><span data-ttu-id="ed07d-103">IDefinitionAppId 接口</span><span class="sxs-lookup"><span data-stu-id="ed07d-103">IDefinitionAppId Interface</span></span>

<span data-ttu-id="ed07d-104">表示定义当前作用域中的应用程序的代码的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ed07d-104">Represents a unique identifier for the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ed07d-105">方法</span><span class="sxs-lookup"><span data-stu-id="ed07d-105">Methods</span></span>  
  
|<span data-ttu-id="ed07d-106">方法</span><span class="sxs-lookup"><span data-stu-id="ed07d-106">Method</span></span>|<span data-ttu-id="ed07d-107">说明</span><span class="sxs-lookup"><span data-stu-id="ed07d-107">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionAppId::get_Codebase`|<span data-ttu-id="ed07d-108">获取表示此对象中的代码的格式化字符串 `IDefinitionAppId` 。</span><span class="sxs-lookup"><span data-stu-id="ed07d-108">Gets a formatted string that represents the code in this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_Codebase`|<span data-ttu-id="ed07d-109">将此对象的代码设置 `IDefinitionAppId` 为指定的格式化字符串值。</span><span class="sxs-lookup"><span data-stu-id="ed07d-109">Sets the code of this `IDefinitionAppId` object to the specified formatted string value.</span></span>|  
|`IDefinitionAppId::EnumAppPath`|<span data-ttu-id="ed07d-110">获取一个指向 [IEnumDefinitionIdentity](ienumdefinitionidentity-interface.md) 对象的接口指针，该对象包含当前应用程序路径中的程序集。</span><span class="sxs-lookup"><span data-stu-id="ed07d-110">Gets an interface pointer to an [IEnumDefinitionIdentity](ienumdefinitionidentity-interface.md) object that contains the assemblies in the current application path.</span></span>|  
|`IDefinitionAppId::SetAppPath`|<span data-ttu-id="ed07d-111">将当前范围中的程序集的应用程序路径设置为指定的 [IDefinitionIdentity](idefinitionidentity-interface.md) 对象所引用的值。</span><span class="sxs-lookup"><span data-stu-id="ed07d-111">Sets the application path for the assembly in the current scope to the value referenced by the specified [IDefinitionIdentity](idefinitionidentity-interface.md) object.</span></span>|  
|`IDefinitionAppId::get_SubscriptionId`|<span data-ttu-id="ed07d-112">获取一个指针，该指针指向此对象的订阅的标记标识符的字符串表示形式 `IDefinitionAppId` 。</span><span class="sxs-lookup"><span data-stu-id="ed07d-112">Gets a pointer to a string representation of the token identifier for a subscription to this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_SubscriptionId`|<span data-ttu-id="ed07d-113">将此对象的订阅的标记标识符设置 `IDefinitionAppId` 为指定的字符串值。</span><span class="sxs-lookup"><span data-stu-id="ed07d-113">Sets the token identifier for a subscription to this `IDefinitionAppId` object to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ed07d-114">要求</span><span class="sxs-lookup"><span data-stu-id="ed07d-114">Requirements</span></span>  

 <span data-ttu-id="ed07d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed07d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed07d-116">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="ed07d-116">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="ed07d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed07d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed07d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed07d-118">See also</span></span>

- [<span data-ttu-id="ed07d-119">合成接口</span><span class="sxs-lookup"><span data-stu-id="ed07d-119">Fusion Interfaces</span></span>](fusion-interfaces.md)
