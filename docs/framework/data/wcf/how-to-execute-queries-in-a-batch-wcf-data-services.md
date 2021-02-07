---
description: '了解有关详细信息，请参阅如何：在批处理中执行查询 (WCF Data Services) '
title: 如何：在一个批处理作业中执行查询（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, batch requests
ms.assetid: 3b4db7df-bd33-43a1-8ea4-63a18e131f97
ms.openlocfilehash: bcd95be57d2f3f2cea075a4b87fb6858c59ea41e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765290"
---
# <a name="how-to-execute-queries-in-a-batch-wcf-data-services"></a>如何：在一个批处理作业中执行查询（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

通过使用 WCF Data Services 的客户端库，可以对单个批处理中的数据服务执行多个查询。 有关详细信息，请参阅 [批处理操作](batching-operations-wcf-data-services.md)。  
  
 本主题中的示例使用罗斯文示例数据服务和自动生成的客户端数据服务类。 此服务和客户端数据类是在完成 [WCF Data Services 快速入门](quickstart-wcf-data-services.md)时创建的。  
  
## <a name="example"></a>示例  

 下面的示例演示如何调用 <xref:System.Data.Services.Client.DataServiceContext.ExecuteBatch%2A> 方法来执行一个 <xref:System.Data.Services.Client.DataServiceRequest%601> 对象数组，该数组包含从 Northwind 数据服务同时返回 `Customers` 和 `Products` 对象的查询。 此示例将枚举返回的 <xref:System.Data.Services.Client.QueryOperationResponse%601> 中的 <xref:System.Data.Services.Client.DataServiceResponse> 对象的集合，并且还会枚举每个 <xref:System.Data.Services.Client.QueryOperationResponse%601> 中包含的对象的集合。  
  
 [!code-csharp[Astoria Northwind Client#BatchQuery](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#batchquery)]
 [!code-vb[Astoria Northwind Client#BatchQuery](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#batchquery)]  
  
## <a name="see-also"></a>请参阅

- [WCF 数据服务客户端库](wcf-data-services-client-library.md)
