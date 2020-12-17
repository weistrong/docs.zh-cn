---
title: 编译器生成的异常 - C# 编程指南
description: 了解编译器生成的异常。 查看自动引发的异常及其错误情况的列表。
ms.date: 12/09/2020
helpviewer_keywords:
- exceptions [C#], compiler-generated
ms.assetid: 53b52f97-b366-4ed7-b05b-9eb78096b7f9
ms.openlocfilehash: 43bacbb1025bc0af3a5f21979315b3d1b0d61066
ms.sourcegitcommit: 9b877e160c326577e8aa5ead22a937110d80fa44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97110346"
---
# <a name="compiler-generated-exceptions-c-programming-guide"></a><span data-ttu-id="00ced-104">编译器生成的异常（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="00ced-104">Compiler-Generated Exceptions (C# Programming Guide)</span></span>

<span data-ttu-id="00ced-105">当基本操作失败时，.NET 运行时会自动引发一些异常。</span><span class="sxs-lookup"><span data-stu-id="00ced-105">Some exceptions are thrown automatically by the .NET runtime when basic operations fail.</span></span> <span data-ttu-id="00ced-106">这些异常及其错误条件在下表中列出。</span><span class="sxs-lookup"><span data-stu-id="00ced-106">These exceptions and their error conditions are listed in the following table.</span></span>

|<span data-ttu-id="00ced-107">例外</span><span class="sxs-lookup"><span data-stu-id="00ced-107">Exception</span></span>|<span data-ttu-id="00ced-108">描述</span><span class="sxs-lookup"><span data-stu-id="00ced-108">Description</span></span>|
|---------------|-----------------|
|<xref:System.ArithmeticException>|<span data-ttu-id="00ced-109">算术运算期间出现的异常的基类，例如 <xref:System.DivideByZeroException> 和 <xref:System.OverflowException>。</span><span class="sxs-lookup"><span data-stu-id="00ced-109">A base class for exceptions that occur during arithmetic operations, such as <xref:System.DivideByZeroException> and <xref:System.OverflowException>.</span></span>|
|<xref:System.ArrayTypeMismatchException>|<span data-ttu-id="00ced-110">由于元素的实际类型与数组的实际类型不兼容而导致数组无法存储给定元素时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-110">Thrown when an array can't store a given element because the actual type of the element is incompatible with the actual type of the array.</span></span>|
|<xref:System.DivideByZeroException>|<span data-ttu-id="00ced-111">尝试将整数值除以零时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-111">Thrown when an attempt is made to divide an integral value by zero.</span></span>|
|<xref:System.IndexOutOfRangeException>|<span data-ttu-id="00ced-112">索引小于零或超出数组边界时，尝试对数组编制索引时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-112">Thrown when an attempt is made to index an array when the index is less than zero or outside the bounds of the array.</span></span>|
|<xref:System.InvalidCastException>|<span data-ttu-id="00ced-113">从基类型显式转换为接口或派生类型在运行时失败时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-113">Thrown when an explicit conversion from a base type to an interface or to a derived type fails at runtime.</span></span>|
|<xref:System.NullReferenceException>|<span data-ttu-id="00ced-114">尝试引用值为 [null](../../language-reference/keywords/null.md) 的对象时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-114">Thrown when an attempt is made to reference an object whose value is [null](../../language-reference/keywords/null.md).</span></span>|
|<xref:System.OutOfMemoryException>|<span data-ttu-id="00ced-115">尝试使用[新](../../language-reference/operators/new-operator.md)运算符分配内存失败时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-115">Thrown when an attempt to allocate memory using the [new](../../language-reference/operators/new-operator.md) operator fails.</span></span> <span data-ttu-id="00ced-116">此异常表示可用于公共语言运行时的内存已用尽。</span><span class="sxs-lookup"><span data-stu-id="00ced-116">This exception indicates that the memory available to the common language runtime has been exhausted.</span></span>|
|<xref:System.OverflowException>|<span data-ttu-id="00ced-117">`checked` 上下文中的算术运算溢出时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-117">Thrown when an arithmetic operation in a `checked` context overflows.</span></span>|
|<xref:System.StackOverflowException>|<span data-ttu-id="00ced-118">执行堆栈由于有过多挂起的方法调用而用尽时引发；通常表示非常深的递归或无限递归。</span><span class="sxs-lookup"><span data-stu-id="00ced-118">Thrown when the execution stack is exhausted by having too many pending method calls; usually indicates a very deep or infinite recursion.</span></span>|
|<xref:System.TypeInitializationException>|<span data-ttu-id="00ced-119">静态构造函数引发异常并且没有兼容的 `catch` 子句来捕获异常时引发。</span><span class="sxs-lookup"><span data-stu-id="00ced-119">Thrown when a static constructor throws an exception and no compatible `catch` clause exists to catch it.</span></span>|

## <a name="see-also"></a><span data-ttu-id="00ced-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="00ced-120">See also</span></span>

- [<span data-ttu-id="00ced-121">try-catch</span><span class="sxs-lookup"><span data-stu-id="00ced-121">try-catch</span></span>](../../language-reference/keywords/try-catch.md)
- [<span data-ttu-id="00ced-122">try-finally</span><span class="sxs-lookup"><span data-stu-id="00ced-122">try-finally</span></span>](../../language-reference/keywords/try-finally.md)
- [<span data-ttu-id="00ced-123">try-catch-finally</span><span class="sxs-lookup"><span data-stu-id="00ced-123">try-catch-finally</span></span>](../../language-reference/keywords/try-catch-finally.md)
