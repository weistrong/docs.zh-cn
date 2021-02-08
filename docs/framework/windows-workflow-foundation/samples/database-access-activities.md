---
description: 了解详细信息：数据库访问活动
title: 数据库访问活动
ms.date: 03/30/2017
ms.assetid: 174a381e-1343-46a8-a62c-7c2ae2c4f0b2
ms.openlocfilehash: 421da4a55997dac62ccc5c598bc401a20711ec61
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792539"
---
# <a name="database-access-activities"></a><span data-ttu-id="bcea8-103">数据库访问活动</span><span class="sxs-lookup"><span data-stu-id="bcea8-103">Database Access Activities</span></span>

<span data-ttu-id="bcea8-104">数据库访问活动可用于在一个工作流内访问数据库。</span><span class="sxs-lookup"><span data-stu-id="bcea8-104">Database access activities allow you to access a database within a workflow.</span></span> <span data-ttu-id="bcea8-105">这些活动允许访问数据库以检索或修改信息，并使用 [ADO.NET](../../data/adonet/index.md) 来访问数据库。</span><span class="sxs-lookup"><span data-stu-id="bcea8-105">These activities allow accessing databases to retrieve or modify information and use [ADO.NET](../../data/adonet/index.md) to access the database.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bcea8-106">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="bcea8-106">The samples may already be installed on your machine.</span></span> <span data-ttu-id="bcea8-107">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="bcea8-107">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="bcea8-108">如果此目录不存在，请参阅 (下载页面) 下载所有 Windows Communication Foundation (WCF) 和 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 示例。</span><span class="sxs-lookup"><span data-stu-id="bcea8-108">If this directory does not exist, go to (download page) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="bcea8-109">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="bcea8-109">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\DbActivities`

## <a name="database-activities"></a><span data-ttu-id="bcea8-110">数据库活动</span><span class="sxs-lookup"><span data-stu-id="bcea8-110">Database Activities</span></span>

<span data-ttu-id="bcea8-111">以下部分详细介绍了此示例中包含的活动列表。</span><span class="sxs-lookup"><span data-stu-id="bcea8-111">The following sections detail the list of activities included in this sample.</span></span>

## <a name="dbupdate"></a><span data-ttu-id="bcea8-112">DbUpdate</span><span class="sxs-lookup"><span data-stu-id="bcea8-112">DbUpdate</span></span>

<span data-ttu-id="bcea8-113">执行可在数据库中产生修改（插入、更新、删除和其他修改）的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="bcea8-113">Executes a SQL query that produces a modification in the database (insert, update, delete, and other modifications).</span></span>

<span data-ttu-id="bcea8-114">此类采用异步方式执行其工作（它派生自 <xref:System.Activities.AsyncCodeActivity> 并使用其异步功能）。</span><span class="sxs-lookup"><span data-stu-id="bcea8-114">This class performs its work asynchronously (it derives from <xref:System.Activities.AsyncCodeActivity> and uses its asynchronous capabilities).</span></span>

<span data-ttu-id="bcea8-115">通过设置提供程序固定名称 (`ProviderName`) 和连接字符串 (`ConnectionString`)，或仅使用应用程序配置文件中的连接字符串配置名称 (`ConfigFileSectionName`)，可以配置连接信息。</span><span class="sxs-lookup"><span data-stu-id="bcea8-115">The connection information can be configured by setting a provider invariant name (`ProviderName`) and the connection string (`ConnectionString`) or just using a connection string configuration name (`ConfigFileSectionName`) from the application configuration file.</span></span>

<span data-ttu-id="bcea8-116">要执行的查询在其 `Sql` 属性中配置，并通过 `Parameters` 集合传递参数。</span><span class="sxs-lookup"><span data-stu-id="bcea8-116">The query to be executed is configured in its `Sql` property and the parameters are passed through the `Parameters` collection.</span></span>

<span data-ttu-id="bcea8-117">执行 `DbUpdate` 后，在 `AffectedRecords` 属性中返回受影响的记录的数量。</span><span class="sxs-lookup"><span data-stu-id="bcea8-117">After `DbUpdate` is executed, the number of affected records is returned in the `AffectedRecords` property.</span></span>

```csharp
Public class DbUpdate: AsyncCodeActivity
{
    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DefaultValue(null)]
    public InArgument<string> ProviderName { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DependsOn("ProviderName")]
    [DefaultValue(null)]
    public InArgument<string> ConnectionString { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConfigFileSectionName")]
    [DefaultValue(null)]
    public InArgument<string> ConfigName { get; set; }

    [DefaultValue(null)]
    public CommandType CommandType { get; set; }

    [RequiredArgument]
    public InArgument<string> Sql { get; set; }

    [DependsOn("Sql")]
    [DefaultValue(null)]
    public IDictionary<string, Argument> Parameters { get; }

    [DependsOn("Parameters")]
    public OutArgument<int> AffectedRecords { get; set; }
}
```

