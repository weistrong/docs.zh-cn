---
description: 了解详细信息： Visual Basic 中的生存期
title: 生存期
ms.date: 07/20/2015
helpviewer_keywords:
- static variables [Visual Basic], lifetime
- static variables [Visual Basic], Visual Basic
- declared elements [Visual Basic], lifetime
- Shared variable lifetime [Visual Basic]
- lifetime [Visual Basic], declared elements
- lifetime [Visual Basic], Visual Basic
- lifetime [Visual Basic]
ms.assetid: bd91e390-690a-469a-9946-8dca70bc14e7
ms.openlocfilehash: 7c95358209c61b42862f4e995d02a97dfb6e8487
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100471456"
---
# <a name="lifetime-in-visual-basic"></a><span data-ttu-id="0329b-103">Visual Basic 中的生存期</span><span class="sxs-lookup"><span data-stu-id="0329b-103">Lifetime in Visual Basic</span></span>

<span data-ttu-id="0329b-104">已声明元素的 *生存期* 是可供使用的时间段。</span><span class="sxs-lookup"><span data-stu-id="0329b-104">The *lifetime* of a declared element is the period of time during which it is available for use.</span></span> <span data-ttu-id="0329b-105">变量是具有生存期的唯一元素。</span><span class="sxs-lookup"><span data-stu-id="0329b-105">Variables are the only elements that have lifetime.</span></span> <span data-ttu-id="0329b-106">出于此目的，编译器将过程参数和函数返回视为变量的特殊情况。</span><span class="sxs-lookup"><span data-stu-id="0329b-106">For this purpose, the compiler treats procedure parameters and function returns as special cases of variables.</span></span> <span data-ttu-id="0329b-107">变量的生存期表示它可以包含一个值的时间段。</span><span class="sxs-lookup"><span data-stu-id="0329b-107">The lifetime of a variable represents the period of time during which it can hold a value.</span></span> <span data-ttu-id="0329b-108">它的值可以在其生存期内更改，但它始终保存某些值。</span><span class="sxs-lookup"><span data-stu-id="0329b-108">Its value can change over its lifetime, but it always holds some value.</span></span>  
  
## <a name="different-lifetimes"></a><span data-ttu-id="0329b-109">不同生存期</span><span class="sxs-lookup"><span data-stu-id="0329b-109">Different Lifetimes</span></span>  

 <span data-ttu-id="0329b-110">在模块级别声明的 *成员变量* (在任何过程) 通常与声明它的元素具有相同的生存期。</span><span class="sxs-lookup"><span data-stu-id="0329b-110">A *member variable* (declared at module level, outside any procedure) typically has the same lifetime as the element in which it is declared.</span></span> <span data-ttu-id="0329b-111">在类或结构中声明的非共享变量作为为其声明的类或结构的每个实例的单独副本存在。</span><span class="sxs-lookup"><span data-stu-id="0329b-111">A nonshared variable declared in a class or structure exists as a separate copy for each instance of the class or structure in which it is declared.</span></span> <span data-ttu-id="0329b-112">每个此类变量与实例的生存期相同。</span><span class="sxs-lookup"><span data-stu-id="0329b-112">Each such variable has the same lifetime as its instance.</span></span> <span data-ttu-id="0329b-113">但是， `Shared` 变量只有单个生存期，即应用程序运行时的整个生存期。</span><span class="sxs-lookup"><span data-stu-id="0329b-113">However, a `Shared` variable has only a single lifetime, which lasts for the entire time your application is running.</span></span>  
  
 <span data-ttu-id="0329b-114"> (在过程中声明的 *局部变量*) 仅在其声明过程正在运行时才存在。</span><span class="sxs-lookup"><span data-stu-id="0329b-114">A *local variable* (declared inside a procedure) exists only while the procedure in which it is declared is running.</span></span> <span data-ttu-id="0329b-115">这同样适用于该过程的参数和任何函数返回。</span><span class="sxs-lookup"><span data-stu-id="0329b-115">This applies also to that procedure's parameters and to any function return.</span></span> <span data-ttu-id="0329b-116">但是，如果该过程调用其他过程，则在调用的过程正在运行时，本地变量将保留其值。</span><span class="sxs-lookup"><span data-stu-id="0329b-116">However, if that procedure calls other procedures, the local variables retain their values while the called procedures are running.</span></span>  
  
