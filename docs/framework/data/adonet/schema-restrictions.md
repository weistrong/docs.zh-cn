---
description: 了解详细信息：架构限制
title: 架构限制
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 73d2980e-e73c-4987-913a-8ddc93d09144
ms.openlocfilehash: 74ddfe5b8aaf9b8193e0c0b2a929ccde333eac26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719040"
---
# <a name="schema-restrictions"></a><span data-ttu-id="35944-103">架构限制</span><span class="sxs-lookup"><span data-stu-id="35944-103">Schema Restrictions</span></span>

<span data-ttu-id="35944-104">GetSchema 方法的第二个可选参数是用于限制返回的架构信息量的限制，该参数以字符串数组的形式传递给 GetSchema 方法 。</span><span class="sxs-lookup"><span data-stu-id="35944-104">The second optional parameter of the **GetSchema** method is the restrictions that are used to limit the amount of schema information returned, and it is passed to the **GetSchema** method as an array of strings.</span></span> <span data-ttu-id="35944-105">在数组中的位置确定可以传递的值，这等效于限制数。</span><span class="sxs-lookup"><span data-stu-id="35944-105">The position in the array determines the values that you can pass, and this is equivalent to the restriction number.</span></span>  
  
 <span data-ttu-id="35944-106">例如，下表说明使用适用于 SQL Server 的 .NET Framework 数据提供程序时“Tables”架构集合支持的限制。</span><span class="sxs-lookup"><span data-stu-id="35944-106">For example, the following table describes the restrictions supported by the "Tables" schema collection using the .NET Framework Data Provider for SQL Server.</span></span> <span data-ttu-id="35944-107">SQL Server 架构集合的其他限制在本主题的结尾处列出。</span><span class="sxs-lookup"><span data-stu-id="35944-107">Additional restrictions for SQL Server schema collections are listed at the end of this topic.</span></span>  
  
|<span data-ttu-id="35944-108">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-108">Restriction Name</span></span>|<span data-ttu-id="35944-109">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-109">Parameter Name</span></span>|<span data-ttu-id="35944-110">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-110">Restriction Default</span></span>|<span data-ttu-id="35944-111">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-111">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-112">目录</span><span class="sxs-lookup"><span data-stu-id="35944-112">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-113">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-113">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-114">1</span><span class="sxs-lookup"><span data-stu-id="35944-114">1</span></span>|  
|<span data-ttu-id="35944-115">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-115">Owner</span></span>|@Owner|<span data-ttu-id="35944-116">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-116">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-117">2</span><span class="sxs-lookup"><span data-stu-id="35944-117">2</span></span>|  
|<span data-ttu-id="35944-118">表</span><span class="sxs-lookup"><span data-stu-id="35944-118">Table</span></span>|@Name|<span data-ttu-id="35944-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-119">TABLE_NAME</span></span>|<span data-ttu-id="35944-120">3</span><span class="sxs-lookup"><span data-stu-id="35944-120">3</span></span>|  
|<span data-ttu-id="35944-121">TableType</span><span class="sxs-lookup"><span data-stu-id="35944-121">TableType</span></span>|@TableType|<span data-ttu-id="35944-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="35944-122">TABLE_TYPE</span></span>|<span data-ttu-id="35944-123">4</span><span class="sxs-lookup"><span data-stu-id="35944-123">4</span></span>|  
  
