---
description: '了解详细信息：标识符 (实体 SQL) '
title: 标识符 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: d58a5edd-7b5c-48e1-b5d7-a326ff426aa4
ms.openlocfilehash: 932f45e8b65b6244eada330caeb9a04b6560d427
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748656"
---
# <a name="identifiers-entity-sql"></a><span data-ttu-id="0a23e-103">标识符 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="0a23e-103">Identifiers (Entity SQL)</span></span>

<span data-ttu-id="0a23e-104">在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中，标识符用于表示查询表达式别名、变量引用、对象的属性、函数等等。</span><span class="sxs-lookup"><span data-stu-id="0a23e-104">Identifiers are used in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] to represent query expression aliases, variable references, properties of objects, functions, and so on.</span></span> [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="0a23e-105">提供两种标识符：简单标识符和带引号的标识符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-105">provides two kinds of identifiers: simple identifiers and quoted identifiers.</span></span>  
  
## <a name="simple-identifiers"></a><span data-ttu-id="0a23e-106">简单标识符</span><span class="sxs-lookup"><span data-stu-id="0a23e-106">Simple Identifiers</span></span>  

 <span data-ttu-id="0a23e-107">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的简单标识符是字母数字和下划线字符的序列。</span><span class="sxs-lookup"><span data-stu-id="0a23e-107">A simple identifier in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] is a sequence of alphanumeric and underscore characters.</span></span> <span data-ttu-id="0a23e-108">标识符的第一个字符必须是字母字符（a-z 或 A-Z）。</span><span class="sxs-lookup"><span data-stu-id="0a23e-108">The first character of the identifier must be an alphabetical character (a-z or A-Z).</span></span>  
  
## <a name="quoted-identifiers"></a><span data-ttu-id="0a23e-109">带引号的标识符</span><span class="sxs-lookup"><span data-stu-id="0a23e-109">Quoted Identifiers</span></span>  

 <span data-ttu-id="0a23e-110">带引号的标识符是括在方括号 ([]) 中的任何字符序列。</span><span class="sxs-lookup"><span data-stu-id="0a23e-110">A quoted identifier is any sequence of characters enclosed in square brackets ([]).</span></span> <span data-ttu-id="0a23e-111">使用带引号的标识符可以指定含有在标识符中无效的字符的标识符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-111">Quoted identifiers let you specify identifiers with characters that are not valid in identifiers.</span></span> <span data-ttu-id="0a23e-112">方括号之间的所有字符都将成为标识符的一部分，包括所有空格。</span><span class="sxs-lookup"><span data-stu-id="0a23e-112">All characters between the square brackets become part of the identifier, including all white space.</span></span>  
  
 <span data-ttu-id="0a23e-113">带引号的标识符不能包含以下字符：</span><span class="sxs-lookup"><span data-stu-id="0a23e-113">A quoted identifier cannot include the following characters:</span></span>  
  
- <span data-ttu-id="0a23e-114">换行符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-114">Newline.</span></span>  
  
- <span data-ttu-id="0a23e-115">回车符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-115">Carriage returns.</span></span>  
  
- <span data-ttu-id="0a23e-116">制表符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-116">Tabs.</span></span>  
  
- <span data-ttu-id="0a23e-117">Backspace。</span><span class="sxs-lookup"><span data-stu-id="0a23e-117">Backspace.</span></span>  
  