## <a name="beginning-of-lifetime"></a><span data-ttu-id="0329b-117">生存期开头</span><span class="sxs-lookup"><span data-stu-id="0329b-117">Beginning of Lifetime</span></span>  

 <span data-ttu-id="0329b-118">当控件进入声明它的过程时，本地变量的生存期开始。</span><span class="sxs-lookup"><span data-stu-id="0329b-118">A local variable's lifetime begins when control enters the procedure in which it is declared.</span></span> <span data-ttu-id="0329b-119">当过程开始运行时，每个本地变量都将被初始化为其数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="0329b-119">Every local variable is initialized to the default value for its data type as soon as the procedure begins running.</span></span> <span data-ttu-id="0329b-120">当过程遇到 `Dim` 指定初始值的语句时，它会将这些变量设置为这些值，即使您的代码已经为它们分配了其他值。</span><span class="sxs-lookup"><span data-stu-id="0329b-120">When the procedure encounters a `Dim` statement that specifies initial values, it sets those variables to those values, even if your code had already assigned other values to them.</span></span>  
  
 <span data-ttu-id="0329b-121">结构变量的每个成员都初始化为一个单独的变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-121">Each member of a structure variable is initialized as if it were a separate variable.</span></span> <span data-ttu-id="0329b-122">同样，数组变量的每个元素都是单独初始化的。</span><span class="sxs-lookup"><span data-stu-id="0329b-122">Similarly, each element of an array variable is initialized individually.</span></span>  
  
 <span data-ttu-id="0329b-123">在过程中声明的块内声明的变量 (如 `For` 循环) 在进入过程时进行初始化。</span><span class="sxs-lookup"><span data-stu-id="0329b-123">Variables declared within a block inside a procedure (such as a `For` loop) are initialized on entry to the procedure.</span></span> <span data-ttu-id="0329b-124">无论代码是否执行块，这些初始化都将生效。</span><span class="sxs-lookup"><span data-stu-id="0329b-124">These initializations take effect whether or not your code ever executes the block.</span></span>  
  
## <a name="end-of-lifetime"></a><span data-ttu-id="0329b-125">生存期结束</span><span class="sxs-lookup"><span data-stu-id="0329b-125">End of Lifetime</span></span>  

 <span data-ttu-id="0329b-126">过程终止后，不会保留其局部变量的值，Visual Basic 将回收其内存。</span><span class="sxs-lookup"><span data-stu-id="0329b-126">When a procedure terminates, the values of its local variables are not preserved, and Visual Basic reclaims their memory.</span></span> <span data-ttu-id="0329b-127">下一次调用该过程时，将创建不用重新并重新初始化其所有局部变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-127">The next time you call the procedure, all its local variables are created afresh and reinitialized.</span></span>  
  
 <span data-ttu-id="0329b-128">当类或结构的实例终止时，其非共享变量将丢失其内存及其值。</span><span class="sxs-lookup"><span data-stu-id="0329b-128">When an instance of a class or structure terminates, its nonshared variables lose their memory and their values.</span></span> <span data-ttu-id="0329b-129">类或结构的每个新实例都创建并重新初始化其非共享变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-129">Each new instance of the class or structure creates and reinitializes its nonshared variables.</span></span> <span data-ttu-id="0329b-130">但是， `Shared` 会保留变量，直到应用程序停止运行。</span><span class="sxs-lookup"><span data-stu-id="0329b-130">However, `Shared` variables are preserved until your application stops running.</span></span>  
  
