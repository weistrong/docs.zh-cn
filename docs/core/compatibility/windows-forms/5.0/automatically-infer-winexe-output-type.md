---
title: 中断性变更：对于 WPF 和 WinForms 应用，OutputType 设置为 WinExe
description: 了解 .NET SDK 5.0.100 中的以下中断性变更：对于 Windows 窗体应用，OutputType 自动设置为 WinExe。
ms.date: 09/18/2020
ms.openlocfilehash: 0b56db57d5242f2fb001c4de339a7f696c088dfc
ms.sourcegitcommit: 635a0ff775d2447a81ef7233a599b8f88b162e5d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "97633850"
---
# <a name="outputtype-set-to-winexe-for-wpf-and-winforms-apps"></a><span data-ttu-id="0612d-103">对于 WPF 和 WinForms 应用，OutputType 设置为 WinExe</span><span class="sxs-lookup"><span data-stu-id="0612d-103">OutputType set to WinExe for WPF and WinForms apps</span></span>

<span data-ttu-id="0612d-104">对于 Windows Presentation Foundation (WPF) 和 Windows 窗体应用，`OutputType` 自动设置为 `WinExe`。</span><span class="sxs-lookup"><span data-stu-id="0612d-104">`OutputType` is automatically set to `WinExe` for Windows Presentation Foundation (WPF) and Windows Forms apps.</span></span> <span data-ttu-id="0612d-105">如果 `OutputType` 设置为 `WinExe`，则在执行应用时不会打开控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="0612d-105">When `OutputType` is set to `WinExe`, a console window doesn't open when the app is executed.</span></span>

## <a name="change-description"></a><span data-ttu-id="0612d-106">更改说明</span><span class="sxs-lookup"><span data-stu-id="0612d-106">Change description</span></span>

<span data-ttu-id="0612d-107">在早期版本的 .NET SDK 中，使用的是为项目文件中的 `OutputType` 指定的值。</span><span class="sxs-lookup"><span data-stu-id="0612d-107">In previous versions of the .NET SDK, the value that's specified for `OutputType` in the project file is used.</span></span> <span data-ttu-id="0612d-108">例如：</span><span class="sxs-lookup"><span data-stu-id="0612d-108">For example:</span></span>

```xml
<PropertyGroup>
  <OutputType>Exe</OutputType>
</PropertyGroup>
```

<span data-ttu-id="0612d-109">从 .NET SDK 的 5.0.100 版本开始，对于面向任何框架版本（包括 .NET Framework）的 WPF 和 Windows Forms 应用，`OutputType` 会自动设置为 `WinExe`。</span><span class="sxs-lookup"><span data-stu-id="0612d-109">Starting in the 5.0.100 version of the .NET SDK, `OutputType` is automatically set to `WinExe` for WPF and Windows Forms apps that target any framework version, including .NET Framework.</span></span> <span data-ttu-id="0612d-110">例如：</span><span class="sxs-lookup"><span data-stu-id="0612d-110">For example:</span></span>

```xml
<PropertyGroup>
  <OutputType>WinExe</OutputType>
</PropertyGroup>
```

## <a name="reason-for-change"></a><span data-ttu-id="0612d-111">更改原因</span><span class="sxs-lookup"><span data-stu-id="0612d-111">Reason for change</span></span>

<span data-ttu-id="0612d-112">假定在执行 WPF 或 Windows 窗体应用时，大多数用户不希望打开控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="0612d-112">It's assumed that most users don't want a console window to open when a WPF or Windows Forms app is executed.</span></span> <span data-ttu-id="0612d-113">此外，[这些应用程序类型现在使用 .NET SDK](sdk-and-target-framework-change.md) 而不是 Windows 桌面 SDK，因此会设置正确的默认值。</span><span class="sxs-lookup"><span data-stu-id="0612d-113">In addition, [now that these application types use the .NET SDK](sdk-and-target-framework-change.md) instead of the Windows Desktop SDK, the correct default will be set.</span></span> <span data-ttu-id="0612d-114">而且，添加了对面向 iOS 和 Android 的支持时，如果多个平台使用相同的输出类型，则在这些平台之间进行多目标操作将更轻松。</span><span class="sxs-lookup"><span data-stu-id="0612d-114">Further, when support for targeting iOS and Android is added, it will be easier to multi-target between multiple platforms if they all use the same output type.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="0612d-115">引入的版本</span><span class="sxs-lookup"><span data-stu-id="0612d-115">Version introduced</span></span>

<span data-ttu-id="0612d-116">.NET 5.0.100</span><span class="sxs-lookup"><span data-stu-id="0612d-116">.NET 5.0.100</span></span>

## <a name="recommended-action"></a><span data-ttu-id="0612d-117">建议操作</span><span class="sxs-lookup"><span data-stu-id="0612d-117">Recommended action</span></span>

<span data-ttu-id="0612d-118">你无需执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="0612d-118">No action is required in your part.</span></span> <span data-ttu-id="0612d-119">但是，如果你想还原为旧行为，请在项目文件中将 `DisableWinExeOutputInference` 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="0612d-119">However, if you want to revert to the old behavior, set the `DisableWinExeOutputInference` property to `true` in your project file.</span></span>

```xml
<DisableWinExeOutputInference>true</DisableWinExeOutputInference>
```

## <a name="affected-apis"></a><span data-ttu-id="0612d-120">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="0612d-120">Affected APIs</span></span>

<span data-ttu-id="0612d-121">无法通过 API 分析检测到。</span><span class="sxs-lookup"><span data-stu-id="0612d-121">Not detectable via API analysis.</span></span>

<!--

### Affected APIs

Not detectable via API analysis.

### Category

- Windows Forms
- Windows Presentation Framework (WPF)

-->
