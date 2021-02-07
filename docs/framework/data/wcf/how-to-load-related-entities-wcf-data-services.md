---
description: '了解有关详细信息，请参阅如何：加载相关实体 (WCF Data Services) '
title: 如何：加载相关实体（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, deferred content
- WCF Data Services, loading data
ms.assetid: 6f143d30-d997-4e6b-bcf0-d5c394ecb108
ms.openlocfilehash: 004e52b17c399abe8564dd069dd251d7baf296cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765251"
---
# <a name="how-to-load-related-entities-wcf-data-services"></a>如何：加载相关实体（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

需要在 WCF Data Services 中加载关联的实体时，可以 <xref:System.Data.Services.Client.DataServiceContext.LoadProperty%2A> 对类使用方法 <xref:System.Data.Services.Client.DataServiceContext> 。 你还可以使用 <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> 上的方法 <xref:System.Data.Services.Client.DataServiceQuery%601> 来要求在同一查询响应中积极加载相关实体。  
  
 本主题中的示例使用罗斯文示例数据服务和自动生成的客户端数据服务类。 此服务和客户端数据类是在完成 [WCF Data Services 快速入门](quickstart-wcf-data-services.md)时创建的。  
  
## <a name="example"></a>示例  

 下面的示例演示如何显式加载与每个返回的 `Customer` 实例相关的 `Orders`。  
  
 [!code-csharp[Astoria Northwind Client#LoadRelatedOrderCustomer](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#loadrelatedordercustomer)]
 [!code-vb[Astoria Northwind Client#LoadRelatedOrderCustomer](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#loadrelatedordercustomer)]  
  
## <a name="example"></a>示例  

 下面的示例演示如何使用 <xref:System.Data.Services.Client.DataServiceQuery%601.Expand%2A> 方法返回属于由查询返回的 `Order Details` 的 `Orders`。  
  
 [!code-csharp[Astoria Northwind Client#ExpandOrderDetails](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#expandorderdetails)]
 [!code-vb[Astoria Northwind Client#ExpandOrderDetails](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#expandorderdetails)]  
  
## <a name="see-also"></a>请参阅

- [查询数据服务](querying-the-data-service-wcf-data-services.md)
