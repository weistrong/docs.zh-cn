---
description: '了解详细信息：？。  ( # A1 null- (Visual Basic 的条件运算符) '
title: Null 条件运算符
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: 558b8921d0da4089505dd1035cb6039af24a2802
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665362"
---
# <a name="-and--null-conditional-operators-visual-basic"></a><span data-ttu-id="4dab0-104">?.</span><span class="sxs-lookup"><span data-stu-id="4dab0-104">?.</span></span> <span data-ttu-id="4dab0-105"> ( # A1 null- (Visual Basic 的条件运算符) </span><span class="sxs-lookup"><span data-stu-id="4dab0-105">and ?() null-conditional operators (Visual Basic)</span></span>

<span data-ttu-id="4dab0-106">测试 () 的左操作数的值， `Nothing` 然后在执行成员访问 (`?.`) 或索引 (`?()`) 操作; `Nothing` 如果左操作数的计算结果为，则返回 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-106">Tests the value of the left-hand operand for null (`Nothing`) before performing a member access (`?.`) or index (`?()`) operation; returns `Nothing` if the left-hand operand evaluates to `Nothing`.</span></span> <span data-ttu-id="4dab0-107">请注意，在通常返回值类型的表达式中，null 条件运算符将返回 <xref:System.Nullable%601> 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-107">Note that in expressions that ordinarily return value types, the null-conditional operator returns a <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="4dab0-108">这些运算符可帮助编写更少的代码来处理 null 检查，尤其是在对数据结构进行降序操作时。</span><span class="sxs-lookup"><span data-stu-id="4dab0-108">These operators help you write less code to handle null checks, especially when descending into data structures.</span></span> <span data-ttu-id="4dab0-109">例如：</span><span class="sxs-lookup"><span data-stu-id="4dab0-109">For example:</span></span>

```vb
' Nothing if customers is Nothing
Dim length As Integer? = customers?.Length

' Nothing if customers is Nothing
Dim first As Customer = customers?(0)

' Nothing if customers, the first customer, or Orders is Nothing
Dim count As Integer? = customers?(0)?.Orders?.Count()
```

<span data-ttu-id="4dab0-110">为了进行比较，这些表达式中第一个表达式的替代代码没有 null 条件运算符：</span><span class="sxs-lookup"><span data-stu-id="4dab0-110">For comparison, the alternative code for the first of these expressions without a null-conditional operator is:</span></span>

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

<span data-ttu-id="4dab0-111">有时，你需要对可能为 null 的对象执行操作，具体取决于该对象上布尔成员的值 (如下面的示例中的布尔属性 `IsAllowedFreeShipping`) ：</span><span class="sxs-lookup"><span data-stu-id="4dab0-111">Sometimes you need to take an action on an object that may be null, based on the value of a Boolean member on that object (like the Boolean property `IsAllowedFreeShipping` in the following example):</span></span>

```vb
Dim customer = FindCustomerByID(123) 'customer will be Nothing if not found.

If customer IsNot Nothing AndAlso customer.IsAllowedFreeShipping Then
  ApplyFreeShippingToOrders(customer)
End If
```

<span data-ttu-id="4dab0-112">可以通过使用 null 条件运算符来缩短代码，避免手动检查是否为 null，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4dab0-112">You can shorten your code and avoid manually checking for null by using the null-conditional operator as follows:</span></span>

```vb
Dim customer = FindCustomerByID(123) 'customer will be Nothing if not found.

If customer?.IsAllowedFreeShipping Then ApplyFreeShippingToOrders(customer)
```

<span data-ttu-id="4dab0-113">NULL 条件运算符采用最小化求值策略。</span><span class="sxs-lookup"><span data-stu-id="4dab0-113">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="4dab0-114">如果条件成员访问和索引操作链中的某个操作返回，则该 `Nothing` 链的其余执行将停止。</span><span class="sxs-lookup"><span data-stu-id="4dab0-114">If one operation in a chain of conditional member access and index operations returns `Nothing`, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="4dab0-115">在以下示例中， `C(E)` 如果 `A` 、或的 `B` `C` 计算结果为，则不会计算 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-115">In the following example, `C(E)` isn't evaluated if `A`, `B`, or `C` evaluates to `Nothing`.</span></span>

