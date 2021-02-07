---
description: 了解详细信息：基本数据类型
title: 基本数据类型
ms.date: 03/30/2017
ms.assetid: eca2c472-9548-4800-bd31-5d8d9f11752b
ms.openlocfilehash: d0236bc315c884d9e70c3c4a75755c3b66b1f2e4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712605"
---
# <a name="basic-data-types"></a><span data-ttu-id="6581f-103">基本数据类型</span><span class="sxs-lookup"><span data-stu-id="6581f-103">Basic Data Types</span></span>

<span data-ttu-id="6581f-104">因为 LINQ to SQL 查询转换为 Transact-SQL 后才在 Microsoft SQL Server 上执行。</span><span class="sxs-lookup"><span data-stu-id="6581f-104">Because LINQ to SQL queries translate to Transact-SQL before they are executed on the Microsoft SQL Server.</span></span> <span data-ttu-id="6581f-105">LINQ to SQL 支持针对基本数据类型的许多和 SQL Server 一样的内置功能。</span><span class="sxs-lookup"><span data-stu-id="6581f-105">LINQ to SQL supports much of the same built-in functionality that SQL Server does for basic data types.</span></span>  
  
## <a name="casting"></a><span data-ttu-id="6581f-106">强制转换</span><span class="sxs-lookup"><span data-stu-id="6581f-106">Casting</span></span>  

 <span data-ttu-id="6581f-107">支持从源 CLR 类型到目标 CLR 类型的隐式或显式强制转换，前提是在 SQL Server 中存在类似的有效转换。</span><span class="sxs-lookup"><span data-stu-id="6581f-107">Implicit or explicit casts are enabled from a source CLR type to a target CLR type if there is a similar valid conversion within SQL Server.</span></span> <span data-ttu-id="6581f-108">有关 CLR 强制转换的详细信息，请参阅 [CType 函数](../../../../../visual-basic/language-reference/functions/ctype-function.md) (Visual Basic) 和 [类型测试和转换运算符](../../../../../csharp/language-reference/operators/type-testing-and-cast.md)。</span><span class="sxs-lookup"><span data-stu-id="6581f-108">For more information about CLR casting, see [CType Function](../../../../../visual-basic/language-reference/functions/ctype-function.md) (Visual Basic) and [Type-testing and cast operators](../../../../../csharp/language-reference/operators/type-testing-and-cast.md).</span></span> <span data-ttu-id="6581f-109">转换后，强制转换会更改对 CLR 表达式执行的操作的行为，使之与自然映射到目标类型的其他 CLR 表达式的行为匹配。</span><span class="sxs-lookup"><span data-stu-id="6581f-109">After conversion, casts change the behavior of operations performed on a CLR expression to match the behavior of other CLR expressions that naturally map to the destination type.</span></span> <span data-ttu-id="6581f-110">强制转换还可以在继承映射的上下文中进行。</span><span class="sxs-lookup"><span data-stu-id="6581f-110">Casts are also translatable in the context of inheritance mapping.</span></span> <span data-ttu-id="6581f-111">可以将对象强制转换成更具体的实体子类型，以便可以访问其特定于子类型的数据。</span><span class="sxs-lookup"><span data-stu-id="6581f-111">Objects can be cast to more specific entity subtypes so that their subtype-specific data can be accessed.</span></span>  
  
## <a name="equality-operators"></a><span data-ttu-id="6581f-112">相等运算符</span><span class="sxs-lookup"><span data-stu-id="6581f-112">Equality Operators</span></span>  

 <span data-ttu-id="6581f-113">LINQ to SQL 支持以下 LINQ to SQL 查询内部的基本数据类型上的相等运算符：</span><span class="sxs-lookup"><span data-stu-id="6581f-113">LINQ to SQL supports the following equality operators on basic data types inside LINQ to SQL queries:</span></span>  
  
- <span data-ttu-id="6581f-114">等于和不相等运算符：数值、 <xref:System.Boolean> 、和类型支持相等运算符和不相等运算符 <xref:System.DateTime> <xref:System.TimeSpan> 。</span><span class="sxs-lookup"><span data-stu-id="6581f-114">Equal and Inequality Operator: Equality and inequality operators are supported for numeric, <xref:System.Boolean>, <xref:System.DateTime>, and <xref:System.TimeSpan> types.</span></span> <span data-ttu-id="6581f-115">有关 Visual Basic 运算符和的详细信息 `=` `<>` ，请参阅 [比较运算符](../../../../../visual-basic/language-reference/operators/comparison-operators.md)。</span><span class="sxs-lookup"><span data-stu-id="6581f-115">For more about Visual Basic operators `=` and `<>`, see [Comparison Operators](../../../../../visual-basic/language-reference/operators/comparison-operators.md).</span></span> <span data-ttu-id="6581f-116">有关 c # 比较运算符和的详细信息 `==` `!=` ，请参阅 [相等运算符](../../../../../csharp/language-reference/operators/equality-operators.md)。</span><span class="sxs-lookup"><span data-stu-id="6581f-116">For more information about C# comparison operators `==` and `!=`, see [Equality operators](../../../../../csharp/language-reference/operators/equality-operators.md).</span></span>
  
- <span data-ttu-id="6581f-117">Is 运算符：在使用继承映射时，`IS` 运算符具有受支持的转换形式。</span><span class="sxs-lookup"><span data-stu-id="6581f-117">Is operator: The `IS` operator has a supported translation when inheritance mapping is being used.</span></span> <span data-ttu-id="6581f-118">可以使用该运算符，而不用通过直接测试鉴别器列来确定对象是否属于特定实体类型，该运算符会转换为对鉴别器列的检查。</span><span class="sxs-lookup"><span data-stu-id="6581f-118">It can be used instead of directly testing the discriminator column to determine whether an object is of a specific entity type, and is translated to a check on the discriminator column.</span></span> <span data-ttu-id="6581f-119">有关 Visual Basic 和 c # 是运算符的详细信息，请参阅 [Is 运算符](../../../../../visual-basic/language-reference/operators/is-operator.md) 并且 [为](../../../../../csharp/language-reference/operators/type-testing-and-cast.md#is-operator)。</span><span class="sxs-lookup"><span data-stu-id="6581f-119">For more information about the Visual Basic and C# Is operators, see [Is Operator](../../../../../visual-basic/language-reference/operators/is-operator.md) and [is](../../../../../csharp/language-reference/operators/type-testing-and-cast.md#is-operator).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6581f-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="6581f-120">See also</span></span>

- [<span data-ttu-id="6581f-121">SQL-CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="6581f-121">SQL-CLR Type Mapping</span></span>](sql-clr-type-mapping.md)
- [<span data-ttu-id="6581f-122">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="6581f-122">Data Types and Functions</span></span>](data-types-and-functions.md)
