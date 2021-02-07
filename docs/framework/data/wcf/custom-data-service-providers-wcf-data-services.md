---
description: '了解更多相关信息：自定义数据服务提供程序 (WCF Data Services) '
title: 自定义数据服务提供程序（WCF 数据服务）
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, providers
ms.assetid: e702ecdb-3419-4743-92a9-c3c0e7d44082
ms.openlocfilehash: df0cafae46cfdbd71a96341686a9200f032a9938
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766148"
---
# <a name="custom-data-service-providers-wcf-data-services"></a><span data-ttu-id="7bc25-103">自定义数据服务提供程序（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="7bc25-103">Custom Data Service Providers (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="7bc25-104">WCF Data Services 包括一组提供程序，使您能够基于后期绑定数据类型定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="7bc25-104">WCF Data Services includes a set of providers that enables you to define a data model based on late-bound data types.</span></span>  
  
|<span data-ttu-id="7bc25-105">提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-105">Provider</span></span>|<span data-ttu-id="7bc25-106">描述</span><span class="sxs-lookup"><span data-stu-id="7bc25-106">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="7bc25-107">元数据提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-107">Metadata provider</span></span>|<span data-ttu-id="7bc25-108">这是核心的自定义数据服务提供程序，用于通过实现 <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> 接口在运行时定义自定义数据模型。</span><span class="sxs-lookup"><span data-stu-id="7bc25-108">This is the core custom data service provider that enables you to define a custom data model at runtime by implementing the <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> interface.</span></span>|  
|<span data-ttu-id="7bc25-109">查询提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-109">Query provider</span></span>|<span data-ttu-id="7bc25-110">该提供程序用于对使用 <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> 接口定义的自定义数据模型执行查询。</span><span class="sxs-lookup"><span data-stu-id="7bc25-110">This provider enables you to execute queries against a custom data model that is defined by using the <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> interface.</span></span> <span data-ttu-id="7bc25-111">查询提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceQueryProvider> 接口而创建。</span><span class="sxs-lookup"><span data-stu-id="7bc25-111">The query provider is created by implementing the <xref:System.Data.Services.Providers.IDataServiceQueryProvider> interface.</span></span>|  
|<span data-ttu-id="7bc25-112">更新提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-112">Update provider</span></span>|<span data-ttu-id="7bc25-113">该提供程序用于更新在自定义数据服务提供程序中公开的类型和管理并发性。</span><span class="sxs-lookup"><span data-stu-id="7bc25-113">This provider enables you to make updates to types that are exposed in a custom data service provider and to manage concurrency.</span></span> <span data-ttu-id="7bc25-114">更新提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceUpdateProvider> 接口而创建。</span><span class="sxs-lookup"><span data-stu-id="7bc25-114">An update provider is created by implementing the <xref:System.Data.Services.Providers.IDataServiceUpdateProvider> interface</span></span>|  
|<span data-ttu-id="7bc25-115">分页提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-115">Paging provider</span></span>|<span data-ttu-id="7bc25-116">该提供程序用于与自定义数据服务提供程序一起启用服务器驱动的分页支持。</span><span class="sxs-lookup"><span data-stu-id="7bc25-116">This provider is used with the custom data service provider to enable server-driven paging support.</span></span> <span data-ttu-id="7bc25-117">自定义数据服务的分页提供程序通过实现 <xref:System.Data.Services.Providers.IDataServicePagingProvider> 接口而创建。</span><span class="sxs-lookup"><span data-stu-id="7bc25-117">A paging provider for a custom data service is created by implementing the <xref:System.Data.Services.Providers.IDataServicePagingProvider> interface.</span></span>|  
|<span data-ttu-id="7bc25-118">流提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-118">Streaming provider</span></span>|<span data-ttu-id="7bc25-119">此提供程序用于以流形式公开二进制大型对象数据类型。</span><span class="sxs-lookup"><span data-stu-id="7bc25-119">This provider enables you to expose binary large object data types as a stream.</span></span> <span data-ttu-id="7bc25-120">流提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceStreamProvider> 接口而创建。</span><span class="sxs-lookup"><span data-stu-id="7bc25-120">A streaming provider is created by implementing the <xref:System.Data.Services.Providers.IDataServiceStreamProvider> interface.</span></span> <span data-ttu-id="7bc25-121">流提供程序还可与实体框架提供程序和反射数据源提供程序一起使用。</span><span class="sxs-lookup"><span data-stu-id="7bc25-121">The streaming provider can also be used with Entity Framework and reflection data source providers.</span></span> <span data-ttu-id="7bc25-122">有关详细信息，请参阅 [流式处理提供程序](streaming-provider-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="7bc25-122">For more information, see [Streaming Provider](streaming-provider-wcf-data-services.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7bc25-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bc25-123">See also</span></span>

- [<span data-ttu-id="7bc25-124">数据服务提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-124">Data Services Providers</span></span>](data-services-providers-wcf-data-services.md)
- [<span data-ttu-id="7bc25-125">实体框架提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-125">Entity Framework Provider</span></span>](entity-framework-provider-wcf-data-services.md)
- [<span data-ttu-id="7bc25-126">反射提供程序</span><span class="sxs-lookup"><span data-stu-id="7bc25-126">Reflection Provider</span></span>](reflection-provider-wcf-data-services.md)