```vb
A?.B?.C?(E)
```

<span data-ttu-id="4dab0-116">Null 条件成员访问的另一个用途是使用更少的代码以线程安全的方式调用委托。</span><span class="sxs-lookup"><span data-stu-id="4dab0-116">Another use for null-conditional member access is to invoke delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="4dab0-117">下面的示例定义了两个类型： `NewsBroadcaster` 和 `NewsReceiver` 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-117">The following example defines two types, a `NewsBroadcaster` and a `NewsReceiver`.</span></span> <span data-ttu-id="4dab0-118">通过委托将新闻项发送到接收方 `NewsBroadcaster.SendNews` 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-118">News items are sent to the receiver by the `NewsBroadcaster.SendNews` delegate.</span></span>

```vb
Public Module NewsBroadcaster
   Dim SendNews As Action(Of String)

   Public Sub Main()
      Dim rec As New NewsReceiver()
      Dim rec2 As New NewsReceiver()
      SendNews?.Invoke("Just in: A newsworthy item...")
   End Sub

   Public Sub Register(client As Action(Of String))
      SendNews = SendNews.Combine({SendNews, client})
   End Sub
End Module

Public Class NewsReceiver
   Public Sub New()
      NewsBroadcaster.Register(AddressOf Me.DisplayNews)
   End Sub

   Public Sub DisplayNews(newsItem As String)
      Console.WriteLine(newsItem)
   End Sub
End Class
```

<span data-ttu-id="4dab0-119">如果调用列表中没有元素 `SendNews` ，则 `SendNews` 委托将引发 <xref:System.NullReferenceException> 。</span><span class="sxs-lookup"><span data-stu-id="4dab0-119">If there are no elements in the `SendNews` invocation list, the `SendNews` delegate throws a <xref:System.NullReferenceException>.</span></span> <span data-ttu-id="4dab0-120">在 null 条件运算符之前，如下代码确保委托调用列表不是 `Nothing` ：</span><span class="sxs-lookup"><span data-stu-id="4dab0-120">Before null conditional operators, code like the following ensured that the delegate invocation list was not `Nothing`:</span></span>

```vb
SendNews = SendNews.Combine({SendNews, client})
If SendNews IsNot Nothing Then
   SendNews("Just in...")
End If
```

<span data-ttu-id="4dab0-121">新的方法是要简单得多：</span><span class="sxs-lookup"><span data-stu-id="4dab0-121">The new way is much simpler:</span></span>

```vb
SendNews = SendNews.Combine({SendNews, client})
SendNews?.Invoke("Just in...")
```

<span data-ttu-id="4dab0-122">新方法是线程安全的，因为编译器生成的代码仅评估 `SendNews` 一次，从而使结果保持在临时变量中。</span><span class="sxs-lookup"><span data-stu-id="4dab0-122">The new way is thread-safe because the compiler generates code to evaluate `SendNews` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="4dab0-123">你需要显式调用 `Invoke` 方法，因为不存在 NULL 条件委托调用语法 `SendNews?(String)`。</span><span class="sxs-lookup"><span data-stu-id="4dab0-123">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `SendNews?(String)`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dab0-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="4dab0-124">See also</span></span>

- [<span data-ttu-id="4dab0-125">运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4dab0-125">Operators (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="4dab0-126">Visual Basic 编程指南</span><span class="sxs-lookup"><span data-stu-id="4dab0-126">Visual Basic Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="4dab0-127">Visual Basic 语言参考</span><span class="sxs-lookup"><span data-stu-id="4dab0-127">Visual Basic Language Reference</span></span>](../index.md)
