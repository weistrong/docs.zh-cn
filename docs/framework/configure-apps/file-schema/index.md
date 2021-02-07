---
description: 了解详细信息： .NET Framework 的配置文件架构
title: .NET Framework 的配置文件架构
ms.date: 05/01/2017
helpviewer_keywords:
- .NET Framework application configuration, configuration schema
- machine configuration files
- application configuration files, schema
- app.config files, schema
- schema configuration settings
- schemas, configuration settings
- enterprisesec.config files
- well-formed XML
- enterprisesec configuration files
- security.config files
- security [.NET Framework], configuration files
- application development [.NET Framework], schema
- XML tags
- container tags
- machine.config files
- configuration schema [.NET Framework]
- configuration settings [.NET Framework], applications
- configuration file reference [.NET Framework]
ms.assetid: 69003d39-dc8a-460c-a6be-e6d93e690b38
ms.openlocfilehash: eac6d14f29f5ae0eeb65efe5a1416b8f40583be3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729948"
---
# <a name="configuration-file-schema-for-the-net-framework"></a><span data-ttu-id="1cc17-103">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="1cc17-103">Configuration file schema for the .NET Framework</span></span>

<span data-ttu-id="1cc17-104">配置文件是可用来更改应用设置并为其设置策略的标准 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="1cc17-104">Configuration files are standard XML files that you can use to change settings and set policies for your apps.</span></span> <span data-ttu-id="1cc17-105">.NET Framework 配置架构由一些可在配置文件中用来控制应用行为的元素组成。</span><span class="sxs-lookup"><span data-stu-id="1cc17-105">The .NET Framework configuration schema consists of elements that you can use in configuration files to control the behavior of your apps.</span></span> <span data-ttu-id="1cc17-106">本节的目录反映了架构的层次结构：启动、运行时、网络和其他配置设置类型。</span><span class="sxs-lookup"><span data-stu-id="1cc17-106">The table of contents for this section reflects the schema hierarchy for startup, runtime, network, and other types of configuration settings.</span></span>

<span data-ttu-id="1cc17-107">有关配置文件类型、格式和位置的信息，请参阅 [配置应用](../index.md)。</span><span class="sxs-lookup"><span data-stu-id="1cc17-107">For information about the types, format, and location of configuration files, see [Configure apps](../index.md).</span></span> <span data-ttu-id="1cc17-108">若要直接编辑配置文件，需要自行熟悉 XML。</span><span class="sxs-lookup"><span data-stu-id="1cc17-108">Familiarize yourself with XML if you want to edit the configuration files directly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cc17-109">配置文件中的 XML 标记和特性区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1cc17-109">XML tags and attributes in configuration files are case-sensitive.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1cc17-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="1cc17-110">In this section</span></span>

