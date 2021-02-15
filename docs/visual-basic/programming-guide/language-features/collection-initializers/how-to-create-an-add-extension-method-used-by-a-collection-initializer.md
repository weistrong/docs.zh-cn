---
description: '了解有关详细信息，请参阅如何：创建集合初始值设定项使用的 Add 扩展方法 (Visual Basic) '
title: 如何：创建供集合初始化程序使用的 Add 扩展方法
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: f64b52c7-8b11-4410-93a6-cb3aeebcc772
ms.openlocfilehash: 1fbe6f438c4761ae668a6bd6a0a2c38c8efdb439
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475469"
---
# <a name="how-to-create-an-add-extension-method-used-by-a-collection-initializer-visual-basic"></a><span data-ttu-id="fdc5d-103">如何：创建集合初始值设定项所使用的 Add 扩展方法 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fdc5d-103">How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic)</span></span>

<span data-ttu-id="fdc5d-104">使用集合初始值设定项创建集合时，Visual Basic 编译器会搜索集合类型的一个 `Add` 方法，该方法的方法的参数 `Add` 与集合初始值设定项中的值的类型相匹配。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-104">When you use a collection initializer to create a collection, the Visual Basic compiler searches for an `Add` method of the collection type for which the parameters for the `Add` method match the types of the values in the collection initializer.</span></span> <span data-ttu-id="fdc5d-105">此 `Add` 方法用于在集合中填充集合初始值设定项中的值。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-105">This `Add` method is used to populate the collection with the values from the collection initializer.</span></span>  
  
 <span data-ttu-id="fdc5d-106">如果不存在匹配的 `Add` 方法，并且无法修改集合的代码，则可以添加一个名为的扩展方法， `Add` 该方法采用集合初始值设定项所需的参数。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-106">If no matching `Add` method exists and you cannot modify the code for the collection, you can add an extension method called `Add` that takes the parameters that are required by the collection initializer.</span></span> <span data-ttu-id="fdc5d-107">这通常是使用泛型集合的集合初始值设定项时需要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-107">This is typically what you need to do when you use collection initializers for generic collections.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fdc5d-108">示例</span><span class="sxs-lookup"><span data-stu-id="fdc5d-108">Example</span></span>  

 <span data-ttu-id="fdc5d-109">下面的示例演示如何将扩展方法添加到泛型类型， <xref:System.Collections.Generic.List%601> 以便可以使用集合初始值设定项来添加类型的对象 `Employee` 。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-109">The following example shows how to add an extension method to the generic <xref:System.Collections.Generic.List%601> type so that a collection initializer can be used to add objects of type `Employee`.</span></span> <span data-ttu-id="fdc5d-110">通过扩展方法，可以使用简化的集合初始值设定项语法。</span><span class="sxs-lookup"><span data-stu-id="fdc5d-110">The extension method enables you to use the shortened collection initializer syntax.</span></span>  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#1)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#2)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo1#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1/VB/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="fdc5d-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="fdc5d-111">See also</span></span>

- [<span data-ttu-id="fdc5d-112">集合初始值设定项</span><span class="sxs-lookup"><span data-stu-id="fdc5d-112">Collection Initializers</span></span>](index.md)
- [<span data-ttu-id="fdc5d-113">如何：创建供集合初始化程序使用的集合</span><span class="sxs-lookup"><span data-stu-id="fdc5d-113">How to: Create a Collection Used by a Collection Initializer</span></span>](how-to-create-a-collection-used-by-a-collection-initializer.md)