- <span data-ttu-id="0a23e-118">额外的方括号（即括起标识符的方括号中的方括号）。</span><span class="sxs-lookup"><span data-stu-id="0a23e-118">Additional square brackets (that is, square brackets within the square brackets that delineate the identifier).</span></span>  
  
 <span data-ttu-id="0a23e-119">带引号的标识符可以包含 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-119">A quoted-identifier can include Unicode characters.</span></span>  
  
 <span data-ttu-id="0a23e-120">使用带引号的标识符可以创建在标识符中无效的属性名称字符，如下面的示例所示：</span><span class="sxs-lookup"><span data-stu-id="0a23e-120">Quoted identifiers enable you to create property name characters that are not valid in identifiers, as illustrated in the following example:</span></span>  
  
 `SELECT c.ContactName AS [Contact Name] FROM customers AS c`  
  
 <span data-ttu-id="0a23e-121">使用带引号的标识符还可以指定属于 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 保留关键字的标识符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-121">You can also use quoted identifiers to specify an identifier that is a reserved keyword of [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span></span> <span data-ttu-id="0a23e-122">例如，如果类型 `Email` 具有名为“From”的属性，则可以使用方括号来消除与保留关键字“FROM”的歧义，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0a23e-122">For example, if the type `Email` has a property named "From", you can disambiguate it from the reserved keyword FROM by using square brackets, as follows:</span></span>  
  
 `SELECT e.[From] FROM emails AS e`  
  
 <span data-ttu-id="0a23e-123">可以在点 (.) 运算符的右侧使用带引号的标识符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-123">You can use a quoted identifier on the right side of a dot (.) operator.</span></span>  
  
 `SELECT t FROM ts as t WHERE t.[property] == 2`  
  
 <span data-ttu-id="0a23e-124">若要在标识符中使用方括号，请再添加一个方括号。</span><span class="sxs-lookup"><span data-stu-id="0a23e-124">To use the square bracket in an identifier, add an extra square bracket.</span></span> <span data-ttu-id="0a23e-125">在下面的示例中，“`abc]`”为标识符：</span><span class="sxs-lookup"><span data-stu-id="0a23e-125">In the following example "`abc]`" is the identifier:</span></span>  
  
 `SELECT t from ts as t WHERE t.[abc]]] == 2`  
  
 <span data-ttu-id="0a23e-126">对于带引号的标识符比较语义，请参阅 [输入字符集](input-character-set-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="0a23e-126">For quoted identifier comparison semantics, see [Input Character Set](input-character-set-entity-sql.md).</span></span>  
  
## <a name="aliasing-rules"></a><span data-ttu-id="0a23e-127">别名规则</span><span class="sxs-lookup"><span data-stu-id="0a23e-127">Aliasing Rules</span></span>  

 <span data-ttu-id="0a23e-128">如果需要，建议在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询中指定别名，包括以下 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 构造：</span><span class="sxs-lookup"><span data-stu-id="0a23e-128">We recommend specifying aliases in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries whenever needed, including the following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] constructs:</span></span>  
  
- <span data-ttu-id="0a23e-129">行构造函数的字段。</span><span class="sxs-lookup"><span data-stu-id="0a23e-129">Fields of a row constructor.</span></span>  
  
- <span data-ttu-id="0a23e-130">查询表达式的 FROM 子句中的项。</span><span class="sxs-lookup"><span data-stu-id="0a23e-130">Items in the FROM clause of a query expression.</span></span>  
  
- <span data-ttu-id="0a23e-131">查询表达式的 SELECT 子句中的项。</span><span class="sxs-lookup"><span data-stu-id="0a23e-131">Items in the SELECT clause of a query expression.</span></span>  
  
- <span data-ttu-id="0a23e-132">查询表达式的 GROUP BY 子句中的项。</span><span class="sxs-lookup"><span data-stu-id="0a23e-132">Items in the GROUP BY clause of a query expression.</span></span>  
  
### <a name="valid-aliases"></a><span data-ttu-id="0a23e-133">有效别名</span><span class="sxs-lookup"><span data-stu-id="0a23e-133">Valid Aliases</span></span>  

 <span data-ttu-id="0a23e-134">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的有效别名包括任何简单标识符或带引号的标识符。</span><span class="sxs-lookup"><span data-stu-id="0a23e-134">Valid aliases in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] are any simple identifier or quoted identifier.</span></span>  
  
