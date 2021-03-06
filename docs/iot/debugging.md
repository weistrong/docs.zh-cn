---
title: 在 Raspberry Pi 上调试 .NET 应用
description: 了解如何在 Raspberry Pi 和类似设备上调试 .NET 应用。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: how-to
ms.prod: dotnet
zone_pivot_groups: ide-set-one
ms.openlocfilehash: 58858384c49a296e0b33d663f3ef930caf9cace6
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102258060"
---
# <a name="debug-net-apps-on-raspberry-pi"></a><span data-ttu-id="a9f08-103">在 Raspberry Pi 上调试 .NET 应用</span><span class="sxs-lookup"><span data-stu-id="a9f08-103">Debug .NET apps on Raspberry Pi</span></span>

<span data-ttu-id="a9f08-104">调试在基于 ARM 的 IoT 设备上运行的 .NET 应用（如 Raspberry Pi）带来了独特的挑战。</span><span class="sxs-lookup"><span data-stu-id="a9f08-104">Debugging .NET apps running on ARM-based IoT devices like Raspberry Pi presents a unique challenge.</span></span> <span data-ttu-id="a9f08-105">可以在 ARM 设备上开发 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="a9f08-105">It is possible to develop .NET apps on ARM devices.</span></span> <span data-ttu-id="a9f08-106">但是，在 Visual Studio 外调试 .NET 应用程序所需的 OmniSharp 与 ARM 设备不兼容。</span><span class="sxs-lookup"><span data-stu-id="a9f08-106">However, OmniSharp, which is required for debugging .NET apps outside of Visual Studio, is not compatible with ARM devices.</span></span> <span data-ttu-id="a9f08-107">因此，必须从兼容的平台远程调试应用程序。</span><span class="sxs-lookup"><span data-stu-id="a9f08-107">As a result, apps must be debugged remotely from a compatible platform.</span></span>

::: zone pivot="vscode"

## <a name="debug-from-visual-studio-code-cross-platform"></a><span data-ttu-id="a9f08-108">从 Visual Studio Code (跨平台) 调试</span><span class="sxs-lookup"><span data-stu-id="a9f08-108">Debug from Visual Studio Code (cross-platform)</span></span>

<span data-ttu-id="a9f08-109">若要从 Visual Studio Code 调试 Raspberry Pi 上的 .NET，则需要在 Raspberry Pi 上以及项目的 *launch.js文件上* 执行配置步骤。</span><span class="sxs-lookup"><span data-stu-id="a9f08-109">Debugging .NET on Raspberry Pi from Visual Studio Code requires configuration steps on the Raspberry Pi and in the project's *launch.json* file.</span></span>

### <a name="enable-ssh-on-the-raspberry-pi"></a><span data-ttu-id="a9f08-110">在 Raspberry Pi 上启用 SSH</span><span class="sxs-lookup"><span data-stu-id="a9f08-110">Enable SSH on the Raspberry Pi</span></span>

