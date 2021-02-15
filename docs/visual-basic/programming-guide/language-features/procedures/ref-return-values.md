---
description: '了解详细信息：支持引用返回值 (Visual Basic) '
title: 引用返回值
ms.date: 04/28/2017
helpviewer_keywords:
- variables [Visual Basic]
- ref return values [Visual Basic]
- ref returns [Visual Basic]
ms.assetid: 5ef0cc69-eb3a-4a67-92a2-78585f223cb5
ms.openlocfilehash: 215a647c68eb7eadd394a1a7842ceb98c46e04a5
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466544"
---
# <a name="support-for-reference-return-values-visual-basic"></a><span data-ttu-id="84402-103">支持 (Visual Basic 的引用返回值) </span><span class="sxs-lookup"><span data-stu-id="84402-103">Support for reference return values (Visual Basic)</span></span>

<span data-ttu-id="84402-104">从 c # 7.0 开始，c # 语言支持 *引用返回值*。</span><span class="sxs-lookup"><span data-stu-id="84402-104">Starting with C# 7.0, the C# language supports *reference return values*.</span></span> <span data-ttu-id="84402-105">了解引用返回值的一种方法是，它们与通过引用传递给方法的参数相反。</span><span class="sxs-lookup"><span data-stu-id="84402-105">One way to understand reference return values is that they are the opposite of arguments that are passed by reference to a method.</span></span> <span data-ttu-id="84402-106">当修改通过引用传递的参数时，所做的更改将反映在调用方上的变量值中。</span><span class="sxs-lookup"><span data-stu-id="84402-106">When an argument passed by reference is modified, the changes are reflected in value of the variable on the caller.</span></span> <span data-ttu-id="84402-107">当方法为调用方提供引用返回值时，调用方对引用返回值所做的修改会反映在被调用方法的数据中。</span><span class="sxs-lookup"><span data-stu-id="84402-107">When an method provides a reference return value to a caller, modifications made to the reference return value by the caller are reflected in the called method's data.</span></span>

<span data-ttu-id="84402-108">Visual Basic 不允许使用引用返回值创作方法，但允许使用引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-108">Visual Basic does not allow you to author methods with reference return values, but it does allow you to consume reference return values.</span></span> <span data-ttu-id="84402-109">换言之，您可以调用具有引用返回值的方法并修改该返回值，对引用返回值所做的更改将反映在被调用方法的数据中。</span><span class="sxs-lookup"><span data-stu-id="84402-109">In other words, you can call a method with a reference return value and modify that return value, and changes to the reference return value are reflected in the called method's data.</span></span>

## <a name="modifying-the-ref-return-value-directly"></a><span data-ttu-id="84402-110">直接修改引用返回值</span><span class="sxs-lookup"><span data-stu-id="84402-110">Modifying the ref return value directly</span></span>

<span data-ttu-id="84402-111">对于始终成功并且没有参数的方法 `ByRef` ，您可以直接修改引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-111">For methods that always succeed and have no `ByRef` parameters, you can modify the reference return value directly.</span></span> <span data-ttu-id="84402-112">为此，可将新值分配给返回引用返回值的表达式。</span><span class="sxs-lookup"><span data-stu-id="84402-112">You do this by assigning the new value to the expressions that returns the reference return value.</span></span>

<span data-ttu-id="84402-113">下面的 c # 示例定义一个 `NumericValue.IncrementValue` 方法，该方法递增内部值并将其作为引用返回值返回。</span><span class="sxs-lookup"><span data-stu-id="84402-113">The following C# example defines a `NumericValue.IncrementValue` method that increments an internal value and returns it as a reference return value.</span></span>

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/ref-returns1.cs)]

<span data-ttu-id="84402-114">然后，调用方在下面 Visual Basic 示例中修改引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-114">The reference return value is then modified by the caller in the following Visual Basic example.</span></span> <span data-ttu-id="84402-115">请注意，具有 `NumericValue.IncrementValue` 方法调用的行不会向方法分配值。</span><span class="sxs-lookup"><span data-stu-id="84402-115">Note that the line with the `NumericValue.IncrementValue` method call does not assign a value to the method.</span></span> <span data-ttu-id="84402-116">相反，它将值赋给方法返回的引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-116">Instead, it assigns a value to the reference return value returned by the method.</span></span>

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/use-ref-returns1.vb)]

## <a name="using-a-helper-method"></a><span data-ttu-id="84402-117">使用 helper 方法</span><span class="sxs-lookup"><span data-stu-id="84402-117">Using a helper method</span></span>

<span data-ttu-id="84402-118">在其他情况下，可能不会始终需要直接修改方法调用的引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-118">In other cases, modifying the reference return value of a method call directly may not always be desirable.</span></span> <span data-ttu-id="84402-119">例如，返回字符串的搜索方法可能并不总是找到匹配项。</span><span class="sxs-lookup"><span data-stu-id="84402-119">For example, a search method that returns a string may not always find a match.</span></span> <span data-ttu-id="84402-120">在这种情况下，只需在搜索成功时才修改引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-120">In that case, you want to modify the reference return value only if the search is successful.</span></span>

