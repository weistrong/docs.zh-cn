---
title: MSBuild 中断性变更
description: 列出 .NET Core 3.0-3.1 中的 MSBuild 中断性变更。
ms.date: 12/14/2020
ms.openlocfilehash: 1ed5878845406fa7727c644f1e196d63a860646a
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97593443"
---
# <a name="msbuild-breaking-changes-in-net-core-30---31"></a>.NET Core 3.0-3.1 中的 MSBuild 中断性变更

本页记录了以下中断性变更：

| 重大更改 | 引入的版本 |
| - | - |
| [设计时生成仅返回最上层包引用](#design-time-builds-only-return-top-level-package-references) | 3.1 |
| [资源清单文件名更改](#resource-manifest-file-name-change) | 3.0 |

## <a name="net-core-31"></a>.NET Core 3.1

[!INCLUDE [design-time-builds-return-top-level-package-refs](../../../includes/core-changes/msbuild/3.1/design-time-builds-return-top-level-package-refs.md)]

***

## <a name="net-core-30"></a>.NET Core 3.0

[!INCLUDE[Resource file names](~/includes/core-changes/msbuild/3.0/resource-manifest-name.md)]

***
