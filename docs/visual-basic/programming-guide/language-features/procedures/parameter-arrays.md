---
description: '了解详细信息： (Visual Basic 的参数数组) '
title: 参数数组
ms.date: 07/20/2015
helpviewer_keywords:
- parameter arrays [Visual Basic], about parameter arrays
- ParamArray keyword [Visual Basic], parameter arrays
- Visual Basic code, procedures
- parameters [Visual Basic], parameter arrays
- arguments [Visual Basic], parameter arrays
- procedures [Visual Basic], indefinite number of argument values
- arrays [Visual Basic], parameter arrays
ms.assetid: c43edfae-9114-4096-9ebc-8c5c957a1067
ms.openlocfilehash: e71524d9d62f0ece3a8310934eba15e9db16aaa1
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100427578"
---
# <a name="parameter-arrays-visual-basic"></a><span data-ttu-id="d81c0-103">参数数组 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d81c0-103">Parameter Arrays (Visual Basic)</span></span>

<span data-ttu-id="d81c0-104">通常，使用的参数不能比过程声明指定的过程要多。</span><span class="sxs-lookup"><span data-stu-id="d81c0-104">Usually, you cannot call a procedure with more arguments than the procedure declaration specifies.</span></span> <span data-ttu-id="d81c0-105">如果需要无数个参数，可以声明一个 *参数数组*，该数组允许过程接受参数的值数组。</span><span class="sxs-lookup"><span data-stu-id="d81c0-105">When you need an indefinite number of arguments, you can declare a *parameter array*, which allows a procedure to accept an array of values for a parameter.</span></span> <span data-ttu-id="d81c0-106">定义过程时，无需知道参数数组中的元素数目。</span><span class="sxs-lookup"><span data-stu-id="d81c0-106">You do not have to know the number of elements in the parameter array when you define the procedure.</span></span> <span data-ttu-id="d81c0-107">每次调用该过程时，都会单独确定数组大小。</span><span class="sxs-lookup"><span data-stu-id="d81c0-107">The array size is determined individually by each call to the procedure.</span></span>  
  
## <a name="declaring-a-paramarray"></a><span data-ttu-id="d81c0-108">声明 ParamArray</span><span class="sxs-lookup"><span data-stu-id="d81c0-108">Declaring a ParamArray</span></span>  

 <span data-ttu-id="d81c0-109">使用 [ParamArray](../../../language-reference/modifiers/paramarray.md) 关键字在参数列表中表示参数数组。</span><span class="sxs-lookup"><span data-stu-id="d81c0-109">You use the [ParamArray](../../../language-reference/modifiers/paramarray.md) keyword to denote a parameter array in the parameter list.</span></span> <span data-ttu-id="d81c0-110">下列规则适用：</span><span class="sxs-lookup"><span data-stu-id="d81c0-110">The following rules apply:</span></span>  
  
- <span data-ttu-id="d81c0-111">一个过程只能定义一个参数数组，并且它必须是过程定义中的最后一个参数。</span><span class="sxs-lookup"><span data-stu-id="d81c0-111">A procedure can define only one parameter array, and it must be the last parameter in the procedure definition.</span></span>  
  
- <span data-ttu-id="d81c0-112">必须通过值传递参数数组。</span><span class="sxs-lookup"><span data-stu-id="d81c0-112">The parameter array must be passed by value.</span></span> <span data-ttu-id="d81c0-113">在过程定义中显式包含 [ByVal](../../../language-reference/modifiers/byval.md) 关键字是一种很好的编程做法。</span><span class="sxs-lookup"><span data-stu-id="d81c0-113">It is good programming practice to explicitly include the [ByVal](../../../language-reference/modifiers/byval.md) keyword in the procedure definition.</span></span>  
  
- <span data-ttu-id="d81c0-114">参数数组是自动可选的。</span><span class="sxs-lookup"><span data-stu-id="d81c0-114">The parameter array is automatically optional.</span></span> <span data-ttu-id="d81c0-115">它的默认值是一个空的一维数组，它是参数数组的元素类型。</span><span class="sxs-lookup"><span data-stu-id="d81c0-115">Its default value is an empty one-dimensional array of the parameter array's element type.</span></span>  
  
- <span data-ttu-id="d81c0-116">参数数组前面的所有参数都必须是必需的。</span><span class="sxs-lookup"><span data-stu-id="d81c0-116">All parameters preceding the parameter array must be required.</span></span> <span data-ttu-id="d81c0-117">参数数组必须是唯一的可选参数。</span><span class="sxs-lookup"><span data-stu-id="d81c0-117">The parameter array must be the only optional parameter.</span></span>  
  
## <a name="calling-a-paramarray"></a><span data-ttu-id="d81c0-118">调用 ParamArray</span><span class="sxs-lookup"><span data-stu-id="d81c0-118">Calling a ParamArray</span></span>  

 <span data-ttu-id="d81c0-119">调用定义参数数组的过程时，可以通过以下方式之一提供参数：</span><span class="sxs-lookup"><span data-stu-id="d81c0-119">When you call a procedure that defines a parameter array, you can supply the argument in any one of the following ways:</span></span>  
  
