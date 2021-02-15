---
description: '了解详细信息：可选参数 (Visual Basic) '
title: 可选参数
ms.date: 07/20/2015
helpviewer_keywords:
- parameters [Visual Basic], optional
- Visual Basic code, procedures
- procedures [Visual Basic], optional arguments
- optional arguments
- named arguments [Visual Basic], and optional arguments
- optional parameters
- Optional keyword [Visual Basic], optional arguments
- arguments [Visual Basic], optional
- optional arguments [Visual Basic], and named arguments
ms.assetid: 398d2845-1069-4e94-b934-a73b545c8b87
ms.openlocfilehash: 048f940f25fc05a66245e267ff23dc9845fcafdd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100436131"
---
# <a name="optional-parameters-visual-basic"></a><span data-ttu-id="0cb10-103">可选参数 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0cb10-103">Optional Parameters (Visual Basic)</span></span>

<span data-ttu-id="0cb10-104">可以指定过程参数是可选的，并且在调用过程时不必为其提供自变量。</span><span class="sxs-lookup"><span data-stu-id="0cb10-104">You can specify that a procedure parameter is optional and no argument has to be supplied for it when the procedure is called.</span></span> <span data-ttu-id="0cb10-105">*可选参数* 由 `Optional` 过程定义中的关键字指示。</span><span class="sxs-lookup"><span data-stu-id="0cb10-105">*Optional parameters* are indicated by the `Optional` keyword in the procedure definition.</span></span> <span data-ttu-id="0cb10-106">下列规则适用：</span><span class="sxs-lookup"><span data-stu-id="0cb10-106">The following rules apply:</span></span>  
  
- <span data-ttu-id="0cb10-107">过程定义中的每个可选参数都必须指定默认值。</span><span class="sxs-lookup"><span data-stu-id="0cb10-107">Every optional parameter in the procedure definition must specify a default value.</span></span>  
  
- <span data-ttu-id="0cb10-108">可选参数的默认值必须是一个常数表达式。</span><span class="sxs-lookup"><span data-stu-id="0cb10-108">The default value for an optional parameter must be a constant expression.</span></span>  
  
- <span data-ttu-id="0cb10-109">过程定义中跟在可选参数后的每个参数也都必须是可选的。</span><span class="sxs-lookup"><span data-stu-id="0cb10-109">Every parameter following an optional parameter in the procedure definition must also be optional.</span></span>  
  
 <span data-ttu-id="0cb10-110">下面的语法显示带可选参数的过程声明：</span><span class="sxs-lookup"><span data-stu-id="0cb10-110">The following syntax shows a procedure declaration with an optional parameter:</span></span>  
  
```vb  
Sub name(ByVal parameter1 As datatype1, Optional ByVal parameter2 As datatype2 = defaultvalue)  
```  
  
## <a name="calling-procedures-with-optional-parameters"></a><span data-ttu-id="0cb10-111">调用带可选参数的过程</span><span class="sxs-lookup"><span data-stu-id="0cb10-111">Calling Procedures with Optional Parameters</span></span>  

 <span data-ttu-id="0cb10-112">调用带可选参数的过程时，可以选择是否提供该自变量。</span><span class="sxs-lookup"><span data-stu-id="0cb10-112">When you call a procedure with an optional parameter, you can choose whether to supply the argument.</span></span> <span data-ttu-id="0cb10-113">如果不提供，过程将使用为该参数声明的默认值。</span><span class="sxs-lookup"><span data-stu-id="0cb10-113">If you do not, the procedure uses the default value declared for that parameter.</span></span>  
  
 <span data-ttu-id="0cb10-114">当省略自变量列表中的一个或多个可选自变量时，使用连续的逗号来标记它们的位置。</span><span class="sxs-lookup"><span data-stu-id="0cb10-114">When you omit one or more optional arguments in the argument list, you use successive commas to mark their positions.</span></span> <span data-ttu-id="0cb10-115">下面的调用示例提供了第一个和第四个自变量，省略了第二个和第三个：</span><span class="sxs-lookup"><span data-stu-id="0cb10-115">The following example call supplies the first and fourth arguments but not the second or third:</span></span>  
  
