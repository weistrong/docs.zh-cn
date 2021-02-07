---
description: 了解详细信息： SymmetricSecurityBindingElement
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: c158f0bedec91a74b305f359889dd307cff48079
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715296"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="52719-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="52719-103">SymmetricSecurityBindingElement</span></span>

<span data-ttu-id="52719-104">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="52719-104">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52719-105">语法</span><span class="sxs-lookup"><span data-stu-id="52719-105">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="52719-106">方法</span><span class="sxs-lookup"><span data-stu-id="52719-106">Methods</span></span>  

 <span data-ttu-id="52719-107">SymmetricSecurityBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="52719-107">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="52719-108">属性</span><span class="sxs-lookup"><span data-stu-id="52719-108">Properties</span></span>  

 <span data-ttu-id="52719-109">SymmetricSecurityBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="52719-109">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="52719-110">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="52719-110">MessageProtectionOrder</span></span>  

 <span data-ttu-id="52719-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="52719-111">Data type: string</span></span>  
  
 <span data-ttu-id="52719-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="52719-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="52719-113">此绑定的消息加密和签名的顺序。</span><span class="sxs-lookup"><span data-stu-id="52719-113">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="52719-114">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="52719-114">RequireSignatureConfirmation</span></span>  

 <span data-ttu-id="52719-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="52719-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="52719-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="52719-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="52719-117">此绑定是否需要签名确认。</span><span class="sxs-lookup"><span data-stu-id="52719-117">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52719-118">要求</span><span class="sxs-lookup"><span data-stu-id="52719-118">Requirements</span></span>  
  
|<span data-ttu-id="52719-119">MOF</span><span class="sxs-lookup"><span data-stu-id="52719-119">MOF</span></span>|<span data-ttu-id="52719-120">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="52719-120">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="52719-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="52719-121">Namespace</span></span>|<span data-ttu-id="52719-122">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="52719-122">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="52719-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="52719-123">See also</span></span>

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
