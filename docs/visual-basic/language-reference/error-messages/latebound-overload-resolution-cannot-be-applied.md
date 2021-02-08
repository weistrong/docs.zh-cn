---
description: 了解有关以下内容的详细信息： BC30933：后期绑定重载决策不能应用于 " <procedurename> "，因为访问实例是一个接口类型
title: 后期绑定重载决策不能应用于“<procedurename>”，因为访问实例是一个接口类型
ms.date: 07/20/2015
f1_keywords:
- vbc30933
- bc30933
helpviewer_keywords:
- overload resolution [Visual Basic], with late-bound argument
- BC30933
ms.assetid: 8182eea0-dd34-4d6e-9ca0-41d8713e9dc4
ms.openlocfilehash: 3002232c953fa21a10de944bc61e2f0c448ae4fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795906"
---
# <a name="bc30933-latebound-overload-resolution-cannot-be-applied-to-procedurename-because-the-accessing-instance-is-an-interface-type"></a><span data-ttu-id="2bffc-103">BC30933：后期绑定重载决策不能应用于 " \<procedurename> "，因为访问实例是一个接口类型</span><span class="sxs-lookup"><span data-stu-id="2bffc-103">BC30933: Latebound overload resolution cannot be applied to '\<procedurename>' because the accessing instance is an interface type</span></span>

<span data-ttu-id="2bffc-104">编译器尝试解析对重载属性或过程的引用，但引用失败，因为参数的类型为 `Object` ，而引用对象具有接口的数据类型。</span><span class="sxs-lookup"><span data-stu-id="2bffc-104">The compiler is attempting to resolve a reference to an overloaded property or procedure, but the reference fails because an argument is of type `Object` and the referring object has the data type of an interface.</span></span> <span data-ttu-id="2bffc-105">`Object`参数强制编译器将引用解析为晚期绑定。</span><span class="sxs-lookup"><span data-stu-id="2bffc-105">The `Object` argument forces the compiler to resolve the reference as late-bound.</span></span>

<span data-ttu-id="2bffc-106">在这些情况下，编译器通过实现类解析重载，而不是通过基础接口解析。</span><span class="sxs-lookup"><span data-stu-id="2bffc-106">In these circumstances, the compiler resolves the overload through the implementing class instead of through the underlying interface.</span></span> <span data-ttu-id="2bffc-107">如果类重命名其中一个重载版本，则编译器不会将该版本视为重载，因为其名称不同。</span><span class="sxs-lookup"><span data-stu-id="2bffc-107">If the class renames one of the overloaded versions, the compiler does not consider that version to be an overload because its name is different.</span></span> <span data-ttu-id="2bffc-108">这进而导致编译器忽略重命名的版本，因为它可能是解析引用的正确选择。</span><span class="sxs-lookup"><span data-stu-id="2bffc-108">This in turn causes the compiler to ignore the renamed version when it might have been the correct choice to resolve the reference.</span></span>

<span data-ttu-id="2bffc-109">**错误 ID：** BC30933</span><span class="sxs-lookup"><span data-stu-id="2bffc-109">**Error ID:** BC30933</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="2bffc-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2bffc-110">To correct this error</span></span>

- <span data-ttu-id="2bffc-111">使用 `CType` 将参数从强制转换 `Object` 为你要调用的重载的签名所指定的类型。</span><span class="sxs-lookup"><span data-stu-id="2bffc-111">Use `CType` to cast the argument from `Object` to the type specified by the signature of the overload you want to call.</span></span>

  <span data-ttu-id="2bffc-112">请注意，它不会帮助将引用对象强制转换为基础接口。</span><span class="sxs-lookup"><span data-stu-id="2bffc-112">Note that it does not help to cast the referring object to the underlying interface.</span></span> <span data-ttu-id="2bffc-113">必须强制转换参数以避免此错误。</span><span class="sxs-lookup"><span data-stu-id="2bffc-113">You must cast the argument to avoid this error.</span></span>

## <a name="example"></a><span data-ttu-id="2bffc-114">示例</span><span class="sxs-lookup"><span data-stu-id="2bffc-114">Example</span></span>

<span data-ttu-id="2bffc-115">下面的示例演示对重载 `Sub` 过程的调用，该过程在编译时导致此错误。</span><span class="sxs-lookup"><span data-stu-id="2bffc-115">The following example shows a call to an overloaded `Sub` procedure that causes this error at compile time.</span></span>

```vb
Module m1
    Interface i1
        Sub s1(ByVal p1 As Integer)
        Sub s1(ByVal p1 As Double)
    End Interface
    Class c1
        Implements i1
        Public Overloads Sub s1(ByVal p1 As Integer) Implements i1.s1
        End Sub
        Public Overloads Sub s2(ByVal p1 As Double) Implements i1.s1
        End Sub
    End Class
    Sub Main()
        Dim refer As i1 = New c1
        Dim o1 As Object = 3.1415
        ' The following reference is INVALID and causes a compiler error.
        refer.s1(o1)
    End Sub
End Module
```

<span data-ttu-id="2bffc-116">在前面的示例中，如果编译器允许调用编写的 `s1` ，则通过类 `c1` 而不是接口进行解析 `i1` 。</span><span class="sxs-lookup"><span data-stu-id="2bffc-116">In the preceding example, if the compiler allowed the call to `s1` as written, the resolution would take place through the class `c1` instead of the interface `i1`.</span></span> <span data-ttu-id="2bffc-117">这意味着编译器不会考虑 `s2` ，因为它的名称在中是不同的 `c1` ，即使它是定义的正确选择 `i1` 。</span><span class="sxs-lookup"><span data-stu-id="2bffc-117">This would mean that the compiler would not consider `s2` because its name is different in `c1`, even though it is the correct choice as defined by `i1`.</span></span>

<span data-ttu-id="2bffc-118">可以通过将调用更改为以下代码行之一来更正此错误：</span><span class="sxs-lookup"><span data-stu-id="2bffc-118">You can correct the error by changing the call to either of the following lines of code:</span></span>

```vb
refer.s1(CType(o1, Integer))
refer.s1(CType(o1, Double))
```

<span data-ttu-id="2bffc-119">前面的每个代码行显式将变量强制 `Object` 转换 `o1` 为为重载定义的参数类型之一。</span><span class="sxs-lookup"><span data-stu-id="2bffc-119">Each of the preceding lines of code explicitly casts the `Object` variable `o1` to one of the parameter types defined for the overloads.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bffc-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="2bffc-120">See also</span></span>

- [<span data-ttu-id="2bffc-121">过程重载</span><span class="sxs-lookup"><span data-stu-id="2bffc-121">Procedure Overloading</span></span>](../../programming-guide/language-features/procedures/procedure-overloading.md)
- [<span data-ttu-id="2bffc-122">重载决策</span><span class="sxs-lookup"><span data-stu-id="2bffc-122">Overload Resolution</span></span>](../../programming-guide/language-features/procedures/overload-resolution.md)
- [<span data-ttu-id="2bffc-123">CType Function</span><span class="sxs-lookup"><span data-stu-id="2bffc-123">CType Function</span></span>](../functions/ctype-function.md)
