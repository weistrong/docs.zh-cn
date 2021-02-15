---
description: '了解详细信息：如何：声明常量 (Visual Basic) '
title: 如何：声明常量
ms.date: 07/20/2015
f1_keywords:
- vb.constant
helpviewer_keywords:
- Integer data type [Visual Basic], declaring constants
- Single data type [Visual Basic], declaring constants
- Const statement [Visual Basic], declaring constants
- procedures [Visual Basic], declaration
- data types [Visual Basic], constants
- Long data type [Visual Basic], declaring constants
- Visual Basic code, declaring variables and constants
- Double data type [Visual Basic], declaring constants
- Boolean data type [Visual Basic], declaring constants
- modules, declaring constants
- Byte data type [Visual Basic], declaring constants
- constants [Visual Basic], declaring
- Date data type [Visual Basic], declaring constants
- String data type [Visual Basic], declaring constants
- declaring constants [Visual Basic], const keyword
- Currency data type [Visual Basic], declaring constants and variants
- module-level constants and variables
- Object data type [Visual Basic], declaring constants
ms.assetid: f901b4fa-481f-4621-822e-427060577ad1
ms.openlocfilehash: 42b0ecce90e12a7e777b8e51bc9a23ab454f433d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100477497"
---
# <a name="how-to-declare-a-constant-visual-basic"></a><span data-ttu-id="b44d1-103">如何：声明常量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b44d1-103">How to: Declare A Constant (Visual Basic)</span></span>

<span data-ttu-id="b44d1-104">使用 `Const` 语句声明一个常数并设置其值。</span><span class="sxs-lookup"><span data-stu-id="b44d1-104">You use the `Const` statement to declare a constant and set its value.</span></span> <span data-ttu-id="b44d1-105">通过声明常量，可为一个值指定一个有意义的名称。</span><span class="sxs-lookup"><span data-stu-id="b44d1-105">By declaring a constant, you assign a meaningful name to a value.</span></span> <span data-ttu-id="b44d1-106">声明常量后，不能对其进行修改或赋予新值。</span><span class="sxs-lookup"><span data-stu-id="b44d1-106">Once a constant is declared, it cannot be modified or assigned a new value.</span></span>  
  
 <span data-ttu-id="b44d1-107">您可以在过程中或模块、类或结构的声明部分中声明常数。</span><span class="sxs-lookup"><span data-stu-id="b44d1-107">You declare a constant within a procedure or in the declarations section of a module, class, or structure.</span></span> <span data-ttu-id="b44d1-108">默认情况下，类或结构级别常量为， `Private` 但也可以将声明为 `Public` 、 `Friend` 、 `Protected` 或 `Protected Friend` 以用于适当级别的代码访问。</span><span class="sxs-lookup"><span data-stu-id="b44d1-108">Class or structure-level constants are `Private` by default, but may also be declared as `Public`, `Friend`, `Protected`, or `Protected Friend` for the appropriate level of code access.</span></span>  
  
 <span data-ttu-id="b44d1-109">常数必须具有有效的符号名称， (规则与用于创建变量名称的规则相同) 和 (但不) 函数调用的表达式。</span><span class="sxs-lookup"><span data-stu-id="b44d1-109">The constant must have a valid symbolic name (the rules are the same as those for creating variable names) and an expression composed of numeric or string constants and operators (but no function calls).</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-declare-a-constant"></a><span data-ttu-id="b44d1-110">声明常量</span><span class="sxs-lookup"><span data-stu-id="b44d1-110">To declare a constant</span></span>  
  