<span data-ttu-id="84402-121">下面的 c # 示例阐释了这种情况。</span><span class="sxs-lookup"><span data-stu-id="84402-121">The following C# example illustrates this scenario.</span></span> <span data-ttu-id="84402-122">它定义了一个用 `Sentence` c # 编写的类，其中包含一个 `FindNext` 方法，该方法在以指定的子字符串开头的句子中查找下一个单词。</span><span class="sxs-lookup"><span data-stu-id="84402-122">It defines a `Sentence` class written in C# includes a `FindNext` method that finds the next word in a sentence that begins with a specified substring.</span></span> <span data-ttu-id="84402-123">该字符串作为引用返回值返回，方法引用传递的 `Boolean` 变量指示搜索是否成功。</span><span class="sxs-lookup"><span data-stu-id="84402-123">The string is returned as a reference return value, and a `Boolean` variable passed by reference to the method indicates whether the search was successful.</span></span> <span data-ttu-id="84402-124">引用返回值指示除了读取返回的值外，调用方还可以对其进行修改，并且修改会反映在类内部包含的数据中 `Sentence` 。</span><span class="sxs-lookup"><span data-stu-id="84402-124">The reference return value indicates that in addition to reading the returned value, the caller can also modify it, and that modification is reflected in the data contained internally in the `Sentence` class.</span></span>

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-returns.cs)]

<span data-ttu-id="84402-125">在这种情况下直接修改引用返回值是不可靠的，因为方法调用可能找不到匹配项，并返回句子中的第一个单词。</span><span class="sxs-lookup"><span data-stu-id="84402-125">Directly modifying the reference return value in this case is not reliable, since the method call may fail to find a match and return the first word in the sentence.</span></span> <span data-ttu-id="84402-126">在这种情况下，调用方将无意中修改句子的第一个单词。</span><span class="sxs-lookup"><span data-stu-id="84402-126">In that case, the caller will inadvertently modify the first word of the sentence.</span></span> <span data-ttu-id="84402-127">调用方可以通过返回 `null` (或 Visual Basic) 来阻止这种情况 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="84402-127">This could be prevented by the caller returning a `null` (or `Nothing` in Visual Basic).</span></span> <span data-ttu-id="84402-128">但在这种情况下，试图修改值为的字符串将 `Nothing` 引发 <xref:System.NullReferenceException> 。</span><span class="sxs-lookup"><span data-stu-id="84402-128">But in that case, attempting to modify a string whose value is `Nothing` throws a <xref:System.NullReferenceException>.</span></span> <span data-ttu-id="84402-129">如果调用方也可能会阻止返回 <xref:System.String.Empty?displayProperty=nameWithType> ，但这要求调用方定义值为的字符串变量 <xref:System.String.Empty?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="84402-129">If could also be prevented by the caller returning <xref:System.String.Empty?displayProperty=nameWithType>, but this requires that the caller define a string variable whose value is <xref:System.String.Empty?displayProperty=nameWithType>.</span></span> <span data-ttu-id="84402-130">虽然调用方可以修改该字符串，但修改本身并没有作用，因为修改后的字符串与类存储的句子中的单词无关 `Sentence` 。</span><span class="sxs-lookup"><span data-stu-id="84402-130">While the caller can modify that string, the modification itself serves no purpose, since the modified string has no relationship to the words in the sentence stored by the `Sentence` class.</span></span>

<span data-ttu-id="84402-131">处理此方案的最佳方式是通过引用向 helper 方法传递引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-131">The best way to handle this scenario is to pass the reference return value by reference to a helper method.</span></span> <span data-ttu-id="84402-132">然后，帮助器方法包含用于确定方法调用是否成功的逻辑，如果是，则修改引用返回值。</span><span class="sxs-lookup"><span data-stu-id="84402-132">The helper method then contains the logic to determine whether the method call succeeded and, if it did, to modify the reference return value.</span></span> <span data-ttu-id="84402-133">下面的示例提供了一个可能的实现。</span><span class="sxs-lookup"><span data-stu-id="84402-133">The following example provides a possible implementation.</span></span>

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-return-helper.vb#1)]

## <a name="see-also"></a><span data-ttu-id="84402-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="84402-134">See also</span></span>

- [<span data-ttu-id="84402-135">按值和按引用传递自变量</span><span class="sxs-lookup"><span data-stu-id="84402-135">Passing arguments by value and by reference</span></span>](passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="84402-136">Visual Basic 中的过程</span><span class="sxs-lookup"><span data-stu-id="84402-136">Procedures in Visual Basic</span></span>](index.md)
