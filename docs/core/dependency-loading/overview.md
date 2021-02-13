---
title: 依赖项加载 - .NET Core
description: .NET Core 中的托管和非托管依赖项加载概述
ms.date: 08/09/2019
author: sdmaclea
ms.author: stmaclea
ms.topic: overview
ms.openlocfilehash: 2eaa01fad3913272dc90891592d0e35cd89ad2ab
ms.sourcegitcommit: f2ab02d9a780819ca2e5310bbcf5cfe5b7993041
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "99506313"
---
# <a name="dependency-loading-in-net-core"></a>.NET Core 中的依赖项加载

每个 .NET Core 应用程序都有依赖项。 即使是简单的 `hello world` 应用程序也在 .NET Core 类库的各个部分中有依赖项。

了解 .NET Core 默认程序集加载逻辑有助于理解和调试典型的部署问题。

在某些应用程序中，在运行时动态确定依赖项。 在这些情况下，了解托管程序集和非托管依赖项的加载方式至关重要。

## <a name="understanding-assemblyloadcontext"></a>了解 AssemblyLoadContext

<xref:System.Runtime.Loader.AssemblyLoadContext> API 是 .NET Core 加载设计的核心。 [了解 AssemblyLoadContext ](understanding-assemblyloadcontext.md) 一文提供了有关设计的概念性概述。

## <a name="loading-details"></a>加载详细信息

以下几篇文章简要介绍了加载算法的详细信息：

- [托管程序集加载算法](loading-managed.md)
- [附属程序集加载算法](loading-resources.md)
- [非托管（本机）库加载算法](loading-unmanaged.md)
- [默认探测](default-probing.md)

## <a name="create-a-net-core-application-with-plugins"></a>使用插件创建 .NET Core 应用程序

[创建包含插件的 .NET Core 应用程序](../tutorials/creating-app-with-plugin-support.md)教程介绍了如何创建自定义 AssemblyLoadContext。 它使用 <xref:System.Runtime.Loader.AssemblyDependencyResolver> 来解析插件的依赖项。 该教程正确地将插件依赖项与主机应用程序隔离开来。

## <a name="how-to-use-and-debug-assembly-unloadability-in-net-core"></a>如何在 .NET Core 中使用和调试程序集可卸载性

[如何在 .NET Core 中使用和调试程序集可卸载性](../../standard/assembly/unloadability.md)一文是逐步骤教程。 其中显示了如何加载 .NET Core 应用程序、执行以及将其卸载。 该文章还提供了调试提示。

## <a name="collect-detailed-assembly-loading-information"></a>收集详细的程序集加载信息

[收集详细的程序集加载信息](collect-details.md)一文介绍了如何收集运行时中托管程序集加载的详细信息。 它使用 [dotnet-trace](../diagnostics/dotnet-trace.md) 工具在正在运行的进程的跟踪中捕获程序集加载程序事件。
