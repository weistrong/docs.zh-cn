---
title: dotnet-sos 诊断工具 - .NET CLI
description: 了解如何安装和使用 dotnet-sos CLI 工具来管理 SOS 调试器扩展，该扩展可与 Windows 和 Linux 上的本机调试器一起使用。
ms.date: 11/17/2020
ms.openlocfilehash: 09e8228c47bdc632bccf3c9ad2296d55fe420060
ms.sourcegitcommit: c0b803bffaf101e12f071faf94ca21b46d04ff30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/24/2020
ms.locfileid: "97765002"
---
# <a name="sos-installer-dotnet-sos"></a><span data-ttu-id="77351-103">SOS 安装程序 (dotnet-sos)</span><span class="sxs-lookup"><span data-stu-id="77351-103">SOS installer (dotnet-sos)</span></span>

<span data-ttu-id="77351-104">本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="77351-104">**This article applies to:** ✔️ .NET Core 2.1 SDK and later versions</span></span>

## <a name="install"></a><span data-ttu-id="77351-105">安装</span><span class="sxs-lookup"><span data-stu-id="77351-105">Install</span></span>

<span data-ttu-id="77351-106">可采用两种方法来下载和安装 `dotnet-sos`：</span><span class="sxs-lookup"><span data-stu-id="77351-106">There are two ways to download and install `dotnet-sos`:</span></span>

