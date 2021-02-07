---
description: 了解详细信息： ServiceToEndpointAssociation
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 1ae2ce2bcc0b3494b00fffa750f3ca46d26fe08f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715335"
---
# <a name="servicetoendpointassociation"></a><span data-ttu-id="035c3-103">ServiceToEndpointAssociation</span><span class="sxs-lookup"><span data-stu-id="035c3-103">ServiceToEndpointAssociation</span></span>

<span data-ttu-id="035c3-104">将服务映射到终结点。</span><span class="sxs-lookup"><span data-stu-id="035c3-104">Maps a service to an endpoint.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="035c3-105">语法</span><span class="sxs-lookup"><span data-stu-id="035c3-105">Syntax</span></span>  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="035c3-106">方法</span><span class="sxs-lookup"><span data-stu-id="035c3-106">Methods</span></span>  

 <span data-ttu-id="035c3-107">ServiceToEndpointAssociation 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="035c3-107">The ServiceToEndpointAssociation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="035c3-108">属性</span><span class="sxs-lookup"><span data-stu-id="035c3-108">Properties</span></span>  

 <span data-ttu-id="035c3-109">ServiceToEndpointAssociation 类有以下属性：</span><span class="sxs-lookup"><span data-stu-id="035c3-109">The ServiceToEndpointAssociation class has the following properties:</span></span>  
  
### <a name="ref"></a><span data-ttu-id="035c3-110">ref</span><span class="sxs-lookup"><span data-stu-id="035c3-110">ref</span></span>  

 <span data-ttu-id="035c3-111">数据类型：Service</span><span class="sxs-lookup"><span data-stu-id="035c3-111">Data type: Service</span></span>  
  
 <span data-ttu-id="035c3-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="035c3-112">Access type: Read-only</span></span>  
<span data-ttu-id="035c3-113">限定符：键</span><span class="sxs-lookup"><span data-stu-id="035c3-113">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="035c3-114">与终结点关联的服务。</span><span class="sxs-lookup"><span data-stu-id="035c3-114">The service associated with the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="035c3-115">ref</span><span class="sxs-lookup"><span data-stu-id="035c3-115">ref</span></span>  

 <span data-ttu-id="035c3-116">数据类型：Endpoint</span><span class="sxs-lookup"><span data-stu-id="035c3-116">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="035c3-117">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="035c3-117">Access type: Read-only</span></span>  
<span data-ttu-id="035c3-118">限定符：键</span><span class="sxs-lookup"><span data-stu-id="035c3-118">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="035c3-119">与服务关联的终结点。</span><span class="sxs-lookup"><span data-stu-id="035c3-119">The endpoint associated with the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="035c3-120">要求</span><span class="sxs-lookup"><span data-stu-id="035c3-120">Requirements</span></span>  
  
|<span data-ttu-id="035c3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="035c3-121">MOF</span></span>|<span data-ttu-id="035c3-122">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="035c3-122">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="035c3-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="035c3-123">Namespace</span></span>|<span data-ttu-id="035c3-124">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="035c3-124">Defined in root\ServiceModel</span></span>|
