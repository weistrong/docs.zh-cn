---
description: 了解详细信息： SqlClient 实体框架
title: 用于实体框架的 SqlClient
ms.date: 03/30/2017
ms.assetid: 9a5d6d39-d955-43a5-a5c2-931c239398f1
ms.openlocfilehash: eba5602c13f66d1ee4404bbc27035304e34c1cd0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673123"
---
# <a name="sqlclient-for-the-entity-framework"></a><span data-ttu-id="d0145-103">用于实体框架的 SqlClient</span><span class="sxs-lookup"><span data-stu-id="d0145-103">SqlClient for the Entity Framework</span></span>

<span data-ttu-id="d0145-104">本节介绍用于 SQL Server (SqlClient) 的 .NET Framework 数据提供程序，该提供程序使实体框架能够在 Microsoft SQL Server 上工作。</span><span class="sxs-lookup"><span data-stu-id="d0145-104">This section describes the .NET Framework Data Provider for SQL Server (SqlClient), which enables the Entity Framework to work over Microsoft SQL Server.</span></span>  
  
## <a name="provider-schema-attribute"></a><span data-ttu-id="d0145-105">Provider 架构属性</span><span class="sxs-lookup"><span data-stu-id="d0145-105">Provider Schema Attribute</span></span>  

 <span data-ttu-id="d0145-106">`Provider` 是以存储架构定义语言 (SSDL) 表示的 `Schema` 元素的一个特性。</span><span class="sxs-lookup"><span data-stu-id="d0145-106">`Provider` is an attribute of the `Schema` element in store schema definition language (SSDL).</span></span>  
  
 <span data-ttu-id="d0145-107">若要使用 SqlClient，请将字符串“System.Data.SqlClient”分配给 `Provider` 元素的 `Schema` 属性。</span><span class="sxs-lookup"><span data-stu-id="d0145-107">To use SqlClient, assign the string "System.Data.SqlClient" to the `Provider` attribute of the `Schema` element.</span></span>  
  
## <a name="providermanifesttoken-schema-attribute"></a><span data-ttu-id="d0145-108">ProviderManifestToken 架构属性</span><span class="sxs-lookup"><span data-stu-id="d0145-108">ProviderManifestToken Schema Attribute</span></span>  

 <span data-ttu-id="d0145-109">`ProviderManifestToken` 是以 SSDL 表示的 `Schema` 元素的一个必需特性。</span><span class="sxs-lookup"><span data-stu-id="d0145-109">`ProviderManifestToken` is a required attribute of the `Schema` element in SSDL.</span></span> <span data-ttu-id="d0145-110">此标记用于为脱机方案加载提供程序清单。</span><span class="sxs-lookup"><span data-stu-id="d0145-110">This token is used to load the provider manifest for offline scenarios.</span></span> <span data-ttu-id="d0145-111">有关特性的详细信息 `ProviderManifestToken` ，请参阅 [ (SSDL) 的架构元素 ](/ef/ef6/modeling/designer/advanced/edmx/ssdl-spec#schema-element-ssdl)。</span><span class="sxs-lookup"><span data-stu-id="d0145-111">For more information about `ProviderManifestToken` attribute, see [Schema Element (SSDL)](/ef/ef6/modeling/designer/advanced/edmx/ssdl-spec#schema-element-ssdl).</span></span>  
  
 <span data-ttu-id="d0145-112">SqlClient 可用作 SQL Server 的不同版本的数据访问接口。</span><span class="sxs-lookup"><span data-stu-id="d0145-112">SqlClient can be used as a data provider for different versions of SQL Server.</span></span> <span data-ttu-id="d0145-113">这些版本具有不同的功能。</span><span class="sxs-lookup"><span data-stu-id="d0145-113">These versions have different capabilities.</span></span> <span data-ttu-id="d0145-114">例如，SQL Server 2000 不支持 `varchar(max)` 和 `nvarchar(max)` SQL Server 2005 引入的类型。</span><span class="sxs-lookup"><span data-stu-id="d0145-114">For example, SQL Server 2000 does not support `varchar(max)` and `nvarchar(max)` types that were introduced with SQL Server 2005.</span></span>  
  
 <span data-ttu-id="d0145-115">针对不同版本的 SQL Server，SqlClient 生成和接受以下提供程序清单标记。</span><span class="sxs-lookup"><span data-stu-id="d0145-115">SqlClient produces and accepts the following provider manifest tokens for different versions of SQL Server.</span></span>  
  
|<span data-ttu-id="d0145-116">SQL Server 2000</span><span class="sxs-lookup"><span data-stu-id="d0145-116">SQL Server 2000</span></span>|<span data-ttu-id="d0145-117">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="d0145-117">SQL Server 2005</span></span>|<span data-ttu-id="d0145-118">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0145-118">SQL Server 2008</span></span>|  
|-|-|-|  
|<span data-ttu-id="d0145-119">2000</span><span class="sxs-lookup"><span data-stu-id="d0145-119">2000</span></span>|<span data-ttu-id="d0145-120">2005</span><span class="sxs-lookup"><span data-stu-id="d0145-120">2005</span></span>|<span data-ttu-id="d0145-121">2008</span><span class="sxs-lookup"><span data-stu-id="d0145-121">2008</span></span>|  
  
> [!NOTE]
> <span data-ttu-id="d0145-122">从 Visual Studio 2010 开始， [ADO.NET 实体数据模型工具](/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100)) 不支持 SQL Server 2000。</span><span class="sxs-lookup"><span data-stu-id="d0145-122">Starting with Visual Studio 2010, the [ADO.NET Entity Data Model Tools](/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100)) do not support SQL Server 2000.</span></span>  
  
