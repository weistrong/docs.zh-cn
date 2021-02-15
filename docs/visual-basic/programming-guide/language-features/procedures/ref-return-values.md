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
# <a name="support-for-reference-return-values-visual-basic"></a>支持 (Visual Basic 的引用返回值) 

从 c # 7.0 开始，c # 语言支持 *引用返回值*。 了解引用返回值的一种方法是，它们与通过引用传递给方法的参数相反。 当修改通过引用传递的参数时，所做的更改将反映在调用方上的变量值中。 当方法为调用方提供引用返回值时，调用方对引用返回值所做的修改会反映在被调用方法的数据中。

Visual Basic 不允许使用引用返回值创作方法，但允许使用引用返回值。 换言之，您可以调用具有引用返回值的方法并修改该返回值，对引用返回值所做的更改将反映在被调用方法的数据中。

## <a name="modifying-the-ref-return-value-directly"></a>直接修改引用返回值

对于始终成功并且没有参数的方法 `ByRef` ，您可以直接修改引用返回值。 为此，可将新值分配给返回引用返回值的表达式。

下面的 c # 示例定义一个 `NumericValue.IncrementValue` 方法，该方法递增内部值并将其作为引用返回值返回。

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/ref-returns1.cs)]

然后，调用方在下面 Visual Basic 示例中修改引用返回值。 请注意，具有 `NumericValue.IncrementValue` 方法调用的行不会向方法分配值。 相反，它将值赋给方法返回的引用返回值。

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/use-ref-returns1.vb)]

## <a name="using-a-helper-method"></a>使用 helper 方法

在其他情况下，可能不会始终需要直接修改方法调用的引用返回值。 例如，返回字符串的搜索方法可能并不总是找到匹配项。 在这种情况下，只需在搜索成功时才修改引用返回值。

下面的 c # 示例阐释了这种情况。 它定义了一个用 `Sentence` c # 编写的类，其中包含一个 `FindNext` 方法，该方法在以指定的子字符串开头的句子中查找下一个单词。 该字符串作为引用返回值返回，方法引用传递的 `Boolean` 变量指示搜索是否成功。 引用返回值指示除了读取返回的值外，调用方还可以对其进行修改，并且修改会反映在类内部包含的数据中 `Sentence` 。

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-returns.cs)]

在这种情况下直接修改引用返回值是不可靠的，因为方法调用可能找不到匹配项，并返回句子中的第一个单词。 在这种情况下，调用方将无意中修改句子的第一个单词。 调用方可以通过返回 `null` (或 Visual Basic) 来阻止这种情况 `Nothing` 。 但在这种情况下，试图修改值为的字符串将 `Nothing` 引发 <xref:System.NullReferenceException> 。 如果调用方也可能会阻止返回 <xref:System.String.Empty?displayProperty=nameWithType> ，但这要求调用方定义值为的字符串变量 <xref:System.String.Empty?displayProperty=nameWithType> 。 虽然调用方可以修改该字符串，但修改本身并没有作用，因为修改后的字符串与类存储的句子中的单词无关 `Sentence` 。

处理此方案的最佳方式是通过引用向 helper 方法传递引用返回值。 然后，帮助器方法包含用于确定方法调用是否成功的逻辑，如果是，则修改引用返回值。 下面的示例提供了一个可能的实现。

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-return-helper.vb#1)]

## <a name="see-also"></a>请参阅

- [按值和按引用传递自变量](passing-arguments-by-value-and-by-reference.md)
- [Visual Basic 中的过程](index.md)
