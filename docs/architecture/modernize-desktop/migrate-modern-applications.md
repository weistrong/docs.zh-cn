---
title: 迁移新式桌面应用程序
description: 对于新式桌面应用程序的迁移过程，需要了解的所有内容。
ms.date: 01/19/2021
ms.openlocfilehash: b5bea6e601dc040adfd8ed410320a3416cb3372e
ms.sourcegitcommit: 632818f4b527e5bf3c48fc04e0c7f3b4bdb8a248
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "98615758"
---
# <a name="migrating-modern-desktop-applications"></a><span data-ttu-id="e0417-103">迁移新式桌面应用程序</span><span class="sxs-lookup"><span data-stu-id="e0417-103">Migrating Modern Desktop applications</span></span>

<span data-ttu-id="e0417-104">在本章中，我们将探讨在将现有应用程序从 .NET Framework 迁移到 .NET 时遇到的最常见问题。</span><span class="sxs-lookup"><span data-stu-id="e0417-104">In this chapter, we're exploring the most common issues and challenges you can face when migrating an existing application from .NET Framework to .NET.</span></span>

<span data-ttu-id="e0417-105">复杂的桌面应用程序不能隔离，并且需要与可能驻留在本地计算机或远程服务器上的子系统进行某种类型的交互。</span><span class="sxs-lookup"><span data-stu-id="e0417-105">A complex desktop application doesn't work in isolation and needs some kind of interaction with subsystems that may reside on the local machine or on a remote server.</span></span> <span data-ttu-id="e0417-106">可能需要某种类型的数据库以本地或远程方式连接为永久性存储。</span><span class="sxs-lookup"><span data-stu-id="e0417-106">It will probably need some kind of database to connect as a persistence storage either locally or remotely.</span></span> <span data-ttu-id="e0417-107">随着 Internet 和面向服务的体系结构的增加，通常将应用程序连接到驻留在远程服务器或云中的某种服务。</span><span class="sxs-lookup"><span data-stu-id="e0417-107">With the raise of Internet and service-oriented architectures, it's common to have your application connected to some sort of service residing on a remote server or in the cloud.</span></span> <span data-ttu-id="e0417-108">可能需要访问计算机文件系统才能实现某些功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-108">You may need to access the machine file system to implement some functionality.</span></span> <span data-ttu-id="e0417-109">或者，可能使用的是位于应用程序外的 COM 对象内的一项功能，例如，如果要在应用程序中集成 Office 程序集，这是一个常见方案。</span><span class="sxs-lookup"><span data-stu-id="e0417-109">Alternatively, maybe you're using a piece of functionality that resides inside a COM object outside your application, which is a common scenario if, for example, you're integrating Office assemblies in your app.</span></span>

<span data-ttu-id="e0417-110">此外，在 .NET Framework 和 .NET 公开的 API 图面上存在差异，并且 .NET Framework 上可用的某些功能在 .NET 上不可用。</span><span class="sxs-lookup"><span data-stu-id="e0417-110">Besides, there are differences in the API surface that is exposed by .NET Framework and .NET, and some features that are available on .NET Framework aren't available on .NET.</span></span> <span data-ttu-id="e0417-111">因此，在规划迁移时，必须了解并考虑这些问题。</span><span class="sxs-lookup"><span data-stu-id="e0417-111">So, it's important for you to know and take them into account when planning a migration.</span></span>

## <a name="configuration-files"></a><span data-ttu-id="e0417-112">配置文件</span><span class="sxs-lookup"><span data-stu-id="e0417-112">Configuration files</span></span>

<span data-ttu-id="e0417-113">配置文件可用于存储在运行时读取的属性集，并影响我们的应用程序的行为，例如在何处查找数据库或执行循环的次数。</span><span class="sxs-lookup"><span data-stu-id="e0417-113">Configuration files offer the possibility to store sets of properties that are read at run time and affect the behavior of our apps, such as where to locate a database or how many times to execute a loop.</span></span> <span data-ttu-id="e0417-114">此方法的优点是，您可以修改应用程序的某些方面，而无需重新编码并重新编译。</span><span class="sxs-lookup"><span data-stu-id="e0417-114">The beauty of this technique is that you can modify some aspects of the application without the need to recode and recompile.</span></span> <span data-ttu-id="e0417-115">例如，当同一应用程序代码在具有一组特定配置值的开发环境中运行时，以及在生产环境中使用不同的配置值运行时，这会很方便。</span><span class="sxs-lookup"><span data-stu-id="e0417-115">This comes in handy when, for example, the same app code runs on a development environment with a certain set of configuration values and in production with a different one.</span></span>

### <a name="configuration-on-net-framework"></a><span data-ttu-id="e0417-116">.NET Framework 上的配置</span><span class="sxs-lookup"><span data-stu-id="e0417-116">Configuration on .NET Framework</span></span>

<span data-ttu-id="e0417-117">如果使用的是工作 .NET Framework 桌面应用程序，则可能是通过 <xref:System.Configuration.AppSettingsSection> 命名空间中的类访问了app.config文件 `System.Configuration` 。</span><span class="sxs-lookup"><span data-stu-id="e0417-117">If you have a working .NET Framework desktop application, chances are you have an *app.config* file accessed through the <xref:System.Configuration.AppSettingsSection> class from the `System.Configuration` namespace.</span></span>

