---
description: 了解详细信息： AsymmetricSecurityBindingElement
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 25d0ac205491e9ce27c59d3a0670d1e4a3150e21
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757938"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="24c1a-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="24c1a-103">AsymmetricSecurityBindingElement</span></span>

<span data-ttu-id="24c1a-104">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="24c1a-104">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24c1a-105">语法</span><span class="sxs-lookup"><span data-stu-id="24c1a-105">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="24c1a-106">方法</span><span class="sxs-lookup"><span data-stu-id="24c1a-106">Methods</span></span>  

 <span data-ttu-id="24c1a-107">AsymmetricSecurityBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="24c1a-107">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="24c1a-108">属性</span><span class="sxs-lookup"><span data-stu-id="24c1a-108">Properties</span></span>  

 <span data-ttu-id="24c1a-109">AsymmetricSecurityBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="24c1a-109">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="24c1a-110">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="24c1a-110">MessageProtectionOrder</span></span>  

 <span data-ttu-id="24c1a-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="24c1a-111">Data type: string</span></span>  
  
 <span data-ttu-id="24c1a-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="24c1a-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="24c1a-113">此绑定的消息加密和签名的顺序。</span><span class="sxs-lookup"><span data-stu-id="24c1a-113">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="24c1a-114">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="24c1a-114">RequireSignatureConfirmation</span></span>  

 <span data-ttu-id="24c1a-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="24c1a-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="24c1a-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="24c1a-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="24c1a-117">此绑定是否需要签名确认。</span><span class="sxs-lookup"><span data-stu-id="24c1a-117">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24c1a-118">要求</span><span class="sxs-lookup"><span data-stu-id="24c1a-118">Requirements</span></span>  
  
|<span data-ttu-id="24c1a-119">MOF</span><span class="sxs-lookup"><span data-stu-id="24c1a-119">MOF</span></span>|<span data-ttu-id="24c1a-120">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="24c1a-120">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="24c1a-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="24c1a-121">Namespace</span></span>|<span data-ttu-id="24c1a-122">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="24c1a-122">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="24c1a-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="24c1a-123">See also</span></span>

- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
