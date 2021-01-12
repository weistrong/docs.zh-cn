---
title: NETSDK1005 和 NETSDK1047：资产文件缺少目标
description: 如何解决资产文件缺少目标的问题。
author: sfoslund
ms.topic: error-reference
ms.date: 12/17/2020
f1_keywords:
- NETSDK1005
- NETSDK1047
ms.openlocfilehash: e3e7389adf6a9a715d44661a5f7cbae5efe299e4
ms.sourcegitcommit: 4b79862c5b41fbd86cf38f926f6a49516059f6f2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/18/2020
ms.locfileid: "97678173"
---
# <a name="netsdk1005-and-netsdk1047-asset-file-is-missing-target"></a>NETSDK1005 和 NETSDK1047：资产文件缺少目标

本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本

当 .NET SDK 发出错误 NETSDK1005 或 NETSDK1047 时，项目的资产文件缺失某个目标框架的相关信息。 NuGet 在“obj”文件夹中写入名为 project.assets.json 的文件，.NET SDK 使用该文件来获取有关要传递到编译器的包的信息 。 在 .NET 5 中，NuGet 添加了名为 `TargetFrameworkAlias` 的新字段，以便早期版本的 MSBuild 或 NuGet 在没有新字段的情况下生成资产文件。 有关详细信息，请参阅[错误 NETSDK1005](https://developercommunity.visualstudio.com/content/problem/1248649/error-netsdk1005-assets-file-projectassetsjson-doe.html)。

可以采取下面的一些操作来解决错误：

* 确保使用的是 MSBuild 版本 16.8 或更高版本以及 NuGet 版本 5.8 或更高版本，并在更新工具后还原项目。 使用 NuGet 版本 5.8 或更高版本时，应使用 Visual Studio 2019 版本 16.8 或更高版本、MSBuild 版本 16.8 或更高版本以及 .NET 5.0 SDK 或更高版本。

* 如果在安装版本 16.8 或在更改项目的目标框架后首次在 Visual Studio 2019 中生成项目时出现错误，请再次生成项目。

* 在生成项目之前删除“obj”文件夹。

* 请确保项目的 `TargetFrameworks` 属性中包含缺少的目标值。