<span data-ttu-id="e0417-118">在 .NET Framework 基础结构中，有一个从其父项继承属性的配置文件的层次结构。</span><span class="sxs-lookup"><span data-stu-id="e0417-118">Within the .NET Framework infrastructure, there's a hierarchy of configuration files that inherit properties from its parents.</span></span> <span data-ttu-id="e0417-119">您可以找到一个 *machine.config* 文件，该文件定义了许多可在任何子代配置文件中使用或重写的属性和配置节。</span><span class="sxs-lookup"><span data-stu-id="e0417-119">You can find a *machine.config* file that defines many properties and configuration sections that can be used or overridden in any descendant configuration file.</span></span>

### <a name="configuration-on-net"></a><span data-ttu-id="e0417-120">.NET 上的配置</span><span class="sxs-lookup"><span data-stu-id="e0417-120">Configuration on .NET</span></span>

<span data-ttu-id="e0417-121">.NET world 中没有 *machine.config* 的文件。</span><span class="sxs-lookup"><span data-stu-id="e0417-121">In the .NET world, there's no *machine.config* file.</span></span> <span data-ttu-id="e0417-122">即使您可以继续使用旧的传统 <xref:System.Configuration> 命名空间，您也可以考虑切换到新式 <xref:Microsoft.Extensions.Configuration> ，这提供了很多增强功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-122">And even though you can continue to use the old fashioned <xref:System.Configuration> namespace, you may consider switching to the modern <xref:Microsoft.Extensions.Configuration>, which offers a good number of enhancements.</span></span>

<span data-ttu-id="e0417-123">配置 API 支持配置提供程序的概念，该概念定义用于加载配置的数据源。</span><span class="sxs-lookup"><span data-stu-id="e0417-123">The configuration API supports the concept of configuration provider, which defines the data source to be used to load the configuration.</span></span> <span data-ttu-id="e0417-124">内置提供程序有不同种类，例如：</span><span class="sxs-lookup"><span data-stu-id="e0417-124">There are different kinds of built-in providers, such as:</span></span>

- <span data-ttu-id="e0417-125">内存中的 .NET 对象</span><span class="sxs-lookup"><span data-stu-id="e0417-125">In-memory .NET objects</span></span>
- <span data-ttu-id="e0417-126">INI 文件</span><span class="sxs-lookup"><span data-stu-id="e0417-126">INI files</span></span>
- <span data-ttu-id="e0417-127">JSON 文件</span><span class="sxs-lookup"><span data-stu-id="e0417-127">JSON files</span></span>
- <span data-ttu-id="e0417-128">XML 文件</span><span class="sxs-lookup"><span data-stu-id="e0417-128">XML files</span></span>
- <span data-ttu-id="e0417-129">命令行参数</span><span class="sxs-lookup"><span data-stu-id="e0417-129">Command-line arguments</span></span>
- <span data-ttu-id="e0417-130">环境变量</span><span class="sxs-lookup"><span data-stu-id="e0417-130">Environment variables</span></span>
- <span data-ttu-id="e0417-131">加密的用户存储</span><span class="sxs-lookup"><span data-stu-id="e0417-131">Encrypted user store</span></span>

 <span data-ttu-id="e0417-132">您也可以构建自己的。</span><span class="sxs-lookup"><span data-stu-id="e0417-132">Or you can build your own.</span></span>

<span data-ttu-id="e0417-133">新配置允许可分组为多层层次结构的名称-值对的列表。</span><span class="sxs-lookup"><span data-stu-id="e0417-133">The new configuration allows a list of name-value pairs that can be grouped into a multi-level hierarchy.</span></span> <span data-ttu-id="e0417-134">任何存储的值都映射到一个字符串，并且提供内置的绑定支持，使你能够将设置反序列化为自定义的普通旧 CLR 对象 (POCO) 对象。</span><span class="sxs-lookup"><span data-stu-id="e0417-134">Any stored value maps to a string, and there's built-in binding support that allows you to deserialize settings into a custom plain old CLR object (POCO) object.</span></span>

<span data-ttu-id="e0417-135"><xref:Microsoft.Extensions.Configuration.ConfigurationBuilder>对象允许你添加应用程序可能需要的多个配置提供程序，并使用优先规则解析首选项。</span><span class="sxs-lookup"><span data-stu-id="e0417-135">The <xref:Microsoft.Extensions.Configuration.ConfigurationBuilder> object lets you add as many configuration providers you may need for your application, using a precedence rule to resolve preference.</span></span> <span data-ttu-id="e0417-136">因此，在代码中添加的最后一个提供程序将覆盖其他提供程序。</span><span class="sxs-lookup"><span data-stu-id="e0417-136">So, the last provider you add in your code will override the others.</span></span> <span data-ttu-id="e0417-137">这是一项很好的功能，可用于管理不同的执行环境，因为开发、测试和生产环境可以定义不同的配置，并在代码中的单个函数上管理它们。</span><span class="sxs-lookup"><span data-stu-id="e0417-137">This is a great feature for managing different environments for execution since you can define different configurations for development, testing and production environments, and manage them on a single function inside your code.</span></span>

