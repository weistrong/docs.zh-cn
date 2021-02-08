---
description: 了解详细信息：插入、更新和删除操作
title: 插入、更新和删除操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 26a43a4f-83c9-4732-806d-bb23aad0ff6b
ms.openlocfilehash: 2d0470ed6abe654ca08f954c3de97de207adb75d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803810"
---
# <a name="insert-update-and-delete-operations"></a><span data-ttu-id="35cb6-103">插入、更新和删除操作</span><span class="sxs-lookup"><span data-stu-id="35cb6-103">Insert, Update, and Delete Operations</span></span>

<span data-ttu-id="35cb6-104">在 `Insert` 中执行 `Update`、`Delete` 和 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 操作的方法是：向对象模型中添加对象、更改和移除对象模型中的对象。</span><span class="sxs-lookup"><span data-stu-id="35cb6-104">You perform `Insert`, `Update`, and `Delete` operations in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] by adding, changing, and removing objects in your object model.</span></span> <span data-ttu-id="35cb6-105">默认情况下，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 会将您所做的操作转换成 SQL，然后将这些更改提交至数据库。</span><span class="sxs-lookup"><span data-stu-id="35cb6-105">By default, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] translates your actions to SQL and submits the changes to the database.</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="35cb6-106">在操作和保持对对象所做更改方面有着最大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="35cb6-106">offers maximum flexibility in manipulating and persisting changes that you made to your objects.</span></span> <span data-ttu-id="35cb6-107">实体对象可用（通过查询检索它们或通过重新构造它们）后，就可以像应用程序中的典型对象一样更改实体对象。</span><span class="sxs-lookup"><span data-stu-id="35cb6-107">As soon as entity objects are available (either by retrieving them through a query or by constructing them anew), you can change them as typical objects in your application.</span></span> <span data-ttu-id="35cb6-108">也就是说，可以更改它们的值，将它们添加到集合中，以及从集合中移除它们。</span><span class="sxs-lookup"><span data-stu-id="35cb6-108">That is, you can change their values, you can add them to your collections, and you can remove them from your collections.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="35cb6-109">会跟踪您所做的更改，并且在您调用 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 时就可以将这些更改传回数据库。</span><span class="sxs-lookup"><span data-stu-id="35cb6-109">tracks your changes and is ready to transmit them back to the database when you call <xref:System.Data.Linq.DataContext.SubmitChanges%2A>.</span></span>

> [!NOTE]
> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="35cb6-110">不支持且无法识别级联删除操作。</span><span class="sxs-lookup"><span data-stu-id="35cb6-110">does not support or recognize cascade-delete operations.</span></span> <span data-ttu-id="35cb6-111">如果要删除表中具有约束的行，则必须在 `ON DELETE CASCADE` 数据库的外键约束中设置规则，或者使用自己的代码先删除阻止删除父对象的子对象的子对象。</span><span class="sxs-lookup"><span data-stu-id="35cb6-111">If you want to delete a row in a table that has constraints against it, you must either set the `ON DELETE CASCADE` rule in the foreign-key constraint in the database, or use your own code to first delete the child objects that prevent the parent object from being deleted.</span></span> <span data-ttu-id="35cb6-112">否则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="35cb6-112">Otherwise, an exception is thrown.</span></span> <span data-ttu-id="35cb6-113">有关详细信息，请参阅 [如何：从数据库中删除行](how-to-delete-rows-from-the-database.md)。</span><span class="sxs-lookup"><span data-stu-id="35cb6-113">For more information, see [How to: Delete Rows From the Database](how-to-delete-rows-from-the-database.md).</span></span>

<span data-ttu-id="35cb6-114">以下摘录会用到 Northwind 示例数据库中的 `Customer` 和 `Order` 类。</span><span class="sxs-lookup"><span data-stu-id="35cb6-114">The following excerpts use the `Customer` and `Order` classes from the Northwind sample database.</span></span> <span data-ttu-id="35cb6-115">为简洁起见，不显示类定义。</span><span class="sxs-lookup"><span data-stu-id="35cb6-115">Class definitions are not shown for brevity.</span></span>

[!code-csharp[DLinqCRUDOps#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCRUDOps/cs/Program.cs#1)]
[!code-vb[DLinqCRUDOps#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCRUDOps/vb/Module1.vb#1)]

<span data-ttu-id="35cb6-116">当您调用 <xref:System.Data.Linq.DataContext.SubmitChanges%2A> 时，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 会自动生成并执行它为将您所做的更改传回数据库而必须具备的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="35cb6-116">When you call <xref:System.Data.Linq.DataContext.SubmitChanges%2A>, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] automatically generates and executes the SQL commands that it must have to transmit your changes back to the database.</span></span>

> [!NOTE]
> <span data-ttu-id="35cb6-117">您可以使用自己的自定义逻辑来重写此行为，这通常是通过存储过程来实现的。</span><span class="sxs-lookup"><span data-stu-id="35cb6-117">You can override this behavior by using your own custom logic, typically by way of a stored procedure.</span></span> <span data-ttu-id="35cb6-118">有关详细信息，请参阅 [开发人员在重写默认行为中的责任](responsibilities-of-the-developer-in-overriding-default-behavior.md)。</span><span class="sxs-lookup"><span data-stu-id="35cb6-118">For more information, see [Responsibilities of the Developer In Overriding Default Behavior](responsibilities-of-the-developer-in-overriding-default-behavior.md).</span></span>
>
> <span data-ttu-id="35cb6-119">使用 Visual Studio 的开发人员可以使用对象关系设计器来开发用于实现此目的的存储过程。</span><span class="sxs-lookup"><span data-stu-id="35cb6-119">Developers using Visual Studio can use the Object Relational Designer to develop stored procedures for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="35cb6-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="35cb6-120">See also</span></span>

- [<span data-ttu-id="35cb6-121">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="35cb6-121">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
- [<span data-ttu-id="35cb6-122">自定义插入、更新和删除操作</span><span class="sxs-lookup"><span data-stu-id="35cb6-122">Customizing Insert, Update, and Delete Operations</span></span>](customizing-insert-update-and-delete-operations.md)
