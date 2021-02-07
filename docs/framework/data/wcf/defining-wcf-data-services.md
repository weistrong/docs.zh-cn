---
description: 了解详细信息：定义 WCF Data Services
title: 定义 WCF 数据服务
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 05006ff3-02dc-410e-831e-54ec3e7e24ef
ms.openlocfilehash: 43a4887226b03e80c4a966a118f210fe8a28000d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766083"
---
# <a name="defining-wcf-data-services"></a><span data-ttu-id="1e542-103">定义 WCF 数据服务</span><span class="sxs-lookup"><span data-stu-id="1e542-103">Defining WCF Data Services</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="1e542-104">本部分介绍如何创建和配置 WCF Data Services 以将数据作为 Open Data Protocol (OData) 源公开。</span><span class="sxs-lookup"><span data-stu-id="1e542-104">This section describes how to create and configure WCF Data Services to expose data as an Open Data Protocol (OData) feed.</span></span> <span data-ttu-id="1e542-105">有关创建数据服务所需的基本步骤的详细信息，请参阅 [将数据作为服务公开](exposing-your-data-as-a-service-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="1e542-105">For more information about the basic steps required to create a data service, see [Exposing Your Data as a Service](exposing-your-data-as-a-service-wcf-data-services.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e542-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="1e542-106">In This Section</span></span>

 [<span data-ttu-id="1e542-107">配置数据服务</span><span class="sxs-lookup"><span data-stu-id="1e542-107">Configuring the Data Service</span></span>](configuring-the-data-service-wcf-data-services.md)

 <span data-ttu-id="1e542-108">介绍 WCF Data Services 提供的数据服务配置选项。</span><span class="sxs-lookup"><span data-stu-id="1e542-108">Describes the data service configuration options provided by WCF Data Services.</span></span>

 [<span data-ttu-id="1e542-109">数据服务提供程序</span><span class="sxs-lookup"><span data-stu-id="1e542-109">Data Services Providers</span></span>](data-services-providers-wcf-data-services.md)

 <span data-ttu-id="1e542-110">描述用于将数据作为数据服务公开的提供程序模型。</span><span class="sxs-lookup"><span data-stu-id="1e542-110">Describes the provider models for exposing data as a data service.</span></span>

 [<span data-ttu-id="1e542-111">服务操作</span><span class="sxs-lookup"><span data-stu-id="1e542-111">Service Operations</span></span>](service-operations-wcf-data-services.md)

 <span data-ttu-id="1e542-112">描述如何定义在服务器上公开方法的服务操作。</span><span class="sxs-lookup"><span data-stu-id="1e542-112">Describes how to define service operations that expose methods on the server.</span></span>

 [<span data-ttu-id="1e542-113">源自定义</span><span class="sxs-lookup"><span data-stu-id="1e542-113">Feed Customization</span></span>](feed-customization-wcf-data-services.md)

 <span data-ttu-id="1e542-114">描述如何在数据服务提供程序定义的数据模型中的实体与数据源中的元素之间创建映射。</span><span class="sxs-lookup"><span data-stu-id="1e542-114">Describes how to create a mapping between entities in the data model defined by the data service provider and elements in the data feed.</span></span>

 [<span data-ttu-id="1e542-115">侦听器</span><span class="sxs-lookup"><span data-stu-id="1e542-115">Interceptors</span></span>](interceptors-wcf-data-services.md)

 <span data-ttu-id="1e542-116">描述如何定义侦听器方法用于对数据服务请求执行自定义业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="1e542-116">Describes how to define interceptor methods to perform custom business logic on requests to the data service.</span></span>

 [<span data-ttu-id="1e542-117">开发和部署 WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="1e542-117">Developing and Deploying WCF Data Services</span></span>](developing-and-deploying-wcf-data-services.md)

 <span data-ttu-id="1e542-118">描述如何使用 Visual Studio 开发和部署数据服务。</span><span class="sxs-lookup"><span data-stu-id="1e542-118">Describes how to develop and deploy a data service by using Visual Studio.</span></span>

 [<span data-ttu-id="1e542-119">WCF 数据服务的安全</span><span class="sxs-lookup"><span data-stu-id="1e542-119">Securing WCF Data Services</span></span>](securing-wcf-data-services.md)

 <span data-ttu-id="1e542-120">描述数据服务的身份验证和授权以及其他安全注意事项。</span><span class="sxs-lookup"><span data-stu-id="1e542-120">Describes authentication and authorization for the data service and other security considerations.</span></span>

 [<span data-ttu-id="1e542-121">承载数据服务</span><span class="sxs-lookup"><span data-stu-id="1e542-121">Hosting the Data Service</span></span>](hosting-the-data-service-wcf-data-services.md)

 <span data-ttu-id="1e542-122">描述如何为数据服务选择宿主。</span><span class="sxs-lookup"><span data-stu-id="1e542-122">Describes how to select a host for your data service.</span></span>

 [<span data-ttu-id="1e542-123">数据服务版本控制</span><span class="sxs-lookup"><span data-stu-id="1e542-123">Data Service Versioning</span></span>](data-service-versioning-wcf-data-services.md)

 <span data-ttu-id="1e542-124">介绍如何使用不同版本的 OData。</span><span class="sxs-lookup"><span data-stu-id="1e542-124">Describes how to work with different versions of the OData.</span></span>

 [<span data-ttu-id="1e542-125">WCF 数据服务协议实现详细信息</span><span class="sxs-lookup"><span data-stu-id="1e542-125">WCF Data Services Protocol Implementation Details</span></span>](wcf-data-services-protocol-implementation-details.md)

 <span data-ttu-id="1e542-126">描述 WCF Data Services 当前未实现的 OData 协议的可选功能。</span><span class="sxs-lookup"><span data-stu-id="1e542-126">Describes optional functionalities of the OData protocol that are not currently implemented by WCF Data Services.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e542-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="1e542-127">See also</span></span>

- [<span data-ttu-id="1e542-128">WCF 数据服务客户端库</span><span class="sxs-lookup"><span data-stu-id="1e542-128">WCF Data Services Client Library</span></span>](wcf-data-services-client-library.md)
- [<span data-ttu-id="1e542-129">访问数据服务资源</span><span class="sxs-lookup"><span data-stu-id="1e542-129">Accessing Data Service Resources</span></span>](accessing-data-service-resources-wcf-data-services.md)
- [<span data-ttu-id="1e542-130">入门</span><span class="sxs-lookup"><span data-stu-id="1e542-130">Getting Started</span></span>](getting-started-with-wcf-data-services.md)
