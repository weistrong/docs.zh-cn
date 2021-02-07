---
description: '了解详细信息：扩大 (Visual Basic) '
title: Widening
ms.date: 07/20/2015
f1_keywords:
- vb.widening
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Widening keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 646ae263-94d3-40a2-b0cc-64f619292f56
ms.openlocfilehash: de290296ba2b7716ba992c6bed46443053048282
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700697"
---
# <a name="widening-visual-basic"></a><span data-ttu-id="46cb1-103">Widening (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46cb1-103">Widening (Visual Basic)</span></span>

<span data-ttu-id="46cb1-104">指示转换运算符 (`CType`) 将类或结构转换为可以保存原始类或结构的所有可能值的类型。</span><span class="sxs-lookup"><span data-stu-id="46cb1-104">Indicates that a conversion operator (`CType`) converts a class or structure to a type that can hold all possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-widening-keyword"></a><span data-ttu-id="46cb1-105">用扩大关键字转换</span><span class="sxs-lookup"><span data-stu-id="46cb1-105">Converting with the Widening Keyword</span></span>  

 <span data-ttu-id="46cb1-106">除了之外，转换过程必须指定 `Public Shared` `Widening` 。</span><span class="sxs-lookup"><span data-stu-id="46cb1-106">The conversion procedure must specify `Public Shared` in addition to `Widening`.</span></span>  
  
 <span data-ttu-id="46cb1-107">扩大转换始终会在运行时成功，不会导致数据丢失。</span><span class="sxs-lookup"><span data-stu-id="46cb1-107">Widening conversions always succeed at run time and never incur data loss.</span></span> <span data-ttu-id="46cb1-108">示例包括 `Single` 对 `Double` `Char` `String` 其基类型的、向和派生的类型。</span><span class="sxs-lookup"><span data-stu-id="46cb1-108">Examples are `Single` to `Double`, `Char` to `String`, and a derived type to its base type.</span></span> <span data-ttu-id="46cb1-109">由于派生类型包含基类型的所有成员，因此是最新的转换，因此是基类型的实例。</span><span class="sxs-lookup"><span data-stu-id="46cb1-109">This last conversion is widening because the derived type contains all the members of the base type and thus is an instance of the base type.</span></span>  
  
 <span data-ttu-id="46cb1-110">使用代码不必使用 `CType` 进行扩大转换，即使 `Option Strict` 是 `On` 。</span><span class="sxs-lookup"><span data-stu-id="46cb1-110">The consuming code does not have to use `CType` for widening conversions, even if `Option Strict` is `On`.</span></span>  
  
 <span data-ttu-id="46cb1-111">`Widening`关键字可以在此上下文中使用：</span><span class="sxs-lookup"><span data-stu-id="46cb1-111">The `Widening` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="46cb1-112">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="46cb1-112">Operator Statement</span></span>](../statements/operator-statement.md)  
  
 <span data-ttu-id="46cb1-113">有关扩展和收缩转换运算符的定义示例，请参阅 [如何：定义转换运算符](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)。</span><span class="sxs-lookup"><span data-stu-id="46cb1-113">For example definitions of widening and narrowing conversion operators, see [How to: Define a Conversion Operator](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46cb1-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="46cb1-114">See also</span></span>

- [<span data-ttu-id="46cb1-115">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="46cb1-115">Operator Statement</span></span>](../statements/operator-statement.md)
- [<span data-ttu-id="46cb1-116">Narrowing</span><span class="sxs-lookup"><span data-stu-id="46cb1-116">Narrowing</span></span>](narrowing.md)
- [<span data-ttu-id="46cb1-117">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="46cb1-117">Widening and Narrowing Conversions</span></span>](../../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="46cb1-118">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="46cb1-118">How to: Define an Operator</span></span>](../../programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="46cb1-119">CType Function</span><span class="sxs-lookup"><span data-stu-id="46cb1-119">CType Function</span></span>](../functions/ctype-function.md)
- [<span data-ttu-id="46cb1-120">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="46cb1-120">Option Strict Statement</span></span>](../statements/option-strict-statement.md)
- [<span data-ttu-id="46cb1-121">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="46cb1-121">How to: Define a Conversion Operator</span></span>](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