## <a name="specifying-restriction-values"></a><span data-ttu-id="35944-124">指定限制值</span><span class="sxs-lookup"><span data-stu-id="35944-124">Specifying Restriction Values</span></span>  

 <span data-ttu-id="35944-125">要使用“Tables”架构集合的一个限制，只需创建一个包含四个元素的字符串数组，然后在与限制数匹配的元素中填充值。</span><span class="sxs-lookup"><span data-stu-id="35944-125">To use one of the restrictions of the "Tables" schema collection, simply create an array of strings with four elements, then place a value in the element that matches the restriction number.</span></span> <span data-ttu-id="35944-126">例如，要将 GetSchema 方法返回的表限制为仅返回“Sales”架构中的表，可将数组的第二个元素设置为“Sales”，然后再将其传递给 GetSchema 方法 。</span><span class="sxs-lookup"><span data-stu-id="35944-126">For example, to restrict the tables returned by the **GetSchema** method to only those tables in the "Sales" schema, set the second element of the array to "Sales" before passing it to the **GetSchema** method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="35944-127">`SqlClient` 和 `OracleClient` 的限制集合还有附加的 `ParameterName` 列。</span><span class="sxs-lookup"><span data-stu-id="35944-127">The restrictions collections for `SqlClient` and `OracleClient` have an additional `ParameterName` column.</span></span> <span data-ttu-id="35944-128">为了向后兼容，仍提供限制默认列，但是目前忽略该列。</span><span class="sxs-lookup"><span data-stu-id="35944-128">The restriction default column is still there for backwards compatibility, but is currently ignored.</span></span> <span data-ttu-id="35944-129">在指定限制值时，应使用参数化查询（而不是字符串替换）来最大程度地降低受到 SQL 注入式攻击的风险。</span><span class="sxs-lookup"><span data-stu-id="35944-129">Parameterized queries rather than string replacement should be used to minimize the risk of an SQL injection attack when specifying restriction values.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="35944-130">数组中的元素数必须小于或等于指定架构集合支持的限制数，否则，将引发 <xref:System.ArgumentException>。</span><span class="sxs-lookup"><span data-stu-id="35944-130">The number of elements in the array must be less than or equal to the number of restrictions supported for the specified schema collection else an <xref:System.ArgumentException> will be thrown.</span></span> <span data-ttu-id="35944-131">可以小于最大限制数。</span><span class="sxs-lookup"><span data-stu-id="35944-131">There can be fewer than the maximum number of restrictions.</span></span> <span data-ttu-id="35944-132">缺少的限制假定为空（无限制）。</span><span class="sxs-lookup"><span data-stu-id="35944-132">The missing restrictions are assumed to be null (unrestricted).</span></span>  
  
 <span data-ttu-id="35944-133">可以通过将 **GetSchema** 方法与限制架构集合的名称（即 "限制"）一起调用，来 .NET Framework 查询受支持的限制列表。</span><span class="sxs-lookup"><span data-stu-id="35944-133">You can query a .NET Framework managed provider to determine the list of supported restrictions by calling the **GetSchema** method with the name of the restrictions schema collection, which is "Restrictions".</span></span> <span data-ttu-id="35944-134">此时将返回 <xref:System.Data.DataTable>，包含集合名称、限制名称、默认限制值和限制数的列表。</span><span class="sxs-lookup"><span data-stu-id="35944-134">This will return a <xref:System.Data.DataTable> with a list of the collection names, the restriction names, the default restriction values, and the restriction numbers.</span></span>  
  
### <a name="example"></a><span data-ttu-id="35944-135">示例</span><span class="sxs-lookup"><span data-stu-id="35944-135">Example</span></span>  

 <span data-ttu-id="35944-136">下面的示例演示如何使用 <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> SQL Server 类的 .NET Framework 数据提供程序的方法 <xref:System.Data.SqlClient.SqlConnection> 来检索与 **AdventureWorks** 示例数据库中包含的所有表有关的架构信息，并将返回的信息仅限于 "Sales" 架构中的表：</span><span class="sxs-lookup"><span data-stu-id="35944-136">The following examples demonstrate how to use the <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of the .NET Framework Data Provider for the SQL Server <xref:System.Data.SqlClient.SqlConnection> class to retrieve schema information about all of the tables contained in the **AdventureWorks** sample database, and to restrict the information returned to only those tables in the "Sales" schema:</span></span>  
  
```vb  
Imports System.Data.SqlClient  
  
Module Module1  
Sub Main()  
  Dim connectionString As String = _  
    "Data Source=(local);Database=AdventureWorks;" & _  
       "Integrated Security=true;";  
  
  Dim restrictions(3) As String  
  Using connection As New SqlConnection(connectionString)  
    connection.Open()  
  
    'Specify the restrictions.  
    restrictions(1) = "Sales"  
    Dim table As DataTable = connection.GetSchema("Tables", _  
       restrictions)  
  
    ' Display the contents of the table.  
      For Each row As DataRow In table.Rows  
         For Each col As DataColumn In table.Columns  
            Console.WriteLine("{0} = {1}", col.ColumnName, row(col))  
         Next  
         Console.WriteLine("============================")  
      Next  
    Console.WriteLine("Press any key to continue.")  
    Console.ReadKey()  
  End Using  
End Sub  
End Module  
```  
  