|<span data-ttu-id="bcea8-118">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-118">Argument</span></span>|<span data-ttu-id="bcea8-119">说明</span><span class="sxs-lookup"><span data-stu-id="bcea8-119">Description</span></span>|
|-|-|
|<span data-ttu-id="bcea8-120">ProviderName</span><span class="sxs-lookup"><span data-stu-id="bcea8-120">ProviderName</span></span>|<span data-ttu-id="bcea8-121">ADO.NET 提供程序固定名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-121">ADO.NET provider invariant name.</span></span> <span data-ttu-id="bcea8-122">如果设置此自变量，则必须还要设置 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-122">If this argument is set, then the `ConnectionString` must also be set.</span></span>|
|<span data-ttu-id="bcea8-123">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bcea8-123">ConnectionString</span></span>|<span data-ttu-id="bcea8-124">用于连接到数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="bcea8-124">Connection string to connect to the database.</span></span> <span data-ttu-id="bcea8-125">如果设置此自变量，则必须还要设置 `ProviderName`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-125">If this argument is set, then `ProviderName` must also be set.</span></span>|
|<span data-ttu-id="bcea8-126">ConfigName</span><span class="sxs-lookup"><span data-stu-id="bcea8-126">ConfigName</span></span>|<span data-ttu-id="bcea8-127">存储连接信息的配置文件部分的名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-127">Name of the configuration file section where the connection information is stored.</span></span> <span data-ttu-id="bcea8-128">设置此自变量之后，将不再需要 `ProviderName` 和 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-128">When this argument is set `ProviderName` and `ConnectionString` are not required.</span></span>|
|<span data-ttu-id="bcea8-129">CommandType</span><span class="sxs-lookup"><span data-stu-id="bcea8-129">CommandType</span></span>|<span data-ttu-id="bcea8-130">要执行的 <xref:System.Data.Common.DbCommand> 的类型。</span><span class="sxs-lookup"><span data-stu-id="bcea8-130">Type of the <xref:System.Data.Common.DbCommand> to be executed.</span></span>|
|<span data-ttu-id="bcea8-131">Sql</span><span class="sxs-lookup"><span data-stu-id="bcea8-131">Sql</span></span>|<span data-ttu-id="bcea8-132">要执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="bcea8-132">The SQL command to be executed.</span></span>|
|<span data-ttu-id="bcea8-133">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-133">Parameters</span></span>|<span data-ttu-id="bcea8-134">SQL 查询的参数集合。</span><span class="sxs-lookup"><span data-stu-id="bcea8-134">Collection of the parameters of the SQL query.</span></span>|
|<span data-ttu-id="bcea8-135">AffectedRecords</span><span class="sxs-lookup"><span data-stu-id="bcea8-135">AffectedRecords</span></span>|<span data-ttu-id="bcea8-136">最后一个操作影响的记录的数量。</span><span class="sxs-lookup"><span data-stu-id="bcea8-136">Number of records affected by the last operation.</span></span>|

## <a name="dbqueryscalar"></a><span data-ttu-id="bcea8-137">DbQueryScalar</span><span class="sxs-lookup"><span data-stu-id="bcea8-137">DbQueryScalar</span></span>

<span data-ttu-id="bcea8-138">执行可从数据库检索单个值的查询。</span><span class="sxs-lookup"><span data-stu-id="bcea8-138">Executes a query that retrieves a single value from the database.</span></span>

<span data-ttu-id="bcea8-139">此类采用异步方式执行其工作（它派生自 <xref:System.Activities.AsyncCodeActivity%601> 并使用其异步功能）。</span><span class="sxs-lookup"><span data-stu-id="bcea8-139">This class performs its work asynchronously (it derives from <xref:System.Activities.AsyncCodeActivity%601> and uses its asynchronous capabilities).</span></span>

<span data-ttu-id="bcea8-140">通过设置提供程序固定名称 (`ProviderName`) 和连接字符串 (`ConnectionString`)，或仅使用应用程序配置文件中的连接字符串配置名称 (`ConfigFileSectionName`)，可以配置连接信息。</span><span class="sxs-lookup"><span data-stu-id="bcea8-140">The connection information can be configured by setting a provider invariant name (`ProviderName`) and the connection string (`ConnectionString`) or just using a connection string configuration name (`ConfigFileSectionName`) from the application configuration file.</span></span>

<span data-ttu-id="bcea8-141">要执行的查询在其 `Sql` 属性中配置，并通过 `Parameters` 集合传递参数。</span><span class="sxs-lookup"><span data-stu-id="bcea8-141">The query to be executed is configured in its `Sql` property and the parameters are passed through the `Parameters` collection.</span></span>

