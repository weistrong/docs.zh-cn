---
description: '了解有关详细信息，请参阅如何：使用反射提供程序创建数据服务 (WCF Data Services) '
title: 如何：使用反射提供程序创建数据服务（WCF 数据服务）
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, providers
ms.assetid: 7315c6d8-f452-4fb2-a0c1-76ab0593c146
ms.openlocfilehash: 1c4d131b21c69e11dd6d8b574e4c22a6af7c5a25
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766219"
---
# <a name="how-to-create-a-data-service-using-the-reflection-provider-wcf-data-services"></a>如何：使用反射提供程序创建数据服务（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

WCF Data Services 使你可以定义基于任意类的数据模型，前提是这些类作为实现接口的对象公开 <xref:System.Linq.IQueryable%601> 。 有关详细信息，请参阅 [数据服务提供程序](data-services-providers-wcf-data-services.md)。  
  
## <a name="example"></a>示例  

 下面的示例定义一个包括 `Orders` 和 `Items` 的数据模型。 实体容器类 `OrderItemData` 具有两个公共方法，这两个方法返回 <xref:System.Linq.IQueryable%601> 接口。 这些接口是 `Orders` 和 `Items` 实体类型的实体集。 `Order` 可以包括多个 `Items`，因此 `Orders` 实体类型具有一个返回 `Items` 对象集合的 `Items` 导航属性。 `OrderItemData` 实体容器类是 <xref:System.Data.Services.DataService%601> 数据服务派生自的 `OrderItems` 类的泛型类型。  
  
> [!NOTE]
> 由于此示例演示内存中数据提供程序，且未在当前对象实例外保存更改，因此实现 <xref:System.Data.Services.IUpdatable> 接口不会带来任何好处。 有关实现接口的示例 <xref:System.Data.Services.IUpdatable> ，请参阅 [如何：使用 LINQ to SQL 数据源创建数据服务](create-a-data-service-using-linq-to-sql-wcf.md)。  
  
 [!code-csharp[Astoria Reflection Provider#CustomIQueryable](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_reflection_provider/cs/orderitems.svc.cs#customiqueryable)]
 [!code-vb[Astoria Reflection Provider#CustomIQueryable](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_reflection_provider/vb/orderitems.svc.vb#customiqueryable)]  
  
## <a name="see-also"></a>请参阅

- [如何：使用 LINQ to SQL 数据源创建数据服务](create-a-data-service-using-linq-to-sql-wcf.md)
- [数据服务提供程序](data-services-providers-wcf-data-services.md)
- [如何：使用 ADO.NET 实体框架数据源创建数据服务](create-a-data-service-using-an-adonet-ef-data-wcf.md)