```csharp  
using System;  
using System.Data;  
using System.Data.SqlClient;  
  
class Program  
{  
  static void Main()  
  {  
    string connectionString =
       "Data Source=(local);Database=AdventureWorks;" +  
       "Integrated Security=true;";  
    using (SqlConnection connection =  
       new SqlConnection(connectionString))  
    {  
        connection.Open();  
  
        // Specify the restrictions.  
        string[] restrictions = new string[4];  
        restrictions[1] = "Sales";  
        System.Data.DataTable table = connection.GetSchema(  
          "Tables", restrictions);  
  
        // Display the contents of the table.  
        foreach (System.Data.DataRow row in table.Rows)  
        {  
            foreach (System.Data.DataColumn col in table.Columns)  
            {  
                Console.WriteLine("{0} = {1}",
                  col.ColumnName, row[col]);  
            }  
            Console.WriteLine("============================");  
        }  
        Console.WriteLine("Press any key to continue.");  
        Console.ReadKey();  
    }  
  }  
  
  private static string GetConnectionString()  
  {  
     // To avoid storing the connection string in your code,  
     // you can retrieve it from a configuration file.  
     return "Data Source=(local);Database=AdventureWorks;" +  
        "Integrated Security=true;";  
  }  
  
  private static void DisplayData(System.Data.DataTable table)  
  {  
     foreach (System.Data.DataRow row in table.Rows)  
     {  
        foreach (System.Data.DataColumn col in table.Columns)  
        {  
           Console.WriteLine("{0} = {1}", col.ColumnName, row[col]);  
        }  
     Console.WriteLine("============================");  
     }  
  }  
}  
```  
  
## <a name="sql-server-schema-restrictions"></a><span data-ttu-id="35944-137">SQL Server 架构限制</span><span class="sxs-lookup"><span data-stu-id="35944-137">SQL Server Schema Restrictions</span></span>  

 <span data-ttu-id="35944-138">下表列出了 SQL Server 架构集合的限制。</span><span class="sxs-lookup"><span data-stu-id="35944-138">The following tables list the restrictions for SQL Server schema collections.</span></span>  
  
### <a name="users"></a><span data-ttu-id="35944-139">用户</span><span class="sxs-lookup"><span data-stu-id="35944-139">Users</span></span>  
  
|<span data-ttu-id="35944-140">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-140">Restriction Name</span></span>|<span data-ttu-id="35944-141">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-141">Parameter Name</span></span>|<span data-ttu-id="35944-142">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-142">Restriction Default</span></span>|<span data-ttu-id="35944-143">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-143">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-144">User_Name</span><span class="sxs-lookup"><span data-stu-id="35944-144">User_Name</span></span>|@Name|<span data-ttu-id="35944-145">name</span><span class="sxs-lookup"><span data-stu-id="35944-145">name</span></span>|<span data-ttu-id="35944-146">1</span><span class="sxs-lookup"><span data-stu-id="35944-146">1</span></span>|  
  
### <a name="databases"></a><span data-ttu-id="35944-147">数据库</span><span class="sxs-lookup"><span data-stu-id="35944-147">Databases</span></span>  
  
|<span data-ttu-id="35944-148">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-148">Restriction Name</span></span>|<span data-ttu-id="35944-149">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-149">Parameter Name</span></span>|<span data-ttu-id="35944-150">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-150">Restriction Default</span></span>|<span data-ttu-id="35944-151">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-151">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-152">名称</span><span class="sxs-lookup"><span data-stu-id="35944-152">Name</span></span>|@Name|<span data-ttu-id="35944-153">名称</span><span class="sxs-lookup"><span data-stu-id="35944-153">Name</span></span>|<span data-ttu-id="35944-154">1</span><span class="sxs-lookup"><span data-stu-id="35944-154">1</span></span>|  
  
### <a name="tables"></a><span data-ttu-id="35944-155">表</span><span class="sxs-lookup"><span data-stu-id="35944-155">Tables</span></span>  
  