<span data-ttu-id="bcea8-142">`DbQueryScalar`执行之后，将在类型为的参数 (中返回标量， `Result out` `TResult` 该参数在基类) 中定义 <xref:System.Activities.AsyncCodeActivity%601> 。</span><span class="sxs-lookup"><span data-stu-id="bcea8-142">After `DbQueryScalar` is executed, the scalar is returned in the `Result out` argument (of type `TResult`, that is defined in the base class <xref:System.Activities.AsyncCodeActivity%601>).</span></span>

```csharp
public class DbQueryScalar<TResult> : AsyncCodeActivity<TResult>
{
    // public arguments
    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DefaultValue(null)]
    public InArgument<string> ProviderName { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DependsOn("ProviderName")]
    [DefaultValue(null)]
    public InArgument<string> ConnectionString { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConfigFileSectionName")]
    [DefaultValue(null)]
    public InArgument<string> ConfigName { get; set; }

    [DefaultValue(null)]
    public CommandType CommandType { get; set; }

    [RequiredArgument]
    public InArgument<string> Sql { get; set; }

    [DependsOn("Sql")]
    [DefaultValue(null)]
    public IDictionary<string, Argument> Parameters { get; }
}
```

|<span data-ttu-id="bcea8-143">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-143">Argument</span></span>|<span data-ttu-id="bcea8-144">说明</span><span class="sxs-lookup"><span data-stu-id="bcea8-144">Description</span></span>|
|-|-|
|<span data-ttu-id="bcea8-145">ProviderName</span><span class="sxs-lookup"><span data-stu-id="bcea8-145">ProviderName</span></span>|<span data-ttu-id="bcea8-146">ADO.NET 提供程序固定名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-146">ADO.NET provider invariant name.</span></span> <span data-ttu-id="bcea8-147">如果设置此自变量，则必须还要设置 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-147">If this argument is set, then the `ConnectionString` must also be set.</span></span>|
|<span data-ttu-id="bcea8-148">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bcea8-148">ConnectionString</span></span>|<span data-ttu-id="bcea8-149">用于连接到数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="bcea8-149">Connection string to connect to the database.</span></span> <span data-ttu-id="bcea8-150">如果设置此自变量，则必须还要设置 `ProviderName`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-150">If this argument is set, then `ProviderName` must also be set.</span></span>|
|<span data-ttu-id="bcea8-151">ConfigName</span><span class="sxs-lookup"><span data-stu-id="bcea8-151">ConfigName</span></span>|<span data-ttu-id="bcea8-152">存储连接信息的配置文件部分的名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-152">Name of the configuration file section where the connection information is stored.</span></span> <span data-ttu-id="bcea8-153">设置此自变量之后，将不再需要 `ProviderName` 和 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-153">When this argument is set `ProviderName` and `ConnectionString` are not required.</span></span>|
|<span data-ttu-id="bcea8-154">CommandType</span><span class="sxs-lookup"><span data-stu-id="bcea8-154">CommandType</span></span>|<span data-ttu-id="bcea8-155">要执行的 <xref:System.Data.Common.DbCommand> 的类型。</span><span class="sxs-lookup"><span data-stu-id="bcea8-155">Type of the <xref:System.Data.Common.DbCommand> to be executed.</span></span>|
|<span data-ttu-id="bcea8-156">Sql</span><span class="sxs-lookup"><span data-stu-id="bcea8-156">Sql</span></span>|<span data-ttu-id="bcea8-157">要执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="bcea8-157">The SQL command to be executed.</span></span>|
|<span data-ttu-id="bcea8-158">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-158">Parameters</span></span>|<span data-ttu-id="bcea8-159">SQL 查询的参数集合。</span><span class="sxs-lookup"><span data-stu-id="bcea8-159">Collection of the parameters of the SQL query.</span></span>|
|<span data-ttu-id="bcea8-160">结果</span><span class="sxs-lookup"><span data-stu-id="bcea8-160">Result</span></span>|<span data-ttu-id="bcea8-161">执行查询后获得的标量。</span><span class="sxs-lookup"><span data-stu-id="bcea8-161">Scalar that is obtained after the query is executed.</span></span> <span data-ttu-id="bcea8-162">此自变量的类型为 `TResult`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-162">This argument is of type `TResult`.</span></span>|

## <a name="dbquery"></a><span data-ttu-id="bcea8-163">DbQuery</span><span class="sxs-lookup"><span data-stu-id="bcea8-163">DbQuery</span></span>