<span data-ttu-id="a9f08-111">远程调试需要 SSH。</span><span class="sxs-lookup"><span data-stu-id="a9f08-111">SSH is required for remote debugging.</span></span> <span data-ttu-id="a9f08-112">若要启用 SSH，请 [参阅 Raspberry Pi 文档中的 *enable ssh*](https://www.raspberrypi.org/documentation/remote-access/ssh/)。</span><span class="sxs-lookup"><span data-stu-id="a9f08-112">To enable SSH, [refer to *Enable SSH* in the Raspberry Pi documentation](https://www.raspberrypi.org/documentation/remote-access/ssh/).</span></span>

### <a name="install-the-visual-studio-remote-debugger-on-the-raspberry-pi"></a><span data-ttu-id="a9f08-113">在 Raspberry Pi 上安装 Visual Studio 远程调试器</span><span class="sxs-lookup"><span data-stu-id="a9f08-113">Install the Visual Studio Remote Debugger on the Raspberry Pi</span></span>

<span data-ttu-id="a9f08-114">在 Raspberry Pi 上的 Bash 控制台 (本地或通过 SSH) ，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a9f08-114">Within a Bash console on the Raspberry Pi (either locally or via SSH), complete the following steps:</span></span>

1. <span data-ttu-id="a9f08-115">执行以下命令以下载并安装 Raspberry Pi 上的 Visual Studio 远程调试器：</span><span class="sxs-lookup"><span data-stu-id="a9f08-115">Execute the following command to download and install the Visual Studio Remote Debugger on the Raspberry Pi:</span></span>

    ```bash
    curl -sSL https://aka.ms/getvsdbgsh | /bin/sh /dev/stdin -v latest -l ~/vsdbg
    ```

1. <span data-ttu-id="a9f08-116">调试器需要作为运行 `root` 。</span><span class="sxs-lookup"><span data-stu-id="a9f08-116">The debugger requires running as `root`.</span></span> <span data-ttu-id="a9f08-117">默认情况下， `root` 在 Raspberry Pi 上没有密码。</span><span class="sxs-lookup"><span data-stu-id="a9f08-117">By default, `root` has no password on Raspberry Pi.</span></span> <span data-ttu-id="a9f08-118">`root`通过执行以下命令并按照提示设置密码。</span><span class="sxs-lookup"><span data-stu-id="a9f08-118">Set a password for `root` by executing the following command and following the prompts.</span></span>

    ```bash
    sudo passwd root
    ```

1. <span data-ttu-id="a9f08-119">Visual Studio Code 使用 SSH 协议进行远程调试。</span><span class="sxs-lookup"><span data-stu-id="a9f08-119">Visual Studio Code uses the SSH protocol to debug remotely.</span></span> <span data-ttu-id="a9f08-120">出于安全考虑， `root` 默认情况下不允许通过 SSH 登录。</span><span class="sxs-lookup"><span data-stu-id="a9f08-120">For security purposes, `root` is not permitted to log on via SSH by default.</span></span> <span data-ttu-id="a9f08-121">若要启用 `root` 通过 SSH 登录，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a9f08-121">To enable `root` to log on via SSH, complete the following steps:</span></span>

    1. <span data-ttu-id="a9f08-122">执行以下命令以在 [nano](https://www.nano-editor.org/docs.php)中打开 */etc/ssh/sshd_config* 。</span><span class="sxs-lookup"><span data-stu-id="a9f08-122">Execute the following command to open */etc/ssh/sshd_config* in [nano](https://www.nano-editor.org/docs.php).</span></span>

        ```bash
        sudo nano /etc/ssh/sshd_config
        ```

    1. <span data-ttu-id="a9f08-123">按 <kbd>Ctrl + W</kbd> 并搜索 **PermitRootLogin**。</span><span class="sxs-lookup"><span data-stu-id="a9f08-123">Press <kbd>Ctrl+W</kbd> and search for **PermitRootLogin**.</span></span>
    1. <span data-ttu-id="a9f08-124">如果需要，则取消注释行的 **PermitRootLogin** 。</span><span class="sxs-lookup"><span data-stu-id="a9f08-124">Uncomment the line with **PermitRootLogin** if needed.</span></span>
    1. <span data-ttu-id="a9f08-125">按如下所示将行更改为：</span><span class="sxs-lookup"><span data-stu-id="a9f08-125">Change the line to read as follows:</span></span>

        ```console
        PermitRootLogin yes
        ```

        > [!NOTE]
        > <span data-ttu-id="a9f08-126">如果 */etc/ssh/sshd_config* 中没有 **PermitRootLogin** 行，请使用上面所示的值添加新行。</span><span class="sxs-lookup"><span data-stu-id="a9f08-126">If there is no **PermitRootLogin** line in */etc/ssh/sshd_config*, add a new line with the value shown above.</span></span>

    1. <span data-ttu-id="a9f08-127">按 <kbd>Ctrl + X</kbd> 退出并节省机会。</span><span class="sxs-lookup"><span data-stu-id="a9f08-127">Press <kbd>Ctrl+X</kbd> to exit and save your chances.</span></span> <span data-ttu-id="a9f08-128">当系统提示 **"保存已修改的缓冲区？**" 时，按 <kbd>Y</kbd> 确认。</span><span class="sxs-lookup"><span data-stu-id="a9f08-128">When prompted **Save modified buffer?**, press <kbd>Y</kbd> to confirm.</span></span> <span data-ttu-id="a9f08-129">按 <kbd>enter</kbd> 确认覆盖原始文件。</span><span class="sxs-lookup"><span data-stu-id="a9f08-129">Press <kbd>Enter</kbd> to confirm overwriting the original file.</span></span>
    1. <span data-ttu-id="a9f08-130">通过执行以下命令重新启动 Raspberry Pi：</span><span class="sxs-lookup"><span data-stu-id="a9f08-130">Reboot the Raspberry Pi by executing the following command:</span></span>

        ```bash
        sudo reboot
        ```

### <a name="setup-launchjson-in-visual-studio-code"></a><span data-ttu-id="a9f08-131">在 Visual Studio Code 中设置 launch.js</span><span class="sxs-lookup"><span data-stu-id="a9f08-131">Setup launch.json in Visual Studio Code</span></span>

<span data-ttu-id="a9f08-132">将启动配置添加到项目的 *launch.js*。</span><span class="sxs-lookup"><span data-stu-id="a9f08-132">Add a launch configuration to the project's *launch.json*.</span></span> <span data-ttu-id="a9f08-133">如果项目没有 *launch.js的* 文件，请通过以下方式添加一个：切换到 " **运行** " 选项卡，选择 " **在文件上创建 launch.js**"，然后在对话框中选择 " **.net** " 或 " **.net Core** "。</span><span class="sxs-lookup"><span data-stu-id="a9f08-133">If the project doesn't have a *launch.json* file, add one by switching to the **Run** tab, selecting **create a launch.json file**, and selecting **.NET** or **.NET Core** in the dialog.</span></span>

<span data-ttu-id="a9f08-134">*launch.js上* 的新配置应如下所示：</span><span class="sxs-lookup"><span data-stu-id="a9f08-134">The new configuration in *launch.json* should look similar to this:</span></span>

```json
"configurations": [
    {
        "name": ".NET Core Launch (remote console)",
        "type": "coreclr",
        "request": "launch",
        "preLaunchTask": "build",
        "program": "/home/pi/.dotnet/dotnet",
        "args": ["/home/pi/sample/Sample.dll"],
        "cwd": "/home/pi/sample",
        "stopAtEntry": false,
        "console": "internalConsole",
        "pipeTransport": {
            "pipeCwd": "${workspaceFolder}",
            "pipeProgram": "C:\\Program Files\\PuTTY\\PLINK.EXE",
            "pipeArgs": [
                "-pw",
                "P@ssw0rd",
                "root@raspberrypi"
            ],
            "debuggerPath": "/home/pi/vsdbg/vsdbg"
        }
    },
```

<span data-ttu-id="a9f08-135">请注意以下内容：</span><span class="sxs-lookup"><span data-stu-id="a9f08-135">Notice the following:</span></span>

- <span data-ttu-id="a9f08-136">`program` 是指向 Pi 上的 .NET 运行时的路径。</span><span class="sxs-lookup"><span data-stu-id="a9f08-136">`program` is the path to the .NET runtime on the Pi.</span></span>
- <span data-ttu-id="a9f08-137">`args` 是要在 Pi 上调试的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="a9f08-137">`args` is the path to the assembly to debug on the Pi.</span></span>
- <span data-ttu-id="a9f08-138">`cwd` 在 Pi 上启动应用时使用的工作目录。</span><span class="sxs-lookup"><span data-stu-id="a9f08-138">`cwd` is the working directory to use when launching the app on the Pi.</span></span>
- <span data-ttu-id="a9f08-139">`pipeProgram` 是指向本地计算机上的 SSH 客户端的路径。</span><span class="sxs-lookup"><span data-stu-id="a9f08-139">`pipeProgram` is the path to an SSH client on the local machine.</span></span>
- <span data-ttu-id="a9f08-140">`pipeArgs` 要传递到 SSH 客户端的参数。</span><span class="sxs-lookup"><span data-stu-id="a9f08-140">`pipeArgs` are the parameters to be passed to the SSH client.</span></span> <span data-ttu-id="a9f08-141">请确保指定 password 参数，以及 `root` 该格式的用户 `<user>@<hostname>` 。</span><span class="sxs-lookup"><span data-stu-id="a9f08-141">Be sure to specify the password parameter, as well as the `root` user in the format `<user>@<hostname>`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9f08-142">上面的示例使用 *plink*，它是 [PuTTY](https://www.ssh.com/ssh/putty/) <span class="docon docon-navigate-external x-hidden-focus"></span> SSH 客户端的一个组件。</span><span class="sxs-lookup"><span data-stu-id="a9f08-142">The above example uses *plink*, a component of the [PuTTY](https://www.ssh.com/ssh/putty/)<span class="docon docon-navigate-external x-hidden-focus"></span> SSH client.</span></span> <span data-ttu-id="a9f08-143">[](https://www.openssh.com/)适用 <span class="docon docon-navigate-external x-hidden-focus"></span> 于最新版本的 Windows 和 Linux 的 OpenSSH 可以改为使用。</span><span class="sxs-lookup"><span data-stu-id="a9f08-143">[OpenSSH](https://www.openssh.com/)<span class="docon docon-navigate-external x-hidden-focus"></span>, which is included in recent versions of Windows and Linux, may be used instead.</span></span> <span data-ttu-id="a9f08-144">但是，OpenSSH 不支持以命令行参数的形式发送密码。</span><span class="sxs-lookup"><span data-stu-id="a9f08-144">However, OpenSSH doesn't support sending passwords as a command-line parameter.</span></span> <span data-ttu-id="a9f08-145">若要使用 OpenSSH，请 [为无密码 SSH 访问配置 Raspberry Pi](https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f08-145">To use OpenSSH, [configure your Raspberry Pi for passwordless SSH access](https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md).</span></span>

### <a name="deploy-the-app"></a><span data-ttu-id="a9f08-146">部署应用</span><span class="sxs-lookup"><span data-stu-id="a9f08-146">Deploy the app</span></span>

<span data-ttu-id="a9f08-147">部署应用，如 [将 .net 应用部署到 Raspberry Pi](deployment.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="a9f08-147">Deploy the app as described in [Deploy .NET apps to Raspberry Pi](deployment.md).</span></span> <span data-ttu-id="a9f08-148">确保部署路径与在配置的launch.js中的参数中指定的路径相同 `cwd` 。 </span><span class="sxs-lookup"><span data-stu-id="a9f08-148">Ensure the deployment path is the same path specified in the `cwd` parameter in the *launch.json* configuration.</span></span>

### <a name="launch-the-debugger"></a><span data-ttu-id="a9f08-149">启动调试程序</span><span class="sxs-lookup"><span data-stu-id="a9f08-149">Launch the debugger</span></span>

<span data-ttu-id="a9f08-150">在 " **运行** " 选项卡上，选择 " **.net Core 启动 (远程控制台)** 配置"，然后选择 " **启动调试**"。</span><span class="sxs-lookup"><span data-stu-id="a9f08-150">On the **Run** tab, select the **.NET Core Launch (remote console)** configuration and select **Start Debugging**.</span></span> <span data-ttu-id="a9f08-151">此应用在 Raspberry Pi 上启动。</span><span class="sxs-lookup"><span data-stu-id="a9f08-151">The app launches on the Raspberry Pi.</span></span> <span data-ttu-id="a9f08-152">调试器可用于设置断点、检查局部变量等。</span><span class="sxs-lookup"><span data-stu-id="a9f08-152">The debugger may be used to set breakpoints, inspect locals, and more.</span></span>

## <a name="references"></a><span data-ttu-id="a9f08-153">参考</span><span class="sxs-lookup"><span data-stu-id="a9f08-153">References</span></span>

[<span data-ttu-id="a9f08-154">使用 ARM 上的 .NET Core 在 Windows 上使用 VS Code 远程调试到 Raspberry Pi</span><span class="sxs-lookup"><span data-stu-id="a9f08-154">Remote debugging with VS Code on Windows to a Raspberry Pi using .NET Core on ARM</span></span>](https://www.hanselman.com/blog/remote-debugging-with-vs-code-on-windows-to-a-raspberry-pi-using-net-core-on-arm)

::: zone-end

::: zone pivot="visualstudio"

## <a name="debug-from-visual-studio-on-windows"></a><span data-ttu-id="a9f08-155">在 Windows 上从 Visual Studio 进行调试</span><span class="sxs-lookup"><span data-stu-id="a9f08-155">Debug from Visual Studio on Windows</span></span>

<span data-ttu-id="a9f08-156">Visual Studio 可以通过 SSH 在远程设备上调试 .NET 应用。</span><span class="sxs-lookup"><span data-stu-id="a9f08-156">Visual Studio can debug .NET apps on remote devices via SSH.</span></span> <span data-ttu-id="a9f08-157">设备上不需要专用配置。</span><span class="sxs-lookup"><span data-stu-id="a9f08-157">No specialized configuration is required on the device.</span></span> <span data-ttu-id="a9f08-158">若要详细了解如何使用 Visual Studio 远程调试 .NET，请参阅 [在 Linux 上使用 SSH 远程调试 .net](/visualstudio/debugger/remote-debugging-dotnet-core-linux-with-ssh?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="a9f08-158">For details on using Visual Studio to debug .NET remotely, see [Remote debug .NET on Linux using SSH](/visualstudio/debugger/remote-debugging-dotnet-core-linux-with-ssh?view=vs-2019).</span></span>

::: zone-end