### <a name="alias-generation"></a><span data-ttu-id="0a23e-135">别名生成</span><span class="sxs-lookup"><span data-stu-id="0a23e-135">Alias Generation</span></span>  

 <span data-ttu-id="0a23e-136">如果 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询表达式中未指定别名，则 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 将尝试根据以下简单规则来生成别名：</span><span class="sxs-lookup"><span data-stu-id="0a23e-136">If no alias is specified in an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query expression, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tries to generate an alias based on the following simple rules:</span></span>  
  
- <span data-ttu-id="0a23e-137">如果查询表达式（对该查询表达式未指定别名）是一个简单标识符或带引号的标识符，则该标识符用作别名。</span><span class="sxs-lookup"><span data-stu-id="0a23e-137">If the query expression (for which the alias is unspecified) is a simple or quoted identifier, that identifier is used as the alias.</span></span> <span data-ttu-id="0a23e-138">例如，`ROW(a, [b])` 重命名为 `ROW(a AS a, [b] AS [b])`。</span><span class="sxs-lookup"><span data-stu-id="0a23e-138">For example, `ROW(a, [b])` becomes `ROW(a AS a, [b] AS [b])`.</span></span>  
  
- <span data-ttu-id="0a23e-139">如果查询表达式是较复杂的表达式，但该查询表达式的最后一部分是简单标识符，则该标识符用作别名。</span><span class="sxs-lookup"><span data-stu-id="0a23e-139">If the query expression is a more complex expression, but the last component of that query expression is a simple identifier, then that identifier is used as the alias.</span></span> <span data-ttu-id="0a23e-140">例如，`ROW(a.a1, b.[b1])` 重命名为 `ROW(a.a1 AS a1, b.[b1] AS [b1])`。</span><span class="sxs-lookup"><span data-stu-id="0a23e-140">For example, `ROW(a.a1, b.[b1])` becomes `ROW(a.a1 AS a1, b.[b1] AS [b1])`.</span></span>  
  
 <span data-ttu-id="0a23e-141">如果希望以后使用该别名，建议不要使用隐式别名。</span><span class="sxs-lookup"><span data-stu-id="0a23e-141">We recommend that you do not use implicit aliasing if you want to use the alias name later.</span></span> <span data-ttu-id="0a23e-142">别名（隐式或显式）如果冲突，或在同一作用域内重复，都会出现编译错误。</span><span class="sxs-lookup"><span data-stu-id="0a23e-142">Anytime aliases (implicit or explicit) conflict or are repeated in the same scope, there will be a compile error.</span></span> <span data-ttu-id="0a23e-143">即使存在同名的显式或隐式别名，隐式别名也会通过编译。</span><span class="sxs-lookup"><span data-stu-id="0a23e-143">An implicit alias will pass compilation even if there is an explicit or implicit alias of the same name.</span></span>  
  
 <span data-ttu-id="0a23e-144">隐式别名是根据用户输入自动生成的。</span><span class="sxs-lookup"><span data-stu-id="0a23e-144">Implicit aliases are autogenerated based on user input.</span></span> <span data-ttu-id="0a23e-145">例如，下面一行代码将生成 NAME 作为两个列的别名，从而发生冲突。</span><span class="sxs-lookup"><span data-stu-id="0a23e-145">For example, the following line of code will generate NAME as an alias for both columns and therefore will conflict.</span></span>  
  
```sql  
SELECT product.NAME, person.NAME  
```  
  
 <span data-ttu-id="0a23e-146">下面使用显式别名的代码行也会失败。</span><span class="sxs-lookup"><span data-stu-id="0a23e-146">The following line of code, which uses explicit aliases, will also fail.</span></span> <span data-ttu-id="0a23e-147">但是，通过阅读代码，失败会更为明显。</span><span class="sxs-lookup"><span data-stu-id="0a23e-147">However, the failure will be more apparent by reading the code.</span></span>  
  
```sql  
SELECT 1 AS X, 2 AS X …  
```  
  
