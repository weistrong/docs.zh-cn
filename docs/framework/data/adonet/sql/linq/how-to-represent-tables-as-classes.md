---
description: 了解有关详细信息，请参阅如何：将表表示为类
title: 如何：将表表示为类
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 84dda12b-88a2-4cd2-92b3-8db87b28d14c
ms.openlocfilehash: 9ec5b7309d7d10eaa6e4da6cd6fe4b1d03df1dd9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723577"
---
# <a name="how-to-represent-tables-as-classes"></a><span data-ttu-id="bed3b-103">如何：将表表示为类</span><span class="sxs-lookup"><span data-stu-id="bed3b-103">How to: Represent Tables as Classes</span></span>

<span data-ttu-id="bed3b-104">使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> 属性将类指定为与数据库表关联的实体类。</span><span class="sxs-lookup"><span data-stu-id="bed3b-104">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> attribute to designate a class as an entity class associated with a database table.</span></span>  
  
### <a name="to-map-a-class-to-a-database-table"></a><span data-ttu-id="bed3b-105">将类映射到数据库表</span><span class="sxs-lookup"><span data-stu-id="bed3b-105">To map a class to a database table</span></span>  
  
- <span data-ttu-id="bed3b-106">将 <xref:System.Data.Linq.Mapping.TableAttribute> 属性添加到类声明中。</span><span class="sxs-lookup"><span data-stu-id="bed3b-106">Add the <xref:System.Data.Linq.Mapping.TableAttribute> attribute to the class declaration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bed3b-107">示例</span><span class="sxs-lookup"><span data-stu-id="bed3b-107">Example</span></span>  

 <span data-ttu-id="bed3b-108">下面的代码创建作为与 `Customer` 数据库表关联的实体类的 `Customers` 类。</span><span class="sxs-lookup"><span data-stu-id="bed3b-108">The following code establishes the `Customer` class as an entity class that is associated with the `Customers` database table.</span></span>  
  
 [!code-csharp[DLinqCustomize#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#1)]
 [!code-vb[DLinqCustomize#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#1)]  
  
 <span data-ttu-id="bed3b-109">如果可以推断出名称，您无需指定 <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="bed3b-109">You do not have to specify the <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> property if the name can be inferred.</span></span> <span data-ttu-id="bed3b-110">如果您未指定名称，则假定此名称与此属性或字段的名称相同。</span><span class="sxs-lookup"><span data-stu-id="bed3b-110">If you do not specify a name, the name is presumed to be the same name as that of the property or field.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bed3b-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="bed3b-111">See also</span></span>

- [<span data-ttu-id="bed3b-112">LINQ to SQL 对象模型</span><span class="sxs-lookup"><span data-stu-id="bed3b-112">The LINQ to SQL Object Model</span></span>](the-linq-to-sql-object-model.md)
- [<span data-ttu-id="bed3b-113">如何：通过使用代码编辑器自定义实体类</span><span class="sxs-lookup"><span data-stu-id="bed3b-113">How to: Customize Entity Classes by Using the Code Editor</span></span>](how-to-customize-entity-classes-by-using-the-code-editor.md)