## <a name="extension-of-lifetime"></a><span data-ttu-id="0329b-131">生存期扩展</span><span class="sxs-lookup"><span data-stu-id="0329b-131">Extension of Lifetime</span></span>  

 <span data-ttu-id="0329b-132">如果使用关键字声明局部变量 `Static` ，则其生存期比其过程的执行时间长。</span><span class="sxs-lookup"><span data-stu-id="0329b-132">If you declare a local variable with the `Static` keyword, its lifetime is longer than the execution time of its procedure.</span></span> <span data-ttu-id="0329b-133">下表显示了过程声明如何确定变量存在的时间长度 `Static` 。</span><span class="sxs-lookup"><span data-stu-id="0329b-133">The following table shows how the procedure declaration determines how long a `Static` variable exists.</span></span>  
  
|<span data-ttu-id="0329b-134">过程位置和共享</span><span class="sxs-lookup"><span data-stu-id="0329b-134">Procedure location and sharing</span></span>|<span data-ttu-id="0329b-135">静态变量生存期开始</span><span class="sxs-lookup"><span data-stu-id="0329b-135">Static variable lifetime begins</span></span>|<span data-ttu-id="0329b-136">静态变量生存期结束</span><span class="sxs-lookup"><span data-stu-id="0329b-136">Static variable lifetime ends</span></span>|  
|------------------------------------|-------------------------------------|-----------------------------------|  
|<span data-ttu-id="0329b-137">默认情况下， (共享模块) </span><span class="sxs-lookup"><span data-stu-id="0329b-137">In a module (shared by default)</span></span>|<span data-ttu-id="0329b-138">第一次调用该过程时</span><span class="sxs-lookup"><span data-stu-id="0329b-138">The first time the procedure is called</span></span>|<span data-ttu-id="0329b-139">当应用程序停止运行时</span><span class="sxs-lookup"><span data-stu-id="0329b-139">When your application stops running</span></span>|  
|<span data-ttu-id="0329b-140">在类中， `Shared` (过程不是实例成员) </span><span class="sxs-lookup"><span data-stu-id="0329b-140">In a class, `Shared` (procedure is not an instance member)</span></span>|<span data-ttu-id="0329b-141">第一次在特定实例或类或结构名称本身上调用该过程</span><span class="sxs-lookup"><span data-stu-id="0329b-141">The first time the procedure is called either on a specific instance or on the class or structure name itself</span></span>|<span data-ttu-id="0329b-142">当应用程序停止运行时</span><span class="sxs-lookup"><span data-stu-id="0329b-142">When your application stops running</span></span>|  
|<span data-ttu-id="0329b-143">在类的实例中，不 `Shared` (过程是实例成员) </span><span class="sxs-lookup"><span data-stu-id="0329b-143">In an instance of a class, not `Shared` (procedure is an instance member)</span></span>|<span data-ttu-id="0329b-144">第一次在特定实例上调用该过程时</span><span class="sxs-lookup"><span data-stu-id="0329b-144">The first time the procedure is called on the specific instance</span></span>|<span data-ttu-id="0329b-145">在释放实例以进行垃圾回收 (GC) </span><span class="sxs-lookup"><span data-stu-id="0329b-145">When the instance is released for garbage collection (GC)</span></span>|  
  
## <a name="static-variables-of-the-same-name"></a><span data-ttu-id="0329b-146">具有相同名称的静态变量</span><span class="sxs-lookup"><span data-stu-id="0329b-146">Static Variables of the Same Name</span></span>  

 <span data-ttu-id="0329b-147">可以在多个过程中声明具有相同名称的静态变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-147">You can declare static variables with the same name in more than one procedure.</span></span> <span data-ttu-id="0329b-148">如果这样做，Visual Basic 编译器会将每个此类变量视为一个单独的元素。</span><span class="sxs-lookup"><span data-stu-id="0329b-148">If you do this, the Visual Basic compiler considers each such variable to be a separate element.</span></span> <span data-ttu-id="0329b-149">其中一个变量的初始化不会影响其他变量的值。</span><span class="sxs-lookup"><span data-stu-id="0329b-149">The initialization of one of these variables does not affect the values of the others.</span></span> <span data-ttu-id="0329b-150">如果使用一组重载定义过程，并在每个重载中声明一个具有相同名称的静态变量，则这一点同样适用。</span><span class="sxs-lookup"><span data-stu-id="0329b-150">The same applies if you define a procedure with a set of overloads and declare a static variable with the same name in each overload.</span></span>  
  
