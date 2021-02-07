---
description: 了解详细信息： Web 设置架构
title: Web 设置架构
ms.date: 03/30/2017
helpviewer_keywords:
- Web.config configuration file [ASP.NET]
- ASP.NET configuration system, Web settings schema
- schema Web settings
- Web settings, schema [ASP.NET]
- configuration files [ASP.NET]
- configuration schema [.NET Framework], Web settings
ms.assetid: ae1ac356-267d-4753-8d7a-7a04eb45a9be
ms.openlocfilehash: 262a53ae062788143cbacdc1012085186f4c9652
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681911"
---
# <a name="web-settings-schema"></a><span data-ttu-id="e7bde-103">Web 设置架构</span><span class="sxs-lookup"><span data-stu-id="e7bde-103">Web Settings Schema</span></span>

<span data-ttu-id="e7bde-104">Web 设置指定 CPU 和执行级别 ASP.NET 设置，后者应用于由 ASP.NET 承载层托管的进程范围行为。</span><span class="sxs-lookup"><span data-stu-id="e7bde-104">Web settings specify CPU and execution-level ASP.NET settings that apply to process-wide behavior managed by the ASP.NET hosting layer.</span></span> <span data-ttu-id="e7bde-105">这些设置与 ASP.NET 应用程序的 Web.config 文件中指定的应用程序域类型设置不同。</span><span class="sxs-lookup"><span data-stu-id="e7bde-105">These settings differ from application domain-type settings that are specified in the Web.config file of an ASP.NET application.</span></span>  
  
<span data-ttu-id="e7bde-106">Web 设置包含在 Aspnet.config 文件中，该文件位于各版本 .NET Framework 的安装文件夹内。</span><span class="sxs-lookup"><span data-stu-id="e7bde-106">Web settings are contained in Aspnet.config files, which are located in the installation folders for versions of the .NET Framework.</span></span> <span data-ttu-id="e7bde-107">例如，.NET Framework 2.0 的 Aspnet.config 文件位于以下文件夹中：</span><span class="sxs-lookup"><span data-stu-id="e7bde-107">For example, the Aspnet.config file for .NET Framework 2.0 is in the following folder:</span></span>  
  
`C:\Windows\Microsoft.NET\Framework\v2.0.50727\`  
  
<span data-ttu-id="e7bde-108">其他任何配置文件（如 machine.config 文件、根 Web.config 或应用程序级别的 Web.config 文件）中都不使用 Web 设置。</span><span class="sxs-lookup"><span data-stu-id="e7bde-108">Web settings are not used in any other configuration files such as the machine.config file, the root Web.config, or application-level Web.config files.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.web>**](system-web-element-web-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<applicationPool>**](applicationpool-element-web-settings.md)

|<span data-ttu-id="e7bde-109">元素</span><span class="sxs-lookup"><span data-stu-id="e7bde-109">Element</span></span>|<span data-ttu-id="e7bde-110">说明</span><span class="sxs-lookup"><span data-stu-id="e7bde-110">Description</span></span>|  
|-------------|-----------------|  
|[\<system.web>](system-web-element-web-settings.md)|<span data-ttu-id="e7bde-111">包含 ASP.NET 承载层使用的信息。</span><span class="sxs-lookup"><span data-stu-id="e7bde-111">Contains information that the ASP.NET hosting layer uses.</span></span>|  
|[\<applicationPool>](applicationpool-element-web-settings.md)|<span data-ttu-id="e7bde-112">指定 CPU 和执行级别 ASP.NET 设置，后者应用于由 ASP.NET 承载层托管的进程范围行为。</span><span class="sxs-lookup"><span data-stu-id="e7bde-112">Specifies CPU and execution-level ASP.NET settings that apply to process-wide behavior managed by the ASP.NET hosting layer.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e7bde-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7bde-113">See also</span></span>

- [<span data-ttu-id="e7bde-114">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="e7bde-114">Configuration File Schema</span></span>](../index.md)
