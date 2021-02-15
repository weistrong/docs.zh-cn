---
description: '了解详细信息：参数和参数之间的差异 (Visual Basic) '
title: 形参和实参之间的差异
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- parameters [Visual Basic], and arguments
- procedure arguments
- Visual Basic code, procedures
- arguments [Visual Basic], and parameters
- procedure parameters
- parameters [Visual Basic], definition
ms.assetid: c237c056-74f4-4749-9f2c-15864f139a31
ms.openlocfilehash: 01efc7dc3f451d6aae20cfd091355f531af4431c
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100438757"
---
# <a name="differences-between-parameters-and-arguments-visual-basic"></a><span data-ttu-id="6c3ad-103">参数和变量之间的差异 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6c3ad-103">Differences Between Parameters and Arguments (Visual Basic)</span></span>

<span data-ttu-id="6c3ad-104">在大多数情况下，过程必须具有有关在其中调用该过程的环境的一些信息。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-104">In most cases, a procedure must have some information about the circumstances in which it has been called.</span></span> <span data-ttu-id="6c3ad-105">执行重复或共享任务的过程对每个调用使用不同的信息。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-105">A procedure that performs repeated or shared tasks uses different information for each call.</span></span> <span data-ttu-id="6c3ad-106">此信息包含变量、常量和在您调用过程时传递给该过程的表达式。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-106">This information consists of variables, constants, and expressions that you pass to the procedure when you call it.</span></span>  
  
 <span data-ttu-id="6c3ad-107">若要将此信息传递给过程，过程定义了一个 *参数*，并且调用代码将 *参数* 传递给该参数。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-107">To communicate this information to the procedure, the procedure defines a *parameter*, and the calling code passes an *argument* to that parameter.</span></span> <span data-ttu-id="6c3ad-108">可以将参数视为停车空间，将参数视为汽车。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-108">You can think of the parameter as a parking space and the argument as an automobile.</span></span> <span data-ttu-id="6c3ad-109">正如不同的汽车可以在不同时间的停车空间中停放一样，每次调用该过程时，调用代码都可以将不同的参数传递给相同的参数。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-109">Just as different automobiles can park in a parking space at different times, the calling code can pass a different argument to the same parameter every time that it calls the procedure.</span></span>  
  
## <a name="parameters"></a><span data-ttu-id="6c3ad-110">parameters</span><span class="sxs-lookup"><span data-stu-id="6c3ad-110">Parameters</span></span>  

 <span data-ttu-id="6c3ad-111">*参数* 表示一个值，在调用该过程时，该过程要求您传递该值。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-111">A *parameter* represents a value that the procedure expects you to pass when you call it.</span></span> <span data-ttu-id="6c3ad-112">过程声明定义了其参数。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-112">The procedure's declaration defines its parameters.</span></span>  
  
 <span data-ttu-id="6c3ad-113">在定义 `Function` 或过程时 `Sub` ，请在紧跟在过程名称后面的括号中指定 *参数列表* 。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-113">When you define a `Function` or `Sub` procedure, you specify a *parameter list* in parentheses immediately following the procedure name.</span></span> <span data-ttu-id="6c3ad-114">对于每个参数，请指定名称、数据类型和传递机制 ([ByVal](../../../language-reference/modifiers/byval.md) 或 [ByRef](../../../language-reference/modifiers/byref.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-114">For each parameter, you specify a name, a data type, and a passing mechanism ([ByVal](../../../language-reference/modifiers/byval.md) or [ByRef](../../../language-reference/modifiers/byref.md)).</span></span> <span data-ttu-id="6c3ad-115">还可以指示参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-115">You can also indicate that a parameter is optional.</span></span> <span data-ttu-id="6c3ad-116">这意味着，调用代码不必为其传递值。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-116">This means that the calling code does not have to pass a value for it.</span></span>  
  
 <span data-ttu-id="6c3ad-117">每个参数的名称作为过程中的 *局部变量* 。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-117">The name of each parameter serves as a *local variable* in the procedure.</span></span> <span data-ttu-id="6c3ad-118">使用参数名称的方式与使用任何其他变量的方式相同。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-118">You use the parameter name the same way you use any other variable.</span></span>  
  
## <a name="arguments"></a><span data-ttu-id="6c3ad-119">参数</span><span class="sxs-lookup"><span data-stu-id="6c3ad-119">Arguments</span></span>  

 <span data-ttu-id="6c3ad-120">*参数* 表示在调用过程时传递给过程参数的值。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-120">An *argument* represents the value that you pass to a procedure parameter when you call the procedure.</span></span> <span data-ttu-id="6c3ad-121">调用代码在调用过程时提供自变量。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-121">The calling code supplies the arguments when it calls the procedure.</span></span>  
  
 <span data-ttu-id="6c3ad-122">调用 `Function` 或 `Sub` 过程时，将在紧跟过程名称的括号中包含 *参数列表* 。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-122">When you call a `Function` or `Sub` procedure, you include an *argument list* in parentheses immediately following the procedure name.</span></span> <span data-ttu-id="6c3ad-123">每个参数都对应于列表中同一位置的参数。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-123">Each argument corresponds to the parameter in the same position in the list.</span></span>  
  
 <span data-ttu-id="6c3ad-124">与参数定义不同，参数没有名称。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-124">In contrast to parameter definition, arguments do not have names.</span></span> <span data-ttu-id="6c3ad-125">每个自变量都是一个表达式，它可以包含零个或多个变量、常量和文本。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-125">Each argument is an expression, which can contain zero or more variables, constants, and literals.</span></span> <span data-ttu-id="6c3ad-126">计算表达式的数据类型通常应与为相应参数定义的数据类型匹配，在任何情况下，它都必须可以转换为参数类型。</span><span class="sxs-lookup"><span data-stu-id="6c3ad-126">The data type of the evaluated expression should typically match the data type defined for the corresponding parameter, and in any case it must be convertible to the parameter type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c3ad-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c3ad-127">See also</span></span>

- [<span data-ttu-id="6c3ad-128">过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-128">Procedures</span></span>](./index.md)
- [<span data-ttu-id="6c3ad-129">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-129">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="6c3ad-130">Function 过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-130">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="6c3ad-131">Property 过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-131">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="6c3ad-132">运算符过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-132">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="6c3ad-133">如何：为过程定义参数</span><span class="sxs-lookup"><span data-stu-id="6c3ad-133">How to: Define a Parameter for a Procedure</span></span>](./how-to-define-a-parameter-for-a-procedure.md)
- [<span data-ttu-id="6c3ad-134">如何：将参数传递给过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-134">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="6c3ad-135">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="6c3ad-135">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="6c3ad-136">递归过程</span><span class="sxs-lookup"><span data-stu-id="6c3ad-136">Recursive Procedures</span></span>](./recursive-procedures.md)
- [<span data-ttu-id="6c3ad-137">过程重载</span><span class="sxs-lookup"><span data-stu-id="6c3ad-137">Procedure Overloading</span></span>](./procedure-overloading.md)