<span data-ttu-id="bcea8-164">执行可检索对象列表的查询。</span><span class="sxs-lookup"><span data-stu-id="bcea8-164">Executes a query that retrieves a list of objects.</span></span> <span data-ttu-id="bcea8-165">执行查询后，将执行一个映射函数 (它可以是 <xref:System.Func%601> < `DbDataReader` 、 `TResult`> 或 <xref:System.Activities.ActivityFunc%601> < `DbDataReader` `TResult`>) 。</span><span class="sxs-lookup"><span data-stu-id="bcea8-165">After the query is executed, a mapping function is executed (it can be <xref:System.Func%601><`DbDataReader`, `TResult`> or an <xref:System.Activities.ActivityFunc%601><`DbDataReader`, `TResult`>).</span></span> <span data-ttu-id="bcea8-166">此映射函数在 `DbDataReader` 中获取一个记录，并将其映射到要返回的对象。</span><span class="sxs-lookup"><span data-stu-id="bcea8-166">This mapping function gets a record in a `DbDataReader` and maps it to the object to be returned.</span></span>

<span data-ttu-id="bcea8-167">通过设置提供程序固定名称 (`ProviderName`) 和连接字符串 (`ConnectionString`)，或仅使用应用程序配置文件中的连接字符串配置名称 (`ConfigFileSectionName`)，可以配置连接信息。</span><span class="sxs-lookup"><span data-stu-id="bcea8-167">The connection information can be configured by setting a provider invariant name (`ProviderName`) and the connection string (`ConnectionString`) or just using a connection string configuration name (`ConfigFileSectionName`) from the application configuration file.</span></span>

<span data-ttu-id="bcea8-168">要执行的查询在其 `Sql` 属性中配置，并通过 `Parameters` 集合传递参数。</span><span class="sxs-lookup"><span data-stu-id="bcea8-168">The query to be executed is configured in its `Sql` property and the parameters are passed through the `Parameters` collection.</span></span>

<span data-ttu-id="bcea8-169">使用 `DbDataReader` 检索 SQL 查询的结果。</span><span class="sxs-lookup"><span data-stu-id="bcea8-169">The results of the SQL query are retrieved using a `DbDataReader`.</span></span> <span data-ttu-id="bcea8-170">此活动将循环访问 `DbDataReader`，并将 `DbDataReader` 中的行映射到 `TResult` 的实例。</span><span class="sxs-lookup"><span data-stu-id="bcea8-170">The activity iterates through the `DbDataReader` and maps the rows in the `DbDataReader` to an instance of `TResult`.</span></span> <span data-ttu-id="bcea8-171">的用户 `DbQuery` 必须提供映射代码，可以通过两种方式完成此操作：使用 <xref:System.Func%601> < `DbDataReader` 、 `TResult`> 或 <xref:System.Activities.ActivityFunc%601> < `DbDataReader` `TResult`>。</span><span class="sxs-lookup"><span data-stu-id="bcea8-171">The user of `DbQuery` has to provide the mapping code and this can be done in two ways: using a <xref:System.Func%601><`DbDataReader`, `TResult`> or an <xref:System.Activities.ActivityFunc%601><`DbDataReader`, `TResult`>.</span></span> <span data-ttu-id="bcea8-172">在第一种情况下，将在单个执行脉冲中完成映射。</span><span class="sxs-lookup"><span data-stu-id="bcea8-172">In the first case, the map is done in a single pulse of execution.</span></span> <span data-ttu-id="bcea8-173">因此，此方法的速度更快，但无法序列化为 XAML。</span><span class="sxs-lookup"><span data-stu-id="bcea8-173">Therefore, it is faster, but this cannot be serialized to XAML.</span></span> <span data-ttu-id="bcea8-174">在后一种情况下，将在多个脉冲中完成映射。</span><span class="sxs-lookup"><span data-stu-id="bcea8-174">In the last case, the map is performed in multiple pulses.</span></span> <span data-ttu-id="bcea8-175">因此，此方法的速度较慢，但可序列化为 XAML，并以声明方式进行创作（任何现有活动均可参与映射）。</span><span class="sxs-lookup"><span data-stu-id="bcea8-175">Therefore, it might be slower but can be serialized to XAML and authored declaratively (any existing activity can participate in the mapping).</span></span>

```csharp
public class DbQuery<TResult> : AsyncCodeActivity<IList<TResult>> where TResult : class
{
    // public arguments
    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DefaultValue(null)]
    public InArgument<string> ProviderName { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DependsOn("ProviderName")]
    [DefaultValue(null)]
    public InArgument<string> ConnectionString { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConfigFileSectionName")]
    [DefaultValue(null)]
    public InArgument<string> ConfigName { get; set; }

    [DefaultValue(null)]
    public CommandType CommandType { get; set; }

    [RequiredArgument]
    public InArgument<string> Sql { get; set; }

    [DependsOn("Sql")]
    [DefaultValue(null)]
    public IDictionary<string, Argument> Parameters { get; }

    [OverloadGroup("DirectMapping")]
    [DefaultValue(null)]
    public Func<DbDataReader, TResult> Mapper { get; set; }

    [OverloadGroup("MultiplePulseMapping")]
    [DefaultValue(null)]
    public ActivityFunc<DbDataReader, TResult> MapperFunc { get; set; }
}
```

