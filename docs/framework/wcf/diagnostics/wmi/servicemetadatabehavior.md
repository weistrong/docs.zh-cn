---
description: 了解详细信息： ServiceMetadataBehavior
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: 1b1438013ec667b10b300d898687abf6f33f96fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715478"
---
# <a name="servicemetadatabehavior"></a><span data-ttu-id="9f738-103">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="9f738-103">ServiceMetadataBehavior</span></span>

<span data-ttu-id="9f738-104">ServiceMetadataBehavior</span><span class="sxs-lookup"><span data-stu-id="9f738-104">ServiceMetadataBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f738-105">语法</span><span class="sxs-lookup"><span data-stu-id="9f738-105">Syntax</span></span>  
  
```csharp
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9f738-106">方法</span><span class="sxs-lookup"><span data-stu-id="9f738-106">Methods</span></span>  

 <span data-ttu-id="9f738-107">ServiceMetadataBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="9f738-107">The ServiceMetadataBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="9f738-108">属性</span><span class="sxs-lookup"><span data-stu-id="9f738-108">Properties</span></span>  

 <span data-ttu-id="9f738-109">ServiceMetadataBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="9f738-109">The ServiceMetadataBehavior class has the following properties:</span></span>  
  
### <a name="externalmetadatalocation"></a><span data-ttu-id="9f738-110">ExternalMetadataLocation</span><span class="sxs-lookup"><span data-stu-id="9f738-110">ExternalMetadataLocation</span></span>  

 <span data-ttu-id="9f738-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f738-111">Data type: string</span></span>  
  
 <span data-ttu-id="9f738-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f738-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f738-113">设置服务重定向元数据请求的位置。</span><span class="sxs-lookup"><span data-stu-id="9f738-113">Sets the location to which the service redirects metadata requests.</span></span>  
  
### <a name="httpgetenabled"></a><span data-ttu-id="9f738-114">HttpGetEnabled</span><span class="sxs-lookup"><span data-stu-id="9f738-114">HttpGetEnabled</span></span>  

 <span data-ttu-id="9f738-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="9f738-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="9f738-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f738-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f738-117">控制服务是否在 `HttpGetUrl` 属性控制的地址上发布其 WSDL。</span><span class="sxs-lookup"><span data-stu-id="9f738-117">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httpgeturl"></a><span data-ttu-id="9f738-118">HttpGetUrl</span><span class="sxs-lookup"><span data-stu-id="9f738-118">HttpGetUrl</span></span>  

 <span data-ttu-id="9f738-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f738-119">Data type: string</span></span>  
  
 <span data-ttu-id="9f738-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f738-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f738-121">设置位置，在该位置发布服务 WSDL 以便使用 HTTP 进行检索。</span><span class="sxs-lookup"><span data-stu-id="9f738-121">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpsgetenabled"></a><span data-ttu-id="9f738-122">HttpsGetEnabled</span><span class="sxs-lookup"><span data-stu-id="9f738-122">HttpsGetEnabled</span></span>  

 <span data-ttu-id="9f738-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="9f738-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="9f738-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f738-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f738-125">控制服务是否在 `HttpsGetUrl` 属性控制的地址上通过 HTTPS 发布其 WSDL。</span><span class="sxs-lookup"><span data-stu-id="9f738-125">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpsgeturl"></a><span data-ttu-id="9f738-126">HttpsGetUrl</span><span class="sxs-lookup"><span data-stu-id="9f738-126">HttpsGetUrl</span></span>  

 <span data-ttu-id="9f738-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f738-127">Data type: string</span></span>  
  
 <span data-ttu-id="9f738-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f738-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f738-129">设置位置，在该位置发布服务 WSDL 以便使用 HTTPS 进行检索。</span><span class="sxs-lookup"><span data-stu-id="9f738-129">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f738-130">要求</span><span class="sxs-lookup"><span data-stu-id="9f738-130">Requirements</span></span>  
  
|<span data-ttu-id="9f738-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9f738-131">MOF</span></span>|<span data-ttu-id="9f738-132">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="9f738-132">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9f738-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="9f738-133">Namespace</span></span>|<span data-ttu-id="9f738-134">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="9f738-134">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9f738-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f738-135">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