### <a name="migrating-configuration-files"></a><span data-ttu-id="e0417-138">正在迁移配置文件</span><span class="sxs-lookup"><span data-stu-id="e0417-138">Migrating Configuration files</span></span>

<span data-ttu-id="e0417-139">你可以继续使用现有的 app.config XML 文件。</span><span class="sxs-lookup"><span data-stu-id="e0417-139">You can continue to use your existing app.config XML file.</span></span> <span data-ttu-id="e0417-140">但是，你可以利用此机会来迁移配置，使其受益于 .NET 中的多项增强功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-140">However, you could take this opportunity to migrate your configuration to benefit from the several enhancements made on .NET.</span></span>

<span data-ttu-id="e0417-141">若要从旧样式的 *app.config* 迁移到新的配置文件，应选择 XML 格式和 JSON 格式。</span><span class="sxs-lookup"><span data-stu-id="e0417-141">To migrate from an old-style *app.config* to a new configuration file, you should choose between an XML format and a JSON format.</span></span>

<span data-ttu-id="e0417-142">如果选择 XML，则转换会很简单。</span><span class="sxs-lookup"><span data-stu-id="e0417-142">If you choose XML, the conversion is straightforward.</span></span> <span data-ttu-id="e0417-143">由于内容相同，因此只需将 XML 类型的 *app.config* 文件保存为类型即可。</span><span class="sxs-lookup"><span data-stu-id="e0417-143">Since the content is the same, just save the *app.config* file with XML as type.</span></span> <span data-ttu-id="e0417-144">然后，将引用 AppSettings 的代码更改为使用 `ConfigurationBuilder` 类。</span><span class="sxs-lookup"><span data-stu-id="e0417-144">Then, change the code that references AppSettings to use the `ConfigurationBuilder` class.</span></span> <span data-ttu-id="e0417-145">此更改应该很简单。</span><span class="sxs-lookup"><span data-stu-id="e0417-145">This change should be easy.</span></span>