|<span data-ttu-id="bcea8-176">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-176">Argument</span></span>|<span data-ttu-id="bcea8-177">说明</span><span class="sxs-lookup"><span data-stu-id="bcea8-177">Description</span></span>|
|-|-|
|<span data-ttu-id="bcea8-178">ProviderName</span><span class="sxs-lookup"><span data-stu-id="bcea8-178">ProviderName</span></span>|<span data-ttu-id="bcea8-179">ADO.NET 提供程序固定名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-179">ADO.NET provider invariant name.</span></span> <span data-ttu-id="bcea8-180">如果设置此自变量，则必须还要设置 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-180">If this argument is set, then the `ConnectionString` must also be set.</span></span>|
|<span data-ttu-id="bcea8-181">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bcea8-181">ConnectionString</span></span>|<span data-ttu-id="bcea8-182">用于连接到数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="bcea8-182">Connection string to connect to the database.</span></span> <span data-ttu-id="bcea8-183">如果设置此自变量，则必须还要设置 `ProviderName`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-183">If this argument is set, then `ProviderName` must also be set.</span></span>|
|<span data-ttu-id="bcea8-184">ConfigName</span><span class="sxs-lookup"><span data-stu-id="bcea8-184">ConfigName</span></span>|<span data-ttu-id="bcea8-185">存储连接信息的配置文件部分的名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-185">Name of the configuration file section where the connection information is stored.</span></span> <span data-ttu-id="bcea8-186">设置此自变量之后，将不再需要 `ProviderName` 和 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-186">When this argument is set `ProviderName` and `ConnectionString` are not required.</span></span>|
|<span data-ttu-id="bcea8-187">CommandType</span><span class="sxs-lookup"><span data-stu-id="bcea8-187">CommandType</span></span>|<span data-ttu-id="bcea8-188">要执行的 <xref:System.Data.Common.DbCommand> 的类型。</span><span class="sxs-lookup"><span data-stu-id="bcea8-188">Type of the <xref:System.Data.Common.DbCommand> to be executed.</span></span>|
|<span data-ttu-id="bcea8-189">Sql</span><span class="sxs-lookup"><span data-stu-id="bcea8-189">Sql</span></span>|<span data-ttu-id="bcea8-190">要执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="bcea8-190">The SQL command to be executed.</span></span>|
|<span data-ttu-id="bcea8-191">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-191">Parameters</span></span>|<span data-ttu-id="bcea8-192">SQL 查询的参数集合。</span><span class="sxs-lookup"><span data-stu-id="bcea8-192">Collection of the parameters of the SQL query.</span></span>|
|<span data-ttu-id="bcea8-193">Mapper</span><span class="sxs-lookup"><span data-stu-id="bcea8-193">Mapper</span></span>|<span data-ttu-id="bcea8-194">映射函数 (<xref:System.Func%601> < `DbDataReader` ， `TResult`>) ，它采用 `DataReader` 作为执行查询的结果获取的中的记录，并返回 `TResult` 要添加到集合的类型的对象的实例 `Result` 。</span><span class="sxs-lookup"><span data-stu-id="bcea8-194">Mapping function (<xref:System.Func%601><`DbDataReader`, `TResult`>) that takes a record in the `DataReader` obtained as result of executing the query and returns an instance of an object of type `TResult` to be added to the `Result` collection.</span></span><br /><br /> <span data-ttu-id="bcea8-195">在这种情况下，将在单个执行脉冲中完成映射，但不能使用设计器以声明方式创作它。</span><span class="sxs-lookup"><span data-stu-id="bcea8-195">In this case, mapping is done in a single pulse of execution, but it cannot be authored declaratively using the designer.</span></span>|
|<span data-ttu-id="bcea8-196">MapperFunc</span><span class="sxs-lookup"><span data-stu-id="bcea8-196">MapperFunc</span></span>|<span data-ttu-id="bcea8-197">映射函数 (<xref:System.Activities.ActivityFunc%601> < `DbDataReader` ， `TResult`>) ，它采用 `DataReader` 作为执行查询的结果获取的中的记录，并返回 `TResult` 要添加到集合的类型的对象的实例 `Result` 。</span><span class="sxs-lookup"><span data-stu-id="bcea8-197">Mapping function (<xref:System.Activities.ActivityFunc%601><`DbDataReader`, `TResult`>) that takes a record in the `DataReader` obtained as result of executing the query and returns an instance of an object of type `TResult` to be added to the `Result` collection.</span></span><br /><br /> <span data-ttu-id="bcea8-198">在这种情况下，将在多个执行脉冲中完成映射。</span><span class="sxs-lookup"><span data-stu-id="bcea8-198">In this case, the mapping is done in multiple pulses of execution.</span></span> <span data-ttu-id="bcea8-199">此函数可序列化为 XAML，并以声明方式进行创作（任何现有活动均可参与映射）。</span><span class="sxs-lookup"><span data-stu-id="bcea8-199">This function can be serialized to XAML and authored declaratively (any existing activity can participate in the mapping).</span></span>|
|<span data-ttu-id="bcea8-200">结果</span><span class="sxs-lookup"><span data-stu-id="bcea8-200">Result</span></span>|<span data-ttu-id="bcea8-201">对象列表，这些对象是通过执行查询并对 `DataReader` 中的每个记录执行映射函数得到的。</span><span class="sxs-lookup"><span data-stu-id="bcea8-201">List of objects obtained as result of executing the query and executing the mapping function for each record in the `DataReader`.</span></span>|