<span data-ttu-id="1cc17-111">[**\<configuration>** Element](configuration-element.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-111">[**\<configuration>** Element](configuration-element.md)</span></span>\
<span data-ttu-id="1cc17-112">所有配置文件的顶级元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-112">The top-level element for all configuration files.</span></span>

<span data-ttu-id="1cc17-113">[**\<assemblyBinding>** Element](assemblybinding-element-for-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-113">[**\<assemblyBinding>** Element](assemblybinding-element-for-configuration.md)</span></span>\
<span data-ttu-id="1cc17-114">指定配置级的程序集绑定策略。</span><span class="sxs-lookup"><span data-stu-id="1cc17-114">Specifies assembly binding policy at the configuration level.</span></span>

<span data-ttu-id="1cc17-115">[**\<linkedConfiguration>** Element](linkedconfiguration-element.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-115">[**\<linkedConfiguration>** Element](linkedconfiguration-element.md)</span></span>\
<span data-ttu-id="1cc17-116">指定要包含的配置文件。</span><span class="sxs-lookup"><span data-stu-id="1cc17-116">Specifies a configuration file to include.</span></span>

<span data-ttu-id="1cc17-117">[启动设置架构](./startup/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-117">[Startup Settings Schema](./startup/index.md)</span></span>\
<span data-ttu-id="1cc17-118">指定要使用的公共语言运行时版本的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-118">Elements that specify which version of the common language runtime to use.</span></span>

<span data-ttu-id="1cc17-119">[运行时设置架构](./runtime/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-119">[Runtime Settings Schema](./runtime/index.md)</span></span>\
<span data-ttu-id="1cc17-120">配置程序集绑定和运行时行为的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-120">Elements that configure assembly binding and runtime behavior.</span></span>

<span data-ttu-id="1cc17-121">[网络设置架构](./network/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-121">[Network Settings Schema](./network/index.md)</span></span>\
<span data-ttu-id="1cc17-122">指定 .NET Framework 如何连接到 internet 的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-122">Elements that specify how the .NET Framework connects to the internet.</span></span>

<span data-ttu-id="1cc17-123">[加密设置架构](./cryptography/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-123">[Cryptography Settings Schema](./cryptography/index.md)</span></span>\
<span data-ttu-id="1cc17-124">将友好算法名称映射到实现密码算法的类的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-124">Elements that map friendly algorithm names to classes that implement cryptography algorithms.</span></span>

<span data-ttu-id="1cc17-125">[配置节架构](configuration-sections-schema.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-125">[Configuration Sections Schema](configuration-sections-schema.md)</span></span>\
<span data-ttu-id="1cc17-126">用于创建和使用自定义设置的配置节的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-126">Elements used to create and use configuration sections for custom settings.</span></span>

<span data-ttu-id="1cc17-127">[跟踪和调试设置架构](./trace-debug/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-127">[Trace and Debug Settings Schema](./trace-debug/index.md)</span></span>\
<span data-ttu-id="1cc17-128">用于指定跟踪开关和侦听器的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-128">Elements that specify trace switches and listeners.</span></span>

<span data-ttu-id="1cc17-129">[编译器和语言提供程序设置架构](./compiler/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-129">[Compiler and Language Provider Settings Schema](./compiler/index.md)</span></span>\
<span data-ttu-id="1cc17-130">指定可用语言提供程序的编译器配置的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-130">Elements that specify compiler configuration for available language providers.</span></span>

<span data-ttu-id="1cc17-131">[应用程序设置架构](application-settings-schema.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-131">[Application Settings Schema](application-settings-schema.md)</span></span>\
<span data-ttu-id="1cc17-132">使 Windows 窗体或 ASP.NET 应用程序可以存储和检索应用程序范围的设置和用户范围的设置的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-132">Elements that enable a Windows Forms or ASP.NET application to store and retrieve application-scoped and user-scoped settings.</span></span>

<span data-ttu-id="1cc17-133">[应用设置架构](./appsettings/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-133">[App Settings Schema](./appsettings/index.md)</span></span>\
<span data-ttu-id="1cc17-134">包含自定义应用程序设置，如文件路径、XML Web service URL 或应用程序的任何其他自定义配置信息。</span><span class="sxs-lookup"><span data-stu-id="1cc17-134">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span>

<span data-ttu-id="1cc17-135">[Web 设置架构](./web/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-135">[Web Settings Schema](./web/index.md)</span></span>\
<span data-ttu-id="1cc17-136">用于配置 ASP.NET 如何与主机应用程序（如 IIS）一起工作的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-136">Elements for configuring how ASP.NET works with a host application such as IIS.</span></span> <span data-ttu-id="1cc17-137">在 Aspnet.config 文件中使用。</span><span class="sxs-lookup"><span data-stu-id="1cc17-137">Used in *Aspnet.config* files.</span></span>

<span data-ttu-id="1cc17-138">[Windows 窗体配置架构](winforms/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-138">[Windows Forms Configuration Schema](winforms/index.md)</span></span>\
<span data-ttu-id="1cc17-139">Windows 窗体应用程序配置部分中的所有元素，包括多监视器和高 DPI 支持等自定义。</span><span class="sxs-lookup"><span data-stu-id="1cc17-139">All elements in the Windows Forms application configuration section, which includes customizations such as multi-monitor and high-DPI support.</span></span>

<span data-ttu-id="1cc17-140">[WCF 配置架构](./wcf/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-140">[WCF Configuration Schema](./wcf/index.md)</span></span>\
<span data-ttu-id="1cc17-141">使你能够配置 WCF 服务和客户端应用程序的所有元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-141">All elements that enable you to configure WCF service and client applications.</span></span>

<span data-ttu-id="1cc17-142">[WCF 指令语法](./wcf-directive/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-142">[WCF Directive Syntax](./wcf-directive/index.md)</span></span>\
<span data-ttu-id="1cc17-143">介绍 `@ServiceHost` 指令，该指令定义 .svc 编译器使用的特定于页的属性。</span><span class="sxs-lookup"><span data-stu-id="1cc17-143">Describes the `@ServiceHost` directive, which defines page-specific attributes used by the .svc compiler.</span></span>

<span data-ttu-id="1cc17-144">[WIF 配置架构](windows-identity-foundation/index.md)</span><span class="sxs-lookup"><span data-stu-id="1cc17-144">[WIF Configuration Schema](windows-identity-foundation/index.md)</span></span>\
<span data-ttu-id="1cc17-145">Windows Identity Foundation (WIF) 配置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-145">All elements of the Windows Identity Foundation (WIF) configuration schema.</span></span>

## <a name="related-sections"></a><span data-ttu-id="1cc17-146">相关章节</span><span class="sxs-lookup"><span data-stu-id="1cc17-146">Related sections</span></span>

<span data-ttu-id="1cc17-147">[远程处理设置架构](/previous-versions/dotnet/netframework-4.0/z415cf9a(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1cc17-147">[Remoting Settings Schema](/previous-versions/dotnet/netframework-4.0/z415cf9a(v=vs.100))</span></span>\
<span data-ttu-id="1cc17-148">描述对实现远程处理的客户端和服务器应用程序进行配置的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-148">Describes the elements that configure client and server applications that implement remoting.</span></span>

<span data-ttu-id="1cc17-149">[ASP.NET 设置架构](/previous-versions/dotnet/netframework-4.0/b5ysx397(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1cc17-149">[ASP.NET Settings Schema](/previous-versions/dotnet/netframework-4.0/b5ysx397(v=vs.100))</span></span>\
<span data-ttu-id="1cc17-150">描述控制 ASP.NET Web 应用程序的行为的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-150">Describes the elements that control the behavior of ASP.NET Web applications.</span></span>

<span data-ttu-id="1cc17-151">[Web 服务设置架构](/previous-versions/dotnet/netframework-4.0/cctwteet(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1cc17-151">[Web Services Settings Schema](/previous-versions/dotnet/netframework-4.0/cctwteet(v=vs.100))</span></span>\
<span data-ttu-id="1cc17-152">描述控制 ASP.NET Web 服务以及它们的客户端的行为的元素。</span><span class="sxs-lookup"><span data-stu-id="1cc17-152">Describes the elements that control the behavior of ASP.NET Web services and their clients.</span></span>

<span data-ttu-id="1cc17-153">[配置 .NET Framework 应用](/previous-versions/dotnet/netframework-4.0/kza1yk3a(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1cc17-153">[Configuring .NET Framework Apps](/previous-versions/dotnet/netframework-4.0/kza1yk3a(v=vs.100))</span></span>\
<span data-ttu-id="1cc17-154">描述如何在 .NET Framework 中配置安全性、程序集绑定和远程处理。</span><span class="sxs-lookup"><span data-stu-id="1cc17-154">Describes how to configure security, assembly binding, and remoting in the .NET Framework.</span></span>