## <a name="scoping-rules"></a><span data-ttu-id="0a23e-148">作用域规则</span><span class="sxs-lookup"><span data-stu-id="0a23e-148">Scoping Rules</span></span>  

 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="0a23e-149">定义作用域规则，用来确定查询语言中的特定变量何时可见。</span><span class="sxs-lookup"><span data-stu-id="0a23e-149">defines scoping rules that determine when particular variables are visible in the query language.</span></span> <span data-ttu-id="0a23e-150">一些表达式或语句引入了新名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-150">Some expressions or statements introduce new names.</span></span> <span data-ttu-id="0a23e-151">作用域规则确定在何处可以使用这些名称，与另一声明同名的新声明何时或在何处可以隐藏其前置任务。</span><span class="sxs-lookup"><span data-stu-id="0a23e-151">The scoping rules determine where those names can be used, and when or where a new declaration with the same name as another can hide its predecessor.</span></span>  
  
 <span data-ttu-id="0a23e-152">在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询中定义了名称，即是在作用域内定义了名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-152">When names are defined in an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query, they are said to be defined within a scope.</span></span> <span data-ttu-id="0a23e-153">作用域包括查询的整个区域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-153">A scope covers an entire region of the query.</span></span> <span data-ttu-id="0a23e-154">在作用域内定义的名称对该作用域的所有表达式或名称引用都可见。</span><span class="sxs-lookup"><span data-stu-id="0a23e-154">All expressions or name references within a certain scope can see names that are defined within that scope.</span></span> <span data-ttu-id="0a23e-155">作用域内定义的名称不能在作用域开始之前和结束之后进行引用。</span><span class="sxs-lookup"><span data-stu-id="0a23e-155">Before a scope begins and after it ends, names that are defined within the scope cannot be referenced.</span></span>  
  
 <span data-ttu-id="0a23e-156">作用域可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="0a23e-156">Scopes can be nested.</span></span> <span data-ttu-id="0a23e-157">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 的组成部分引入了包含整个区域的新作用域，这些区域可以包含也引入作用域的其他 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 表达式。</span><span class="sxs-lookup"><span data-stu-id="0a23e-157">Parts of [!INCLUDE[esql](../../../../../../includes/esql-md.md)] introduce new scopes that cover entire regions, and these regions can contain other [!INCLUDE[esql](../../../../../../includes/esql-md.md)] expressions that also introduce scopes.</span></span> <span data-ttu-id="0a23e-158">当作用域嵌套时，可以对包含引用的最内层作用域中定义的名称进行引用。</span><span class="sxs-lookup"><span data-stu-id="0a23e-158">When scopes are nested, references can be made to names that are defined in the innermost scope, which contains the reference.</span></span> <span data-ttu-id="0a23e-159">还可以对任一外层作用域中定义的任何名称进行引用。</span><span class="sxs-lookup"><span data-stu-id="0a23e-159">References can also be made to any names that are defined in any outer scopes.</span></span> <span data-ttu-id="0a23e-160">在同一作用域内定义的任何两个作用域可视为同级作用域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-160">Any two scopes defined within the same scope are considered sibling scopes.</span></span> <span data-ttu-id="0a23e-161">不能引用同级作用域内定义的名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-161">References cannot be made to names that are defined within sibling scopes.</span></span>  
  
 <span data-ttu-id="0a23e-162">如果内层作用域中声明的名称与外层作用域中声明的名称相同，则在内层作用域或其内部的作用域内声明的作用域内的引用只能引用新声明的名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-162">If a name declared in an inner scope matches a name declared in an outer scope, references within the inner scope or within scopes declared within that scope refer only to the newly declared name.</span></span> <span data-ttu-id="0a23e-163">外层作用域中的名称为隐藏状态。</span><span class="sxs-lookup"><span data-stu-id="0a23e-163">The name in the outer scope is hidden.</span></span>  
  
 <span data-ttu-id="0a23e-164">即使在同一作用域内，名称也不能在定义前引用。</span><span class="sxs-lookup"><span data-stu-id="0a23e-164">Even within the same scope, names cannot be referenced before they are defined.</span></span>  
  
 <span data-ttu-id="0a23e-165">全局名称可以作为执行环境的一部分存在。</span><span class="sxs-lookup"><span data-stu-id="0a23e-165">Global names can exist as part of the execution environment.</span></span> <span data-ttu-id="0a23e-166">包括持久集合或环境变量的名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-166">This can include names of persistent collections or environment variables.</span></span> <span data-ttu-id="0a23e-167">若要使名称成为全局名称，必须在最外层作用域中声明该名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-167">For a name to be global, it must be declared in the outermost scope.</span></span>  
  
 <span data-ttu-id="0a23e-168">参数不在一个作用域内。</span><span class="sxs-lookup"><span data-stu-id="0a23e-168">Parameters are not in a scope.</span></span> <span data-ttu-id="0a23e-169">由于对参数的引用包含特殊语法，参数名称不会与查询中的其他名称冲突。</span><span class="sxs-lookup"><span data-stu-id="0a23e-169">Because references to parameters include special syntax, names of parameters will never collide with other names in the query.</span></span>  
  
