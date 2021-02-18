---
title: 中断性变更：对于 WPF 和 WinForms 应用，OutputType 设置为 WinExe
description: 了解 .NET SDK 5.0.100 中的以下中断性变更：对于 Windows 窗体应用，OutputType 自动设置为 WinExe。
ms.date: 09/18/2020
ms.openlocfilehash: 38d9b910374f9e44f7e35296808930c6a6d45f0d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100431459"
---
# <a name="outputtype-set-to-winexe-for-wpf-and-winforms-apps"></a>对于 WPF 和 WinForms 应用，OutputType 设置为 WinExe

对于 Windows Presentation Foundation (WPF) 和 Windows 窗体应用，`OutputType` 自动设置为 `WinExe`。 如果 `OutputType` 设置为 `WinExe`，则在执行应用时不会打开控制台窗口。

## <a name="change-description"></a>更改说明

在早期版本的 .NET SDK 中，使用的是为项目文件中的 `OutputType` 指定的值。 例如：

```xml
<PropertyGroup>
  <OutputType>Exe</OutputType>
</PropertyGroup>
```

从 .NET SDK 的 5.0.100 版本开始，当 `OutputType` 设置为 `Exe` 时，对于面向任何框架版本（包括 .NET Framework）的 WPF 和 Windows Forms 应用，它将自动更改为 `WinExe`。

```xml
<PropertyGroup>
  <OutputType>WinExe</OutputType>
</PropertyGroup>
```

 如果未在项目文件中指定 `OutputType`，则它会默认为 `Library`，并且该值不会更改。

## <a name="reason-for-change"></a>更改原因

假定在执行 WPF 或 Windows 窗体应用时，大多数用户不希望打开控制台窗口。 此外，[这些应用程序类型现在使用 .NET SDK](sdk-and-target-framework-change.md) 而不是 Windows 桌面 SDK，因此会设置正确的默认值。 而且，添加了对面向 iOS 和 Android 的支持时，如果多个平台使用相同的输出类型，则在这些平台之间进行多目标操作将更轻松。

## <a name="version-introduced"></a>引入的版本

.NET 5.0.100

## <a name="recommended-action"></a>建议操作

你无需执行任何操作。 但是，如果你想还原为旧行为，请在项目文件中将 `DisableWinExeOutputInference` 属性设置为 `true`。

```xml
<DisableWinExeOutputInference>true</DisableWinExeOutputInference>
```

## <a name="affected-apis"></a>受影响的 API

无法通过 API 分析检测到。

<!--

### Affected APIs

Not detectable via API analysis.

### Category

- Windows Forms
- Windows Presentation Framework (WPF)

-->