|<span data-ttu-id="35944-156">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-156">Restriction Name</span></span>|<span data-ttu-id="35944-157">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-157">Parameter Name</span></span>|<span data-ttu-id="35944-158">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-158">Restriction Default</span></span>|<span data-ttu-id="35944-159">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-159">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-160">目录</span><span class="sxs-lookup"><span data-stu-id="35944-160">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-161">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-161">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-162">1</span><span class="sxs-lookup"><span data-stu-id="35944-162">1</span></span>|  
|<span data-ttu-id="35944-163">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-163">Owner</span></span>|@Owner|<span data-ttu-id="35944-164">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-164">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-165">2</span><span class="sxs-lookup"><span data-stu-id="35944-165">2</span></span>|  
|<span data-ttu-id="35944-166">表</span><span class="sxs-lookup"><span data-stu-id="35944-166">Table</span></span>|@Name|<span data-ttu-id="35944-167">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-167">TABLE_NAME</span></span>|<span data-ttu-id="35944-168">3</span><span class="sxs-lookup"><span data-stu-id="35944-168">3</span></span>|  
|<span data-ttu-id="35944-169">TableType</span><span class="sxs-lookup"><span data-stu-id="35944-169">TableType</span></span>|@TableType|<span data-ttu-id="35944-170">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="35944-170">TABLE_TYPE</span></span>|<span data-ttu-id="35944-171">4</span><span class="sxs-lookup"><span data-stu-id="35944-171">4</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="35944-172">列</span><span class="sxs-lookup"><span data-stu-id="35944-172">Columns</span></span>  
  
|<span data-ttu-id="35944-173">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-173">Restriction Name</span></span>|<span data-ttu-id="35944-174">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-174">Parameter Name</span></span>|<span data-ttu-id="35944-175">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-175">Restriction Default</span></span>|<span data-ttu-id="35944-176">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-176">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-177">目录</span><span class="sxs-lookup"><span data-stu-id="35944-177">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-178">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-178">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-179">1</span><span class="sxs-lookup"><span data-stu-id="35944-179">1</span></span>|  
|<span data-ttu-id="35944-180">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-180">Owner</span></span>|@Owner|<span data-ttu-id="35944-181">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-181">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-182">2</span><span class="sxs-lookup"><span data-stu-id="35944-182">2</span></span>|  
|<span data-ttu-id="35944-183">表</span><span class="sxs-lookup"><span data-stu-id="35944-183">Table</span></span>|@Table|<span data-ttu-id="35944-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-184">TABLE_NAME</span></span>|<span data-ttu-id="35944-185">3</span><span class="sxs-lookup"><span data-stu-id="35944-185">3</span></span>|  
|<span data-ttu-id="35944-186">列</span><span class="sxs-lookup"><span data-stu-id="35944-186">Column</span></span>|@Column|<span data-ttu-id="35944-187">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-187">COLUMN_NAME</span></span>|<span data-ttu-id="35944-188">4</span><span class="sxs-lookup"><span data-stu-id="35944-188">4</span></span>|  
  
### <a name="structuredtypemembers"></a><span data-ttu-id="35944-189">StructuredTypeMembers</span><span class="sxs-lookup"><span data-stu-id="35944-189">StructuredTypeMembers</span></span>  
  
|<span data-ttu-id="35944-190">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-190">Restriction Name</span></span>|<span data-ttu-id="35944-191">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-191">Parameter Name</span></span>|<span data-ttu-id="35944-192">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-192">Restriction Default</span></span>|<span data-ttu-id="35944-193">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-193">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-194">目录</span><span class="sxs-lookup"><span data-stu-id="35944-194">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-195">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-195">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-196">1</span><span class="sxs-lookup"><span data-stu-id="35944-196">1</span></span>|  
|<span data-ttu-id="35944-197">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-197">Owner</span></span>|@Owner|<span data-ttu-id="35944-198">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-198">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-199">2</span><span class="sxs-lookup"><span data-stu-id="35944-199">2</span></span>|  
|<span data-ttu-id="35944-200">表</span><span class="sxs-lookup"><span data-stu-id="35944-200">Table</span></span>|@Table|<span data-ttu-id="35944-201">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-201">TABLE_NAME</span></span>|<span data-ttu-id="35944-202">3</span><span class="sxs-lookup"><span data-stu-id="35944-202">3</span></span>|  
|<span data-ttu-id="35944-203">列</span><span class="sxs-lookup"><span data-stu-id="35944-203">Column</span></span>|@Column|<span data-ttu-id="35944-204">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-204">COLUMN_NAME</span></span>|<span data-ttu-id="35944-205">4</span><span class="sxs-lookup"><span data-stu-id="35944-205">4</span></span>|  
  
### <a name="views"></a><span data-ttu-id="35944-206">视图</span><span class="sxs-lookup"><span data-stu-id="35944-206">Views</span></span>  
  
