---
title: NETSDK1064：找不到包
description: 了解在找不到包时出现的 .NET SDK 错误 NETSDK1064。
ms.topic: error-reference
ms.date: 02/10/2021
f1_keywords:
- NETSDK1064
ms.openlocfilehash: 1a155db1aacbceb9878401dbcac61ece5f1f9824
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488190"
---
# <a name="netsdk1064-package-not-found"></a>NETSDK1064：找不到包

本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本

当生成工具找不到生成项目所需的 NuGet 包时，会发生此错误。 这通常是由于包还原问题导致的。 完整的错误消息类似于以下示例：

> NETSDK1064：找不到版本 x.x.x 的包“PackageName”。 自 NuGet 还原以来，它可能已被删除。 否则，NuGet 还原可能仅部分完成（可能由于最大路径长度限制所致）。

可以执行以下操作来解决此错误：

* 将 `/restore` 选项添加到 MSBuild.exe 命令。 不要使用 `/t:Restore;Build`，因为这可能会导致难以察觉的 bug。 一种替代方法是使用 `dotnet build` 命令，因为它会自动执行包还原。
* 如果使用 Visual Studio 2019 或 MSBuild.exe 运行包还原，则该错误可能是由最大路径长度限制所导致的。 有关详细信息，请参阅[长路径支持 (NuGet CLI)](/nuget/reference/cli-reference/cli-ref-long-path) 和 [NuGet/Home 问题 #3324](https://github.com/NuGet/Home/issues/3324)。
* 如果使用 x86 nuget.exe 进行还原，并使用 x64 MSBuild.exe 进行生成，则不匹配的位数可能会导致此错误。 该生成找不到还原过程声明它所获得的包，因为 project.assets.json 中的路径在不同位数的进程中无法起作用。 若要解决此错误，请使用相同位数的工具进行还原和生成，或将 NuGet 配置为将包还原到未在 x86 和 x64 之间进行虚拟化的文件夹。 有关详细信息，请参阅 [dotnet/core 问题 #4332](https://github.com/dotnet/core/issues/4332)。
* 如果要生成 Docker 映像，请确保 .dockerginore 文件忽略 bin 和 obj 目录。 有关详细信息，请参阅 [NETSDK1064：找不到包 DnsClient 1.2.0](https://stackoverflow.com/questions/61167032/error-netsdk1064-package-dnsclient-1-2-0-was-not-found)。