### <a name="query-expressions"></a><span data-ttu-id="0a23e-170">查询表达式</span><span class="sxs-lookup"><span data-stu-id="0a23e-170">Query Expressions</span></span>  

 <span data-ttu-id="0a23e-171">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询表达式引入一个新的作用域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-171">An [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query expression introduces a new scope.</span></span> <span data-ttu-id="0a23e-172">在 FROM 子句中定义的名称是以从左到右的显示顺序引入“from”作用域的。</span><span class="sxs-lookup"><span data-stu-id="0a23e-172">Names that are defined in the FROM clause are introduced into the from scope in order of appearance, left to right.</span></span> <span data-ttu-id="0a23e-173">在联接列表中，表达式可以引用列表前面定义的名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-173">In the join list, expressions can refer to names that were defined earlier in the list.</span></span> <span data-ttu-id="0a23e-174">在 FROM 子句中标识的元素的公共属性（字段等）不添加到“from”作用域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-174">Public properties (fields and so on) of elements identified in the FROM clause are not added to the from-scope.</span></span> <span data-ttu-id="0a23e-175">它们必须始终由别名限定名称引用。</span><span class="sxs-lookup"><span data-stu-id="0a23e-175">They must be always referenced by the alias-qualified name.</span></span> <span data-ttu-id="0a23e-176">通常，SELECT 表达式的所有部分都被视为在“from”作用域内。</span><span class="sxs-lookup"><span data-stu-id="0a23e-176">Typically, all parts of the SELECT expression are considered within the from-scope.</span></span>  
  
 <span data-ttu-id="0a23e-177">GROUP BY 子句也引入一个新的同级作用域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-177">The GROUP BY clause also introduces a new sibling scope.</span></span> <span data-ttu-id="0a23e-178">每个组都可以有一个引用组中元素集合的组名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-178">Each group can have a group name that refers to the collection of elements in the group.</span></span> <span data-ttu-id="0a23e-179">每个分组表达式也将向“group”作用域引入一个新名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-179">Each grouping expression will also introduce a new name into the group-scope.</span></span> <span data-ttu-id="0a23e-180">此外，嵌套聚合（即命名组）也添加到作用域中。</span><span class="sxs-lookup"><span data-stu-id="0a23e-180">Additionally, the nest aggregate (or the named group) is also added to the scope.</span></span> <span data-ttu-id="0a23e-181">分组表达式本身在“from”作用域中。</span><span class="sxs-lookup"><span data-stu-id="0a23e-181">The grouping expressions themselves are within the from-scope.</span></span> <span data-ttu-id="0a23e-182">但是，当使用 GROUP BY 子句时，选择列表（投影）、HAVING 子句和 ORDER BY 子句被视为在“group”作用域中，而不是在“from”作用域中。</span><span class="sxs-lookup"><span data-stu-id="0a23e-182">However, when a GROUP BY clause is used, the select-list (projection), HAVING clause, and ORDER BY clause are considered to be within the group-scope, and not the from-scope.</span></span> <span data-ttu-id="0a23e-183">聚合有特殊的处理方式，如下列内容所述。</span><span class="sxs-lookup"><span data-stu-id="0a23e-183">Aggregates receive special treatment, as described in the following bulleted list.</span></span>  
  
 <span data-ttu-id="0a23e-184">以下是对作用域的附加说明：</span><span class="sxs-lookup"><span data-stu-id="0a23e-184">The following are additional notes about scopes:</span></span>  
  