|<span data-ttu-id="35944-207">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-207">Restriction Name</span></span>|<span data-ttu-id="35944-208">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-208">Parameter Name</span></span>|<span data-ttu-id="35944-209">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-209">Restriction Default</span></span>|<span data-ttu-id="35944-210">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-210">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-211">目录</span><span class="sxs-lookup"><span data-stu-id="35944-211">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-212">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-212">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-213">1</span><span class="sxs-lookup"><span data-stu-id="35944-213">1</span></span>|  
|<span data-ttu-id="35944-214">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-214">Owner</span></span>|@Owner|<span data-ttu-id="35944-215">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-215">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-216">2</span><span class="sxs-lookup"><span data-stu-id="35944-216">2</span></span>|  
|<span data-ttu-id="35944-217">表</span><span class="sxs-lookup"><span data-stu-id="35944-217">Table</span></span>|@Table|<span data-ttu-id="35944-218">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-218">TABLE_NAME</span></span>|<span data-ttu-id="35944-219">3</span><span class="sxs-lookup"><span data-stu-id="35944-219">3</span></span>|  
  
### <a name="viewcolumns"></a><span data-ttu-id="35944-220">ViewColumns</span><span class="sxs-lookup"><span data-stu-id="35944-220">ViewColumns</span></span>  
  
|<span data-ttu-id="35944-221">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-221">Restriction Name</span></span>|<span data-ttu-id="35944-222">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-222">Parameter Name</span></span>|<span data-ttu-id="35944-223">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-223">Restriction Default</span></span>|<span data-ttu-id="35944-224">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-224">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-225">目录</span><span class="sxs-lookup"><span data-stu-id="35944-225">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-226">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-226">VIEW_CATALOG</span></span>|<span data-ttu-id="35944-227">1</span><span class="sxs-lookup"><span data-stu-id="35944-227">1</span></span>|  
|<span data-ttu-id="35944-228">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-228">Owner</span></span>|@Owner|<span data-ttu-id="35944-229">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-229">VIEW_SCHEMA</span></span>|<span data-ttu-id="35944-230">2</span><span class="sxs-lookup"><span data-stu-id="35944-230">2</span></span>|  
|<span data-ttu-id="35944-231">表</span><span class="sxs-lookup"><span data-stu-id="35944-231">Table</span></span>|@Table|<span data-ttu-id="35944-232">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-232">VIEW_NAME</span></span>|<span data-ttu-id="35944-233">3</span><span class="sxs-lookup"><span data-stu-id="35944-233">3</span></span>|  
|<span data-ttu-id="35944-234">列</span><span class="sxs-lookup"><span data-stu-id="35944-234">Column</span></span>|@Column|<span data-ttu-id="35944-235">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-235">COLUMN_NAME</span></span>|<span data-ttu-id="35944-236">4</span><span class="sxs-lookup"><span data-stu-id="35944-236">4</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="35944-237">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="35944-237">ProcedureParameters</span></span>  
  
|<span data-ttu-id="35944-238">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-238">Restriction Name</span></span>|<span data-ttu-id="35944-239">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-239">Parameter Name</span></span>|<span data-ttu-id="35944-240">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-240">Restriction Default</span></span>|<span data-ttu-id="35944-241">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-241">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-242">目录</span><span class="sxs-lookup"><span data-stu-id="35944-242">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-243">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-243">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="35944-244">1</span><span class="sxs-lookup"><span data-stu-id="35944-244">1</span></span>|  
|<span data-ttu-id="35944-245">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-245">Owner</span></span>|@Owner|<span data-ttu-id="35944-246">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-246">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="35944-247">2</span><span class="sxs-lookup"><span data-stu-id="35944-247">2</span></span>|  
|<span data-ttu-id="35944-248">名称</span><span class="sxs-lookup"><span data-stu-id="35944-248">Name</span></span>|@Name|<span data-ttu-id="35944-249">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-249">SPECIFIC_NAME</span></span>|<span data-ttu-id="35944-250">3</span><span class="sxs-lookup"><span data-stu-id="35944-250">3</span></span>|  
|<span data-ttu-id="35944-251">参数</span><span class="sxs-lookup"><span data-stu-id="35944-251">Parameter</span></span>|@Parameter|<span data-ttu-id="35944-252">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-252">PARAMETER_NAME</span></span>|<span data-ttu-id="35944-253">4</span><span class="sxs-lookup"><span data-stu-id="35944-253">4</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="35944-254">过程</span><span class="sxs-lookup"><span data-stu-id="35944-254">Procedures</span></span>  
  
