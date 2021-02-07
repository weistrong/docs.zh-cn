---
description: '了解详细信息：如何：启用对数据服务的访问 (WCF Data Services) '
title: 如何：启用对数据服务的访问（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 3d830bcd-32b4-4f26-9287-d58a071452c6
ms.openlocfilehash: 42be9c4c31da7bbbfef07958deef685d52df597b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765420"
---
# <a name="how-to-enable-access-to-the-data-service-wcf-data-services"></a><span data-ttu-id="f1dd3-103">如何：启用对数据服务的访问（WCF 数据服务）</span><span class="sxs-lookup"><span data-stu-id="f1dd3-103">How to: Enable Access to the Data Service (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="f1dd3-104">在 WCF Data Services 中，必须显式授予对数据服务公开的资源的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-104">In WCF Data Services, you must explicitly grant access to the resources that are exposed by a data service.</span></span> <span data-ttu-id="f1dd3-105">这意味着您在创建新的数据服务之后，仍必须显式提供对实体集形式的各个资源的访问。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-105">This means that after you create a new data service, you must still explicitly provide access to individual resources as entity sets.</span></span> <span data-ttu-id="f1dd3-106">本主题演示如何启用对 Northwind 数据服务中的五个实体集的读写访问，这些实体集是在完成 [快速入门](quickstart-wcf-data-services.md)时创建的。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-106">This topic shows how to enable read and write access to five of the entity sets in the Northwind data service that is created when you complete the [quickstart](quickstart-wcf-data-services.md).</span></span> <span data-ttu-id="f1dd3-107">由于 <xref:System.Data.Services.EntitySetRights> 枚举是通过使用 <xref:System.FlagsAttribute> 定义的，因此您可以使用逻辑 OR 运算符来为单个实体集指定多个权限。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-107">Because the <xref:System.Data.Services.EntitySetRights> enumeration is defined by using the <xref:System.FlagsAttribute>, you can use a logical OR operator to specify multiple permissions for a single entity set.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f1dd3-108">任何可以访问该 ASP.NET 应用程序的客户端也能够访问由数据服务公开的资源。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-108">Any client that can access the ASP.NET application can also access the resources exposed by the data service.</span></span> <span data-ttu-id="f1dd3-109">在生产数据服务中，为防止对资源进行未经授权的访问，还应保护应用程序本身的安全。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-109">In a production data service, to prevent unauthorized access to resources, you should also secure the application itself.</span></span> <span data-ttu-id="f1dd3-110">有关详细信息，请参阅 [保护 ASP.NET 网站](/previous-versions/aspnet/91f66yxt(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-110">For more information, see [Securing ASP.NET Web Sites](/previous-versions/aspnet/91f66yxt(v=vs.100)).</span></span>  
  
### <a name="to-enable-access-to-the-data-service"></a><span data-ttu-id="f1dd3-111">启用对数据服务的访问</span><span class="sxs-lookup"><span data-stu-id="f1dd3-111">To enable access to the data service</span></span>  
  
- <span data-ttu-id="f1dd3-112">在数据服务的代码中，用下列代码替换 `InitializeService` 函数中的占位符代码：</span><span class="sxs-lookup"><span data-stu-id="f1dd3-112">In the code for the data service, replace the placeholder code in the `InitializeService` function with the following:</span></span>  
  
     [!code-csharp[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_quickstart_service/cs/northwind.svc.cs#allreadconfig)]
     [!code-vb[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_quickstart_service/vb/northwind.svc.vb#allreadconfig)]  
  
     <span data-ttu-id="f1dd3-113">这使得客户端能够对 `Orders` 和 `Order_Details` 实体集进行读写访问，以及对 `Customers` 实体集进行只读访问。</span><span class="sxs-lookup"><span data-stu-id="f1dd3-113">This enables clients to have read and write access to the `Orders` and `Order_Details` entity sets and read-only access to the `Customers` entity sets.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1dd3-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="f1dd3-114">See also</span></span>

- [<span data-ttu-id="f1dd3-115">如何：开发在 IIS 上运行的 WCF 数据服务</span><span class="sxs-lookup"><span data-stu-id="f1dd3-115">How to: Develop a WCF Data Service Running on IIS</span></span>](how-to-develop-a-wcf-data-service-running-on-iis.md)
- [<span data-ttu-id="f1dd3-116">配置数据服务</span><span class="sxs-lookup"><span data-stu-id="f1dd3-116">Configuring the Data Service</span></span>](configuring-the-data-service-wcf-data-services.md)
