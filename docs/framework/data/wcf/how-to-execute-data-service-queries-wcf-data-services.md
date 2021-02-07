---
description: '了解详细信息：如何：执行数据服务查询 (WCF Data Services) '
title: 如何：执行数据服务查询（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- querying the data service [WCF Data Services]
- WCF Data Services, querying
- WCF Data Services, accessing data
ms.assetid: 62997821-e0c6-4c4d-9fb7-1273fb5e5d18
ms.openlocfilehash: 0d78a5a82f23bb6035d21bd45d68a0b1bb76f34b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765316"
---
# <a name="how-to-execute-data-service-queries-wcf-data-services"></a>如何：执行数据服务查询（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

WCF Data Services 使你能够使用生成的客户端数据服务类从基于 .NET Framework 的客户端应用程序查询数据服务。 可以使用下列方法之一执行查询：  
  
- 针对从 <xref:System.Data.Services.Client.DataServiceQuery%601> 工具所生成的 <xref:System.Data.Services.Client.DataServiceContext> 获取的命名 `Add Data Service Reference` 执行 LINQ 查询。  
  
- 隐式枚举从 <xref:System.Data.Services.Client.DataServiceQuery%601> 工具所生成的 <xref:System.Data.Services.Client.DataServiceContext> 获取的命名 `Add Data Service Reference`。  
  
- 显式调用 <xref:System.Data.Services.Client.DataServiceContext.Execute%2A> 的 <xref:System.Data.Services.Client.DataServiceQuery%601> 方法，或显式调用用于异步执行的 <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A> 方法。  
  
 有关详细信息，请参阅 [查询数据服务](querying-the-data-service-wcf-data-services.md)。  
  
 本主题中的示例使用罗斯文示例数据服务和自动生成的客户端数据服务类。 此服务和客户端数据类是在完成 [WCF Data Services 快速入门](quickstart-wcf-data-services.md)时创建的。  
  
## <a name="example"></a>示例  

 下面的示例演示如何定义和执行针对 Northwind 数据服务返回所有 `Customers` 的 LINQ 查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomersLinq](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#getallcustomerslinq)]
 [!code-vb[Astoria Northwind Client#GetAllCustomersLinq](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#getallcustomerslinq)]  
  
## <a name="example"></a>示例  

 下面的示例演示如何使用“`Add Data Service Reference`”工具所生成的上下文来隐式执行针对 Northwind 数据服务返回所有 `Customers` 的查询。 该上下文自动确定请求的 `Customers` 实体集的 URI。 在发生枚举时隐式执行该查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomers](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#getallcustomers)]
 [!code-vb[Astoria Northwind Client#GetAllCustomers](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#getallcustomers)]  
  
## <a name="example"></a>示例  

 下面的示例演示如何使用 <xref:System.Data.Services.Client.DataServiceContext> 显式执行针对 Northwind 数据服务返回所有 `Customers` 的查询。  
  
 [!code-csharp[Astoria Northwind Client#GetAllCustomersExplicit](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#getallcustomersexplicit)]
 [!code-vb[Astoria Northwind Client#GetAllCustomersExplicit](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#getallcustomersexplicit)]  
  
## <a name="see-also"></a>请参阅

- [如何：将查询选项添加到数据服务查询](how-to-add-query-options-to-a-data-service-query-wcf-data-services.md)