|<span data-ttu-id="35944-255">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-255">Restriction Name</span></span>|<span data-ttu-id="35944-256">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-256">Parameter Name</span></span>|<span data-ttu-id="35944-257">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-257">Restriction Default</span></span>|<span data-ttu-id="35944-258">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-258">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-259">目录</span><span class="sxs-lookup"><span data-stu-id="35944-259">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-260">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-260">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="35944-261">1</span><span class="sxs-lookup"><span data-stu-id="35944-261">1</span></span>|  
|<span data-ttu-id="35944-262">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-262">Owner</span></span>|@Owner|<span data-ttu-id="35944-263">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-263">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="35944-264">2</span><span class="sxs-lookup"><span data-stu-id="35944-264">2</span></span>|  
|<span data-ttu-id="35944-265">名称</span><span class="sxs-lookup"><span data-stu-id="35944-265">Name</span></span>|@Name|<span data-ttu-id="35944-266">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-266">SPECIFIC_NAME</span></span>|<span data-ttu-id="35944-267">3</span><span class="sxs-lookup"><span data-stu-id="35944-267">3</span></span>|  
|<span data-ttu-id="35944-268">类型</span><span class="sxs-lookup"><span data-stu-id="35944-268">Type</span></span>|@Type|<span data-ttu-id="35944-269">ROUTINE_TYPE</span><span class="sxs-lookup"><span data-stu-id="35944-269">ROUTINE_TYPE</span></span>|<span data-ttu-id="35944-270">4</span><span class="sxs-lookup"><span data-stu-id="35944-270">4</span></span>|  
  
### <a name="indexcolumns"></a><span data-ttu-id="35944-271">IndexColumns</span><span class="sxs-lookup"><span data-stu-id="35944-271">IndexColumns</span></span>  
  
|<span data-ttu-id="35944-272">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-272">Restriction Name</span></span>|<span data-ttu-id="35944-273">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-273">Parameter Name</span></span>|<span data-ttu-id="35944-274">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-274">Restriction Default</span></span>|<span data-ttu-id="35944-275">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-275">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-276">目录</span><span class="sxs-lookup"><span data-stu-id="35944-276">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-277">db_name()</span><span class="sxs-lookup"><span data-stu-id="35944-277">db_name()</span></span>|<span data-ttu-id="35944-278">1</span><span class="sxs-lookup"><span data-stu-id="35944-278">1</span></span>|  
|<span data-ttu-id="35944-279">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-279">Owner</span></span>|@Owner|<span data-ttu-id="35944-280">user_name()</span><span class="sxs-lookup"><span data-stu-id="35944-280">user_name()</span></span>|<span data-ttu-id="35944-281">2</span><span class="sxs-lookup"><span data-stu-id="35944-281">2</span></span>|  
|<span data-ttu-id="35944-282">表</span><span class="sxs-lookup"><span data-stu-id="35944-282">Table</span></span>|@Table|<span data-ttu-id="35944-283">o.name</span><span class="sxs-lookup"><span data-stu-id="35944-283">o.name</span></span>|<span data-ttu-id="35944-284">3</span><span class="sxs-lookup"><span data-stu-id="35944-284">3</span></span>|  
|<span data-ttu-id="35944-285">ConstraintName</span><span class="sxs-lookup"><span data-stu-id="35944-285">ConstraintName</span></span>|@ConstraintName|<span data-ttu-id="35944-286">x.name</span><span class="sxs-lookup"><span data-stu-id="35944-286">x.name</span></span>|<span data-ttu-id="35944-287">4</span><span class="sxs-lookup"><span data-stu-id="35944-287">4</span></span>|  
|<span data-ttu-id="35944-288">列</span><span class="sxs-lookup"><span data-stu-id="35944-288">Column</span></span>|@Column|<span data-ttu-id="35944-289">c.name</span><span class="sxs-lookup"><span data-stu-id="35944-289">c.name</span></span>|<span data-ttu-id="35944-290">5</span><span class="sxs-lookup"><span data-stu-id="35944-290">5</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="35944-291">索引</span><span class="sxs-lookup"><span data-stu-id="35944-291">Indexes</span></span>  
  