- <span data-ttu-id="b44d1-111">编写包含访问说明符、 `Const` 关键字和表达式的声明，如下面的示例所示：</span><span class="sxs-lookup"><span data-stu-id="b44d1-111">Write a declaration that includes an access specifier, the `Const` keyword, and an expression, as in the following examples:</span></span>  
  
     [!code-vb[VbEnumsTask#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#8)]  
  
     <span data-ttu-id="b44d1-112">如果 [选项推断](../../../language-reference/statements/option-infer-statement.md) 为， `Off` 且 [option Strict](../../../language-reference/statements/option-strict-statement.md) 为 `On` ，则必须通过指定数据类型 (、、、、、、、、、 `Boolean` `Byte` `Char` `DateTime` `Decimal` `Double` `Integer` `Long` `Short` `Single` 或 `String`) 来显式声明常量。</span><span class="sxs-lookup"><span data-stu-id="b44d1-112">When [Option Infer](../../../language-reference/statements/option-infer-statement.md) is `Off` and [Option Strict](../../../language-reference/statements/option-strict-statement.md) is `On`, you must declare a constant explicitly by specifying a data type (`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single`, or `String`).</span></span>  
  
     <span data-ttu-id="b44d1-113">当 `Option Infer` 为 `On` 或 `Option Strict` 时 `Off` ，可以声明常量，而无需使用子句指定数据类型 `As` 。</span><span class="sxs-lookup"><span data-stu-id="b44d1-113">When `Option Infer` is `On` or `Option Strict` is `Off`, you can declare a constant without specifying a data type with an `As` clause.</span></span> <span data-ttu-id="b44d1-114">编译器将确定表达式的类型的常量类型。</span><span class="sxs-lookup"><span data-stu-id="b44d1-114">The compiler determines the type of the constant from the type of the expression.</span></span> <span data-ttu-id="b44d1-115">有关详细信息，请参阅 [常量和文本数据类型](constant-and-literal-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b44d1-115">For more information, see [Constant and Literal Data Types](constant-and-literal-data-types.md).</span></span>  
  
### <a name="to-declare-a-constant-that-has-an-explicitly-stated-data-type"></a><span data-ttu-id="b44d1-116">声明具有显式声明的数据类型的常数</span><span class="sxs-lookup"><span data-stu-id="b44d1-116">To declare a constant that has an explicitly stated data type</span></span>  
  
- <span data-ttu-id="b44d1-117">编写包含 `As` 关键字和显式数据类型的声明，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="b44d1-117">Write a declaration that includes the `As` keyword and an explicit data type, as in the following examples:</span></span>  
  
     [!code-vb[VbEnumsTask#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#9)]  
  
     <span data-ttu-id="b44d1-118">可以在单个行上声明多个常数，不过，如果每行只声明一个常数，代码的可读性就会更高。</span><span class="sxs-lookup"><span data-stu-id="b44d1-118">You can declare multiple constants on a single line, although your code is more readable if you declare only a single constant per line.</span></span> <span data-ttu-id="b44d1-119">如果在单个行上声明多个常量，它们必须具有相同的访问级别 (`Public` 、 `Private` 、、 `Friend` `Protected` 或 `Protected Friend`) 。</span><span class="sxs-lookup"><span data-stu-id="b44d1-119">If you declare multiple constants on a single line, they must all have the same access level (`Public`, `Private`, `Friend`, `Protected`, or `Protected Friend`).</span></span>  
  
### <a name="to-declare-multiple-constants-on-a-single-line"></a><span data-ttu-id="b44d1-120">在单个行上声明多个常量</span><span class="sxs-lookup"><span data-stu-id="b44d1-120">To declare multiple constants on a single line</span></span>  
  
- <span data-ttu-id="b44d1-121">使用逗号和空格分隔声明，如下面的示例所示：</span><span class="sxs-lookup"><span data-stu-id="b44d1-121">Separate the declarations with a comma and a space, as in the following example:</span></span>  
  
    ```vb  
    Public Const Four As Integer = 4, Five As Integer = 5, Six As Integer = 44  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b44d1-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="b44d1-122">See also</span></span>

- [<span data-ttu-id="b44d1-123">Const 语句</span><span class="sxs-lookup"><span data-stu-id="b44d1-123">Const Statement</span></span>](../../../language-reference/statements/const-statement.md)
- [<span data-ttu-id="b44d1-124">常数和文本数据类型</span><span class="sxs-lookup"><span data-stu-id="b44d1-124">Constant and Literal Data Types</span></span>](constant-and-literal-data-types.md)
- [<span data-ttu-id="b44d1-125">常量概述</span><span class="sxs-lookup"><span data-stu-id="b44d1-125">Constants Overview</span></span>](constants-overview.md)
- [<span data-ttu-id="b44d1-126">如何：声明常量</span><span class="sxs-lookup"><span data-stu-id="b44d1-126">How to: Declare A Constant</span></span>](how-to-declare-a-constant.md)
- [<span data-ttu-id="b44d1-127">用户定义常数</span><span class="sxs-lookup"><span data-stu-id="b44d1-127">User-Defined Constants</span></span>](user-defined-constants.md)
- [<span data-ttu-id="b44d1-128">常数和文本数据类型</span><span class="sxs-lookup"><span data-stu-id="b44d1-128">Constant and Literal Data Types</span></span>](constant-and-literal-data-types.md)
- [<span data-ttu-id="b44d1-129">如何：将相关的常量值组合在一起</span><span class="sxs-lookup"><span data-stu-id="b44d1-129">How to: Group Related Constant Values Together</span></span>](how-to-group-related-constant-values-together.md)
- [<span data-ttu-id="b44d1-130">枚举概述</span><span class="sxs-lookup"><span data-stu-id="b44d1-130">Enumerations Overview</span></span>](enumerations-overview.md)
- [<span data-ttu-id="b44d1-131">如何：声明枚举</span><span class="sxs-lookup"><span data-stu-id="b44d1-131">How to: Declare Enumerations</span></span>](how-to-declare-enumerations.md)
- [<span data-ttu-id="b44d1-132">如何：引用枚举成员</span><span class="sxs-lookup"><span data-stu-id="b44d1-132">How to: Refer to an Enumeration Member</span></span>](how-to-refer-to-an-enumeration-member.md)
- [<span data-ttu-id="b44d1-133">枚举和名称限定</span><span class="sxs-lookup"><span data-stu-id="b44d1-133">Enumerations and Name Qualification</span></span>](enumerations-and-name-qualification.md)
- [<span data-ttu-id="b44d1-134">如何：循环访问枚举</span><span class="sxs-lookup"><span data-stu-id="b44d1-134">How to: Iterate Through An Enumeration</span></span>](how-to-iterate-through-an-enumeration.md)
- [<span data-ttu-id="b44d1-135">如何：确定与枚举值关联的字符串</span><span class="sxs-lookup"><span data-stu-id="b44d1-135">How to: Determine the String Associated with an Enumeration Value</span></span>](how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [<span data-ttu-id="b44d1-136">何时使用枚举</span><span class="sxs-lookup"><span data-stu-id="b44d1-136">When to Use an Enumeration</span></span>](when-to-use-an-enumeration.md)

- [<span data-ttu-id="b44d1-137">枚举概述</span><span class="sxs-lookup"><span data-stu-id="b44d1-137">Enumerations Overview</span></span>](enumerations-overview.md)
- [<span data-ttu-id="b44d1-138">常量概述</span><span class="sxs-lookup"><span data-stu-id="b44d1-138">Constants Overview</span></span>](constants-overview.md)
- [<span data-ttu-id="b44d1-139">如何：声明枚举</span><span class="sxs-lookup"><span data-stu-id="b44d1-139">How to: Declare an Enumeration</span></span>](how-to-declare-enumerations.md)
- [<span data-ttu-id="b44d1-140">枚举和名称限定</span><span class="sxs-lookup"><span data-stu-id="b44d1-140">Enumerations and Name Qualification</span></span>](enumerations-and-name-qualification.md)
- [<span data-ttu-id="b44d1-141">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="b44d1-141">Option Strict Statement</span></span>](../../../language-reference/statements/option-strict-statement.md)
- [<span data-ttu-id="b44d1-142">常量和枚举</span><span class="sxs-lookup"><span data-stu-id="b44d1-142">Constants and Enumerations</span></span>](../../../language-reference/constants-and-enumerations.md)
