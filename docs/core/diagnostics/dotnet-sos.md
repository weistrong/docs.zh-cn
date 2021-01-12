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
# <a name="sos-installer-dotnet-sos"></a>SOS 安装程序 (dotnet-sos)

本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本

## <a name="install"></a>安装

可采用两种方法来下载和安装 `dotnet-sos`：

- **dotnet 全局工具：**

  若要安装最新版 `dotnet-sos` [NuGet 包](https://www.nuget.org/packages/dotnet-sos)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：

  ```dotnetcli
  dotnet tool install --global dotnet-sos
  ```

- **直接下载：**

  下载与平台相匹配的工具可执行文件：

  | (OS)  | 平台 |
  | --- | -------- |
  | Windows | [x86](https://aka.ms/dotnet-sos/win-x86) \| [x64](https://aka.ms/dotnet-sos/win-x64) \| [arm](https://aka.ms/dotnet-sos/win-arm) \| [arm-x64](https://aka.ms/dotnet-sos/win-arm64) |
  | macOS   | [x64](https://aka.ms/dotnet-sos/osx-x64) |
  | Linux   | [x64](https://aka.ms/dotnet-sos/linux-x64) \| [arm](https://aka.ms/dotnet-sos/linux-arm) \| [arm64](https://aka.ms/dotnet-sos/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-sos/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-sos/linux-musl-arm64) |

## <a name="synopsis"></a>摘要

```console
dotnet-sos [-h|--help] [options] [command]]
```

## <a name="description"></a>说明

`dotnet-sos` 全局工具将安装 [SOS 调试程序扩展](sos-debugging-extension.md)。 借助此扩展，你可以从本机调试器（如 lldb 和 windbg）检查托管 .NET Core 状态。

> [!NOTE]
> 只有 Linux 或 macOS 需要通过 `dotnet-sos` 工具安装 SOS。  如果使用的是旧版调试工具，则 Windows 也可能需要使用此工具。 [Windows 调试程序](/windows-hardware/drivers/debugger/debugger-download-tools)的最新版本（WinDbg 或 cdb 的版本 10.0.18317.1001 及更高版本）会从 Microsoft 扩展程序库自动加载 SOS。  

## <a name="options"></a>选项

- **`--version`**

  显示版本信息。

- **`-h|--help`**

  显示命令行帮助。

## <a name="dotnet-sos-install"></a>安装 dotnet-sos

在本地安装用于调试 .NET Core 进程的 [SOS 扩展](sos-debugging-extension.md)。 在 macOS 和 Linux 上，将更新 .lldbinit 文件，以便扩展在 lldb 启动时自动加载。 如果要使用较旧的调试工具（低于版本 10.0.18317.1001）在 Windows 上安装 SOS，则需要通过在调试程序中运行 `.load %USERPROFILE%\.dotnet\sos\sos.dll` 以在 WinDbg 或 cdb 中手动加载扩展。

### <a name="synopsis"></a>摘要

```console
dotnet-sos install [--architecture <arch>]
```

### <a name="options"></a>选项

- **`--architecture <arch>`**

  指定要安装的 SOS 二进制文件的处理器体系结构。 默认情况下，`dotnet-sos` 安装主机的体系结构。 当你要为与 dotnet 主机体系结构不同的体系结构安装 SOS 时，请使用此选项。 例如，如果要从 Arm64 主机运行 Arm32 二进制文件，则需要使用 `dotnet-sos install --architecture Arm` 安装 SOS。

  可以使用以下体系结构：

  - `Arm`
  - `Arm64`
  - `X86`
  - `X64`

## <a name="dotnet-sos-uninstall"></a>卸载 dotnet-sos

卸载 [SOS 扩展名](sos-debugging-extension.md)，并在 Linux 和 macOS 上将其从 lldb 配置中删除。

### <a name="synopsis"></a>摘要

```console
dotnet-sos uninstall
```