|<span data-ttu-id="35944-292">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-292">Restriction Name</span></span>|<span data-ttu-id="35944-293">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-293">Parameter Name</span></span>|<span data-ttu-id="35944-294">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-294">Restriction Default</span></span>|<span data-ttu-id="35944-295">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-295">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-296">目录</span><span class="sxs-lookup"><span data-stu-id="35944-296">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-297">db_name()</span><span class="sxs-lookup"><span data-stu-id="35944-297">db_name()</span></span>|<span data-ttu-id="35944-298">1</span><span class="sxs-lookup"><span data-stu-id="35944-298">1</span></span>|  
|<span data-ttu-id="35944-299">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-299">Owner</span></span>|@Owner|<span data-ttu-id="35944-300">user_name()</span><span class="sxs-lookup"><span data-stu-id="35944-300">user_name()</span></span>|<span data-ttu-id="35944-301">2</span><span class="sxs-lookup"><span data-stu-id="35944-301">2</span></span>|  
|<span data-ttu-id="35944-302">表</span><span class="sxs-lookup"><span data-stu-id="35944-302">Table</span></span>|@Table|<span data-ttu-id="35944-303">o.name</span><span class="sxs-lookup"><span data-stu-id="35944-303">o.name</span></span>|<span data-ttu-id="35944-304">3</span><span class="sxs-lookup"><span data-stu-id="35944-304">3</span></span>|  
  
### <a name="userdefinedtypes"></a><span data-ttu-id="35944-305">UserDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="35944-305">UserDefinedTypes</span></span>  
  
|<span data-ttu-id="35944-306">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-306">Restriction Name</span></span>|<span data-ttu-id="35944-307">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-307">Parameter Name</span></span>|<span data-ttu-id="35944-308">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-308">Restriction Default</span></span>|<span data-ttu-id="35944-309">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-309">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-310">assembly_name</span><span class="sxs-lookup"><span data-stu-id="35944-310">assembly_name</span></span>|@AssemblyName|<span data-ttu-id="35944-311">assemblies.name</span><span class="sxs-lookup"><span data-stu-id="35944-311">assemblies.name</span></span>|<span data-ttu-id="35944-312">1</span><span class="sxs-lookup"><span data-stu-id="35944-312">1</span></span>|  
|<span data-ttu-id="35944-313">udt_name</span><span class="sxs-lookup"><span data-stu-id="35944-313">udt_name</span></span>|@UDTName|<span data-ttu-id="35944-314">types.assembly_class</span><span class="sxs-lookup"><span data-stu-id="35944-314">types.assembly_class</span></span>|<span data-ttu-id="35944-315">2</span><span class="sxs-lookup"><span data-stu-id="35944-315">2</span></span>|  
  
### <a name="foreignkeys"></a><span data-ttu-id="35944-316">ForeignKeys</span><span class="sxs-lookup"><span data-stu-id="35944-316">ForeignKeys</span></span>  
  
|<span data-ttu-id="35944-317">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-317">Restriction Name</span></span>|<span data-ttu-id="35944-318">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-318">Parameter Name</span></span>|<span data-ttu-id="35944-319">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-319">Restriction Default</span></span>|<span data-ttu-id="35944-320">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-320">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-321">目录</span><span class="sxs-lookup"><span data-stu-id="35944-321">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-322">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-322">CONSTRAINT_CATALOG</span></span>|<span data-ttu-id="35944-323">1</span><span class="sxs-lookup"><span data-stu-id="35944-323">1</span></span>|  
|<span data-ttu-id="35944-324">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-324">Owner</span></span>|@Owner|<span data-ttu-id="35944-325">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-325">CONSTRAINT_SCHEMA</span></span>|<span data-ttu-id="35944-326">2</span><span class="sxs-lookup"><span data-stu-id="35944-326">2</span></span>|  
|<span data-ttu-id="35944-327">表</span><span class="sxs-lookup"><span data-stu-id="35944-327">Table</span></span>|@Table|<span data-ttu-id="35944-328">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-328">TABLE_NAME</span></span>|<span data-ttu-id="35944-329">3</span><span class="sxs-lookup"><span data-stu-id="35944-329">3</span></span>|  
|<span data-ttu-id="35944-330">名称</span><span class="sxs-lookup"><span data-stu-id="35944-330">Name</span></span>|@Name|<span data-ttu-id="35944-331">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-331">CONSTRAINT_NAME</span></span>|<span data-ttu-id="35944-332">4</span><span class="sxs-lookup"><span data-stu-id="35944-332">4</span></span>|  
  
