---
description: 了解详细信息： ServiceDebugBehavior
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 3b384c209524267c72a12d96bc845b694144ba19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715530"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="10beb-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="10beb-103">ServiceDebugBehavior</span></span>

<span data-ttu-id="10beb-104">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="10beb-104">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10beb-105">语法</span><span class="sxs-lookup"><span data-stu-id="10beb-105">Syntax</span></span>  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="10beb-106">方法</span><span class="sxs-lookup"><span data-stu-id="10beb-106">Methods</span></span>  

 <span data-ttu-id="10beb-107">ServiceDebugBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="10beb-107">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="10beb-108">属性</span><span class="sxs-lookup"><span data-stu-id="10beb-108">Properties</span></span>  

 <span data-ttu-id="10beb-109">ServiceDebugBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="10beb-109">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="10beb-110">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="10beb-110">HttpHelpPageEnabled</span></span>  

 <span data-ttu-id="10beb-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="10beb-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="10beb-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="10beb-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="10beb-113">控制服务是否在 `HttpGetUrl` 属性控制的地址上发布其 WSDL。</span><span class="sxs-lookup"><span data-stu-id="10beb-113">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="10beb-114">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="10beb-114">HttpHelpPageUrl</span></span>  

 <span data-ttu-id="10beb-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="10beb-115">Data type: string</span></span>  
  
 <span data-ttu-id="10beb-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="10beb-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="10beb-117">设置位置，在该位置发布服务 WSDL 以便使用 HTTP 进行检索。</span><span class="sxs-lookup"><span data-stu-id="10beb-117">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="10beb-118">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="10beb-118">HttpsHelpPageEnabled</span></span>  

 <span data-ttu-id="10beb-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="10beb-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="10beb-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="10beb-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="10beb-121">控制服务是否在 `HttpsGetUrl` 属性控制的地址上通过 HTTPS 发布其 WSDL。</span><span class="sxs-lookup"><span data-stu-id="10beb-121">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="10beb-122">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="10beb-122">HttpsHelpPageUrl</span></span>  

 <span data-ttu-id="10beb-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="10beb-123">Data type: string</span></span>  
  
 <span data-ttu-id="10beb-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="10beb-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="10beb-125">设置位置，在该位置发布服务 WSDL 以便使用 HTTPS 进行检索。</span><span class="sxs-lookup"><span data-stu-id="10beb-125">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="10beb-126">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="10beb-126">IncludeExceptionDetailInFaults</span></span>  

 <span data-ttu-id="10beb-127">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="10beb-127">Data type: boolean</span></span>  
  
 <span data-ttu-id="10beb-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="10beb-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="10beb-129">指定是否在返回给客户端的 SOAP 错误详细信息中包含托管异常信息以供调试。</span><span class="sxs-lookup"><span data-stu-id="10beb-129">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10beb-130">要求</span><span class="sxs-lookup"><span data-stu-id="10beb-130">Requirements</span></span>  
  
|<span data-ttu-id="10beb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="10beb-131">MOF</span></span>|<span data-ttu-id="10beb-132">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="10beb-132">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="10beb-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="10beb-133">Namespace</span></span>|<span data-ttu-id="10beb-134">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="10beb-134">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="10beb-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="10beb-135">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceDebugBehavior>
