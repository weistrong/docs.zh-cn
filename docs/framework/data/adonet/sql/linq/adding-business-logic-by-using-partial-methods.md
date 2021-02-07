---
description: 了解详细信息：使用分部方法添加业务逻辑
title: 通过使用分部方法添加业务逻辑
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 3a73991e-fd4e-4610-93fb-7ced4dc6b7f9
ms.openlocfilehash: c34d0d25fa9dba074f1c7ff2abe2e9e24c931a8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672265"
---
# <a name="adding-business-logic-by-using-partial-methods"></a><span data-ttu-id="652b2-103">通过使用分部方法添加业务逻辑</span><span class="sxs-lookup"><span data-stu-id="652b2-103">Adding Business Logic By Using Partial Methods</span></span>

<span data-ttu-id="652b2-104">您可以 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 通过使用 *分部方法* 自定义项目中的 Visual Basic 和 c # 生成的代码。</span><span class="sxs-lookup"><span data-stu-id="652b2-104">You can customize Visual Basic and C# generated code in your [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] projects by using *partial methods*.</span></span> <span data-ttu-id="652b2-105">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 生成的代码定义签名作为分部方法的一部分。</span><span class="sxs-lookup"><span data-stu-id="652b2-105">The code that [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] generates defines signatures as one part of a partial method.</span></span> <span data-ttu-id="652b2-106">如果您要实现此方法，您可以添加自己的分部方法。</span><span class="sxs-lookup"><span data-stu-id="652b2-106">If you want to implement the method, you can add your own partial method.</span></span> <span data-ttu-id="652b2-107">如果您不添加自己的实现，编译器将丢弃分部方法签名并调用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中的默认方法。</span><span class="sxs-lookup"><span data-stu-id="652b2-107">If you do not add your own implementation, the compiler discards the partial methods signature and calls the default methods in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>  
  
> [!NOTE]
> <span data-ttu-id="652b2-108">如果使用的是 Visual Studio，则可以使用对象关系设计器向实体类添加验证及其他自定义项。</span><span class="sxs-lookup"><span data-stu-id="652b2-108">If you are using Visual Studio, you can use the Object Relational Designer to add validation and other customizations to entity classes.</span></span>  
  
 <span data-ttu-id="652b2-109">例如，Northwind 示例数据库中 `Customer` 类的默认映射包括下面的分部方法：</span><span class="sxs-lookup"><span data-stu-id="652b2-109">For example, the default mapping for the `Customer` class in the Northwind sample database includes the following partial method:</span></span>  
  
 [!code-csharp[DLinqOverrideDefault#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefault/cs/northwind.cs#2)]
 [!code-vb[DLinqOverrideDefault#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefault/vb/northwind.vb#2)]  
  
 <span data-ttu-id="652b2-110">您可以向自己的分部 `Customer` 类添加诸如以下内容的代码来实现自己的方法。</span><span class="sxs-lookup"><span data-stu-id="652b2-110">You can implement your own method by adding code such as the following to your own partial `Customer` class:</span></span>  
  
 [!code-csharp[DLinqOverrideDefault#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefault/cs/Program.cs#3)]
 [!code-vb[DLinqOverrideDefault#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefault/vb/Module1.vb#3)]  
  
 <span data-ttu-id="652b2-111">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中通常使用这种方式来重写 `Insert`、`Update`、`Delete` 的默认方法以及在对象生命周期事件过程中验证属性。</span><span class="sxs-lookup"><span data-stu-id="652b2-111">This approach is typically used in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] to override default methods for `Insert`, `Update`, `Delete`, and to validate properties during object life-cycle events.</span></span>  
  
 <span data-ttu-id="652b2-112">有关详细信息，请参阅 [分部方法](../../../../../visual-basic/programming-guide/language-features/procedures/partial-methods.md) (Visual Basic) 或 [部分 (方法) ](../../../../../csharp/language-reference/keywords/partial-method.md) (c #)  (c # 引用 ) 。</span><span class="sxs-lookup"><span data-stu-id="652b2-112">For more information, see [Partial Methods](../../../../../visual-basic/programming-guide/language-features/procedures/partial-methods.md) (Visual Basic) or [partial (Method) (C# Reference)](../../../../../csharp/language-reference/keywords/partial-method.md) (C#).</span></span>  
  
## <a name="example"></a><span data-ttu-id="652b2-113">示例</span><span class="sxs-lookup"><span data-stu-id="652b2-113">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="652b2-114">说明</span><span class="sxs-lookup"><span data-stu-id="652b2-114">Description</span></span>  

 <span data-ttu-id="652b2-115">下面的示例首先显示了 `ExampleClass`，因为它可能是由像 SQLMetal 这样的代码生成工具定义的；然后，此示例演示了如何只实现两个方法之一。</span><span class="sxs-lookup"><span data-stu-id="652b2-115">The following example shows `ExampleClass` first as it might be defined by a code-generating tool such as SQLMetal, and then how you might implement only one of the two methods.</span></span>  
  
### <a name="code"></a><span data-ttu-id="652b2-116">代码</span><span class="sxs-lookup"><span data-stu-id="652b2-116">Code</span></span>  

 [!code-csharp[DLinqSubmittingChanges#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#4)]
 [!code-vb[DLinqSubmittingChanges#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="652b2-117">示例</span><span class="sxs-lookup"><span data-stu-id="652b2-117">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="652b2-118">说明</span><span class="sxs-lookup"><span data-stu-id="652b2-118">Description</span></span>  

 <span data-ttu-id="652b2-119">下面的示例用到了 `Shipper` 和 `Order` 实体之间的关系。</span><span class="sxs-lookup"><span data-stu-id="652b2-119">The following example uses the relationship between `Shipper` and `Order` entities.</span></span> <span data-ttu-id="652b2-120">请注意这些方法中的分部方法 `InsertShipper` 和 `DeleteShipper`。</span><span class="sxs-lookup"><span data-stu-id="652b2-120">Note among the methods the partial methods, `InsertShipper` and `DeleteShipper`.</span></span> <span data-ttu-id="652b2-121">这些方法重写了由 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 映射提供的默认分部方法。</span><span class="sxs-lookup"><span data-stu-id="652b2-121">These methods override the default partial methods supplied by [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] mapping.</span></span>  
  
### <a name="code"></a><span data-ttu-id="652b2-122">代码</span><span class="sxs-lookup"><span data-stu-id="652b2-122">Code</span></span>  

 [!code-csharp[DLinqOverrideDefault#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefault/cs/northwind.cs#1)]
 [!code-vb[DLinqOverrideDefault#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefault/vb/northwind.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="652b2-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="652b2-123">See also</span></span>

- [<span data-ttu-id="652b2-124">进行和提交数据更改</span><span class="sxs-lookup"><span data-stu-id="652b2-124">Making and Submitting Data Changes</span></span>](making-and-submitting-data-changes.md)
- [<span data-ttu-id="652b2-125">自定义插入、更新和删除操作</span><span class="sxs-lookup"><span data-stu-id="652b2-125">Customizing Insert, Update, and Delete Operations</span></span>](customizing-insert-update-and-delete-operations.md)