## <a name="sql-server-2008-schema-restrictions"></a><span data-ttu-id="35944-333">SQL Server 2008     </span><span class="sxs-lookup"><span data-stu-id="35944-333">SQL Server 2008 Schema Restrictions</span></span>  

 <span data-ttu-id="35944-334">下表列出了 SQL Server 2008 架构集合的限制。</span><span class="sxs-lookup"><span data-stu-id="35944-334">The following tables list the restrictions for SQL Server 2008 schema collections.</span></span> <span data-ttu-id="35944-335">这些限制从 .NET Framework 版本 3.5 SP1 和 SQL Server 2008 开始生效。</span><span class="sxs-lookup"><span data-stu-id="35944-335">These restrictions are valid beginning with version 3.5 SP1 of the .NET Framework and SQL Server 2008.</span></span> <span data-ttu-id="35944-336">.NET Framework 和 SQL Server 的早期版本不支持这些限制。</span><span class="sxs-lookup"><span data-stu-id="35944-336">They are not supported in earlier versions of the .NET Framework and SQL Server.</span></span>  
  
### <a name="columnsetcolumns"></a><span data-ttu-id="35944-337">ColumnSetColumns</span><span class="sxs-lookup"><span data-stu-id="35944-337">ColumnSetColumns</span></span>  
  
|<span data-ttu-id="35944-338">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-338">Restriction Name</span></span>|<span data-ttu-id="35944-339">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-339">Parameter Name</span></span>|<span data-ttu-id="35944-340">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-340">Restriction Default</span></span>|<span data-ttu-id="35944-341">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-341">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-342">目录</span><span class="sxs-lookup"><span data-stu-id="35944-342">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-343">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-343">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-344">1</span><span class="sxs-lookup"><span data-stu-id="35944-344">1</span></span>|  
|<span data-ttu-id="35944-345">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-345">Owner</span></span>|@Owner|<span data-ttu-id="35944-346">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-346">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-347">2</span><span class="sxs-lookup"><span data-stu-id="35944-347">2</span></span>|  
|<span data-ttu-id="35944-348">表</span><span class="sxs-lookup"><span data-stu-id="35944-348">Table</span></span>|@Table|<span data-ttu-id="35944-349">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-349">TABLE_NAME</span></span>|<span data-ttu-id="35944-350">3</span><span class="sxs-lookup"><span data-stu-id="35944-350">3</span></span>|  
  
### <a name="allcolumns"></a><span data-ttu-id="35944-351">AllColumns</span><span class="sxs-lookup"><span data-stu-id="35944-351">AllColumns</span></span>  
  
|<span data-ttu-id="35944-352">限制名称</span><span class="sxs-lookup"><span data-stu-id="35944-352">Restriction Name</span></span>|<span data-ttu-id="35944-353">参数名称</span><span class="sxs-lookup"><span data-stu-id="35944-353">Parameter Name</span></span>|<span data-ttu-id="35944-354">限制默认值</span><span class="sxs-lookup"><span data-stu-id="35944-354">Restriction Default</span></span>|<span data-ttu-id="35944-355">限制数</span><span class="sxs-lookup"><span data-stu-id="35944-355">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="35944-356">目录</span><span class="sxs-lookup"><span data-stu-id="35944-356">Catalog</span></span>|@Catalog|<span data-ttu-id="35944-357">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="35944-357">TABLE_CATALOG</span></span>|<span data-ttu-id="35944-358">1</span><span class="sxs-lookup"><span data-stu-id="35944-358">1</span></span>|  
|<span data-ttu-id="35944-359">所有者</span><span class="sxs-lookup"><span data-stu-id="35944-359">Owner</span></span>|@Owner|<span data-ttu-id="35944-360">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="35944-360">TABLE_SCHEMA</span></span>|<span data-ttu-id="35944-361">2</span><span class="sxs-lookup"><span data-stu-id="35944-361">2</span></span>|  
|<span data-ttu-id="35944-362">表</span><span class="sxs-lookup"><span data-stu-id="35944-362">Table</span></span>|@Table|<span data-ttu-id="35944-363">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-363">TABLE_NAME</span></span>|<span data-ttu-id="35944-364">3</span><span class="sxs-lookup"><span data-stu-id="35944-364">3</span></span>|  
|<span data-ttu-id="35944-365">列</span><span class="sxs-lookup"><span data-stu-id="35944-365">Column</span></span>|@Column|<span data-ttu-id="35944-366">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="35944-366">COLUMN_NAME</span></span>|<span data-ttu-id="35944-367">4</span><span class="sxs-lookup"><span data-stu-id="35944-367">4</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="35944-368">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35944-368">See also</span></span>

- [<span data-ttu-id="35944-369">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="35944-369">ADO.NET Overview</span></span>](ado-net-overview.md)
