---
title: 在 Linux 上通过 Snap 安装 .NET - .NET
description: 演示如何通过 Snap 在 Linux 上安装 .NET SDK 或 .NET Runtime。
author: adegeo
ms.author: adegeo
ms.date: 01/06/2021
ms.openlocfilehash: 741933b5ca6f01d73b388675fe7f8a43c4efb0f9
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970922"
---
# <a name="install-the-net-sdk-or-the-net-runtime-with-snap"></a><span data-ttu-id="5e6e1-103">通过 Snap 安装 .NET SDK 或 .NET Runtime</span><span class="sxs-lookup"><span data-stu-id="5e6e1-103">Install the .NET SDK or the .NET Runtime with Snap</span></span>

<span data-ttu-id="5e6e1-104">使用 Snap 包安装 .NET SDK 或 .NET Runtime。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-104">Use a Snap package to install the .NET SDK or .NET Runtime.</span></span> <span data-ttu-id="5e6e1-105">对于内置于 Linux 发行版的包管理器而言，Snap 是一种很好的替代方法。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-105">Snaps are a great alternative to the package manager built into your Linux distribution.</span></span> <span data-ttu-id="5e6e1-106">本文介绍如何通过 [Snap](https://snapcraft.io/dotnet-sdk) 安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-106">This article describes how to install .NET through [Snap](https://snapcraft.io/dotnet-sdk).</span></span>

<span data-ttu-id="5e6e1-107">Snap 是应用及其依赖项的捆绑包，无需修改即可在多个不同的 Linux 发行版中正常运行。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-107">A snap is a bundle of an app and its dependencies that works without modification across many different Linux distributions.</span></span> <span data-ttu-id="5e6e1-108">可以从 Snap Store 中发现和安装 Snap。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-108">Snaps are discoverable and installable from the Snap Store.</span></span> <span data-ttu-id="5e6e1-109">若要详细了解 Snap，请参阅[开始使用 Snap](https://snapcraft.io/docs/getting-started)。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-109">For more information about Snap, see [Getting started with Snap](https://snapcraft.io/docs/getting-started).</span></span>

> [!CAUTION]
> <span data-ttu-id="5e6e1-110">Windows 10 上的 WSL2 不支持 Snap 包。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-110">Snap packages aren't supported in WSL2 on Windows 10.</span></span> <span data-ttu-id="5e6e1-111">作为替代方法，可使用 [`dotnet-install` 脚本](linux-scripted-manual.md#scripted-install)或特定 WSL2 发行版的包管理器。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-111">As an alternative, use the [`dotnet-install` script](linux-scripted-manual.md#scripted-install) or the package manager for the particular WSL2 distribution.</span></span> <span data-ttu-id="5e6e1-112">虽然可以尝试使用 [Snapcraft 论坛中的替代方法](https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033)启用 Snap，但该方法不受支持，因此不建议这样做。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-112">It's not recommended but you can try to enable snap with an [unsupported workaround from the snapcraft forums](https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033).</span></span>

## <a name="net-releases"></a><span data-ttu-id="5e6e1-113">.NET 版本</span><span class="sxs-lookup"><span data-stu-id="5e6e1-113">.NET releases</span></span>

<span data-ttu-id="5e6e1-114">只有 ✔️ 受支持的 .NET SDK 版本，才能通过 Snap 获取。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-114">Only ✔️ supported versions of .NET SDK are available through Snap.</span></span> <span data-ttu-id="5e6e1-115">从版本 2.1 开始，所有.NET Runtime 版本均可通过 Snap 获取。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-115">All versions of the .NET Runtime are available through snap starting with version 2.1.</span></span> <span data-ttu-id="5e6e1-116">下表列出了 .NET（和 .NET Core）版本：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-116">The following table lists the .NET (and .NET Core) releases:</span></span>

| <span data-ttu-id="5e6e1-117">✔️ 受支持</span><span class="sxs-lookup"><span data-stu-id="5e6e1-117">✔️ Supported</span></span> | <span data-ttu-id="5e6e1-118">❌ 不受支持</span><span class="sxs-lookup"><span data-stu-id="5e6e1-118">❌ Unsupported</span></span> |
|-------------|---------------|
| <span data-ttu-id="5e6e1-119">5.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-119">5.0</span></span>         | <span data-ttu-id="5e6e1-120">3.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-120">3.0</span></span>           |
| <span data-ttu-id="5e6e1-121">3.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-121">3.1 (LTS)</span></span>   | <span data-ttu-id="5e6e1-122">2.2</span><span class="sxs-lookup"><span data-stu-id="5e6e1-122">2.2</span></span>           |
| <span data-ttu-id="5e6e1-123">2.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-123">2.1 (LTS)</span></span>   | <span data-ttu-id="5e6e1-124">2.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-124">2.0</span></span>           |
|             | <span data-ttu-id="5e6e1-125">1.1</span><span class="sxs-lookup"><span data-stu-id="5e6e1-125">1.1</span></span>           |
|             | <span data-ttu-id="5e6e1-126">1.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-126">1.0</span></span>           |

<span data-ttu-id="5e6e1-127">有关 .NET 版本的生命周期的详细信息，请参阅 [.NET Core 和 .NET 5 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-127">For more information about the life cycle of .NET releases, see [.NET Core and .NET 5 Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core).</span></span>

## <a name="sdk-or-runtime"></a><span data-ttu-id="5e6e1-128">SDK 或 Runtime</span><span class="sxs-lookup"><span data-stu-id="5e6e1-128">SDK or Runtime</span></span>

[!INCLUDE [linux-intro-sdk-vs-runtime](includes/linux-intro-sdk-vs-runtime.md)]

## <a name="install-the-sdk"></a><span data-ttu-id="5e6e1-129">安装 SDK</span><span class="sxs-lookup"><span data-stu-id="5e6e1-129">Install the SDK</span></span>

<span data-ttu-id="5e6e1-130">适用于 .NET SDK 的 Snap 包都是在同一标识符（即 `dotnet-sdk`）下发布的。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-130">Snap packages for the .NET SDK are all published under the same identifier: `dotnet-sdk`.</span></span> <span data-ttu-id="5e6e1-131">可以通过指定通道来安装特定版本的 SDK。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-131">A specific version of the SDK can be installed by specifying the channel.</span></span> <span data-ttu-id="5e6e1-132">SDK 包括相应的运行时。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-132">The SDK includes the corresponding runtime.</span></span> <span data-ttu-id="5e6e1-133">下表列出了通道：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-133">The following table lists the channels:</span></span>

| <span data-ttu-id="5e6e1-134">.NET 版本</span><span class="sxs-lookup"><span data-stu-id="5e6e1-134">.NET version</span></span> | <span data-ttu-id="5e6e1-135">Snap 包或通道</span><span class="sxs-lookup"><span data-stu-id="5e6e1-135">Snap package or channel</span></span>  |
|--------------|--------------------------|
| <span data-ttu-id="5e6e1-136">5.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-136">5.0</span></span>          | <span data-ttu-id="5e6e1-137">`5.0` 或 `latest/stable`</span><span class="sxs-lookup"><span data-stu-id="5e6e1-137">`5.0` or `latest/stable`</span></span> |
| <span data-ttu-id="5e6e1-138">3.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-138">3.1 (LTS)</span></span>    | <span data-ttu-id="5e6e1-139">`3.1` 或 `lts/stable`</span><span class="sxs-lookup"><span data-stu-id="5e6e1-139">`3.1` or `lts/stable`</span></span>    |
| <span data-ttu-id="5e6e1-140">2.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-140">2.1 (LTS)</span></span>    | `2.1`                    |

<span data-ttu-id="5e6e1-141">若要安装适用于 .NET SDK 的 Snap 包，请运行 `snap install` 命令。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-141">Use the `snap install` command to install a .NET SDK snap package.</span></span> <span data-ttu-id="5e6e1-142">使用 `--channel` 参数来指明要安装哪个版本。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-142">Use the `--channel` parameter to indicate which version to install.</span></span> <span data-ttu-id="5e6e1-143">如果省略此参数，则使用 `latest/stable`。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-143">If this parameter is omitted, `latest/stable` is used.</span></span> <span data-ttu-id="5e6e1-144">在下面的示例中，指定的是 `5.0`：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-144">In this example, `5.0` is specified:</span></span>

```bash
sudo snap install dotnet-sdk --classic --channel=5.0
```

<span data-ttu-id="5e6e1-145">接下来，使用 `snap alias` 命令为系统注册 `dotnet` 命令：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-145">Next, register the `dotnet` command for the system with the `snap alias` command:</span></span>

```bash
sudo snap alias dotnet-sdk.dotnet dotnet
```

<span data-ttu-id="5e6e1-146">此命令的格式为 `sudo snap alias {package}.{command} {alias}`。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-146">This command is formatted as: `sudo snap alias {package}.{command} {alias}`.</span></span> <span data-ttu-id="5e6e1-147">可以选择所需的任何 `{alias}` 名称。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-147">You can choose any `{alias}` name you would like.</span></span> <span data-ttu-id="5e6e1-148">例如，可以根据 Snap 安装的特定版本来命名此命令：`sudo snap alias dotnet-sdk.dotnet dotnet50`。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-148">For example, you could name the command after the specific version installed by snap: `sudo snap alias dotnet-sdk.dotnet dotnet50`.</span></span> <span data-ttu-id="5e6e1-149">运行命令 `dotnet50` 时，将调用这一特定版本的 .NET。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-149">When you use the command `dotnet50`, you'll invoke this specific version of .NET.</span></span> <span data-ttu-id="5e6e1-150">但选择其他别名与大多数教程和示例不兼容，因为它们需要使用 `dotnet` 命令。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-150">But choosing a different alias is incompatible with most tutorials and examples as they expect a `dotnet` command to be used.</span></span>

## <a name="install-the-runtime"></a><span data-ttu-id="5e6e1-151">安装运行时</span><span class="sxs-lookup"><span data-stu-id="5e6e1-151">Install the runtime</span></span>

<span data-ttu-id="5e6e1-152">适用于 .NET Runtime 的 Snap 包都是在各自的包标识符下发布的。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-152">Snap packages for the .NET Runtime are each published under their own package identifier.</span></span> <span data-ttu-id="5e6e1-153">下表列出了这些包标识符：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-153">The following table lists the package identifiers:</span></span>

| <span data-ttu-id="5e6e1-154">.NET 版本</span><span class="sxs-lookup"><span data-stu-id="5e6e1-154">.NET version</span></span>      | <span data-ttu-id="5e6e1-155">Snap 包</span><span class="sxs-lookup"><span data-stu-id="5e6e1-155">Snap package</span></span>        |
|-------------------|---------------------|
| <span data-ttu-id="5e6e1-156">5.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-156">5.0</span></span>               | `dotnet-runtime-50` |
| <span data-ttu-id="5e6e1-157">3.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-157">3.1 (LTS)</span></span>         | `dotnet-runtime-31` |
| <span data-ttu-id="5e6e1-158">3.0</span><span class="sxs-lookup"><span data-stu-id="5e6e1-158">3.0</span></span>               | `dotnet-runtime-30` |
| <span data-ttu-id="5e6e1-159">2.2</span><span class="sxs-lookup"><span data-stu-id="5e6e1-159">2.2</span></span>               | `dotnet-runtime-22` |
| <span data-ttu-id="5e6e1-160">2.1 (LTS)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-160">2.1 (LTS)</span></span>         | `dotnet-runtime-21` |

<span data-ttu-id="5e6e1-161">若要安装适用于 .NET Runtime 的 Snap 包，请运行 `snap install` 命令。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-161">Use the `snap install` command to install a .NET Runtime snap package.</span></span> <span data-ttu-id="5e6e1-162">在下面的示例中，安装的是 .NET 5.0：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-162">In this example, .NET 5.0 is installed:</span></span>

```bash
sudo snap install dotnet-runtime-50 --classic
```

<span data-ttu-id="5e6e1-163">接下来，使用 `snap alias` 命令为系统注册 `dotnet` 命令：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-163">Next, register the `dotnet` command for the system with the `snap alias` command:</span></span>

```bash
sudo snap alias dotnet-runtime-50.dotnet dotnet
```

<span data-ttu-id="5e6e1-164">此命令的格式为 `sudo snap alias {package}.{command} {alias}`。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-164">The command is formatted as: `sudo snap alias {package}.{command} {alias}`.</span></span> <span data-ttu-id="5e6e1-165">可以选择所需的任何 `{alias}` 名称。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-165">You can choose any `{alias}` name you would like.</span></span> <span data-ttu-id="5e6e1-166">例如，可以根据 Snap 安装的特定版本来命名此命令：`sudo snap alias dotnet-runtime-50.dotnet dotnet50`。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-166">For example, you could name the command after the specific version installed by snap: `sudo snap alias dotnet-runtime-50.dotnet dotnet50`.</span></span> <span data-ttu-id="5e6e1-167">运行命令 `dotnet50` 时，将调用特定版本的 .NET。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-167">When you use the command `dotnet50`, you'll invoke a specific version of .NET.</span></span> <span data-ttu-id="5e6e1-168">但选择其他别名与大多数教程和示例不兼容，因为它们需要使用 `dotnet` 命令。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-168">But choosing a different alias is incompatible with most tutorials and examples as they expect a `dotnet` command to be available.</span></span>

## <a name="tlsssl-certificate-errors"></a><span data-ttu-id="5e6e1-169">TLS/SSL 证书错误</span><span class="sxs-lookup"><span data-stu-id="5e6e1-169">TLS/SSL Certificate errors</span></span>

<span data-ttu-id="5e6e1-170">通过 Snap 安装 .NET 后，可能会在某些发行版上找不到 .NET TLS/SSL 证书，并且可能会在 `restore` 期间看到以下错误：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-170">When .NET is installed through Snap, it's possible that on some distros the .NET TLS/SSL certificates may not be found and you may receive an error during `restore`:</span></span>

```bash
Processing post-creation actions...
Running 'dotnet restore' on /home/myhome/test/test.csproj...
  Restoring packages for /home/myhome/test/test.csproj...
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error : Unable to load the service index for source https://api.nuget.org/v3/index.json. [/home/myhome/test/test.csproj]
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error :   The SSL connection could not be established, see inner exception. [/home/myhome/test/test.csproj]
/snap/dotnet-sdk/27/sdk/2.2.103/NuGet.targets(114,5): error :   The remote certificate is invalid according to the validation procedure. [/home/myhome/test/test.csproj]
```

<span data-ttu-id="5e6e1-171">若要解决此问题，请设置一些环境变量：</span><span class="sxs-lookup"><span data-stu-id="5e6e1-171">To resolve this problem, set a few environment variables:</span></span>

```bash
export SSL_CERT_FILE=[path-to-certificate-file]
export SSL_CERT_DIR=/dev/null
```

<span data-ttu-id="5e6e1-172">证书位置因发行版而异。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-172">The certificate location will vary by distro.</span></span> <span data-ttu-id="5e6e1-173">下面是我们在发行版中遇到此问题的位置。</span><span class="sxs-lookup"><span data-stu-id="5e6e1-173">Here are the locations for the distros where the issue has been experienced.</span></span>

| <span data-ttu-id="5e6e1-174">分发</span><span class="sxs-lookup"><span data-stu-id="5e6e1-174">Distribution</span></span> | <span data-ttu-id="5e6e1-175">位置</span><span class="sxs-lookup"><span data-stu-id="5e6e1-175">Location</span></span>                                            |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="5e6e1-176">**Fedora**</span><span class="sxs-lookup"><span data-stu-id="5e6e1-176">**Fedora**</span></span>   | `/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem` |
| <span data-ttu-id="5e6e1-177">**OpenSUSE**</span><span class="sxs-lookup"><span data-stu-id="5e6e1-177">**OpenSUSE**</span></span> | `/etc/ssl/ca-bundle.pem`                            |
| <span data-ttu-id="5e6e1-178">**Solus**</span><span class="sxs-lookup"><span data-stu-id="5e6e1-178">**Solus**</span></span>    | `/etc/ssl/certs/ca-certificates.crt`                |

## <a name="next-steps"></a><span data-ttu-id="5e6e1-179">后续步骤</span><span class="sxs-lookup"><span data-stu-id="5e6e1-179">Next steps</span></span>

- [<span data-ttu-id="5e6e1-180">如何为 .NET CLI 启用 Tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="5e6e1-180">How to enable TAB completion for the .NET CLI</span></span>](../tools/enable-tab-autocomplete.md)
- [<span data-ttu-id="5e6e1-181">教程：使用 Visual Studio Code 通过 .NET SDK 创建控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="5e6e1-181">Tutorial: Create a console application with .NET SDK using Visual Studio Code</span></span>](../tutorials/with-visual-studio-code.md)
