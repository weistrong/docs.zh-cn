---
description: 了解详细信息： SQL-CLR 类型映射
title: SQL-CLR 类型映射
ms.date: 07/23/2018
ms.assetid: 4ed76327-54a7-414b-82a9-7579bfcec04b
ms.openlocfilehash: 59d3594287ceb20f5c3887c58a0f5527df35218a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803732"
---
# <a name="sql-clr-type-mapping"></a><span data-ttu-id="ff980-103">SQL-CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-103">SQL-CLR Type Mapping</span></span>

<span data-ttu-id="ff980-104">在 LINQ to SQL 中，关系数据库的数据模型映射到用您所选择的编程语言表示的对象模型。</span><span class="sxs-lookup"><span data-stu-id="ff980-104">In LINQ to SQL, the data model of a relational database maps to an object model that is expressed in the programming language of your choice.</span></span> <span data-ttu-id="ff980-105">当应用程序运行时，LINQ to SQL 会将对象模型中的语言集成查询转换为 SQL，然后将它们发送到数据库进行执行。</span><span class="sxs-lookup"><span data-stu-id="ff980-105">When the application runs, LINQ to SQL translates the language-integrated queries in the object model into SQL and sends them to the database for execution.</span></span> <span data-ttu-id="ff980-106">当数据库返回结果时，LINQ to SQL 会将它们转换回您可以用您自己的编程语言处理的对象。</span><span class="sxs-lookup"><span data-stu-id="ff980-106">When the database returns the results, LINQ to SQL translates the results back to objects that you can work with in your own programming language.</span></span>  
  
 <span data-ttu-id="ff980-107">为了转换对象模型和数据库之间的数据，必须定义 *类型映射* 。</span><span class="sxs-lookup"><span data-stu-id="ff980-107">In order to translate data between the object model and the database, a *type mapping* must be defined.</span></span> <span data-ttu-id="ff980-108">LINQ to SQL 使用类型映射将每个公共语言运行时 (CLR) 类型与一种特定 SQL Server 类型相匹配。</span><span class="sxs-lookup"><span data-stu-id="ff980-108">LINQ to SQL uses a type mapping to match each common language runtime (CLR) type with a particular SQL Server type.</span></span> <span data-ttu-id="ff980-109">您可以使用基于属性的映射在对象模型内部定义类型映射和其他映射信息，例如数据库结构和表关系。</span><span class="sxs-lookup"><span data-stu-id="ff980-109">You can define type mappings and other mapping information, such as database structure and table relationships, inside the object model with attribute-based mapping.</span></span> <span data-ttu-id="ff980-110">或者，您可以使用外部映射文件在对象模型外部指定映射信息。</span><span class="sxs-lookup"><span data-stu-id="ff980-110">Alternatively, you can specify the mapping information outside the object model with an external mapping file.</span></span> <span data-ttu-id="ff980-111">有关详细信息，请参阅 [基于属性的映射](attribute-based-mapping.md) 和 [外部映射](external-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-111">For more information, see [Attribute-Based Mapping](attribute-based-mapping.md) and [External Mapping](external-mapping.md).</span></span>  
  
 <span data-ttu-id="ff980-112">本主题讨论下列内容：</span><span class="sxs-lookup"><span data-stu-id="ff980-112">This topic discusses the following points:</span></span>  
  
- [<span data-ttu-id="ff980-113">默认类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-113">Default Type Mapping</span></span>](#DefaultTypeMapping)  
  
- [<span data-ttu-id="ff980-114">类型映射运行时行为矩阵</span><span class="sxs-lookup"><span data-stu-id="ff980-114">Type Mapping Run-time Behavior Matrix</span></span>](#BehaviorMatrix)  
  
- [<span data-ttu-id="ff980-115">CLR 和 SQL 执行之间的行为差异</span><span class="sxs-lookup"><span data-stu-id="ff980-115">Behavior Differences Between CLR and SQL Execution</span></span>](#BehaviorDiffs)  
  
- [<span data-ttu-id="ff980-116">枚举映射</span><span class="sxs-lookup"><span data-stu-id="ff980-116">Enum Mapping</span></span>](#EnumMapping)  
  
- [<span data-ttu-id="ff980-117">数值映射</span><span class="sxs-lookup"><span data-stu-id="ff980-117">Numeric Mapping</span></span>](#NumericMapping)  
  
- [<span data-ttu-id="ff980-118">文本和 XML 映射</span><span class="sxs-lookup"><span data-stu-id="ff980-118">Text and XML Mapping</span></span>](#TextMapping)  
  
- [<span data-ttu-id="ff980-119">日期和时间映射</span><span class="sxs-lookup"><span data-stu-id="ff980-119">Date and Time Mapping</span></span>](#DateMapping)  
  
- [<span data-ttu-id="ff980-120">二进制映射</span><span class="sxs-lookup"><span data-stu-id="ff980-120">Binary Mapping</span></span>](#BinaryMapping)  
  
- [<span data-ttu-id="ff980-121">杂项映射</span><span class="sxs-lookup"><span data-stu-id="ff980-121">Miscellaneous Mapping</span></span>](#MiscMapping)  
  
<a name="DefaultTypeMapping"></a>

## <a name="default-type-mapping"></a><span data-ttu-id="ff980-122">默认类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-122">Default Type Mapping</span></span>  

 <span data-ttu-id="ff980-123">您可以使用对象关系设计器（O/R 设计器）或 SQLMetal 命令行工具自动创建对象模型或外部映射文件。</span><span class="sxs-lookup"><span data-stu-id="ff980-123">You can create the object model or external mapping file automatically with the Object Relational Designer (O/R Designer) or the SQLMetal command-line tool.</span></span> <span data-ttu-id="ff980-124">这些工具的默认类型映射定义选择何种 CLR 类型来映射到 SQL Server 数据库内部的列。</span><span class="sxs-lookup"><span data-stu-id="ff980-124">The default type mappings for these tools define which CLR types are chosen to map to columns inside the SQL Server database.</span></span> <span data-ttu-id="ff980-125">有关使用这些工具的详细信息，请参阅 [创建对象模型](creating-the-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-125">For more information about using these tools, see [Creating the Object Model](creating-the-object-model.md).</span></span>  
  
 <span data-ttu-id="ff980-126">您也可以使用 <xref:System.Data.Linq.DataContext.CreateDatabase%2A> 方法来创建基于对象模型或外部映射文件中的映射信息的 SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="ff980-126">You can also use the <xref:System.Data.Linq.DataContext.CreateDatabase%2A> method to create a SQL Server database based on the mapping information in the object model or external mapping file.</span></span> <span data-ttu-id="ff980-127"><xref:System.Data.Linq.DataContext.CreateDatabase%2A> 方法的默认类型映射定义创建何种 SQL Server 列来映射到对象模型中的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-127">The default type mappings for the <xref:System.Data.Linq.DataContext.CreateDatabase%2A> method define which type of SQL Server columns are created to map to the CLR types in the object model.</span></span> <span data-ttu-id="ff980-128">有关详细信息，请参阅 [如何：动态创建数据库](how-to-dynamically-create-a-database.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-128">For more information, see [How to: Dynamically Create a Database](how-to-dynamically-create-a-database.md).</span></span>  
  
<a name="BehaviorMatrix"></a>

## <a name="type-mapping-run-time-behavior-matrix"></a><span data-ttu-id="ff980-129">类型映射运行时行为矩阵</span><span class="sxs-lookup"><span data-stu-id="ff980-129">Type Mapping Run-time Behavior Matrix</span></span>  

 <span data-ttu-id="ff980-130">下图显示了数据从数据库检索或保存到数据库时特定类型映射的预期运行时行为。</span><span class="sxs-lookup"><span data-stu-id="ff980-130">The following diagram shows the expected run-time behavior of specific type mappings when data is retrieved from or saved to the database.</span></span> <span data-ttu-id="ff980-131">除序列化之外，LINQ to SQL 不支持任何该矩阵中未指定的 CLR 或 SQL Server 数据类型之间的映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-131">With the exception of serialization, LINQ to SQL does not support mapping between any CLR or SQL Server data types that are not specified in this matrix.</span></span> <span data-ttu-id="ff980-132">有关序列化支持的详细信息，请参阅 [二进制序列化](#BinarySerialization)。</span><span class="sxs-lookup"><span data-stu-id="ff980-132">For more information on serialization support, see [Binary Serialization](#BinarySerialization).</span></span>  

![SQL Server SQL CLR 数据类型映射表](./media/sql-clr-type-mapping.png)

> [!NOTE]
> <span data-ttu-id="ff980-134">在进行数据库转换时，某些类型映射可能会导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-134">Some type mappings may result in overflow or data loss exceptions while translating to or from the database.</span></span>  
  
### <a name="custom-type-mapping"></a><span data-ttu-id="ff980-135">自定义类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-135">Custom Type Mapping</span></span>  

 <span data-ttu-id="ff980-136">通过使用 LINQ to SQL，您并非仅可以使用 O/R 设计器、SQLMetal 和 <xref:System.Data.Linq.DataContext.CreateDatabase%2A> 方法所使用的默认类型映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-136">With LINQ to SQL, you are not limited to the default type mappings used by the O/R Designer, SQLMetal, and the <xref:System.Data.Linq.DataContext.CreateDatabase%2A> method.</span></span> <span data-ttu-id="ff980-137">您可以通过在 DBML 文件中显式指定自定义类型映射来创建它们。</span><span class="sxs-lookup"><span data-stu-id="ff980-137">You can create custom type mappings by explicitly specifying them in a DBML file.</span></span> <span data-ttu-id="ff980-138">然后，可以使用该 DBML 文件创建对象模型代码和映射文件。</span><span class="sxs-lookup"><span data-stu-id="ff980-138">Then you can use that DBML file to create the object model code and mapping file.</span></span> <span data-ttu-id="ff980-139">有关详细信息，请参阅 [SQL-CLR 自定义类型映射](sql-clr-custom-type-mappings.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-139">For more information, see [SQL-CLR Custom Type Mappings](sql-clr-custom-type-mappings.md).</span></span>  
  
<a name="BehaviorDiffs"></a>

## <a name="behavior-differences-between-clr-and-sql-execution"></a><span data-ttu-id="ff980-140">CLR 和 SQL 执行之间的行为差异</span><span class="sxs-lookup"><span data-stu-id="ff980-140">Behavior Differences Between CLR and SQL Execution</span></span>  

 <span data-ttu-id="ff980-141">由于 CLR 和 SQL Server 之间的精度及执行差异，可能会收到不同的结果或体验不同的行为，这取决于执行计算的位置。</span><span class="sxs-lookup"><span data-stu-id="ff980-141">Because of differences in precision and execution between the CLR and SQL Server, you may receive different results or experience different behavior depending on where you perform your calculations.</span></span> <span data-ttu-id="ff980-142">在 LINQ to SQL 查询中执行的计算实际上转换为 Transact-SQL，然后在 SQL Server 数据库上执行。</span><span class="sxs-lookup"><span data-stu-id="ff980-142">Calculations performed in LINQ to SQL queries are actually translated to Transact-SQL and then executed on the SQL Server database.</span></span> <span data-ttu-id="ff980-143">在 LINQ to SQL 查询外执行的计算则在 CLR 的上下文中执行。</span><span class="sxs-lookup"><span data-stu-id="ff980-143">Calculations performed outside LINQ to SQL queries are executed within the context of the CLR.</span></span>  
  
 <span data-ttu-id="ff980-144">例如，以下是一些 CLR 和 SQL Server 之间的行为差异：</span><span class="sxs-lookup"><span data-stu-id="ff980-144">For example, the following are some differences in behavior between the CLR and SQL Server:</span></span>  
  
- <span data-ttu-id="ff980-145">SQL Server 对一些数据类型的排序不同于 CLR 中等效类型数据的排序。</span><span class="sxs-lookup"><span data-stu-id="ff980-145">SQL Server orders some data types differently than data of equivalent type in the CLR.</span></span> <span data-ttu-id="ff980-146">例如，SQL Server 类型 `UNIQUEIDENTIFIER` 的数据排序不同于 CLR 类型 <xref:System.Guid?displayProperty=nameWithType> 的数据排序。</span><span class="sxs-lookup"><span data-stu-id="ff980-146">For example, SQL Server data of type `UNIQUEIDENTIFIER` is ordered differently than CLR data of type <xref:System.Guid?displayProperty=nameWithType>.</span></span>  
  
- <span data-ttu-id="ff980-147">SQL Server 处理一些字符串比较操作的方式不同于 CLR。</span><span class="sxs-lookup"><span data-stu-id="ff980-147">SQL Server handles some string comparison operations differently than the CLR.</span></span> <span data-ttu-id="ff980-148">在 SQL Server 中，字符串比较行为取决于服务器上的排序规则设置。</span><span class="sxs-lookup"><span data-stu-id="ff980-148">In SQL Server, string comparison behavior depends on the collation settings on the server.</span></span> <span data-ttu-id="ff980-149">有关详细信息，请参阅在 Microsoft SQL Server 联机丛书中使用 [排序规则](/previous-versions/sql/sql-server-2008-r2/ms187582(v=sql.105)) 。</span><span class="sxs-lookup"><span data-stu-id="ff980-149">For more information, see [Working with Collations](/previous-versions/sql/sql-server-2008-r2/ms187582(v=sql.105)) in the Microsoft SQL Server Books Online.</span></span>  
  
- <span data-ttu-id="ff980-150">对于一些映射函数，SQL Server 返回的函数值可能与 CLR 不同。</span><span class="sxs-lookup"><span data-stu-id="ff980-150">SQL Server may return different values for some mapped functions than the CLR.</span></span> <span data-ttu-id="ff980-151">例如，相等函数会不同，因为在两个字符串仅在尾随空白不同的情况下，SQL Server 会视这两个字符串相等，而 CLR 则视其不相等。</span><span class="sxs-lookup"><span data-stu-id="ff980-151">For example, equality functions will differ because SQL Server considers two strings to be equal if they only differ in trailing white space; whereas the CLR considers them to be not equal.</span></span>  
  
<a name="EnumMapping"></a>

## <a name="enum-mapping"></a><span data-ttu-id="ff980-152">枚举映射</span><span class="sxs-lookup"><span data-stu-id="ff980-152">Enum Mapping</span></span>  

 <span data-ttu-id="ff980-153">LINQ to SQL 支持使用如下两种方式将 CLR <xref:System.Enum?displayProperty=nameWithType> 类型映射到 SQL Server 类型：</span><span class="sxs-lookup"><span data-stu-id="ff980-153">LINQ to SQL supports mapping the CLR <xref:System.Enum?displayProperty=nameWithType> type to SQL Server types in two ways:</span></span>  
  
- <span data-ttu-id="ff980-154">映射到 SQL 数值类型（`TINYINT`、`SMALLINT`、`INT`、`BIGINT`）</span><span class="sxs-lookup"><span data-stu-id="ff980-154">Mapping to SQL numeric types (`TINYINT`, `SMALLINT`, `INT`, `BIGINT`)</span></span>  
  
     <span data-ttu-id="ff980-155">将 CLR <xref:System.Enum?displayProperty=nameWithType> 类型映射到 SQL 数值类型时，您会将此 CLR <xref:System.Enum?displayProperty=nameWithType> 的基础整数值映射到 SQL Server 数据库列的值。</span><span class="sxs-lookup"><span data-stu-id="ff980-155">When you map a CLR <xref:System.Enum?displayProperty=nameWithType> type to a SQL numeric type, you map the underlying integer value of the CLR <xref:System.Enum?displayProperty=nameWithType> to the value of the SQL Server database column.</span></span> <span data-ttu-id="ff980-156">例如，如果一个名为 <xref:System.Enum?displayProperty=nameWithType> 的 `DaysOfWeek` 包含一个名为 `Tue` 且基础整数值为 3 的成员，则此成员映射到数据库值 3。</span><span class="sxs-lookup"><span data-stu-id="ff980-156">For example, if a <xref:System.Enum?displayProperty=nameWithType> named `DaysOfWeek` contains a member named `Tue` with an underlying integer value of 3, that member maps to a database value of 3.</span></span>  
  
- <span data-ttu-id="ff980-157">映射到 SQL 文本类型（`CHAR`、`NCHAR`、`VARCHAR`、`NVARCHAR`）</span><span class="sxs-lookup"><span data-stu-id="ff980-157">Mapping to SQL text types (`CHAR`, `NCHAR`, `VARCHAR`, `NVARCHAR`)</span></span>  
  
     <span data-ttu-id="ff980-158">将 CLR <xref:System.Enum?displayProperty=nameWithType> 类型映射到 SQL 文本类型时，SQL 数据库值会映射到 CLR <xref:System.Enum?displayProperty=nameWithType> 成员的名称。</span><span class="sxs-lookup"><span data-stu-id="ff980-158">When you map a CLR <xref:System.Enum?displayProperty=nameWithType> type to a SQL text type, the SQL database value is mapped to the names of the CLR <xref:System.Enum?displayProperty=nameWithType> members.</span></span> <span data-ttu-id="ff980-159">例如，如果一个名为 <xref:System.Enum?displayProperty=nameWithType> 的 `DaysOfWeek` 包含一个名为 `Tue` 且基础整数值为 3 的成员，则此成员映射到数据库值 `Tue`。</span><span class="sxs-lookup"><span data-stu-id="ff980-159">For example, if a <xref:System.Enum?displayProperty=nameWithType> named `DaysOfWeek` contains a member named `Tue` with an underlying integer value of 3, that member maps to a database value of `Tue`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ff980-160">将 SQL 文本类型映射到 CLR <xref:System.Enum?displayProperty=nameWithType> 时，映射的 SQL 列中仅包含 <xref:System.Enum> 成员的名称。</span><span class="sxs-lookup"><span data-stu-id="ff980-160">When mapping SQL text types to a CLR <xref:System.Enum?displayProperty=nameWithType>, include only the names of the <xref:System.Enum> members in the mapped SQL column.</span></span> <span data-ttu-id="ff980-161"><xref:System.Enum> 映射的 SQL 列不支持其他值。</span><span class="sxs-lookup"><span data-stu-id="ff980-161">Other values are not supported in the <xref:System.Enum>-mapped SQL column.</span></span>  
  
 <span data-ttu-id="ff980-162">O/R 设计器和 SQLMetal 命令行工具无法将 SQL 类型自动映射到 CLR <xref:System.Enum> 类。</span><span class="sxs-lookup"><span data-stu-id="ff980-162">The O/R Designer and SQLMetal command-line tool cannot automatically map a SQL type to a CLR <xref:System.Enum> class.</span></span> <span data-ttu-id="ff980-163">您必须通过自定义 DBML 文件以供 O/R 设计器和 SQLMetal 使用来显式配置此映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-163">You must explicitly configure this mapping by customizing a DBML file for use by the O/R Designer and SQLMetal.</span></span> <span data-ttu-id="ff980-164">有关自定义类型映射的详细信息，请参阅 [SQL-CLR 自定义类型映射](sql-clr-custom-type-mappings.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-164">For more information about custom type mapping, see [SQL-CLR Custom Type Mappings](sql-clr-custom-type-mappings.md).</span></span>  
  
 <span data-ttu-id="ff980-165">因为用于枚举的 SQL 列将与其他数字和文本列的类型相同;这些工具不会识别你的意图，并按以下 [数字映射](#NumericMapping) 和 [文本和 XML 映射](#TextMapping) 部分所述的方式进行映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-165">Because a SQL column intended for enumeration will be of the same type as other numeric and text columns; these tools will not recognize your intent and default to mapping as described in the following [Numeric Mapping](#NumericMapping) and [Text and XML Mapping](#TextMapping) sections.</span></span> <span data-ttu-id="ff980-166">有关生成带 DBML 文件的代码的详细信息，请参阅 [LINQ to SQL 中的代码生成](code-generation-in-linq-to-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-166">For more information about generating code with the DBML file, see [Code Generation in LINQ to SQL](code-generation-in-linq-to-sql.md).</span></span>  
  
 <span data-ttu-id="ff980-167"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法创建一个数值类型的 SQL 列以映射 CLR <xref:System.Enum?displayProperty=nameWithType> 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-167">The <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method creates a SQL column of numeric type to map a CLR <xref:System.Enum?displayProperty=nameWithType> type.</span></span>  
  
<a name="NumericMapping"></a>

## <a name="numeric-mapping"></a><span data-ttu-id="ff980-168">数值映射</span><span class="sxs-lookup"><span data-stu-id="ff980-168">Numeric Mapping</span></span>  

 <span data-ttu-id="ff980-169">LINQ to SQL 允许您映射多种 CLR 和 SQL Server 数值类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-169">LINQ to SQL lets you map many CLR and SQL Server numeric types.</span></span> <span data-ttu-id="ff980-170">下表显示生成基于数据库的对象模型或外部映射文件时 O/R 设计器和 SQLMetal 选择的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-170">The following table shows the CLR types that O/R Designer and SQLMetal select when building an object model or external mapping file based on your database.</span></span>  
  
|<span data-ttu-id="ff980-171">SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-171">SQL Server Type</span></span>|<span data-ttu-id="ff980-172">O/R 设计器和 SQLMetal 使用的默认 CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-172">Default CLR Type mapping used by O/R Designer and SQLMetal</span></span>|  
|---------------------|-----------------------------------------------------------------|  
|`BIT`|<xref:System.Boolean?displayProperty=nameWithType>|  
|`TINYINT`|<xref:System.Int16?displayProperty=nameWithType>|  
|`INT`|<xref:System.Int32?displayProperty=nameWithType>|  
|`BIGINT`|<xref:System.Int64?displayProperty=nameWithType>|  
|`SMALLMONEY`|<xref:System.Decimal?displayProperty=nameWithType>|  
|`MONEY`|<xref:System.Decimal?displayProperty=nameWithType>|  
|`DECIMAL`|<xref:System.Decimal?displayProperty=nameWithType>|  
|`NUMERIC`|<xref:System.Decimal?displayProperty=nameWithType>|  
|`REAL/FLOAT(24)`|<xref:System.Single?displayProperty=nameWithType>|  
|`FLOAT/FLOAT(53)`|<xref:System.Double?displayProperty=nameWithType>|  
  
 <span data-ttu-id="ff980-173">下一个表显示 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法使用的默认类型映射，以定义创建何种 SQL 列来映射到对象模型或外部映射文件中定义的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-173">The next table shows the default type mappings used by the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method to define which type of SQL columns are created to map to the CLR types defined in your object model or external mapping file.</span></span>  
  
|<span data-ttu-id="ff980-174">CLR 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-174">CLR Type</span></span>|<span data-ttu-id="ff980-175"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 使用的默认 SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-175">Default SQL Server Type used by <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType></span></span>|  
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Boolean?displayProperty=nameWithType>|`BIT`|  
|<xref:System.Byte?displayProperty=nameWithType>|`TINYINT`|  
|<xref:System.Int16?displayProperty=nameWithType>|`SMALLINT`|  
|<xref:System.Int32?displayProperty=nameWithType>|`INT`|  
|<xref:System.Int64?displayProperty=nameWithType>|`BIGINT`|  
|<xref:System.SByte?displayProperty=nameWithType>|`SMALLINT`|  
|<xref:System.UInt16?displayProperty=nameWithType>|`INT`|  
|<xref:System.UInt32?displayProperty=nameWithType>|`BIGINT`|  
|<xref:System.UInt64?displayProperty=nameWithType>|`DECIMAL(20)`|  
|<xref:System.Decimal?displayProperty=nameWithType>|`DECIMAL(29,4)`|  
|<xref:System.Single?displayProperty=nameWithType>|`REAL`|  
|<xref:System.Double?displayProperty=nameWithType>|`FLOAT`|  
  
 <span data-ttu-id="ff980-176">有许多其他可以选择的数值映射，但是某些数值映射在转换到数据库或从数据库中转换时，可能会导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-176">There are many other numeric mappings you can choose, but some may result in overflow or data loss exceptions while translating to or from the database.</span></span> <span data-ttu-id="ff980-177">有关详细信息，请参阅 [类型映射运行时行为矩阵](#BehaviorMatrix)。</span><span class="sxs-lookup"><span data-stu-id="ff980-177">For more information, see the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix).</span></span>  
  
### <a name="decimal-and-money-types"></a><span data-ttu-id="ff980-178">Decimal 和 Money 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-178">Decimal and Money Types</span></span>  

 <span data-ttu-id="ff980-179">SQL Server 类型的默认精度 `DECIMAL` (小数点左和右的18个十进制数字) 比默认配对的 CLR 类型的精度小得多 <xref:System.Decimal?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="ff980-179">The default precision of SQL Server `DECIMAL` type (18 decimal digits to the left and right of the decimal point) is much smaller than the precision of the CLR <xref:System.Decimal?displayProperty=nameWithType> type that it is paired with by default.</span></span> <span data-ttu-id="ff980-180">这可导致将数据保存到数据库时的精度降低。</span><span class="sxs-lookup"><span data-stu-id="ff980-180">This can result in precision loss when you save data to the database.</span></span> <span data-ttu-id="ff980-181">但是，如果将 SQL Server `DECIMAL` 类型配置为大于 29 位精度，则会产生相反的结果。</span><span class="sxs-lookup"><span data-stu-id="ff980-181">However, just the opposite can happen if the SQL Server `DECIMAL` type is configured with greater than 29 digits of precision.</span></span> <span data-ttu-id="ff980-182">将 SQL Server `DECIMAL` 类型的精度配置为大于 CLR <xref:System.Decimal?displayProperty=nameWithType> 时，则在从数据库检索数据时会发生精度降低。</span><span class="sxs-lookup"><span data-stu-id="ff980-182">When a SQL Server `DECIMAL` type has been configured with a greater precision than the CLR <xref:System.Decimal?displayProperty=nameWithType>, precision loss can occur when retrieving data from the database.</span></span>  
  
 <span data-ttu-id="ff980-183">默认情况下和 CLR `MONEY` 类型成对使用的 SQL Server `SMALLMONEY` 和 <xref:System.Decimal?displayProperty=nameWithType> 具有非常小的精度，在将数据保存到数据库时可导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-183">The SQL Server `MONEY` and `SMALLMONEY` types, which are also paired with the CLR <xref:System.Decimal?displayProperty=nameWithType> type by default, have a much smaller precision, which can result in overflow or data loss exceptions when saving data to the database.</span></span>  
  
<a name="TextMapping"></a>

## <a name="text-and-xml-mapping"></a><span data-ttu-id="ff980-184">文本和 XML 映射</span><span class="sxs-lookup"><span data-stu-id="ff980-184">Text and XML Mapping</span></span>  

 <span data-ttu-id="ff980-185">还有很多基于文本的类型和 XML 类型，您可以使用 LINQ to SQL 将其映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-185">There are also many text-based and XML types that you can map with LINQ to SQL.</span></span> <span data-ttu-id="ff980-186">下表显示生成基于数据库的对象模型或外部映射文件时 O/R 设计器和 SQLMetal 选择的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-186">The following table shows the CLR types that O/R Designer and SQLMetal select when building an object model or external mapping file based on your database.</span></span>  
  
|<span data-ttu-id="ff980-187">SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-187">SQL Server Type</span></span>|<span data-ttu-id="ff980-188">O/R 设计器和 SQLMetal 使用的默认 CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-188">Default CLR Type mapping used by O/R Designer and SQLMetal</span></span>|  
|---------------------|-----------------------------------------------------------------|  
|`CHAR`|<xref:System.String?displayProperty=nameWithType>|  
|`NCHAR`|<xref:System.String?displayProperty=nameWithType>|  
|`VARCHAR`|<xref:System.String?displayProperty=nameWithType>|  
|`NVARCHAR`|<xref:System.String?displayProperty=nameWithType>|  
|`TEXT`|<xref:System.String?displayProperty=nameWithType>|  
|`NTEXT`|<xref:System.String?displayProperty=nameWithType>|  
|`XML`|<xref:System.Xml.Linq.XElement?displayProperty=nameWithType>|  
  
 <span data-ttu-id="ff980-189">下一个表显示 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法使用的默认类型映射，以定义创建何种 SQL 列来映射到对象模型或外部映射文件中定义的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-189">The next table shows the default type mappings used by the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method to define which type of SQL columns are created to map to the CLR types defined in your object model or external mapping file.</span></span>  
  
|<span data-ttu-id="ff980-190">CLR 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-190">CLR Type</span></span>|<span data-ttu-id="ff980-191"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 使用的默认 SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-191">Default SQL Server Type used by <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType></span></span>|  
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Char?displayProperty=nameWithType>|`NCHAR(1)`|  
|<xref:System.String?displayProperty=nameWithType>|`NVARCHAR(4000)`|  
|<span data-ttu-id="ff980-192"><xref:System.Char?displayProperty=nameWithType>[]</span><span class="sxs-lookup"><span data-stu-id="ff980-192"><xref:System.Char?displayProperty=nameWithType>[]</span></span>|`NVARCHAR(4000)`|  
|<span data-ttu-id="ff980-193">实现 `Parse()` 和 `ToString()` 的自定义类型</span><span class="sxs-lookup"><span data-stu-id="ff980-193">Custom type implementing `Parse()` and `ToString()`</span></span>|`NVARCHAR(MAX)`|  
  
 <span data-ttu-id="ff980-194">有许多其他可以选择的基于文本的映射和 XML 映射，但是某些映射在转换到数据库或从数据库中转换时，可能会导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-194">There are many other text-based and XML mappings you can choose, but some may result in overflow or data loss exceptions while translating to or from the database.</span></span> <span data-ttu-id="ff980-195">有关详细信息，请参阅 [类型映射运行时行为矩阵](#BehaviorMatrix)。</span><span class="sxs-lookup"><span data-stu-id="ff980-195">For more information, see the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix).</span></span>  
  
### <a name="xml-types"></a><span data-ttu-id="ff980-196">XML 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-196">XML Types</span></span>  

 <span data-ttu-id="ff980-197">从 Microsoft SQL Server 2005 开始，提供了 SQL Server `XML` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-197">The SQL Server `XML` data type is available starting in Microsoft SQL Server 2005.</span></span> <span data-ttu-id="ff980-198">您可以将 SQL Server `XML` 数据类型映射到 <xref:System.Xml.Linq.XElement>、<xref:System.Xml.Linq.XDocument> 或 <xref:System.String>。</span><span class="sxs-lookup"><span data-stu-id="ff980-198">You can map the SQL Server `XML` data type to <xref:System.Xml.Linq.XElement>, <xref:System.Xml.Linq.XDocument>, or <xref:System.String>.</span></span> <span data-ttu-id="ff980-199">如果列中存储了无法读入 <xref:System.Xml.Linq.XElement> 的 XML 片段，则此列必须映射到 <xref:System.String> 以免出现运行时错误。</span><span class="sxs-lookup"><span data-stu-id="ff980-199">If the column stores XML fragments that cannot be read into <xref:System.Xml.Linq.XElement>, the column must be mapped to <xref:System.String> to avoid run-time errors.</span></span> <span data-ttu-id="ff980-200">必须映射到 <xref:System.String> 的 XML 片段包括：</span><span class="sxs-lookup"><span data-stu-id="ff980-200">XML fragments that must be mapped to <xref:System.String> include the following:</span></span>  
  
- <span data-ttu-id="ff980-201">XML 元素的序列。</span><span class="sxs-lookup"><span data-stu-id="ff980-201">A sequence of XML elements</span></span>  
  
- <span data-ttu-id="ff980-202">特性</span><span class="sxs-lookup"><span data-stu-id="ff980-202">Attributes</span></span>  
  
- <span data-ttu-id="ff980-203">公共标识符 (PI)</span><span class="sxs-lookup"><span data-stu-id="ff980-203">Public Identifiers (PI)</span></span>  
  
- <span data-ttu-id="ff980-204">注释</span><span class="sxs-lookup"><span data-stu-id="ff980-204">Comments</span></span>  
  
 <span data-ttu-id="ff980-205">尽管可以 <xref:System.Xml.Linq.XElement> <xref:System.Xml.Linq.XDocument> 按 [类型映射运行时行为矩阵](#BehaviorMatrix)中所示的方式映射和到 SQL Server，但此 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法没有适用于这些类型的默认 SQL Server 类型映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-205">Although you can map <xref:System.Xml.Linq.XElement> and <xref:System.Xml.Linq.XDocument> to SQL Server as shown in the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix), the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method has no default SQL Server type mapping for these types.</span></span>  
  
### <a name="custom-types"></a><span data-ttu-id="ff980-206">自定义类型</span><span class="sxs-lookup"><span data-stu-id="ff980-206">Custom Types</span></span>  

 <span data-ttu-id="ff980-207">如果类实现了 `Parse()` 和 `ToString()` ，则可以将对象映射到任何 SQL 文本类型 (`CHAR` 、 `NCHAR` 、 `VARCHAR` 、 `NVARCHAR` 、、、 `TEXT` `NTEXT` `XML`) 。</span><span class="sxs-lookup"><span data-stu-id="ff980-207">If a class implements `Parse()` and `ToString()`, you can map the object to any SQL text type (`CHAR`, `NCHAR`, `VARCHAR`, `NVARCHAR`, `TEXT`, `NTEXT`, `XML`).</span></span> <span data-ttu-id="ff980-208">通过将 `ToString()` 返回的值发送到映射的数据库列，把对象存储在数据库中。</span><span class="sxs-lookup"><span data-stu-id="ff980-208">The object is stored in the database by sending the value returned by `ToString()` to the mapped database column.</span></span> <span data-ttu-id="ff980-209">通过在数据库返回的字符串上调用 `Parse()` 重新构造对象。</span><span class="sxs-lookup"><span data-stu-id="ff980-209">The object is reconstructed by invoking `Parse()` on the string returned by the database.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ff980-210">LINQ to SQL 不支持使用 <xref:System.Xml.Serialization.IXmlSerializable?displayProperty=nameWithType> 进行序列化。</span><span class="sxs-lookup"><span data-stu-id="ff980-210">LINQ to SQL does not support serialization by using <xref:System.Xml.Serialization.IXmlSerializable?displayProperty=nameWithType>.</span></span>  
  
<a name="DateMapping"></a>

## <a name="date-and-time-mapping"></a><span data-ttu-id="ff980-211">日期和时间映射</span><span class="sxs-lookup"><span data-stu-id="ff980-211">Date and Time Mapping</span></span>  

 <span data-ttu-id="ff980-212">通过使用 LINQ to SQL，您可以映射多种 SQL Server 日期和时间类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-212">With LINQ to SQL, you can map many SQL Server date and time types.</span></span> <span data-ttu-id="ff980-213">下表显示生成基于数据库的对象模型或外部映射文件时 O/R 设计器和 SQLMetal 选择的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-213">The following table shows the CLR types that O/R Designer and SQLMetal select when building an object model or external mapping file based on your database.</span></span>  
  
|<span data-ttu-id="ff980-214">SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-214">SQL Server Type</span></span>|<span data-ttu-id="ff980-215">O/R 设计器和 SQLMetal 使用的默认 CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-215">Default CLR Type mapping used by O/R Designer and SQLMetal</span></span>|  
|---------------------|-----------------------------------------------------------------|  
|`SMALLDATETIME`|<xref:System.DateTime?displayProperty=nameWithType>|  
|`DATETIME`|<xref:System.DateTime?displayProperty=nameWithType>|  
|`DATETIME2`|<xref:System.DateTime?displayProperty=nameWithType>|  
|`DATETIMEOFFSET`|<xref:System.DateTimeOffset?displayProperty=nameWithType>|  
|`DATE`|<xref:System.DateTime?displayProperty=nameWithType>|  
|`TIME`|<xref:System.TimeSpan?displayProperty=nameWithType>|  
  
 <span data-ttu-id="ff980-216">下一个表显示 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法使用的默认类型映射，以定义创建何种 SQL 列来映射到对象模型或外部映射文件中定义的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-216">The next table shows the default type mappings used by the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method to define which type of SQL columns are created to map to the CLR types defined in your object model or external mapping file.</span></span>  
  
|<span data-ttu-id="ff980-217">CLR 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-217">CLR Type</span></span>|<span data-ttu-id="ff980-218"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 使用的默认 SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-218">Default SQL Server Type used by <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType></span></span>|  
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.DateTime?displayProperty=nameWithType>|`DATETIME`|  
|<xref:System.DateTimeOffset?displayProperty=nameWithType>|`DATETIMEOFFSET`|  
|<xref:System.TimeSpan?displayProperty=nameWithType>|`TIME`|  
  
 <span data-ttu-id="ff980-219">有许多其他可以选择的日期和时间映射，但是某些映射在转换到数据库或从数据库中转换时，可能会导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-219">There are many other date and time mappings you can choose, but some may result in overflow or data loss exceptions while translating to or from the database.</span></span> <span data-ttu-id="ff980-220">有关详细信息，请参阅 [类型映射运行时行为矩阵](#BehaviorMatrix)。</span><span class="sxs-lookup"><span data-stu-id="ff980-220">For more information, see the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ff980-221">从 Microsoft SQL Server 2008 开始，提供了 SQL Server 类型 `DATETIME2`、`DATETIMEOFFSET`、`DATE` 和 `TIME`。</span><span class="sxs-lookup"><span data-stu-id="ff980-221">The SQL Server types `DATETIME2`, `DATETIMEOFFSET`, `DATE`, and `TIME` are available starting with Microsoft SQL Server 2008.</span></span> <span data-ttu-id="ff980-222">从 .NET Framework 版本 3.5 SP1 开始，LINQ to SQL 支持映射到这些新类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-222">LINQ to SQL supports mapping to these new types starting with the .NET Framework version 3.5 SP1.</span></span>  
  
### <a name="systemdatetime"></a><span data-ttu-id="ff980-223">System.Datetime</span><span class="sxs-lookup"><span data-stu-id="ff980-223">System.Datetime</span></span>  

 <span data-ttu-id="ff980-224">CLR <xref:System.DateTime?displayProperty=nameWithType> 类型的范围和精度大于 SQL Server `DATETIME` 类型，这是 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法的默认类型映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-224">The range and precision of the CLR <xref:System.DateTime?displayProperty=nameWithType> type is greater than the range and precision of the SQL Server `DATETIME` type, which is the default type mapping for the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="ff980-225">要避免与 `DATETIME` 范围之外的日期相关的异常，请使用 `DATETIME2`（从 Microsoft SQL Server 2008 开始可用）。</span><span class="sxs-lookup"><span data-stu-id="ff980-225">To help avoid exceptions related to dates outside the range of `DATETIME`, use `DATETIME2`, which is available starting with Microsoft SQL Server 2008.</span></span> <span data-ttu-id="ff980-226">`DATETIME2` 可以与 CLR 的范围和精度相匹配 <xref:System.DateTime?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="ff980-226">`DATETIME2` can match the range and precision of the CLR <xref:System.DateTime?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="ff980-227">SQL Server 日期不具有 <xref:System.TimeZone>（CLR 中得到充分支持的一种功能）的概念。</span><span class="sxs-lookup"><span data-stu-id="ff980-227">SQL Server dates have no concept of <xref:System.TimeZone>, a feature that is richly supported in the CLR.</span></span> <span data-ttu-id="ff980-228">无论原始 <xref:System.TimeZone> 信息如何，<xref:System.TimeZone> 值均不进行 <xref:System.DateTimeKind> 转换，按原样保存到数据库中。</span><span class="sxs-lookup"><span data-stu-id="ff980-228"><xref:System.TimeZone> values are saved as is to the database without <xref:System.TimeZone> conversion, regardless of the original <xref:System.DateTimeKind> information.</span></span> <span data-ttu-id="ff980-229">从数据库中检索到 <xref:System.DateTime> 值时，它们的值按原样加载到 <xref:System.DateTime> 为 <xref:System.DateTimeKind> 的 <xref:System.DateTimeKind.Unspecified> 中。</span><span class="sxs-lookup"><span data-stu-id="ff980-229">When <xref:System.DateTime> values are retrieved from the database, their value is loaded as is into a <xref:System.DateTime> with a <xref:System.DateTimeKind> of <xref:System.DateTimeKind.Unspecified>.</span></span> <span data-ttu-id="ff980-230">有关支持的方法的详细信息 <xref:System.DateTime?displayProperty=nameWithType> ，请参阅 [system.web 方法](system-datetime-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-230">For more information about supported <xref:System.DateTime?displayProperty=nameWithType> methods, see [System.DateTime Methods](system-datetime-methods.md).</span></span>  
  
### <a name="systemtimespan"></a><span data-ttu-id="ff980-231">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ff980-231">System.TimeSpan</span></span>  

 <span data-ttu-id="ff980-232">Microsoft SQL Server 2008 和 .NET Framework 3.5 SP1 允许您将 CLR <xref:System.TimeSpan?displayProperty=nameWithType> 类型映射到 SQL Server `TIME` 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-232">Microsoft SQL Server 2008 and the .NET Framework 3.5 SP1 let you map the CLR <xref:System.TimeSpan?displayProperty=nameWithType> type to the SQL Server `TIME` type.</span></span> <span data-ttu-id="ff980-233">但是，CLR <xref:System.TimeSpan?displayProperty=nameWithType> 支持的范围和 SQL Server `TIME` 类型支持的范围之间存在很大的差异。</span><span class="sxs-lookup"><span data-stu-id="ff980-233">However, there is a large difference between the range that the CLR <xref:System.TimeSpan?displayProperty=nameWithType> supports and what the SQL Server `TIME` type supports.</span></span> <span data-ttu-id="ff980-234">SQL `TIME` 的映射值小于 0 或大于 23:59:59.9999999 小时将导致溢出异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-234">Mapping values less than 0 or greater than 23:59:59.9999999 hours to the SQL `TIME` will result in overflow exceptions.</span></span> <span data-ttu-id="ff980-235">有关详细信息，请参阅 [System.web 方法](system-timespan-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-235">For more information, see [System.TimeSpan Methods](system-timespan-methods.md).</span></span>  
  
 <span data-ttu-id="ff980-236">在 Microsoft SQL Server 2000 和 SQL Server 2005 中，您无法将数据库字段映射到 <xref:System.TimeSpan>。</span><span class="sxs-lookup"><span data-stu-id="ff980-236">In Microsoft SQL Server 2000 and SQL Server 2005, you cannot map database fields to <xref:System.TimeSpan>.</span></span> <span data-ttu-id="ff980-237">但是，支持对 <xref:System.TimeSpan> 的操作，原因是可以通过 <xref:System.TimeSpan> 减法运算返回 <xref:System.DateTime> 值或将这些值作为文本或绑定变量引入表达式。</span><span class="sxs-lookup"><span data-stu-id="ff980-237">However, operations on <xref:System.TimeSpan> are supported because <xref:System.TimeSpan> values can be returned from <xref:System.DateTime> subtraction or introduced into an expression as a literal or bound variable.</span></span>  
  
<a name="BinaryMapping"></a>

## <a name="binary-mapping"></a><span data-ttu-id="ff980-238">二进制映射</span><span class="sxs-lookup"><span data-stu-id="ff980-238">Binary Mapping</span></span>  

 <span data-ttu-id="ff980-239">还有很多可以映射到 CLR 类型 <xref:System.Data.Linq.Binary?displayProperty=nameWithType> 的 SQL Server 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-239">There are many SQL Server types that can map to the CLR type <xref:System.Data.Linq.Binary?displayProperty=nameWithType>.</span></span> <span data-ttu-id="ff980-240">下表显示生成基于数据库的对象模型或外部映射文件时使 O/R 设计器和 SQLMetal 定义 CLR <xref:System.Data.Linq.Binary?displayProperty=nameWithType> 类型的 SQL Server 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-240">The following table shows the SQL Server types that cause O/R Designer and SQLMetal to define a CLR <xref:System.Data.Linq.Binary?displayProperty=nameWithType> type when building an object model or external mapping file based on your database.</span></span>  
  
|<span data-ttu-id="ff980-241">SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-241">SQL Server Type</span></span>|<span data-ttu-id="ff980-242">O/R 设计器和 SQLMetal 使用的默认 CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-242">Default CLR Type mapping used by O/R Designer and SQLMetal</span></span>|  
|---------------------|-----------------------------------------------------------------|  
|`BINARY(50)`|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
|`VARBINARY(50)`|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
|`VARBINARY(MAX)`|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
|<span data-ttu-id="ff980-243">`VARBINARY(MAX)` 具有 `FILESTREAM` 属性</span><span class="sxs-lookup"><span data-stu-id="ff980-243">`VARBINARY(MAX)` with the `FILESTREAM` attribute</span></span>|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
|`IMAGE`|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
|`TIMESTAMP`|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|  
  
 <span data-ttu-id="ff980-244">下一个表显示 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法使用的默认类型映射，以定义创建何种 SQL 列来映射到对象模型或外部映射文件中定义的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-244">The next table shows the default type mappings used by the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method to define which type of SQL columns are created to map to the CLR types defined in your object model or external mapping file.</span></span>  
  
|<span data-ttu-id="ff980-245">CLR 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-245">CLR Type</span></span>|<span data-ttu-id="ff980-246"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 使用的默认 SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-246">Default SQL Server Type used by <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType></span></span>|  
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Data.Linq.Binary?displayProperty=nameWithType>|`VARBINARY(MAX)`|  
|<xref:System.Byte?displayProperty=nameWithType>|`VARBINARY(MAX)`|  
|<xref:System.Runtime.Serialization.ISerializable?displayProperty=nameWithType>|`VARBINARY(MAX)`|  
  
 <span data-ttu-id="ff980-247">有许多其他可以选择的二进制映射，但是某些映射在转换到数据库或从数据库中转换时，可能会导致溢出或数据丢失异常。</span><span class="sxs-lookup"><span data-stu-id="ff980-247">There are many other binary mappings you can choose, but some may result in overflow or data loss exceptions while translating to or from the database.</span></span> <span data-ttu-id="ff980-248">有关详细信息，请参阅 [类型映射运行时行为矩阵](#BehaviorMatrix)。</span><span class="sxs-lookup"><span data-stu-id="ff980-248">For more information, see the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix).</span></span>  
  
### <a name="sql-server-filestream"></a><span data-ttu-id="ff980-249">SQL Server FILESTREAM</span><span class="sxs-lookup"><span data-stu-id="ff980-249">SQL Server FILESTREAM</span></span>  

 <span data-ttu-id="ff980-250">从 Microsoft SQL Server 2008 开始，提供了 `FILESTREAM` 列的 `VARBINARY(MAX)` 属性；从 .NET Framework 版本 3.5 SP1 开始，您可以使用 LINQ to SQL 映射到该属性。</span><span class="sxs-lookup"><span data-stu-id="ff980-250">The `FILESTREAM` attribute for `VARBINARY(MAX)` columns is available starting with Microsoft SQL Server 2008; you can map to it with LINQ to SQL starting with the .NET Framework version 3.5 SP1.</span></span>  
  
 <span data-ttu-id="ff980-251">尽管您可以使用 `VARBINARY(MAX)` 属性将 `FILESTREAM` 列映射到 <xref:System.Data.Linq.Binary> 对象，但是 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法无法使用 `FILESTREAM` 属性自动创建列。</span><span class="sxs-lookup"><span data-stu-id="ff980-251">Although you can map `VARBINARY(MAX)` columns with the `FILESTREAM` attribute to <xref:System.Data.Linq.Binary> objects, the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method is unable to automatically create columns with the `FILESTREAM` attribute.</span></span> <span data-ttu-id="ff980-252">有关的详细信息 `FILESTREAM` ，请参阅 [FILESTREAM 概述](/previous-versions/sql/sql-server-2008-r2/bb933993(v=sql.105))。</span><span class="sxs-lookup"><span data-stu-id="ff980-252">For more information about `FILESTREAM`, see [FILESTREAM Overview](/previous-versions/sql/sql-server-2008-r2/bb933993(v=sql.105)).</span></span>  
  
<a name="BinarySerialization"></a>

### <a name="binary-serialization"></a><span data-ttu-id="ff980-253">二进制序列化</span><span class="sxs-lookup"><span data-stu-id="ff980-253">Binary Serialization</span></span>  

 <span data-ttu-id="ff980-254">如果一个类实现了 <xref:System.Runtime.Serialization.ISerializable> 接口，则可以将对象序列化到任何 SQL 二进制字段 (`BINARY`、`VARBINARY`、`IMAGE`)。</span><span class="sxs-lookup"><span data-stu-id="ff980-254">If a class implements the <xref:System.Runtime.Serialization.ISerializable> interface, you can serialize an object to any SQL binary field (`BINARY`, `VARBINARY`, `IMAGE`).</span></span> <span data-ttu-id="ff980-255">将根据如何实现 <xref:System.Runtime.Serialization.ISerializable> 接口来对对象进行序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="ff980-255">The object is serialized and deserialized according to how the <xref:System.Runtime.Serialization.ISerializable> interface is implemented.</span></span> <span data-ttu-id="ff980-256">有关详细信息，请参阅 [二进制序列化](../../../../../standard/serialization/binary-serialization.md)。</span><span class="sxs-lookup"><span data-stu-id="ff980-256">For more information, see [Binary Serialization](../../../../../standard/serialization/binary-serialization.md).</span></span>
  
<a name="MiscMapping"></a>

## <a name="miscellaneous-mapping"></a><span data-ttu-id="ff980-257">杂项映射</span><span class="sxs-lookup"><span data-stu-id="ff980-257">Miscellaneous Mapping</span></span>  

 <span data-ttu-id="ff980-258">下表显示一些尚未提及的杂项类型的默认类型映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-258">The following table shows the default type mappings for some miscellaneous types that have not yet been mentioned.</span></span> <span data-ttu-id="ff980-259">下表显示生成基于数据库的对象模型或外部映射文件时 O/R 设计器和 SQLMetal 选择的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-259">The following table shows the CLR types that O/R Designer and SQLMetal select when building an object model or external mapping file based on your database.</span></span>  
  
|<span data-ttu-id="ff980-260">SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-260">SQL Server Type</span></span>|<span data-ttu-id="ff980-261">O/R 设计器和 SQLMetal 使用的默认 CLR 类型映射</span><span class="sxs-lookup"><span data-stu-id="ff980-261">Default CLR Type mapping used by O/R Designer and SQLMetal</span></span>|  
|---------------------|-----------------------------------------------------------------|  
|`UNIQUEIDENTIFIER`|<xref:System.Guid?displayProperty=nameWithType>|  
|`SQL_VARIANT`|<xref:System.Object?displayProperty=nameWithType>|  
  
 <span data-ttu-id="ff980-262">下一个表显示 <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 方法使用的默认类型映射，以定义创建何种 SQL 列来映射到对象模型或外部映射文件中定义的 CLR 类型。</span><span class="sxs-lookup"><span data-stu-id="ff980-262">The next table shows the default type mappings used by the <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> method to define which type of SQL columns are created to map to the CLR types defined in your object model or external mapping file.</span></span>  
  
|<span data-ttu-id="ff980-263">CLR 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-263">CLR Type</span></span>|<span data-ttu-id="ff980-264"><xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType> 使用的默认 SQL Server 类型</span><span class="sxs-lookup"><span data-stu-id="ff980-264">Default SQL Server Type used by <xref:System.Data.Linq.DataContext.CreateDatabase%2A?displayProperty=nameWithType></span></span>|  
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Guid?displayProperty=nameWithType>|`UNIQUEIDENTIFIER`|  
|<xref:System.Object?displayProperty=nameWithType>|`SQL_VARIANT`|  
  
 <span data-ttu-id="ff980-265">LINQ to SQL 不支持这些杂项类型的任何其他类型映射。</span><span class="sxs-lookup"><span data-stu-id="ff980-265">LINQ to SQL does not support any other type mappings for these miscellaneous types.</span></span>  <span data-ttu-id="ff980-266">有关详细信息，请参阅 [类型映射运行时行为矩阵](#BehaviorMatrix)。</span><span class="sxs-lookup"><span data-stu-id="ff980-266">For more information, see the [Type Mapping Run Time Behavior Matrix](#BehaviorMatrix).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff980-267">请参阅</span><span class="sxs-lookup"><span data-stu-id="ff980-267">See also</span></span>

- [<span data-ttu-id="ff980-268">基于特性的映射</span><span class="sxs-lookup"><span data-stu-id="ff980-268">Attribute-Based Mapping</span></span>](attribute-based-mapping.md)
- [<span data-ttu-id="ff980-269">外部映射</span><span class="sxs-lookup"><span data-stu-id="ff980-269">External Mapping</span></span>](external-mapping.md)
- [<span data-ttu-id="ff980-270">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="ff980-270">Data Types and Functions</span></span>](data-types-and-functions.md)
- [<span data-ttu-id="ff980-271">SQL-CLR 类型不匹配</span><span class="sxs-lookup"><span data-stu-id="ff980-271">SQL-CLR Type Mismatches</span></span>](sql-clr-type-mismatches.md)
