---
description: '了解详细信息：如何：声明具有混合访问级别的属性 (Visual Basic) '
title: 如何：声明具有混合访问级别的属性
ms.date: 07/20/2015
helpviewer_keywords:
- access levels [Visual Basic], properties
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- mixed access levels
- Visual Basic code, properties
- properties [Visual Basic], access levels
- Property statement [Visual Basic], declaring mixed access levels
ms.assetid: fdbb2d97-279a-4956-b26c-cbdfbc34915a
ms.openlocfilehash: e01849b0a590e499c1ee7b4a67d6aa794cd7cc5d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472457"
---
# <a name="how-to-declare-a-property-with-mixed-access-levels-visual-basic"></a><span data-ttu-id="6d312-103">如何：声明具有混合访问级别的属性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6d312-103">How to: Declare a Property with Mixed Access Levels (Visual Basic)</span></span>

<span data-ttu-id="6d312-104">如果希望属性的 `Get` 和 `Set` 过程具有不同的访问级别，则可以在语句中使用更多的权限级别， `Property` 或在或语句中使用更严格的 `Get` 级别 `Set` 。</span><span class="sxs-lookup"><span data-stu-id="6d312-104">If you want the `Get` and `Set` procedures on a property to have different access levels, you can use the more permissive level in the `Property` statement and the more restrictive level in either the `Get` or `Set` statement.</span></span> <span data-ttu-id="6d312-105">如果希望代码的某些部分能够获取属性的值，并且代码的某些其他部分可以更改值，则可以对属性使用混合访问级别。</span><span class="sxs-lookup"><span data-stu-id="6d312-105">You use mixed access levels on a property when you want certain parts of the code to be able to get the property's value, and certain other parts of the code to be able to change the value.</span></span>  
  
 <span data-ttu-id="6d312-106">有关访问级别的详细信息，请参阅 [Visual Basic 中的访问级别](../declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="6d312-106">For more information on access levels, see [Access levels in Visual Basic](../declared-elements/access-levels.md).</span></span>  
  
### <a name="to-declare-a-property-with-mixed-access-levels"></a><span data-ttu-id="6d312-107">声明具有混合访问级别的属性</span><span class="sxs-lookup"><span data-stu-id="6d312-107">To declare a property with mixed access levels</span></span>  
  
1. <span data-ttu-id="6d312-108">以正常方式声明属性，并指定限制性较低的访问级别 (如 `Public` 语句中) `Property` 。</span><span class="sxs-lookup"><span data-stu-id="6d312-108">Declare the property in the normal way, and specify the less restrictive access level (such as `Public`) in the `Property` statement.</span></span>  
  
2. <span data-ttu-id="6d312-109">声明 `Get` 或 `Set` 指定限制性更强的访问级别 (如 `Friend`) 。</span><span class="sxs-lookup"><span data-stu-id="6d312-109">Declare either the `Get` or the `Set` procedure specifying the more restrictive access level (such as `Friend`).</span></span>  
  
3. <span data-ttu-id="6d312-110">不要指定其他属性过程的访问级别。</span><span class="sxs-lookup"><span data-stu-id="6d312-110">Do not specify an access level on the other property procedure.</span></span> <span data-ttu-id="6d312-111">它假定在语句中声明了访问级别 `Property` 。</span><span class="sxs-lookup"><span data-stu-id="6d312-111">It assumes the access level declared in the `Property` statement.</span></span> <span data-ttu-id="6d312-112">你可以仅对其中一个属性过程进行访问限制。</span><span class="sxs-lookup"><span data-stu-id="6d312-112">You can restrict access on only one of the property procedures.</span></span>  
  
     [!code-vb[VbVbcnProcedures#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#10)]  
  
     <span data-ttu-id="6d312-113">在前面的示例中，该 `Get` 过程具有与 `Protected` 属性本身相同的访问权限，而此 `Set` 过程具有 `Private` 访问权限。</span><span class="sxs-lookup"><span data-stu-id="6d312-113">In the preceding example, the `Get` procedure has the same `Protected` access as the property itself, while the `Set` procedure has `Private` access.</span></span> <span data-ttu-id="6d312-114">派生自的类 `employee` 可以读取 `salary` 值，但只有 `employee` 类可以对其进行设置。</span><span class="sxs-lookup"><span data-stu-id="6d312-114">A class derived from `employee` can read the `salary` value, but only the `employee` class can set it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d312-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d312-115">See also</span></span>

- [<span data-ttu-id="6d312-116">过程</span><span class="sxs-lookup"><span data-stu-id="6d312-116">Procedures</span></span>](./index.md)
- [<span data-ttu-id="6d312-117">Property 过程</span><span class="sxs-lookup"><span data-stu-id="6d312-117">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="6d312-118">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="6d312-118">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="6d312-119">Property Statement</span><span class="sxs-lookup"><span data-stu-id="6d312-119">Property Statement</span></span>](../../../language-reference/statements/property-statement.md)
- [<span data-ttu-id="6d312-120">Visual Basic 中属性和变量的差异</span><span class="sxs-lookup"><span data-stu-id="6d312-120">Differences Between Properties and Variables in Visual Basic</span></span>](./differences-between-properties-and-variables.md)
- [<span data-ttu-id="6d312-121">如何：创建属性</span><span class="sxs-lookup"><span data-stu-id="6d312-121">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="6d312-122">如何：调用 Property 过程</span><span class="sxs-lookup"><span data-stu-id="6d312-122">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="6d312-123">如何：在 Visual Basic 中声明和调用默认属性</span><span class="sxs-lookup"><span data-stu-id="6d312-123">How to: Declare and Call a Default Property in Visual Basic</span></span>](./how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="6d312-124">如何：在属性中放置值</span><span class="sxs-lookup"><span data-stu-id="6d312-124">How to: Put a Value in a Property</span></span>](./how-to-put-a-value-in-a-property.md)
- [<span data-ttu-id="6d312-125">如何：从属性获取值</span><span class="sxs-lookup"><span data-stu-id="6d312-125">How to: Get a Value from a Property</span></span>](./how-to-get-a-value-from-a-property.md)