## <a name="dbquerydataset"></a><span data-ttu-id="bcea8-202">DbQueryDataSet</span><span class="sxs-lookup"><span data-stu-id="bcea8-202">DbQueryDataSet</span></span>

<span data-ttu-id="bcea8-203">执行可返回 <xref:System.Data.DataSet> 的查询。</span><span class="sxs-lookup"><span data-stu-id="bcea8-203">Executes a query that returns a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="bcea8-204">此类以异步方式执行其工作。</span><span class="sxs-lookup"><span data-stu-id="bcea8-204">This class performs its work asynchronously.</span></span> <span data-ttu-id="bcea8-205">它派生自 <xref:System.Activities.AsyncCodeActivity> < `TResult`>，并使用其异步功能。</span><span class="sxs-lookup"><span data-stu-id="bcea8-205">It derives from <xref:System.Activities.AsyncCodeActivity><`TResult`> and uses its asynchronous capabilities.</span></span>

<span data-ttu-id="bcea8-206">通过设置提供程序固定名称 (`ProviderName`) 和连接字符串 (`ConnectionString`)，或仅使用应用程序配置文件中的连接字符串配置名称 (`ConfigFileSectionName`)，可以配置连接信息。</span><span class="sxs-lookup"><span data-stu-id="bcea8-206">The connection information can be configured by setting a provider invariant name (`ProviderName`) and the connection string (`ConnectionString`) or just using a connection string configuration name (`ConfigFileSectionName`) from the application configuration file.</span></span>

<span data-ttu-id="bcea8-207">要执行的查询在其 `Sql` 属性中配置，并通过 `Parameters` 集合传递参数。</span><span class="sxs-lookup"><span data-stu-id="bcea8-207">The query to be executed is configured in its `Sql` property and the parameters are passed through the `Parameters` collection.</span></span>

<span data-ttu-id="bcea8-208">执行之后，将 `DbQueryDataSet` `DataSet` 在类型为的参数 (中返回 `Result out` `TResult` ，该参数在基类) 中定义 <xref:System.Activities.AsyncCodeActivity%601> 。</span><span class="sxs-lookup"><span data-stu-id="bcea8-208">After the `DbQueryDataSet` is executed the `DataSet` is returned in the `Result out` argument (of type `TResult`, that is defined in the base class <xref:System.Activities.AsyncCodeActivity%601>).</span></span>

```csharp
public class DbQueryDataSet : AsyncCodeActivity<DataSet>
{
    // public arguments
    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DefaultValue(null)]
    public InArgument<string> ProviderName { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConnectionString")]
    [DependsOn("ProviderName")]
    [DefaultValue(null)]
    public InArgument<string> ConnectionString { get; set; }

    [RequiredArgument]
    [OverloadGroup("ConfigFileSectionName")]
    [DefaultValue(null)]
    public InArgument<string> ConfigName { get; set; }

    [DefaultValue(null)]
    public CommandType CommandType { get; set; }

    [RequiredArgument]
    public InArgument<string> Sql { get; set; }

    [DependsOn("Sql")]
    [DefaultValue(null)]
    public IDictionary<string, Argument> Parameters { get; }
}
```

