---
description: 了解详细信息：启动设置架构
title: 启动设置架构
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
ms.openlocfilehash: 268b8d8dc2598add61435dd6b07031aa06831737
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726086"
---
# <a name="startup-settings-schema"></a><span data-ttu-id="86691-103">启动设置架构</span><span class="sxs-lookup"><span data-stu-id="86691-103">Startup settings schema</span></span>

<span data-ttu-id="86691-104">启动设置会指定应运行应用程序的公共语言运行时的版本。</span><span class="sxs-lookup"><span data-stu-id="86691-104">Startup settings specify the version of the common language runtime that should run the application.</span></span>  
  
|<span data-ttu-id="86691-105">元素</span><span class="sxs-lookup"><span data-stu-id="86691-105">Element</span></span>|<span data-ttu-id="86691-106">说明</span><span class="sxs-lookup"><span data-stu-id="86691-106">Description</span></span>|  
|-------------|-----------------|  
|[\<requiredRuntime>](requiredruntime-element.md)|<span data-ttu-id="86691-107">指定应用程序仅支持 1.0 版本的公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="86691-107">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="86691-108">使用运行时版本1.1 生成的应用程序应使用 **\<supportedRuntime>** 元素。</span><span class="sxs-lookup"><span data-stu-id="86691-108">Applications built with runtime version 1.1 should use the **\<supportedRuntime>** element.</span></span>|  
|[\<supportedRuntime>](supportedruntime-element.md)|<span data-ttu-id="86691-109">指定应用程序支持的公共语言运行时版本。</span><span class="sxs-lookup"><span data-stu-id="86691-109">Specifies which versions of the common language runtime the application supports.</span></span>|  
|[\<startup>](startup-element.md)|<span data-ttu-id="86691-110">包含 **\<requiredRuntime>** 和 **\<supportedRuntime>** 元素。</span><span class="sxs-lookup"><span data-stu-id="86691-110">Contains the **\<requiredRuntime>** and **\<supportedRuntime>** elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="86691-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="86691-111">See also</span></span>

- [<span data-ttu-id="86691-112">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="86691-112">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="86691-113">如何：将应用配置为支持 .NET Framework 4 或更高版本</span><span class="sxs-lookup"><span data-stu-id="86691-113">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)