## <a name="containing-elements-for-static-variables"></a><span data-ttu-id="0329b-151">包含静态变量的元素</span><span class="sxs-lookup"><span data-stu-id="0329b-151">Containing Elements for Static Variables</span></span>  

 <span data-ttu-id="0329b-152">可以在类中声明静态局部变量，即在该类的过程中。</span><span class="sxs-lookup"><span data-stu-id="0329b-152">You can declare a static local variable within a class, that is, inside a procedure in that class.</span></span> <span data-ttu-id="0329b-153">但是，不能在结构中声明静态局部变量，要么作为结构成员，要么在该结构内作为过程的局部变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-153">However, you cannot declare a static local variable within a structure, either as a structure member or as a local variable of a procedure within that structure.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0329b-154">示例</span><span class="sxs-lookup"><span data-stu-id="0329b-154">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="0329b-155">说明</span><span class="sxs-lookup"><span data-stu-id="0329b-155">Description</span></span>  

 <span data-ttu-id="0329b-156">下面的示例使用 [Static](../../../language-reference/modifiers/static.md) 关键字声明一个变量。</span><span class="sxs-lookup"><span data-stu-id="0329b-156">The following example declares a variable with the [Static](../../../language-reference/modifiers/static.md) keyword.</span></span> <span data-ttu-id="0329b-157"> (注意， `Dim` [Dim 语句](../../../language-reference/statements/dim-statement.md) 使用修饰符（如）时不需要关键字 `Static` 。 ) </span><span class="sxs-lookup"><span data-stu-id="0329b-157">(Note that you do not need the `Dim` keyword when the [Dim Statement](../../../language-reference/statements/dim-statement.md) uses a modifier such as `Static`.)</span></span>  
  