|<span data-ttu-id="bcea8-209">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-209">Argument</span></span>|<span data-ttu-id="bcea8-210">说明</span><span class="sxs-lookup"><span data-stu-id="bcea8-210">Description</span></span>|
|-|-|
|<span data-ttu-id="bcea8-211">ProviderName</span><span class="sxs-lookup"><span data-stu-id="bcea8-211">ProviderName</span></span>|<span data-ttu-id="bcea8-212">ADO.NET 提供程序固定名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-212">ADO.NET provider invariant name.</span></span> <span data-ttu-id="bcea8-213">如果设置此自变量，则必须还要设置 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-213">If this argument is set, then the `ConnectionString` must also be set.</span></span>|
|<span data-ttu-id="bcea8-214">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bcea8-214">ConnectionString</span></span>|<span data-ttu-id="bcea8-215">用于连接到数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="bcea8-215">Connection string to connect to the database.</span></span> <span data-ttu-id="bcea8-216">如果设置此自变量，则必须还要设置 `ProviderName`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-216">If this argument is set, then `ProviderName` must also be set.</span></span>|
|<span data-ttu-id="bcea8-217">ConfigName</span><span class="sxs-lookup"><span data-stu-id="bcea8-217">ConfigName</span></span>|<span data-ttu-id="bcea8-218">存储连接信息的配置文件部分的名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-218">Name of the configuration file section where the connection information is stored.</span></span> <span data-ttu-id="bcea8-219">设置此自变量之后，将不再需要 `ProviderName` 和 `ConnectionString`。</span><span class="sxs-lookup"><span data-stu-id="bcea8-219">When this argument is set `ProviderName` and `ConnectionString` are not required.</span></span>|
|<span data-ttu-id="bcea8-220">CommandType</span><span class="sxs-lookup"><span data-stu-id="bcea8-220">CommandType</span></span>|<span data-ttu-id="bcea8-221">要执行的 <xref:System.Data.Common.DbCommand> 的类型。</span><span class="sxs-lookup"><span data-stu-id="bcea8-221">Type of the <xref:System.Data.Common.DbCommand> to be executed.</span></span>|
|<span data-ttu-id="bcea8-222">Sql</span><span class="sxs-lookup"><span data-stu-id="bcea8-222">Sql</span></span>|<span data-ttu-id="bcea8-223">要执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="bcea8-223">The SQL command to be executed.</span></span>|
|<span data-ttu-id="bcea8-224">参数</span><span class="sxs-lookup"><span data-stu-id="bcea8-224">Parameters</span></span>|<span data-ttu-id="bcea8-225">SQL 查询的参数集合。</span><span class="sxs-lookup"><span data-stu-id="bcea8-225">Collection of the parameters of the SQL query.</span></span>|
|<span data-ttu-id="bcea8-226">结果</span><span class="sxs-lookup"><span data-stu-id="bcea8-226">Result</span></span>|<span data-ttu-id="bcea8-227">执行查询后获得的 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="bcea8-227"><xref:System.Data.DataSet> that is obtained after the query is executed.</span></span>|

## <a name="configuring-connection-information"></a><span data-ttu-id="bcea8-228">配置连接信息</span><span class="sxs-lookup"><span data-stu-id="bcea8-228">Configuring Connection Information</span></span>

<span data-ttu-id="bcea8-229">所有 DbActivities 共享相同的配置参数。</span><span class="sxs-lookup"><span data-stu-id="bcea8-229">All DbActivities share the same configuration parameters.</span></span> <span data-ttu-id="bcea8-230">可以通过两种方式进行相关配置：</span><span class="sxs-lookup"><span data-stu-id="bcea8-230">They can be configured in two ways:</span></span>

- <span data-ttu-id="bcea8-231">`ConnectionString + InvariantName`：设置 ADO.NET 提供程序固定名称和连接字符串。</span><span class="sxs-lookup"><span data-stu-id="bcea8-231">`ConnectionString + InvariantName`: Set the ADO.NET provider invariant name and connection string.</span></span>

  ```csharp
  Activity dbSelectCount = new DbQueryScalar<DateTime>()
  {
      ProviderName = "System.Data.SqlClient",
      ConnectionString = @"Data Source=.\SQLExpress;
                            Initial Catalog=DbActivitiesSample;
                            Integrated Security=True",
      Sql = "SELECT GetDate()"
  };
  ```

- <span data-ttu-id="bcea8-232">`ConfigName`：设置包含连接信息的配置部分的名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-232">`ConfigName`: Set the name of the configuration section that contains the connection information.</span></span>

  ```xml
  <connectionStrings>
      <add name="DbActivitiesSample"
            providerName="System.Data.SqlClient"
            connectionString="Data Source=.\SQLExpress;Initial Catalog=DbActivitiesSample;Integrated Security=true"/>
    </connectionStrings>
  ```

- <span data-ttu-id="bcea8-233">在活动中：</span><span class="sxs-lookup"><span data-stu-id="bcea8-233">In the activity:</span></span>

  ```csharp
  Activity dbSelectCount = new DbQueryScalar<int>()
  {
      ConfigName = "DbActivitiesSample",
      Sql = "SELECT COUNT(*) FROM Roles"
  };
  ```

## <a name="running-this-sample"></a><span data-ttu-id="bcea8-234">运行此示例</span><span class="sxs-lookup"><span data-stu-id="bcea8-234">Running this sample</span></span>

### <a name="setup-instructions"></a><span data-ttu-id="bcea8-235">设置说明</span><span class="sxs-lookup"><span data-stu-id="bcea8-235">Setup instructions</span></span>