- <span data-ttu-id="d81c0-120">无-也就是说，可以省略 [ParamArray](../../../language-reference/modifiers/paramarray.md) 参数。</span><span class="sxs-lookup"><span data-stu-id="d81c0-120">Nothing — that is, you can omit the [ParamArray](../../../language-reference/modifiers/paramarray.md) argument.</span></span> <span data-ttu-id="d81c0-121">在这种情况下，空数组将传递给该过程。</span><span class="sxs-lookup"><span data-stu-id="d81c0-121">In this case, an empty array is passed to the procedure.</span></span> <span data-ttu-id="d81c0-122">如果显式传递 [Nothing](../../../language-reference/nothing.md) 关键字，则空数组将传递给该过程，并且如果被调用的过程不检查此条件，则可能导致 NullReferenceException。</span><span class="sxs-lookup"><span data-stu-id="d81c0-122">If you explicitly pass the [Nothing](../../../language-reference/nothing.md) keyword, a null array is passed to the procedure and may result in a NullReferenceException if the called procedure does not check for this condition.</span></span>
  
- <span data-ttu-id="d81c0-123">任意数量的参数的列表（用逗号分隔）。</span><span class="sxs-lookup"><span data-stu-id="d81c0-123">A list of an arbitrary number of arguments, separated by commas.</span></span> <span data-ttu-id="d81c0-124">每个参数的数据类型必须可隐式转换为 `ParamArray` 元素类型。</span><span class="sxs-lookup"><span data-stu-id="d81c0-124">The data type of each argument must be implicitly convertible to the `ParamArray` element type.</span></span>  
  
- <span data-ttu-id="d81c0-125">元素类型与参数数组的元素类型相同的数组。</span><span class="sxs-lookup"><span data-stu-id="d81c0-125">An array with the same element type as the parameter array's element type.</span></span>  
  
 <span data-ttu-id="d81c0-126">在所有情况下，该过程中的代码将参数数组视为一维数组，其元素的数据类型与 `ParamArray` 数据类型相同。</span><span class="sxs-lookup"><span data-stu-id="d81c0-126">In all cases, the code within the procedure treats the parameter array as a one-dimensional array with elements of the same data type as the `ParamArray` data type.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="d81c0-127">无论何时处理可能会无限大的阵列，都有 overrunning 应用程序的一些内部容量的风险。</span><span class="sxs-lookup"><span data-stu-id="d81c0-127">Whenever you deal with an array which can be indefinitely large, there is a risk of overrunning some internal capacity of your application.</span></span> <span data-ttu-id="d81c0-128">如果接受参数数组，则应测试调用代码传递给它的数组大小。</span><span class="sxs-lookup"><span data-stu-id="d81c0-128">If you accept a parameter array, you should test for the size of the array that the calling code passed to it.</span></span> <span data-ttu-id="d81c0-129">如果对应用程序来说太大，请采取适当的措施。</span><span class="sxs-lookup"><span data-stu-id="d81c0-129">Take appropriate steps if it is too large for your application.</span></span> <span data-ttu-id="d81c0-130">有关详细信息，请参阅 [array](../arrays/index.md)。</span><span class="sxs-lookup"><span data-stu-id="d81c0-130">For more information, see [Arrays](../arrays/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d81c0-131">示例</span><span class="sxs-lookup"><span data-stu-id="d81c0-131">Example</span></span>  

 <span data-ttu-id="d81c0-132">下面的示例定义并调用函数 `calcSum` 。</span><span class="sxs-lookup"><span data-stu-id="d81c0-132">The following example defines and calls the function `calcSum`.</span></span> <span data-ttu-id="d81c0-133">`ParamArray`参数的修饰符 `args` 使函数接受数量可变的参数。</span><span class="sxs-lookup"><span data-stu-id="d81c0-133">The `ParamArray` modifier for the parameter `args` enables the function to accept a variable number of arguments.</span></span>  
  
 [!code-vb[VbVbalrStatements#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#26)]  
  
 <span data-ttu-id="d81c0-134">下面的示例使用参数数组定义过程，并输出传递给参数数组的所有数组元素的值。</span><span class="sxs-lookup"><span data-stu-id="d81c0-134">The following example defines a procedure with a parameter array, and outputs the values of all the array elements passed to the parameter array.</span></span>  
  
 [!code-vb[VbVbcnProcedures#48](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#48)]  
  
 [!code-vb[VbVbcnProcedures#49](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#49)]  
  
## <a name="see-also"></a><span data-ttu-id="d81c0-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="d81c0-135">See also</span></span>

- <xref:Microsoft.VisualBasic.Information.UBound%2A>
- [<span data-ttu-id="d81c0-136">过程</span><span class="sxs-lookup"><span data-stu-id="d81c0-136">Procedures</span></span>](./index.md)
- [<span data-ttu-id="d81c0-137">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="d81c0-137">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="d81c0-138">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="d81c0-138">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="d81c0-139">按位置和按名称传递自变量</span><span class="sxs-lookup"><span data-stu-id="d81c0-139">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="d81c0-140">可选参数</span><span class="sxs-lookup"><span data-stu-id="d81c0-140">Optional Parameters</span></span>](./optional-parameters.md)
- [<span data-ttu-id="d81c0-141">过程重载</span><span class="sxs-lookup"><span data-stu-id="d81c0-141">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="d81c0-142">数组</span><span class="sxs-lookup"><span data-stu-id="d81c0-142">Arrays</span></span>](../arrays/index.md)
- [<span data-ttu-id="d81c0-143">可选</span><span class="sxs-lookup"><span data-stu-id="d81c0-143">Optional</span></span>](../../../language-reference/modifiers/optional.md)