### <a name="code"></a><span data-ttu-id="0329b-158">代码</span><span class="sxs-lookup"><span data-stu-id="0329b-158">Code</span></span>  

 [!code-vb[VbVbalrKeywords#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class7.vb#13)]  
  
### <a name="comments"></a><span data-ttu-id="0329b-159">注释</span><span class="sxs-lookup"><span data-stu-id="0329b-159">Comments</span></span>  

 <span data-ttu-id="0329b-160">在前面的示例中，该变量将在 `applesSold` 该过程 `runningTotal` 返回到调用代码后继续存在。</span><span class="sxs-lookup"><span data-stu-id="0329b-160">In the preceding example, the variable `applesSold` continues to exist after the procedure `runningTotal` returns to the calling code.</span></span> <span data-ttu-id="0329b-161">下次调用时 `runningTotal` ，将 `applesSold` 保留其以前计算的值。</span><span class="sxs-lookup"><span data-stu-id="0329b-161">The next time `runningTotal` is called, `applesSold` retains its previously calculated value.</span></span>  
  
 <span data-ttu-id="0329b-162">如果在未 `applesSold` 使用的情况 `Static` 下声明了，则在对的调用中不会保留以前的累计值 `runningTotal` 。</span><span class="sxs-lookup"><span data-stu-id="0329b-162">If `applesSold` had been declared without using `Static`, the previous accumulated values would not be preserved across calls to `runningTotal`.</span></span> <span data-ttu-id="0329b-163">下一次 `runningTotal` 调用时， `applesSold` 将重新创建并将其初始化为0，并 `runningTotal` 只返回与调用该值相同的值。</span><span class="sxs-lookup"><span data-stu-id="0329b-163">The next time `runningTotal` was called, `applesSold` would have been recreated and initialized to 0, and `runningTotal` would have simply returned the same value with which it was called.</span></span>  
  
### <a name="compile-the-code"></a><span data-ttu-id="0329b-164">编译代码</span><span class="sxs-lookup"><span data-stu-id="0329b-164">Compile the code</span></span>  

 <span data-ttu-id="0329b-165">您可以将静态局部变量的值初始化为其声明的一部分。</span><span class="sxs-lookup"><span data-stu-id="0329b-165">You can initialize the value of a static local variable as part of its declaration.</span></span> <span data-ttu-id="0329b-166">如果将数组声明为 `Static` ，则可以将其级别 (的维度) 、每个维度的长度以及各个元素的值进行初始化。</span><span class="sxs-lookup"><span data-stu-id="0329b-166">If you declare an array to be `Static`, you can initialize its rank (number of dimensions), the length of each dimension, and the values of the individual elements.</span></span>  
  
### <a name="security"></a><span data-ttu-id="0329b-167">安全性</span><span class="sxs-lookup"><span data-stu-id="0329b-167">Security</span></span>  

 <span data-ttu-id="0329b-168">在前面的示例中，可以通过在模块级别声明来生成相同的生存期 `applesSold` 。</span><span class="sxs-lookup"><span data-stu-id="0329b-168">In the preceding example, you can produce the same lifetime by declaring `applesSold` at module level.</span></span> <span data-ttu-id="0329b-169">但是，如果您以这种方式更改了变量的作用域，则该过程将不再具有对它的独占访问权限。</span><span class="sxs-lookup"><span data-stu-id="0329b-169">If you changed the scope of a variable this way, however, the procedure would no longer have exclusive access to it.</span></span> <span data-ttu-id="0329b-170">由于其他过程可能会访问 `applesSold` 和更改其值，因此，运行总计可能不可靠，并且代码可能更难以维护。</span><span class="sxs-lookup"><span data-stu-id="0329b-170">Because other procedures could access `applesSold` and change its value, the running total could be unreliable and the code could be more difficult to maintain.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0329b-171">请参阅</span><span class="sxs-lookup"><span data-stu-id="0329b-171">See also</span></span>

- [<span data-ttu-id="0329b-172">共享</span><span class="sxs-lookup"><span data-stu-id="0329b-172">Shared</span></span>](../../../language-reference/modifiers/shared.md)
- [<span data-ttu-id="0329b-173">无</span><span class="sxs-lookup"><span data-stu-id="0329b-173">Nothing</span></span>](../../../language-reference/nothing.md)
- [<span data-ttu-id="0329b-174">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="0329b-174">Declared Element Names</span></span>](declared-element-names.md)
- [<span data-ttu-id="0329b-175">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="0329b-175">References to Declared Elements</span></span>](references-to-declared-elements.md)
- [<span data-ttu-id="0329b-176">Visual Basic 中的范围</span><span class="sxs-lookup"><span data-stu-id="0329b-176">Scope in Visual Basic</span></span>](scope.md)
- [<span data-ttu-id="0329b-177">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="0329b-177">Access levels in Visual Basic</span></span>](access-levels.md)
- [<span data-ttu-id="0329b-178">变量</span><span class="sxs-lookup"><span data-stu-id="0329b-178">Variables</span></span>](../variables/index.md)
- [<span data-ttu-id="0329b-179">变量声明</span><span class="sxs-lookup"><span data-stu-id="0329b-179">Variable Declaration</span></span>](../variables/variable-declaration.md)
- [<span data-ttu-id="0329b-180">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="0329b-180">Troubleshooting Data Types</span></span>](../data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="0329b-181">静态</span><span class="sxs-lookup"><span data-stu-id="0329b-181">Static</span></span>](../../../language-reference/modifiers/static.md)