## <a name="provider-namespace-name"></a><span data-ttu-id="d0145-123">提供程序命名空间名称</span><span class="sxs-lookup"><span data-stu-id="d0145-123">Provider Namespace Name</span></span>  

 <span data-ttu-id="d0145-124">所有提供程序都必须指定一个命名空间。</span><span class="sxs-lookup"><span data-stu-id="d0145-124">All providers must specify a namespace.</span></span> <span data-ttu-id="d0145-125">实体框架通过此属性获知提供程序为特定构造（如类型和函数）使用哪个前缀。</span><span class="sxs-lookup"><span data-stu-id="d0145-125">This property tells the Entity Framework which prefix is used by the provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="d0145-126">SqlClient 提供程序清单的命名空间为 `SqlServer`。</span><span class="sxs-lookup"><span data-stu-id="d0145-126">The namespace for SqlClient provider manifests is `SqlServer`.</span></span> <span data-ttu-id="d0145-127">有关命名空间的详细信息，请参阅 [命名空间](./language-reference/namespaces-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="d0145-127">For more information about namespaces, see [Namespaces](./language-reference/namespaces-entity-sql.md).</span></span>  
  
## <a name="types"></a><span data-ttu-id="d0145-128">类型</span><span class="sxs-lookup"><span data-stu-id="d0145-128">Types</span></span>  

 <span data-ttu-id="d0145-129">实体框架的 SqlClient 提供程序提供概念模型类型与 SQL Server 类型之间的映射信息。</span><span class="sxs-lookup"><span data-stu-id="d0145-129">The SqlClient provider for the Entity Framework provides mapping information between conceptual model types and SQL Server types.</span></span> <span data-ttu-id="d0145-130">有关详细信息，请参阅 [SqlClient For Entity sqlclient 类型](sqlclient-for-ef-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d0145-130">For more information, see [SqlClient for Entity FrameworkTypes](sqlclient-for-ef-types.md).</span></span>  
  
## <a name="functions"></a><span data-ttu-id="d0145-131">函数</span><span class="sxs-lookup"><span data-stu-id="d0145-131">Functions</span></span>  

 <span data-ttu-id="d0145-132">实体框架的 SqlClient 提供程序定义提供程序支持的函数列表。</span><span class="sxs-lookup"><span data-stu-id="d0145-132">The SqlClient provider for the Entity Framework defines the list of functions supported by the provider.</span></span> <span data-ttu-id="d0145-133">有关支持的函数的列表，请参阅 [SqlClient for 实体框架函数](sqlclient-for-ef-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="d0145-133">For a list of the supported functions, see [SqlClient for Entity Framework Functions](sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d0145-134">本节内容</span><span class="sxs-lookup"><span data-stu-id="d0145-134">In This Section</span></span>  

 [<span data-ttu-id="d0145-135">用于实体框架函数的 SqlClient</span><span class="sxs-lookup"><span data-stu-id="d0145-135">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)  
  
 [<span data-ttu-id="d0145-136">用于实体框架的 SqlClient 类型</span><span class="sxs-lookup"><span data-stu-id="d0145-136">SqlClient for Entity FrameworkTypes</span></span>](sqlclient-for-ef-types.md)  
  
 [<span data-ttu-id="d0145-137">SqlClient 中的已知问题（实体框架）</span><span class="sxs-lookup"><span data-stu-id="d0145-137">Known Issues in SqlClient for Entity Framework</span></span>](known-issues-in-sqlclient-for-entity-framework.md)  
  
## <a name="see-also"></a><span data-ttu-id="d0145-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0145-138">See also</span></span>

- [<span data-ttu-id="d0145-139">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="d0145-139">Entity SQL Language</span></span>](./language-reference/entity-sql-language.md)
- [<span data-ttu-id="d0145-140">语言参考</span><span class="sxs-lookup"><span data-stu-id="d0145-140">Language Reference</span></span>](./language-reference/index.md)
- [<span data-ttu-id="d0145-141">用于实体框架的 SqlClient 提供程序中的已知问题</span><span class="sxs-lookup"><span data-stu-id="d0145-141">Known Issues in SqlClient Provider for Entity Framework</span></span>](sqlclient-for-the-entity-framework.md)