<span data-ttu-id="e0417-146">如果要使用 JSON 格式，而不想手动迁移，则可以在 .NET 上使用一个名为 [dotnet-config2json](https://www.nuget.org/packages/dotnet-config2json/) 的工具，该工具可以将 *app.config* 文件转换为 JSON 配置文件。</span><span class="sxs-lookup"><span data-stu-id="e0417-146">If you want to use a JSON format and you don't want to migrate by hand, there's a tool called [dotnet-config2json](https://www.nuget.org/packages/dotnet-config2json/) available on .NET that can convert an *app.config* file to a JSON configuration file.</span></span>

<span data-ttu-id="e0417-147">使用 *machine.config* 文件中定义的配置节时，还可能会遇到一些问题。</span><span class="sxs-lookup"><span data-stu-id="e0417-147">You may also come across some issues when using configuration sections that were defined in the *machine.config* file.</span></span> <span data-ttu-id="e0417-148">例如，请考虑以下配置：</span><span class="sxs-lookup"><span data-stu-id="e0417-148">For example, consider the following configuration:</span></span>

```xml
<configuration>
    <system.diagnostics>
        <switches>
            <add name="General" value="4" />
        </switches>
        <trace autoflush="true" indentsize="2">
            <listeners>
                <add name="myListener"
                     type="System.Diagnostics.TextWriterTraceListener,
                           System, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"
                     initializeData="MyListener.log"
                     traceOutputOptions="ProcessId, LogicalOperationStack, Timestamp, ThreadId, Callstack, DateTime" />
            </listeners>
        </trace>
    </system.diagnostics>
</configuration>
```

<span data-ttu-id="e0417-149">如果将此配置用于 .NET，则会出现异常：</span><span class="sxs-lookup"><span data-stu-id="e0417-149">If you take this configuration to a .NET, you'll get an exception:</span></span>

> <span data-ttu-id="e0417-150">无法识别的配置节系统。诊断</span><span class="sxs-lookup"><span data-stu-id="e0417-150">Unrecognized configuration section System.Diagnostics</span></span>

<span data-ttu-id="e0417-151">发生此异常的原因是，该部分和负责处理该节的程序集已在 *machine.config* 文件中定义，该文件现在不存在。</span><span class="sxs-lookup"><span data-stu-id="e0417-151">This exception occurs because that section and the assembly responsible for handling that section was defined in the *machine.config* file, which now doesn't exist.</span></span>

<span data-ttu-id="e0417-152">若要轻松地解决此问题，可以将部分定义从旧的 *machine.config* 复制到新的配置文件中：</span><span class="sxs-lookup"><span data-stu-id="e0417-152">To easily fix the issue, you can copy the section definition from your old *machine.config* to your new configuration file:</span></span>

```xml
<configSections>
    <section name="system.diagnostics"
             type="System.Diagnostics.SystemDiagnosticsSection,
                   System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
</configSections>
```

## <a name="accessing-databases"></a><span data-ttu-id="e0417-153">访问数据库</span><span class="sxs-lookup"><span data-stu-id="e0417-153">Accessing databases</span></span>

<span data-ttu-id="e0417-154">几乎每个桌面应用程序都需要某种类型的数据库。</span><span class="sxs-lookup"><span data-stu-id="e0417-154">Almost every desktop application needs some kind of database.</span></span> <span data-ttu-id="e0417-155">对于桌面版，通常可以使用桌面应用程序和数据库引擎之间的直接连接来查找客户端-服务器体系结构。</span><span class="sxs-lookup"><span data-stu-id="e0417-155">For desktop, it's common to find client-server architectures with a direct connection between the desktop app and the database engine.</span></span> <span data-ttu-id="e0417-156">这些数据库可以是本地的，也可以是远程的，具体取决于需要在不同用户之间共享信息。</span><span class="sxs-lookup"><span data-stu-id="e0417-156">These databases can be local or remote depending on the need to share information between different users.</span></span>

<span data-ttu-id="e0417-157">从代码的角度来看，有许多技术和框架，使开发人员能够连接、查询和更新数据库。</span><span class="sxs-lookup"><span data-stu-id="e0417-157">From the code perspective, there have been many technologies and frameworks to give the developer the possibility to connect, query, and update a database.</span></span>

<span data-ttu-id="e0417-158">当您谈论 Windows 桌面应用程序时，您可以找到的最常见数据库示例为 Microsoft Access 和 Microsoft SQL Server。</span><span class="sxs-lookup"><span data-stu-id="e0417-158">The most common examples of database you can find when talking about Windows Desktop application are Microsoft Access and Microsoft SQL Server.</span></span> <span data-ttu-id="e0417-159">如果你的桌面编程经验超过20多年，ODBC、OLEDB、RDO、ADO、ADO.NET、LINQ 和实体框架等名称将非常熟悉。</span><span class="sxs-lookup"><span data-stu-id="e0417-159">If you have more than 20 years of experience programming for the desktop, names like ODBC, OLEDB, RDO, ADO, ADO.NET, LINQ, and Entity Framework will sound familiar.</span></span>

### <a name="odbc"></a><span data-ttu-id="e0417-160">ODBC</span><span class="sxs-lookup"><span data-stu-id="e0417-160">ODBC</span></span>

<span data-ttu-id="e0417-161">由于 Microsoft 提供 `System.Data.Odbc` 与 .NET Standard 2.0 兼容的库，因此你可以继续在 .net 上使用 ODBC。</span><span class="sxs-lookup"><span data-stu-id="e0417-161">You can continue to use ODBC on .NET since Microsoft is providing the `System.Data.Odbc` library compatible with .NET Standard 2.0.</span></span>

### <a name="ole-db"></a><span data-ttu-id="e0417-162">OLE DB</span><span class="sxs-lookup"><span data-stu-id="e0417-162">OLE DB</span></span>

<span data-ttu-id="e0417-163">[OLE DB](/previous-versions/windows/desktop/ms722784(v=vs.85)) 是一种以统一方式访问各种数据源的好方法。</span><span class="sxs-lookup"><span data-stu-id="e0417-163">[OLE DB](/previous-versions/windows/desktop/ms722784(v=vs.85)) has been a great way to access various data sources in a uniform manner.</span></span> <span data-ttu-id="e0417-164">但它是基于 COM 的，后者是一种仅适用于 Windows 的技术，因此不适合用于 .NET 等跨平台技术。</span><span class="sxs-lookup"><span data-stu-id="e0417-164">But it was based on COM, which is a Windows-only technology, and as such wasn't the best fit for a cross-platform technology such as .NET.</span></span> <span data-ttu-id="e0417-165">在 SQL Server 版本2014及更高版本中也不受支持。</span><span class="sxs-lookup"><span data-stu-id="e0417-165">It's also unsupported in SQL Server versions 2014 and later.</span></span> <span data-ttu-id="e0417-166">由于这些原因，.NET 不支持 OLE DB。</span><span class="sxs-lookup"><span data-stu-id="e0417-166">For those reasons, OLE DB won't be supported by .NET.</span></span>

### <a name="adonet"></a><span data-ttu-id="e0417-167">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e0417-167">ADO.NET</span></span>

<span data-ttu-id="e0417-168">你仍可以从 .NET 上现有的桌面代码使用 ADO.NET。</span><span class="sxs-lookup"><span data-stu-id="e0417-168">You can still use ADO.NET from your existing desktop code on .NET.</span></span> <span data-ttu-id="e0417-169">只需更新某些 NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="e0417-169">You just need to update some NuGet packages.</span></span>

### <a name="ef-core-vs-ef6"></a><span data-ttu-id="e0417-170">EF Core 与 EF6</span><span class="sxs-lookup"><span data-stu-id="e0417-170">EF Core vs. EF6</span></span>

<span data-ttu-id="e0417-171">当前支持的两个版本实体框架 (EF) ，实体框架 6 (EF6) 和 EF Core。</span><span class="sxs-lookup"><span data-stu-id="e0417-171">There are two currently supported versions of Entity Framework (EF), Entity Framework 6 (EF6) and EF Core.</span></span>

<span data-ttu-id="e0417-172">作为 .NET Framework 世界中发布的最新技术实体框架，6.4 是最新版本。</span><span class="sxs-lookup"><span data-stu-id="e0417-172">The latest technology released as part of the .NET Framework world is Entity Framework, with 6.4 being the latest version.</span></span> <span data-ttu-id="e0417-173">通过启动 .NET Core，Microsoft 还发布了基于实体框架的新数据访问堆栈，并将其称为 Entity Framework Core。</span><span class="sxs-lookup"><span data-stu-id="e0417-173">With the launch of .NET Core, Microsoft also released a new data access stack based on Entity Framework and called Entity Framework Core.</span></span>

<span data-ttu-id="e0417-174">可以从 .NET Framework 和 .NET 使用 EF 6.4 和 EF Core。</span><span class="sxs-lookup"><span data-stu-id="e0417-174">You can use EF 6.4 and EF Core from both .NET Framework and .NET.</span></span> <span data-ttu-id="e0417-175">那么，有哪些决策驱动因素可帮助确定这两者之间的关系呢？</span><span class="sxs-lookup"><span data-stu-id="e0417-175">So, what are the decision drivers to help to decide between the two?</span></span>

<span data-ttu-id="e0417-176">EF 6.3 是 EF6 的第一个版本，可在 .NET 上运行并跨平台工作。</span><span class="sxs-lookup"><span data-stu-id="e0417-176">EF 6.3 is the first version of EF6 that can run on .NET and work cross-platform.</span></span> <span data-ttu-id="e0417-177">事实上，此版本的主要目标是为了更轻松地将使用 EF6 的现有应用程序迁移到 .NET。</span><span class="sxs-lookup"><span data-stu-id="e0417-177">In fact, the main goal of this release was to make it easier to migrate existing applications that use EF6 to .NET.</span></span>

<span data-ttu-id="e0417-178">EF Core 旨在提供类似于 EF6 的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="e0417-178">EF Core was designed to provide a developer experience similar to EF6.</span></span> <span data-ttu-id="e0417-179">大多数顶级 API 保持不变，因此，用过 EF6 的开发人员都会对 EF Core 感到很熟悉。</span><span class="sxs-lookup"><span data-stu-id="e0417-179">Most of the top-level APIs remain the same, so EF Core will feel familiar to developers who have used EF6.</span></span>

<span data-ttu-id="e0417-180">尽管兼容，但在做出决定之前，应检查实现情况。</span><span class="sxs-lookup"><span data-stu-id="e0417-180">Although compatible, there are differences on the implementation you should check before making a decision.</span></span>
<span data-ttu-id="e0417-181">有关详细信息，请参阅 [EF6 & 比较 EF Core](/ef/efcore-and-ef6/)。</span><span class="sxs-lookup"><span data-stu-id="e0417-181">For more information, see [Compare EF Core & EF6](/ef/efcore-and-ef6/).</span></span>

<span data-ttu-id="e0417-182">建议在以下情况中使用 EF Core：</span><span class="sxs-lookup"><span data-stu-id="e0417-182">The recommendation is to use EF Core if:</span></span>

* <span data-ttu-id="e0417-183">应用需要 .NET 功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-183">The app needs the capabilities of .NET.</span></span>
* <span data-ttu-id="e0417-184">EF Core 支持应用需要的所有功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-184">EF Core supports all of the features that the app requires.</span></span>

<span data-ttu-id="e0417-185">如果以下两个条件都成立，请考虑使用 EF6：</span><span class="sxs-lookup"><span data-stu-id="e0417-185">Consider using EF6 if both of the following conditions are true:</span></span>

* <span data-ttu-id="e0417-186">该应用程序将在 Windows 上运行，并 .NET Framework 4.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="e0417-186">The app will run on Windows and .NET Framework 4.0 or later.</span></span>
* <span data-ttu-id="e0417-187">EF6 支持应用需要的所有功能。</span><span class="sxs-lookup"><span data-stu-id="e0417-187">EF6 supports all of the features that the app requires.</span></span>

### <a name="relational-databases"></a><span data-ttu-id="e0417-188">关系数据库</span><span class="sxs-lookup"><span data-stu-id="e0417-188">Relational databases</span></span>

#### <a name="sql-server"></a><span data-ttu-id="e0417-189">SQL Server</span><span class="sxs-lookup"><span data-stu-id="e0417-189">SQL Server</span></span>

<span data-ttu-id="e0417-190">如果你在几年前就为桌面开发，SQL Server 是所选的一个数据库。</span><span class="sxs-lookup"><span data-stu-id="e0417-190">SQL Server has been one of the databases of choice if you were developing for the desktop some years ago.</span></span> <span data-ttu-id="e0417-191">使用 <xref:System.Data.SqlClient> .NET Framework 中的，你可以访问 SQL Server 的版本，它封装了特定于数据库的协议。</span><span class="sxs-lookup"><span data-stu-id="e0417-191">With the use of <xref:System.Data.SqlClient> in .NET Framework, you could access versions of SQL Server, which encapsulates database-specific protocols.</span></span>

<span data-ttu-id="e0417-192">在 .NET 中，可以找到 `SqlClient` 与 .NET Framework 中现有的类完全兼容的新类，但这些类位于 <xref:Microsoft.Data.SqlClient> 库中。</span><span class="sxs-lookup"><span data-stu-id="e0417-192">In .NET, you can find a new `SqlClient` class, fully compatible with the one existing in the .NET Framework but located in the <xref:Microsoft.Data.SqlClient> library.</span></span> <span data-ttu-id="e0417-193">只需添加对 [SqlClient](https://www.nuget.org/packages/Microsoft.Data.SqlClient/) NuGet 包的引用，并对命名空间进行一些重命名，一切都应按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="e0417-193">You just have to add a reference to the [Microsoft.Data.SqlClient](https://www.nuget.org/packages/Microsoft.Data.SqlClient/) NuGet package and do some renaming for the namespaces and everything should work as expected.</span></span>

#### <a name="microsoft-access"></a><span data-ttu-id="e0417-194">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="e0417-194">Microsoft Access</span></span>

<span data-ttu-id="e0417-195">Microsoft Access 已用于多年，当不需要复杂的、可缩放的 SQL Server 时。</span><span class="sxs-lookup"><span data-stu-id="e0417-195">Microsoft Access has been used for years when the sophisticated and more scalable SQL Server wasn't needed.</span></span> <span data-ttu-id="e0417-196">你仍可以使用库连接到 Microsoft Access <xref:System.Data.Odbc> 。</span><span class="sxs-lookup"><span data-stu-id="e0417-196">You can still connect to Microsoft Access using the <xref:System.Data.Odbc> library.</span></span>

## <a name="consuming-services"></a><span data-ttu-id="e0417-197">使用服务</span><span class="sxs-lookup"><span data-stu-id="e0417-197">Consuming services</span></span>

<span data-ttu-id="e0417-198">随着面向服务的体系结构的引发，桌面应用程序开始从客户端-服务器模型发展为三层方法。</span><span class="sxs-lookup"><span data-stu-id="e0417-198">With the raise of service-oriented architectures, desktop applications began to evolve from a client-server model to the three-layer approach.</span></span> <span data-ttu-id="e0417-199">在客户端-服务器方法中，将建立直接的数据库连接，该客户端通常在单个 EXE 文件中包含业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="e0417-199">In the client-server approach, a direct database connection is established from the client holding the business logic usually inside a single EXE file.</span></span> <span data-ttu-id="e0417-200">另一方面，三层方法建立了一个实现业务逻辑和数据库访问的中间服务层，从而实现更好的安全性、可伸缩性和可重用性。</span><span class="sxs-lookup"><span data-stu-id="e0417-200">On the other hand, the three-layer approach establishes an intermediate service layer implementing business logic and database access allowing for better security, scalability, and reusability.</span></span> <span data-ttu-id="e0417-201">该层方法不是直接使用数据的数据集，而是依赖于一组实现协定和类型对象的服务来实现数据传输。</span><span class="sxs-lookup"><span data-stu-id="e0417-201">Instead of working directly with datasets of data, the layer approach relies in a set of services implementing contracts and types objects as a way to implement data transfer.</span></span>

<span data-ttu-id="e0417-202">如果你有使用 WCF 服务的桌面应用程序，并且想要将其迁移到 .NET，则需要考虑一些事项。</span><span class="sxs-lookup"><span data-stu-id="e0417-202">If you have a desktop application using a WCF service and you want to migrate it to .NET, there are some things to consider.</span></span>

<span data-ttu-id="e0417-203">第一件事是如何解析配置以访问服务。</span><span class="sxs-lookup"><span data-stu-id="e0417-203">The first thing is how to resolve the configuration to access the service.</span></span> <span data-ttu-id="e0417-204">因为 .NET 中的配置不同，所以需要在配置文件中进行一些更新。</span><span class="sxs-lookup"><span data-stu-id="e0417-204">Because the configuration is different on .NET, you'll need to make some updates in your configuration file.</span></span>

<span data-ttu-id="e0417-205">其次，你需要通过 Visual Studio 2019 上提供的新工具重新生成服务客户端。</span><span class="sxs-lookup"><span data-stu-id="e0417-205">Second, you'll need to regenerate the service client with the new tools present on Visual Studio 2019.</span></span> <span data-ttu-id="e0417-206">在此步骤中，您必须考虑激活同步操作的生成，以使客户端与现有代码兼容。</span><span class="sxs-lookup"><span data-stu-id="e0417-206">In this step, you must consider activating the generation of the synchronous operations to make the client compatible with your existing code.</span></span>

<span data-ttu-id="e0417-207">迁移后，如果发现 .NET 上没有所需的库，则可以添加对 [Microsoft. 兼容性](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) NuGet 包的引用，并查看是否存在缺少的函数。</span><span class="sxs-lookup"><span data-stu-id="e0417-207">After the migration, if you find that there are libraries you need that aren't present on .NET, you can add a reference to the [Microsoft.Windows.Compatibility](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) NuGet package and see if the missing functions are there.</span></span>

<span data-ttu-id="e0417-208">如果要使用 <xref:System.Net.WebRequest> 类来执行 web 服务调用，可能会发现 .net 有一些不同之处。</span><span class="sxs-lookup"><span data-stu-id="e0417-208">If you're using the <xref:System.Net.WebRequest> class to perform web service calls, you may find some differences on .NET.</span></span> <span data-ttu-id="e0417-209">建议改为使用 HttpClient 的。</span><span class="sxs-lookup"><span data-stu-id="e0417-209">The recommendation is to use the System.Net.Http.HttpClient instead.</span></span>

## <a name="consuming-a-com-object"></a><span data-ttu-id="e0417-210">使用 COM 对象</span><span class="sxs-lookup"><span data-stu-id="e0417-210">Consuming a COM Object</span></span>

<span data-ttu-id="e0417-211">目前，无法从 Visual Studio 2019 添加对 COM 对象的引用以与 .NET 一起使用。</span><span class="sxs-lookup"><span data-stu-id="e0417-211">Currently, there's no way to add a reference to a COM object from Visual Studio 2019 to use with .NET.</span></span> <span data-ttu-id="e0417-212">因此，你必须手动修改项目文件。</span><span class="sxs-lookup"><span data-stu-id="e0417-212">So, you have to manually modify the project file.</span></span>

<span data-ttu-id="e0417-213">`COMReference`在项目文件中插入结构，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="e0417-213">Insert a `COMReference` structure inside the project file like in the following example:</span></span>

```xml
<ItemGroup>
    <COMReference Include="MSHTML">
        <Guid>{3050F1C5-98B5-11CF-BB82-00AA00BDCE0B}\</Guid>
        <VersionMajor>4</VersionMajor>
        <VersionMinor>0</VersionMinor>
        <Lcid>0</Lcid>
        <WrapperTool>primary</WrapperTool>
        <Isolated>false</Isolated>
    </COMReference>
</ItemGroup>
```

## <a name="more-things-to-consider"></a><span data-ttu-id="e0417-214">更多注意事项</span><span class="sxs-lookup"><span data-stu-id="e0417-214">More things to consider</span></span>

<span data-ttu-id="e0417-215">可用于 .NET Framework 库的多种技术对于 .NET Core 或 .NET 5 不可用。</span><span class="sxs-lookup"><span data-stu-id="e0417-215">Several technologies available to .NET Framework libraries aren't available for .NET Core or .NET 5.</span></span> <span data-ttu-id="e0417-216">如果你的代码依赖于其中一些技术，请考虑此部分中所述的替代方法。</span><span class="sxs-lookup"><span data-stu-id="e0417-216">If your code relies on some of these technologies, consider the alternative approaches outlined in this section.</span></span>

<span data-ttu-id="e0417-217">[Windows 兼容性包](../../core/porting/windows-compat-pack.md)提供对以前仅对 .NET Framework 可用的 api 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="e0417-217">The [Windows Compatibility Pack](../../core/porting/windows-compat-pack.md) provides access to APIs that were previously available only for .NET Framework.</span></span> <span data-ttu-id="e0417-218">它可用于 .NET Core 和 .NET Standard 项目。</span><span class="sxs-lookup"><span data-stu-id="e0417-218">It can be used on .NET Core and .NET Standard projects.</span></span>

<span data-ttu-id="e0417-219">有关 API 兼容性的详细信息，可以在中找到有关重大更改和弃用的 Api 的文档 <https://docs.microsoft.com/dotnet/core/compatibility/fx-core> 。</span><span class="sxs-lookup"><span data-stu-id="e0417-219">For more information on API compatibility, you can find documentation about breaking changes and deprecated/legacy APIs at <https://docs.microsoft.com/dotnet/core/compatibility/fx-core>.</span></span>

### <a name="appdomains"></a><span data-ttu-id="e0417-220">AppDomain</span><span class="sxs-lookup"><span data-stu-id="e0417-220">AppDomains</span></span>

<span data-ttu-id="e0417-221">应用程序域 (AppDomain) 可将应用相互隔离。</span><span class="sxs-lookup"><span data-stu-id="e0417-221">Application domains (AppDomains) isolate apps from one another.</span></span> <span data-ttu-id="e0417-222">Appdomain 需要运行时支持，而且成本高昂。</span><span class="sxs-lookup"><span data-stu-id="e0417-222">AppDomains require runtime support and are expensive.</span></span> <span data-ttu-id="e0417-223">不支持创建其他应用程序域。</span><span class="sxs-lookup"><span data-stu-id="e0417-223">Creating additional app domains isn't supported.</span></span> <span data-ttu-id="e0417-224">对于代码隔离，建议将流程分隔开来或将容器用作一种替代方法。</span><span class="sxs-lookup"><span data-stu-id="e0417-224">For code isolation, we recommend separate processes or using containers as an alternative.</span></span> <span data-ttu-id="e0417-225">对于动态加载的程序集，我们建议使用新的 <xref:System.Runtime.Loader.AssemblyLoadContext> 类。</span><span class="sxs-lookup"><span data-stu-id="e0417-225">For the dynamic loading of assemblies, we recommend the new <xref:System.Runtime.Loader.AssemblyLoadContext> class.</span></span>

<span data-ttu-id="e0417-226">为了更轻松地从 .NET Framework 迁移代码，.NET 公开了某些 `AppDomain` API 图面。</span><span class="sxs-lookup"><span data-stu-id="e0417-226">To make code migration from .NET Framework easier, .NET exposes some of the `AppDomain` API surface.</span></span> <span data-ttu-id="e0417-227">一些 API 可正常工作（例如 <xref:System.AppDomain.UnhandledException?displayProperty=nameWithType>），一些成员不会执行任何操作（例如 <xref:System.AppDomain.SetCachePath%2A>），也有一些会引发 <xref:System.PlatformNotSupportedException>（例如 <xref:System.AppDomain.CreateDomain%2A>）。</span><span class="sxs-lookup"><span data-stu-id="e0417-227">Some of the APIs function normally (for example, <xref:System.AppDomain.UnhandledException?displayProperty=nameWithType>), some members do nothing (for example, <xref:System.AppDomain.SetCachePath%2A>), and some of them throw <xref:System.PlatformNotSupportedException> (for example, <xref:System.AppDomain.CreateDomain%2A>).</span></span>

### <a name="remoting"></a><span data-ttu-id="e0417-228">远程处理</span><span class="sxs-lookup"><span data-stu-id="e0417-228">Remoting</span></span>

<span data-ttu-id="e0417-229">.NET 远程处理用于跨 AppDomain 通信，这不再受支持。</span><span class="sxs-lookup"><span data-stu-id="e0417-229">.NET Remoting was used for cross-AppDomain communication, which is no longer supported.</span></span> <span data-ttu-id="e0417-230">同样，远程处理也需要运行时支持，进行维护的成本较高。</span><span class="sxs-lookup"><span data-stu-id="e0417-230">Also, Remoting requires runtime support, which is expensive to maintain.</span></span> <span data-ttu-id="e0417-231">由于这些原因，.net 不支持 .net 远程处理。</span><span class="sxs-lookup"><span data-stu-id="e0417-231">For these reasons, .NET Remoting isn't supported on .NET.</span></span>

<span data-ttu-id="e0417-232">对于跨进程的通信，应考虑将进程间通信 (IPC) 机制，作为远程处理（如或类）的替代方法 <xref:System.IO.Pipes?displayProperty=nameWithType> <xref:System.IO.MemoryMappedFiles.MemoryMappedFile> 。</span><span class="sxs-lookup"><span data-stu-id="e0417-232">For communication across processes, you should consider inter-process communication (IPC) mechanisms as an alternative to Remoting, such as the <xref:System.IO.Pipes?displayProperty=nameWithType> or the <xref:System.IO.MemoryMappedFiles.MemoryMappedFile> class.</span></span>

<span data-ttu-id="e0417-233">对于跨计算机的通信，可将基于网络的解决方案用作备用方案。</span><span class="sxs-lookup"><span data-stu-id="e0417-233">Across machines, use a network-based solution as an alternative.</span></span> <span data-ttu-id="e0417-234">最好使用低开销的明文协议，如 HTTP。</span><span class="sxs-lookup"><span data-stu-id="e0417-234">Preferably, use a low-overhead plaintext protocol, such as HTTP.</span></span> <span data-ttu-id="e0417-235">此处，ASP.NET Core 使用的 Web 服务器 Kestrel Web 服务器是一个选择。</span><span class="sxs-lookup"><span data-stu-id="e0417-235">The Kestrel web server, the web server used by ASP.NET Core, is an option here.</span></span>

### <a name="code-access-security-cas"></a><span data-ttu-id="e0417-236">代码访问安全性 (CAS)</span><span class="sxs-lookup"><span data-stu-id="e0417-236">Code Access Security (CAS)</span></span>

<span data-ttu-id="e0417-237">沙盒，它依赖于运行时或框架来约束托管应用程序或库使用或运行的资源，但在 .NET 上不受支持。</span><span class="sxs-lookup"><span data-stu-id="e0417-237">Sandboxing, which relies on the runtime or the framework to constrain which resources a managed application or library uses or runs, isn't supported on .NET.</span></span>

<span data-ttu-id="e0417-238">使用由操作系统提供的安全边界，如虚拟化、容器或用户帐户，用于以最小特权集运行进程。</span><span class="sxs-lookup"><span data-stu-id="e0417-238">Use security boundaries that are provided by the operating system, such as virtualization, containers, or user accounts for running processes with the minimum set of privileges.</span></span>

### <a name="security-transparency"></a><span data-ttu-id="e0417-239">安全透明度</span><span class="sxs-lookup"><span data-stu-id="e0417-239">Security Transparency</span></span>

<span data-ttu-id="e0417-240">与 CAS 相似，借助安全透明度可以以声明性方式将沙盒代码与安全关键代码隔离，但是不再支持将它作为安全边界。</span><span class="sxs-lookup"><span data-stu-id="e0417-240">Similar to CAS, Security Transparency separates sandboxed code from security critical code in a declarative fashion but is no longer supported as a security boundary.</span></span>

<span data-ttu-id="e0417-241">使用由操作系统提供的安全边界，如虚拟化、容器或用户帐户，以便使用最少的权限集来运行进程。</span><span class="sxs-lookup"><span data-stu-id="e0417-241">Use security boundaries that are provided by the operating system, such as virtualization, containers, or user accounts for running processes with the least set of privileges.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="e0417-242">[上一页](whats-new-dotnet.md )
>[下一页](windows-migration.md)</span><span class="sxs-lookup"><span data-stu-id="e0417-242">[Previous](whats-new-dotnet.md )
[Next](windows-migration.md)</span></span>