- <span data-ttu-id="77351-107">**dotnet 全局工具：**</span><span class="sxs-lookup"><span data-stu-id="77351-107">**dotnet global tool:**</span></span>

  <span data-ttu-id="77351-108">若要安装最新版 `dotnet-sos` [NuGet 包](https://www.nuget.org/packages/dotnet-sos)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="77351-108">To install the latest release version of the `dotnet-sos` [NuGet package](https://www.nuget.org/packages/dotnet-sos), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

  ```dotnetcli
  dotnet tool install --global dotnet-sos
  ```

- <span data-ttu-id="77351-109">**直接下载：**</span><span class="sxs-lookup"><span data-stu-id="77351-109">**Direct download:**</span></span>

  <span data-ttu-id="77351-110">下载与平台相匹配的工具可执行文件：</span><span class="sxs-lookup"><span data-stu-id="77351-110">Download the tool executable that matches your platform:</span></span>

  | <span data-ttu-id="77351-111">(OS)</span><span class="sxs-lookup"><span data-stu-id="77351-111">OS</span></span>  | <span data-ttu-id="77351-112">平台</span><span class="sxs-lookup"><span data-stu-id="77351-112">Platform</span></span> |
  | --- | -------- |
  | <span data-ttu-id="77351-113">Windows</span><span class="sxs-lookup"><span data-stu-id="77351-113">Windows</span></span> | <span data-ttu-id="77351-114">[x86](https://aka.ms/dotnet-sos/win-x86) \| [x64](https://aka.ms/dotnet-sos/win-x64) \| [arm](https://aka.ms/dotnet-sos/win-arm) \| [arm-x64](https://aka.ms/dotnet-sos/win-arm64)</span><span class="sxs-lookup"><span data-stu-id="77351-114">[x86](https://aka.ms/dotnet-sos/win-x86) \| [x64](https://aka.ms/dotnet-sos/win-x64) \| [arm](https://aka.ms/dotnet-sos/win-arm) \| [arm-x64](https://aka.ms/dotnet-sos/win-arm64)</span></span> |
  | <span data-ttu-id="77351-115">macOS</span><span class="sxs-lookup"><span data-stu-id="77351-115">macOS</span></span>   | [<span data-ttu-id="77351-116">x64</span><span class="sxs-lookup"><span data-stu-id="77351-116">x64</span></span>](https://aka.ms/dotnet-sos/osx-x64) |
  | <span data-ttu-id="77351-117">Linux</span><span class="sxs-lookup"><span data-stu-id="77351-117">Linux</span></span>   | <span data-ttu-id="77351-118">[x64](https://aka.ms/dotnet-sos/linux-x64) \| [arm](https://aka.ms/dotnet-sos/linux-arm) \| [arm64](https://aka.ms/dotnet-sos/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-sos/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-sos/linux-musl-arm64)</span><span class="sxs-lookup"><span data-stu-id="77351-118">[x64](https://aka.ms/dotnet-sos/linux-x64) \| [arm](https://aka.ms/dotnet-sos/linux-arm) \| [arm64](https://aka.ms/dotnet-sos/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-sos/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-sos/linux-musl-arm64)</span></span> |

## <a name="synopsis"></a><span data-ttu-id="77351-119">摘要</span><span class="sxs-lookup"><span data-stu-id="77351-119">Synopsis</span></span>

```console
dotnet-sos [-h|--help] [options] [command]]
```

## <a name="description"></a><span data-ttu-id="77351-120">说明</span><span class="sxs-lookup"><span data-stu-id="77351-120">Description</span></span>

<span data-ttu-id="77351-121">`dotnet-sos` 全局工具将安装 [SOS 调试程序扩展](sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="77351-121">The `dotnet-sos` global tool installs the [SOS debugger extension](sos-debugging-extension.md).</span></span> <span data-ttu-id="77351-122">借助此扩展，你可以从本机调试器（如 lldb 和 windbg）检查托管 .NET Core 状态。</span><span class="sxs-lookup"><span data-stu-id="77351-122">This extension lets you inspect managed .NET Core state from native debuggers like lldb and windbg.</span></span>

> [!NOTE]
> <span data-ttu-id="77351-123">只有 Linux 或 macOS 需要通过 `dotnet-sos` 工具安装 SOS。</span><span class="sxs-lookup"><span data-stu-id="77351-123">Installing SOS via the `dotnet-sos` tool is only needed on Linux or macOS.</span></span>  <span data-ttu-id="77351-124">如果使用的是旧版调试工具，则 Windows 也可能需要使用此工具。</span><span class="sxs-lookup"><span data-stu-id="77351-124">It may also be needed on Windows if you're using older debugging tools.</span></span> <span data-ttu-id="77351-125">[Windows 调试程序](/windows-hardware/drivers/debugger/debugger-download-tools)的最新版本（WinDbg 或 cdb 的版本 10.0.18317.1001 及更高版本）会从 Microsoft 扩展程序库自动加载 SOS。</span><span class="sxs-lookup"><span data-stu-id="77351-125">Recent versions of the [Windows Debugger](/windows-hardware/drivers/debugger/debugger-download-tools) (>= version 10.0.18317.1001 of WinDbg or cdb) load SOS automatically from the Microsoft extension gallery.</span></span>  

## <a name="options"></a><span data-ttu-id="77351-126">选项</span><span class="sxs-lookup"><span data-stu-id="77351-126">Options</span></span>

- **`--version`**

  <span data-ttu-id="77351-127">显示版本信息。</span><span class="sxs-lookup"><span data-stu-id="77351-127">Displays version information.</span></span>

- **`-h|--help`**

  <span data-ttu-id="77351-128">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="77351-128">Shows command-line help.</span></span>

## <a name="dotnet-sos-install"></a><span data-ttu-id="77351-129">安装 dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="77351-129">dotnet-sos install</span></span>

<span data-ttu-id="77351-130">在本地安装用于调试 .NET Core 进程的 [SOS 扩展](sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="77351-130">Installs the [SOS extension](sos-debugging-extension.md) locally for debugging .NET Core processes.</span></span> <span data-ttu-id="77351-131">在 macOS 和 Linux 上，将更新 .lldbinit 文件，以便扩展在 lldb 启动时自动加载。</span><span class="sxs-lookup"><span data-stu-id="77351-131">On macOS and Linux, the *.lldbinit* file will be updated so that the extension automatically loads at lldb startup.</span></span> <span data-ttu-id="77351-132">如果要使用较旧的调试工具（低于版本 10.0.18317.1001）在 Windows 上安装 SOS，则需要通过在调试程序中运行 `.load %USERPROFILE%\.dotnet\sos\sos.dll` 以在 WinDbg 或 cdb 中手动加载扩展。</span><span class="sxs-lookup"><span data-stu-id="77351-132">If you're installing SOS on Windows with older debugging tools (prior to version 10.0.18317.1001), you will need to manually load the extension in WinDbg or cdb by running `.load %USERPROFILE%\.dotnet\sos\sos.dll` in the debugger.</span></span>

### <a name="synopsis"></a><span data-ttu-id="77351-133">摘要</span><span class="sxs-lookup"><span data-stu-id="77351-133">Synopsis</span></span>

```console
dotnet-sos install [--architecture <arch>]
```

### <a name="options"></a><span data-ttu-id="77351-134">选项</span><span class="sxs-lookup"><span data-stu-id="77351-134">Options</span></span>

- **`--architecture <arch>`**

  <span data-ttu-id="77351-135">指定要安装的 SOS 二进制文件的处理器体系结构。</span><span class="sxs-lookup"><span data-stu-id="77351-135">Specifies the processor architecture of the SOS binaries to install.</span></span> <span data-ttu-id="77351-136">默认情况下，`dotnet-sos` 安装主机的体系结构。</span><span class="sxs-lookup"><span data-stu-id="77351-136">By default, `dotnet-sos` installs the architecture of the host machine.</span></span> <span data-ttu-id="77351-137">当你要为与 dotnet 主机体系结构不同的体系结构安装 SOS 时，请使用此选项。</span><span class="sxs-lookup"><span data-stu-id="77351-137">Use this option when you want to install SOS for an architecture that's different from the dotnet host architecture.</span></span> <span data-ttu-id="77351-138">例如，如果要从 Arm64 主机运行 Arm32 二进制文件，则需要使用 `dotnet-sos install --architecture Arm` 安装 SOS。</span><span class="sxs-lookup"><span data-stu-id="77351-138">For example, if you're running Arm32 binaries from an Arm64 host, you will need to install SOS with `dotnet-sos install --architecture Arm`.</span></span>

  <span data-ttu-id="77351-139">可以使用以下体系结构：</span><span class="sxs-lookup"><span data-stu-id="77351-139">The following architectures are available:</span></span>

  - `Arm`
  - `Arm64`
  - `X86`
  - `X64`

## <a name="dotnet-sos-uninstall"></a><span data-ttu-id="77351-140">卸载 dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="77351-140">dotnet-sos uninstall</span></span>

<span data-ttu-id="77351-141">卸载 [SOS 扩展名](sos-debugging-extension.md)，并在 Linux 和 macOS 上将其从 lldb 配置中删除。</span><span class="sxs-lookup"><span data-stu-id="77351-141">Uninstalls the [SOS extension](sos-debugging-extension.md) and, on Linux and macOS, removes it from lldb configuration.</span></span>

### <a name="synopsis"></a><span data-ttu-id="77351-142">摘要</span><span class="sxs-lookup"><span data-stu-id="77351-142">Synopsis</span></span>

```console
dotnet-sos uninstall
```