- <span data-ttu-id="0a23e-185">选择列表可将新名称按顺序引入作用域。</span><span class="sxs-lookup"><span data-stu-id="0a23e-185">The select-list can introduce new names into the scope, in order.</span></span> <span data-ttu-id="0a23e-186">右侧的投影表达式可以引用投影在左侧的名称。</span><span class="sxs-lookup"><span data-stu-id="0a23e-186">Projection expressions to the right might refer to names projected on the left.</span></span>  
  
- <span data-ttu-id="0a23e-187">ORDER BY 子句可以引用选择列表中指定的名称（别名）。</span><span class="sxs-lookup"><span data-stu-id="0a23e-187">The ORDER BY clause can refer to names (aliases) specified in the select list.</span></span>  
  
- <span data-ttu-id="0a23e-188">SELECT 表达式内的子句计算顺序确定名称引入作用域的顺序。</span><span class="sxs-lookup"><span data-stu-id="0a23e-188">The order of evaluation of clauses within the SELECT expression determines the order that names are introduced into the scope.</span></span> <span data-ttu-id="0a23e-189">计算的顺序首先是 FROM 子句，其次是 WHERE 子句、GROUP BY 子句、HAVING 子句、SELECT 子句，最后是 ORDER BY 子句。</span><span class="sxs-lookup"><span data-stu-id="0a23e-189">The FROM clause is evaluated first, followed by the WHERE clause, GROUP BY clause, HAVING clause, SELECT clause, and finally the ORDER BY clause.</span></span>  
  
### <a name="aggregate-handling"></a><span data-ttu-id="0a23e-190">聚合处理</span><span class="sxs-lookup"><span data-stu-id="0a23e-190">Aggregate Handling</span></span>  

 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="0a23e-191">支持两种形式的聚合：基于集合的聚合和基于组的聚合。</span><span class="sxs-lookup"><span data-stu-id="0a23e-191">supports two forms of aggregates: collection-based aggregates and group-based aggregates.</span></span> <span data-ttu-id="0a23e-192">基于集合的聚合是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 的首选构造，支持基于组的聚合则是为了实现 SQL 兼容性。</span><span class="sxs-lookup"><span data-stu-id="0a23e-192">Collection-based aggregates are the preferred construct in [!INCLUDE[esql](../../../../../../includes/esql-md.md)], and group-based aggregates are supported for SQL compatibility.</span></span>  
  
 <span data-ttu-id="0a23e-193">在解析聚合时，[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 首先尝试将它视为基于集合的聚合。</span><span class="sxs-lookup"><span data-stu-id="0a23e-193">When resolving an aggregate, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] first tries to treat it as a collection-based aggregate.</span></span> <span data-ttu-id="0a23e-194">如果失败，[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 将聚合输入转换为对嵌套聚合的引用，并尝试解析这个新的表达式，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="0a23e-194">If that fails, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] transforms the aggregate input into a reference to the nest aggregate and tries to resolve this new expression, as illustrated in the following example.</span></span>  
  
 `AVG(t.c) becomes AVG(group..(t.c))`  
  
## <a name="see-also"></a><span data-ttu-id="0a23e-195">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a23e-195">See also</span></span>

- [<span data-ttu-id="0a23e-196">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="0a23e-196">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="0a23e-197">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="0a23e-197">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="0a23e-198">输入字符集</span><span class="sxs-lookup"><span data-stu-id="0a23e-198">Input Character Set</span></span>](input-character-set-entity-sql.md)