<span data-ttu-id="bcea8-236">此示例使用一个数据库。</span><span class="sxs-lookup"><span data-stu-id="bcea8-236">This sample uses a database.</span></span> <span data-ttu-id="bcea8-237">此示例提供了一个安装和加载脚本 (Setup.cmd)。</span><span class="sxs-lookup"><span data-stu-id="bcea8-237">A set-up and load script (Setup.cmd) is provided with the sample.</span></span> <span data-ttu-id="bcea8-238">必须使用命令提示执行该文件。</span><span class="sxs-lookup"><span data-stu-id="bcea8-238">You must execute that file using the command prompt.</span></span>

<span data-ttu-id="bcea8-239">Setup.cmd 脚本调用 CreateDb.sql 脚本文件，该文件包含可执行下列操作的 SQL 命令：</span><span class="sxs-lookup"><span data-stu-id="bcea8-239">The Setup.cmd script invokes the CreateDb.sql script file, which contains SQL commands that do the following:</span></span>

- <span data-ttu-id="bcea8-240">创建一个名为 DbActivitiesSample 的数据库。</span><span class="sxs-lookup"><span data-stu-id="bcea8-240">Creates a database called DbActivitiesSample.</span></span>

- <span data-ttu-id="bcea8-241">创建 Roles 表。</span><span class="sxs-lookup"><span data-stu-id="bcea8-241">Creates the Roles table.</span></span>

- <span data-ttu-id="bcea8-242">创建 Employees 表。</span><span class="sxs-lookup"><span data-stu-id="bcea8-242">Creates Employees table.</span></span>

- <span data-ttu-id="bcea8-243">将 3 个记录插入到 Roles 表中。</span><span class="sxs-lookup"><span data-stu-id="bcea8-243">Inserts three records into the Roles table.</span></span>

- <span data-ttu-id="bcea8-244">将 12 个记录插入到 Employees 表中。</span><span class="sxs-lookup"><span data-stu-id="bcea8-244">Inserts twelve records into the Employees table.</span></span>

##### <a name="to-run-setupcmd"></a><span data-ttu-id="bcea8-245">运行 Setup.cmd</span><span class="sxs-lookup"><span data-stu-id="bcea8-245">To run Setup.cmd</span></span>

1. <span data-ttu-id="bcea8-246">打开命令提示符。</span><span class="sxs-lookup"><span data-stu-id="bcea8-246">Open a command prompt.</span></span>

2. <span data-ttu-id="bcea8-247">转到 DbActivities 示例文件夹。</span><span class="sxs-lookup"><span data-stu-id="bcea8-247">Go to the DbActivities sample folder.</span></span>

3. <span data-ttu-id="bcea8-248">键入 "setup .cmd"，然后按 ENTER。</span><span class="sxs-lookup"><span data-stu-id="bcea8-248">Type "setup.cmd" and press ENTER.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bcea8-249">Setup.cmd 尝试将此示例安装在您本地计算机的 SqlExpress 实例中。</span><span class="sxs-lookup"><span data-stu-id="bcea8-249">Setup.cmd attempts to install the sample in your local machine SqlExpress instance.</span></span> <span data-ttu-id="bcea8-250">如果您需要在其他 SQL Server 实例中安装它，请将 Setup.cmd 改为使用新的实例名称。</span><span class="sxs-lookup"><span data-stu-id="bcea8-250">If you want to install it in other SQL server instance, edit Setup.cmd with the new instance name.</span></span>

##### <a name="to-uninstall-the-sample-database"></a><span data-ttu-id="bcea8-251">卸载示例数据库</span><span class="sxs-lookup"><span data-stu-id="bcea8-251">To uninstall the sample database</span></span>

1. <span data-ttu-id="bcea8-252">在命令提示中运行示例文件夹中的 Cleanup.cmd。</span><span class="sxs-lookup"><span data-stu-id="bcea8-252">Run Cleanup.cmd from the sample folder in a command prompt.</span></span>

##### <a name="to-run-the-sample"></a><span data-ttu-id="bcea8-253">运行示例</span><span class="sxs-lookup"><span data-stu-id="bcea8-253">To run the sample</span></span>

1. <span data-ttu-id="bcea8-254">在 Visual Studio 2010 中打开解决方案</span><span class="sxs-lookup"><span data-stu-id="bcea8-254">Open the solution in Visual Studio 2010</span></span>

2. <span data-ttu-id="bcea8-255">若要编译解决方案，请按 CTRL+SHIFT+B。</span><span class="sxs-lookup"><span data-stu-id="bcea8-255">To compile the solution, press CTRL+SHIFT+B.</span></span>

3. <span data-ttu-id="bcea8-256">若要运行示例而不进行调试，按 Ctrl+F5。</span><span class="sxs-lookup"><span data-stu-id="bcea8-256">To run the sample without debugging, press CTRL+F5.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bcea8-257">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="bcea8-257">The samples may already be installed on your machine.</span></span> <span data-ttu-id="bcea8-258">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="bcea8-258">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="bcea8-259">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcea8-259">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="bcea8-260">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="bcea8-260">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\DbActivities`