```vb  
Sub name(argument 1, , , argument 4)  
```  
  
 <span data-ttu-id="0cb10-116">下面的示例对 `MsgBox` 函数进行多次调用。</span><span class="sxs-lookup"><span data-stu-id="0cb10-116">The following example makes several calls to the `MsgBox` function.</span></span> <span data-ttu-id="0cb10-117">`MsgBox` 有一个必需参数和两个可选参数。</span><span class="sxs-lookup"><span data-stu-id="0cb10-117">`MsgBox` has one required parameter and two optional parameters.</span></span>  
  
 <span data-ttu-id="0cb10-118">对 `MsgBox` 的第一个调用将按照 `MsgBox` 定义参数的顺序提供所有三个参数。</span><span class="sxs-lookup"><span data-stu-id="0cb10-118">The first call to `MsgBox` supplies all three arguments in the order that `MsgBox` defines them.</span></span> <span data-ttu-id="0cb10-119">第二个调用仅提供必选自变量。</span><span class="sxs-lookup"><span data-stu-id="0cb10-119">The second call supplies only the required argument.</span></span> <span data-ttu-id="0cb10-120">第三个和第四个调用分别提供第一个和第三个自变量。</span><span class="sxs-lookup"><span data-stu-id="0cb10-120">The third and fourth calls supply the first and third arguments.</span></span> <span data-ttu-id="0cb10-121">第三个调用按位置提供参数，第四个调用按名称提供参数。</span><span class="sxs-lookup"><span data-stu-id="0cb10-121">The third call does this by position, and the fourth call does it by name.</span></span>  
  
 [!code-vb[VbVbcnProcedures#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#47)]  
  
## <a name="determining-whether-an-optional-argument-is-present"></a><span data-ttu-id="0cb10-122">确定可选自变量是否存在</span><span class="sxs-lookup"><span data-stu-id="0cb10-122">Determining Whether an Optional Argument Is Present</span></span>  

 <span data-ttu-id="0cb10-123">过程在运行时无法检测到给定的自变量是否已被省略，或者调用代码是否已显式提供默认值。</span><span class="sxs-lookup"><span data-stu-id="0cb10-123">A procedure cannot detect at run time whether a given argument has been omitted or the calling code has explicitly supplied the default value.</span></span> <span data-ttu-id="0cb10-124">如果需要弄清楚这一点，可以设置一个不可能的值作为默认值。</span><span class="sxs-lookup"><span data-stu-id="0cb10-124">If you need to make this distinction, you can set an unlikely value as the default.</span></span> <span data-ttu-id="0cb10-125">下面的过程定义可选参数 `office` ，并测试其默认值， `QJZ` 以确定是否在调用中省略了该参数：</span><span class="sxs-lookup"><span data-stu-id="0cb10-125">The following procedure defines the optional parameter `office`, and tests for its default value, `QJZ`, to see if it has been omitted in the call:</span></span>  
  
 [!code-vb[VbVbcnProcedures#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#46)]  
  
 <span data-ttu-id="0cb10-126">如果可选参数是像 `String` 这样的引用类型，只要它不是该自变量所预期的值，就可以使用 `Nothing` 作为默认值。</span><span class="sxs-lookup"><span data-stu-id="0cb10-126">If the optional parameter is a reference type such as a `String`, you can use `Nothing` as the default value, provided this is not an expected value for the argument.</span></span>  
  
## <a name="optional-parameters-and-overloading"></a><span data-ttu-id="0cb10-127">可选参数和重载</span><span class="sxs-lookup"><span data-stu-id="0cb10-127">Optional Parameters and Overloading</span></span>  

 <span data-ttu-id="0cb10-128">定义带可选参数的过程的另一种方法是使用重载。</span><span class="sxs-lookup"><span data-stu-id="0cb10-128">Another way to define a procedure with optional parameters is to use overloading.</span></span> <span data-ttu-id="0cb10-129">如果有一个可选参数，可以定义过程的两个重载版本，一个接受此参数，另一个则不带参数。</span><span class="sxs-lookup"><span data-stu-id="0cb10-129">If you have one optional parameter, you can define two overloaded versions of the procedure, one accepting the parameter and one without it.</span></span> <span data-ttu-id="0cb10-130">此方法随可选参数数目的增加而变得更复杂。</span><span class="sxs-lookup"><span data-stu-id="0cb10-130">This approach becomes more complicated as the number of optional parameters increases.</span></span> <span data-ttu-id="0cb10-131">然而，这样做的优点是可以完全确定调用程序是否提供了每个可选自变量。</span><span class="sxs-lookup"><span data-stu-id="0cb10-131">However, its advantage is that you can be absolutely sure whether the calling program supplied each optional argument.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0cb10-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="0cb10-132">See also</span></span>

- [<span data-ttu-id="0cb10-133">过程</span><span class="sxs-lookup"><span data-stu-id="0cb10-133">Procedures</span></span>](./index.md)
- [<span data-ttu-id="0cb10-134">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="0cb10-134">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="0cb10-135">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="0cb10-135">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="0cb10-136">按位置和按名称传递自变量</span><span class="sxs-lookup"><span data-stu-id="0cb10-136">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="0cb10-137">参数数组</span><span class="sxs-lookup"><span data-stu-id="0cb10-137">Parameter Arrays</span></span>](./parameter-arrays.md)
- [<span data-ttu-id="0cb10-138">过程重载</span><span class="sxs-lookup"><span data-stu-id="0cb10-138">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="0cb10-139">可选</span><span class="sxs-lookup"><span data-stu-id="0cb10-139">Optional</span></span>](../../../language-reference/modifiers/optional.md)
- [<span data-ttu-id="0cb10-140">ParamArray</span><span class="sxs-lookup"><span data-stu-id="0cb10-140">ParamArray</span></span>](../../../language-reference/modifiers/paramarray.md)
