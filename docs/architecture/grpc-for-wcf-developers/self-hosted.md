---
title: 自承载 gRPC 应用程序-WCF 开发人员 gRPC
description: 将 ASP.NET Core gRPC 应用程序部署为自承载服务。
ms.date: 12/15/2020
ms.openlocfilehash: a5e2316b8d76593f4eb53760d2609b5bbbc9d2c5
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938528"
---
# <a name="self-hosted-grpc-applications"></a><span data-ttu-id="4272e-103">自承载的 gRPC 应用程序</span><span class="sxs-lookup"><span data-stu-id="4272e-103">Self-hosted gRPC applications</span></span>

<span data-ttu-id="4272e-104">尽管 ASP.NET Core 5.0 应用程序可在 Windows Server 上的 IIS 中进行托管，但目前无法在 IIS 中承载 gRPC 应用程序，因为某些 HTTP/2 功能不受支持。</span><span class="sxs-lookup"><span data-stu-id="4272e-104">Although ASP.NET Core 5.0 applications can be hosted in IIS on Windows Server, currently it isn't possible to host a gRPC application in IIS because some of the HTTP/2 functionality isn't supported.</span></span> <span data-ttu-id="4272e-105">此功能是将来对 Windows Server 进行更新的目标。</span><span class="sxs-lookup"><span data-stu-id="4272e-105">This functionality is a goal for a future update to Windows Server.</span></span>

<span data-ttu-id="4272e-106">你可以将应用程序作为 Windows 服务运行。</span><span class="sxs-lookup"><span data-stu-id="4272e-106">You can run your application as a Windows service.</span></span> <span data-ttu-id="4272e-107">或者，你可以将其作为由 [systemd](https://en.wikipedia.org/wiki/Systemd)控制的 Linux 服务运行，因为 .net 5.0 托管扩展中的新增功能。</span><span class="sxs-lookup"><span data-stu-id="4272e-107">Or you can run it as a Linux service controlled by [systemd](https://en.wikipedia.org/wiki/Systemd), because of new features in the .NET 5.0 hosting extensions.</span></span>

## <a name="run-your-app-as-a-windows-service"></a><span data-ttu-id="4272e-108">以 Windows 服务的形式运行你的应用</span><span class="sxs-lookup"><span data-stu-id="4272e-108">Run your app as a Windows service</span></span>

<span data-ttu-id="4272e-109">若要将 ASP.NET Core 应用程序配置为作为 Windows 服务运行，请从 NuGet 安装 [WindowsServices](https://www.nuget.org/packages/Microsoft.Extensions.Hosting.WindowsServices) 包。</span><span class="sxs-lookup"><span data-stu-id="4272e-109">To configure your ASP.NET Core application to run as a Windows service, install the [Microsoft.Extensions.Hosting.WindowsServices](https://www.nuget.org/packages/Microsoft.Extensions.Hosting.WindowsServices) package from NuGet.</span></span> <span data-ttu-id="4272e-110">然后，将对的调用添加到 `UseWindowsService` `CreateHostBuilder` 中的方法 `Program.cs` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-110">Then add a call to `UseWindowsService` to the `CreateHostBuilder` method in `Program.cs`.</span></span>

```csharp
public static IHostBuilder CreateHostBuilder(string[] args) =>
    Host.CreateDefaultBuilder(args)
        .UseWindowsService() // Enable running as a Windows service
        .ConfigureWebHostDefaults(webBuilder =>
        {
            webBuilder.UseStartup<Startup>();
        });
```

> [!NOTE]
> <span data-ttu-id="4272e-111">如果应用程序不是作为 Windows 服务运行，则该 `UseWindowsService` 方法不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="4272e-111">If the application isn't running as a Windows service, the `UseWindowsService` method doesn't do anything.</span></span>

<span data-ttu-id="4272e-112">现在，使用以下方法之一发布应用程序：</span><span class="sxs-lookup"><span data-stu-id="4272e-112">Now publish your application by using one of these methods:</span></span>

* <span data-ttu-id="4272e-113">在 Visual Studio 中，右键单击项目，然后选择快捷菜单上的 " **发布** "。</span><span class="sxs-lookup"><span data-stu-id="4272e-113">From Visual Studio by right-clicking the project and selecting **Publish** on the shortcut menu.</span></span>
* <span data-ttu-id="4272e-114">从 .NET CLI。</span><span class="sxs-lookup"><span data-stu-id="4272e-114">From the .NET CLI.</span></span>

<span data-ttu-id="4272e-115">发布 .NET 应用程序时，可以选择创建 *依赖于框架的* 部署或 *独立* 部署。</span><span class="sxs-lookup"><span data-stu-id="4272e-115">When you publish a .NET application, you can choose to create a *framework-dependent* deployment or a *self-contained* deployment.</span></span> <span data-ttu-id="4272e-116">依赖于框架的部署要求在运行的主机上安装 .NET 共享运行时。</span><span class="sxs-lookup"><span data-stu-id="4272e-116">Framework-dependent deployments require the .NET Shared Runtime to be installed on the host where they are run.</span></span> <span data-ttu-id="4272e-117">自包含的部署是使用 .NET 运行时和框架的完整副本发布的，可以在任何主机上运行。</span><span class="sxs-lookup"><span data-stu-id="4272e-117">Self-contained deployments are published with a complete copy of the .NET runtime and framework and can be run on any host.</span></span> <span data-ttu-id="4272e-118">有关详细信息，包括每种方法的优点和缺点，请参阅 [.net 应用程序部署](../../core/deploying/index.md) 文档。</span><span class="sxs-lookup"><span data-stu-id="4272e-118">For more information, including the advantages and disadvantages of each approach, see the [.NET application deployment](../../core/deploying/index.md) documentation.</span></span>

<span data-ttu-id="4272e-119">若要发布不需要在主机上安装 .NET 5.0 运行时的应用程序的自包含生成，请指定要包含在该应用程序中的运行时。</span><span class="sxs-lookup"><span data-stu-id="4272e-119">To publish a self-contained build of the application that does not require the .NET 5.0 runtime to be installed on the host, specify the runtime to be included with the application.</span></span> <span data-ttu-id="4272e-120">使用 `-r` (或 `--runtime`) 标志。</span><span class="sxs-lookup"><span data-stu-id="4272e-120">Use the `-r` (or `--runtime`) flag.</span></span>

```dotnetcli
dotnet publish -c Release -r win-x64 -o ./publish
```

<span data-ttu-id="4272e-121">若要发布依赖于框架的生成，请省略 `-r` 标志。</span><span class="sxs-lookup"><span data-stu-id="4272e-121">To publish a framework-dependent build, omit the `-r` flag.</span></span>

```dotnetcli
dotnet publish -c Release -o ./publish
```

<span data-ttu-id="4272e-122">将目录的完整内容复制 `publish` 到安装文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4272e-122">Copy the complete contents of the `publish` directory to an installation folder.</span></span> <span data-ttu-id="4272e-123">然后，使用 [sc 工具](/windows/desktop/services/controlling-a-service-using-sc) 为可执行文件创建 Windows 服务。</span><span class="sxs-lookup"><span data-stu-id="4272e-123">Then, use the [sc tool](/windows/desktop/services/controlling-a-service-using-sc) to create a Windows service for the executable file.</span></span>

```console
sc create MyService binPath=C:\MyService\MyService.exe
```

### <a name="log-to-the-windows-event-log"></a><span data-ttu-id="4272e-124">记录到 Windows 事件日志</span><span class="sxs-lookup"><span data-stu-id="4272e-124">Log to the Windows event log</span></span>

<span data-ttu-id="4272e-125">`UseWindowsService`方法自动添加将日志消息写入 Windows 事件日志的[日志记录](/aspnet/core/fundamentals/logging/)提供程序。</span><span class="sxs-lookup"><span data-stu-id="4272e-125">The `UseWindowsService` method automatically adds a [logging](/aspnet/core/fundamentals/logging/) provider that writes log messages to the Windows event log.</span></span> <span data-ttu-id="4272e-126">你可以通过将 `EventLog` 条目添加到 `Logging` `appsettings.json` 或其他配置源的部分来配置此提供程序的日志记录。</span><span class="sxs-lookup"><span data-stu-id="4272e-126">You can configure logging for this provider by adding an `EventLog` entry to the `Logging` section of `appsettings.json` or another configuration source.</span></span>

<span data-ttu-id="4272e-127">通过在这些设置中设置属性，可以重写事件日志中使用的源名称 `SourceName` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-127">You can override the source name used in the event log by setting a `SourceName` property in these settings.</span></span> <span data-ttu-id="4272e-128">如果未指定名称，则默认的应用程序名称 (将使用的可执行程序集名称) 。</span><span class="sxs-lookup"><span data-stu-id="4272e-128">If you don't specify a name, the default application name (normally the executable assembly name) will be used.</span></span>

<span data-ttu-id="4272e-129">本章末尾介绍了日志记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4272e-129">More information on logging is at the end of this chapter.</span></span>

## <a name="run-your-app-as-a-linux-service-with-systemd"></a><span data-ttu-id="4272e-130">使用 systemd 将应用作为 Linux 服务运行</span><span class="sxs-lookup"><span data-stu-id="4272e-130">Run your app as a Linux service with systemd</span></span>

<span data-ttu-id="4272e-131">若要将 ASP.NET Core 应用程序配置为在 Linux 行话) 中以 Linux 服务 (或 *守护* 程序运行，请从 NuGet 安装 [Microsoft.Extensions.Hosting.Systemd](https://www.nuget.org/packages/Microsoft.Extensions.Hosting.Systemd) 包。</span><span class="sxs-lookup"><span data-stu-id="4272e-131">To configure your ASP.NET Core application to run as a Linux service (or *daemon* in Linux parlance), install the [Microsoft.Extensions.Hosting.Systemd](https://www.nuget.org/packages/Microsoft.Extensions.Hosting.Systemd) package from NuGet.</span></span> <span data-ttu-id="4272e-132">然后，将对的调用添加到 `UseSystemd` `CreateHostBuilder` 中的方法 `Program.cs` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-132">Then add a call to `UseSystemd` to the `CreateHostBuilder` method in `Program.cs`.</span></span>

```csharp
public static IHostBuilder CreateHostBuilder(string[] args) =>
    Host.CreateDefaultBuilder(args)
        .UseSystemd() // Enable running as a Systemd service
        .ConfigureWebHostDefaults(webBuilder =>
        {
            webBuilder.UseStartup<Startup>();
        });
```

> [!NOTE]
> <span data-ttu-id="4272e-133">如果应用程序未作为 Linux 服务运行，则该 `UseSystemd` 方法不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="4272e-133">If the application isn't running as a Linux service, the `UseSystemd` method doesn't do anything.</span></span>

<span data-ttu-id="4272e-134">现在发布应用程序。</span><span class="sxs-lookup"><span data-stu-id="4272e-134">Now publish your application.</span></span> <span data-ttu-id="4272e-135">应用程序可以是依赖于框架的依赖项，也可以独立于适用的 Linux 运行时 (例如 `linux-x64`) 。</span><span class="sxs-lookup"><span data-stu-id="4272e-135">The application can be either framework dependent or self-contained for the relevant Linux runtime (for example, `linux-x64`).</span></span> <span data-ttu-id="4272e-136">您可以使用以下方法之一发布：</span><span class="sxs-lookup"><span data-stu-id="4272e-136">You can publish by using one of these methods:</span></span>

* <span data-ttu-id="4272e-137">在 Visual Studio 中，右键单击项目，然后选择快捷菜单上的 " **发布** "。</span><span class="sxs-lookup"><span data-stu-id="4272e-137">From Visual Studio by right-clicking the project and selecting **Publish** on the shortcut menu.</span></span>
* <span data-ttu-id="4272e-138">在 .NET CLI 中，使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="4272e-138">From the .NET CLI, by using the following command:</span></span>

  ```dotnetcli
  dotnet publish -c Release -r linux-x64 -o ./publish
  ```
  
<span data-ttu-id="4272e-139">将目录的完整内容复制 `publish` 到 Linux 主机上的安装文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4272e-139">Copy the complete contents of the `publish` directory to an installation folder on the Linux host.</span></span> <span data-ttu-id="4272e-140">注册服务需要将一个名为 *unit file* 的特殊文件添加到 `/etc/systemd/system` 目录中。</span><span class="sxs-lookup"><span data-stu-id="4272e-140">Registering the service requires a special file, called a *unit file*, to be added to the `/etc/systemd/system` directory.</span></span> <span data-ttu-id="4272e-141">你需要 root 权限才能在此文件夹中创建文件。</span><span class="sxs-lookup"><span data-stu-id="4272e-141">You'll need root permission to create a file in this folder.</span></span> <span data-ttu-id="4272e-142">使用要使用的标识符和扩展名来命名该文件 `systemd` `.service` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-142">Name the file with the identifier that you want `systemd` to use and the `.service` extension.</span></span> <span data-ttu-id="4272e-143">例如，使用 `/etc/systemd/system/myapp.service`。</span><span class="sxs-lookup"><span data-stu-id="4272e-143">For example, use `/etc/systemd/system/myapp.service`.</span></span>

<span data-ttu-id="4272e-144">服务文件使用 INI 格式，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="4272e-144">The service file uses INI format, as shown in this example:</span></span>

```ini
[Unit]
Description=My gRPC Application

[Service]
Type=notify
ExecStart=/usr/sbin/myapp

[Install]
WantedBy=multi-user.target
```

<span data-ttu-id="4272e-145">`Type=notify`属性指示 `systemd` 应用程序在启动和关闭时将通知它。</span><span class="sxs-lookup"><span data-stu-id="4272e-145">The `Type=notify` property tells `systemd` that the application will notify it on startup and shutdown.</span></span> <span data-ttu-id="4272e-146">此 `WantedBy=multi-user.target` 设置将导致在 Linux 系统达到 "运行级别 2" 时启动服务，这意味着非图形、多用户 shell 处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="4272e-146">The `WantedBy=multi-user.target` setting will cause the service to start when the Linux system reaches "runlevel 2," which means a non-graphical, multi-user shell is active.</span></span>

<span data-ttu-id="4272e-147">`systemd`需要重新加载其配置，然后才能识别该服务。</span><span class="sxs-lookup"><span data-stu-id="4272e-147">Before `systemd` will recognize the service, it needs to reload its configuration.</span></span> <span data-ttu-id="4272e-148">您可以 `systemd` 使用命令进行控制 `systemctl` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-148">You control `systemd` by using the `systemctl` command.</span></span> <span data-ttu-id="4272e-149">重新加载后，请使用 `status` 子命令确认应用程序已成功注册。</span><span class="sxs-lookup"><span data-stu-id="4272e-149">After reloading, use the `status` subcommand to confirm that the application has registered successfully.</span></span>

```console
sudo systemctl daemon-reload
sudo systemctl status myapp
```

<span data-ttu-id="4272e-150">如果已正确配置服务，则会看到以下输出：</span><span class="sxs-lookup"><span data-stu-id="4272e-150">If you've configured the service correctly, you'll get the following output:</span></span>

```text
myapp.service - My gRPC Application
 Loaded: loaded (/etc/systemd/system/myapp.service; disabled; vendor preset: enabled)
 Active: inactive (dead)
```

<span data-ttu-id="4272e-151">使用 `start` 命令启动服务。</span><span class="sxs-lookup"><span data-stu-id="4272e-151">Use the `start` command to start the service.</span></span>

```console
sudo systemctl start myapp.service
```

> [!TIP]
> <span data-ttu-id="4272e-152">`.service`使用时，扩展插件是可选的 `systemctl start` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-152">The `.service` extension is optional when you're using `systemctl start`.</span></span>

<span data-ttu-id="4272e-153">若要通知 `systemd` 在系统启动时自动启动该服务，请使用 `enable` 命令。</span><span class="sxs-lookup"><span data-stu-id="4272e-153">To tell `systemd` to start the service automatically on system startup, use the `enable` command.</span></span>

```console
sudo systemctl enable myapp
```

### <a name="log-to-journald"></a><span data-ttu-id="4272e-154">登录到 journald</span><span class="sxs-lookup"><span data-stu-id="4272e-154">Log to journald</span></span>

<span data-ttu-id="4272e-155">Windows 事件日志的 Linux 等效项是 `journald` 中包含的结构化日志记录系统服务 `systemd` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-155">The Linux equivalent of the Windows event log is `journald`, a structured logging system service that's part of `systemd`.</span></span> <span data-ttu-id="4272e-156">由 Linux 后台程序写入标准输出的日志消息将自动写入到 `journald` 中。</span><span class="sxs-lookup"><span data-stu-id="4272e-156">Log messages written to the standard output by a Linux daemon are automatically written to `journald`.</span></span> <span data-ttu-id="4272e-157">若要配置日志记录级别，请使用 `Console` 日志记录配置的部分。</span><span class="sxs-lookup"><span data-stu-id="4272e-157">To configure logging levels, use the `Console` section of the logging configuration.</span></span> <span data-ttu-id="4272e-158">`UseSystemd`主机生成器方法自动配置控制台输出格式以适合日志。</span><span class="sxs-lookup"><span data-stu-id="4272e-158">The `UseSystemd` host builder method automatically configures the console output format to suit the journal.</span></span>

<span data-ttu-id="4272e-159">由于 `journald` 是 Linux 日志的标准，因此各种工具与之集成。</span><span class="sxs-lookup"><span data-stu-id="4272e-159">Because `journald` is the standard for Linux logs, a variety of tools integrate with it.</span></span> <span data-ttu-id="4272e-160">可以轻松地将日志从路由 `journald` 到外部日志记录系统。</span><span class="sxs-lookup"><span data-stu-id="4272e-160">You can easily route logs from `journald` to an external logging system.</span></span> <span data-ttu-id="4272e-161">在本地运行的主机上，可以使用 `journalctl` 命令从命令行中查看日志。</span><span class="sxs-lookup"><span data-stu-id="4272e-161">Working locally on the host, you can use the `journalctl` command to view logs from the command line.</span></span>

```console
sudo journalctl -u myapp
```

> [!TIP]
> <span data-ttu-id="4272e-162">如果主机上有可用的 GUI 环境，则可以使用一些图形日志查看器，如 *QJournalctl* 和 *gnome 日志*。</span><span class="sxs-lookup"><span data-stu-id="4272e-162">If you have a GUI environment available on your host, a few graphical log viewers are available for Linux, such as *QJournalctl* and *gnome-logs*.</span></span>

<span data-ttu-id="4272e-163">若要了解有关 `systemd` 使用从命令行查询日志的详细信息 `journalctl` ，请参阅 [manpages](https://manpages.debian.org/buster/systemd/journalctl.1)。</span><span class="sxs-lookup"><span data-stu-id="4272e-163">To learn more about querying the `systemd` journal from the command line by using `journalctl`, see [the manpages](https://manpages.debian.org/buster/systemd/journalctl.1).</span></span>

## <a name="https-certificates-for-self-hosted-applications"></a><span data-ttu-id="4272e-164">用于自承载应用程序的 HTTPS 证书</span><span class="sxs-lookup"><span data-stu-id="4272e-164">HTTPS certificates for self-hosted applications</span></span>

<span data-ttu-id="4272e-165">在生产环境中运行 gRPC 应用程序时，应使用来自受信任证书颁发机构 (CA) 的 TLS 证书。</span><span class="sxs-lookup"><span data-stu-id="4272e-165">When you're running a gRPC application in production, you should use a TLS certificate from a trusted certificate authority (CA).</span></span> <span data-ttu-id="4272e-166">此 CA 可以是公共 CA，也可以是组织的内部 ca。</span><span class="sxs-lookup"><span data-stu-id="4272e-166">This CA might be a public CA, or an internal one for your organization.</span></span>

<span data-ttu-id="4272e-167">在 Windows 主机上，你可以使用类从安全的 [证书存储区](/windows/win32/seccrypto/managing-certificates-with-certificate-stores) 中加载证书 <xref:System.Security.Cryptography.X509Certificates.X509Store> 。</span><span class="sxs-lookup"><span data-stu-id="4272e-167">On Windows hosts, you can load the certificate from a secure [certificate store](/windows/win32/seccrypto/managing-certificates-with-certificate-stores) by using the <xref:System.Security.Cryptography.X509Certificates.X509Store> class.</span></span> <span data-ttu-id="4272e-168">你还可以将 `X509Store` 类用于某些 Linux 主机上的 OpenSSL 密钥存储。</span><span class="sxs-lookup"><span data-stu-id="4272e-168">You can also use the `X509Store` class with the OpenSSL key store on some Linux hosts.</span></span>

<span data-ttu-id="4272e-169">还可以通过使用 [X509Certificate2 构造函数](xref:System.Security.Cryptography.X509Certificates.X509Certificate2.%23ctor%2A)之一创建证书，方法如下：</span><span class="sxs-lookup"><span data-stu-id="4272e-169">You can also create certificates by using one of the [X509Certificate2 constructors](xref:System.Security.Cryptography.X509Certificates.X509Certificate2.%23ctor%2A), from either:</span></span>

* <span data-ttu-id="4272e-170">文件，如 `.pfx` 受强密码保护的文件</span><span class="sxs-lookup"><span data-stu-id="4272e-170">A file, such as a `.pfx` file protected by a strong password</span></span>
* <span data-ttu-id="4272e-171">从安全存储服务（如[Azure Key Vault](https://azure.microsoft.com/services/key-vault/) ）检索的二进制数据</span><span class="sxs-lookup"><span data-stu-id="4272e-171">Binary data retrieved from a secure storage service such as [Azure Key Vault](https://azure.microsoft.com/services/key-vault/)</span></span>

<span data-ttu-id="4272e-172">可以通过两种方式将 Kestrel 配置为使用证书：通过配置或代码。</span><span class="sxs-lookup"><span data-stu-id="4272e-172">You can configure Kestrel to use a certificate in two ways: from configuration or in code.</span></span>

### <a name="set-https-certificates-by-using-configuration"></a><span data-ttu-id="4272e-173">使用配置设置 HTTPS 证书</span><span class="sxs-lookup"><span data-stu-id="4272e-173">Set HTTPS certificates by using configuration</span></span>

<span data-ttu-id="4272e-174">配置方法要求在 `.pfx` Kestrel 配置节中设置证书文件的路径和密码。</span><span class="sxs-lookup"><span data-stu-id="4272e-174">The configuration approach requires setting the path to the certificate `.pfx` file and the password in the Kestrel configuration section.</span></span> <span data-ttu-id="4272e-175">在中 `appsettings.json` ，这将如下所示：</span><span class="sxs-lookup"><span data-stu-id="4272e-175">In `appsettings.json`, that would look like this:</span></span>

```json
{
  "Kestrel": {
    "Certificates": {
      "Default": {
        "Path": "cert.pfx",
        "Password": "DO NOT STORE PLAINTEXT PASSWORDS IN APPSETTINGS FILES"
      }
    }
  }
}
```

<span data-ttu-id="4272e-176">使用安全配置源（如 Azure Key Vault 或 Hashicorp 保管库）提供密码。</span><span class="sxs-lookup"><span data-stu-id="4272e-176">Provide the password by using a secure configuration source such as Azure Key Vault or Hashicorp Vault.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4272e-177">不要在配置文件中存储未加密的密码。</span><span class="sxs-lookup"><span data-stu-id="4272e-177">Don't store unencrypted passwords in configuration files.</span></span>

### <a name="set-https-certificates-in-code"></a><span data-ttu-id="4272e-178">在代码中设置 HTTPS 证书</span><span class="sxs-lookup"><span data-stu-id="4272e-178">Set HTTPS certificates in code</span></span>

<span data-ttu-id="4272e-179">若要在代码中的 Kestrel 上配置 HTTPS，请使用 `ConfigureKestrel` `IWebHostBuilder` 类中的方法 `Program` 。</span><span class="sxs-lookup"><span data-stu-id="4272e-179">To configure HTTPS on Kestrel in code, use the `ConfigureKestrel` method on `IWebHostBuilder` in the `Program` class.</span></span>

```csharp
public static IHostBuilder CreateHostBuilder(string[] args) =>
    Host.CreateDefaultBuilder(args)
        .ConfigureWebHostDefaults(webBuilder =>
        {
            webBuilder.UseStartup<Startup>();
            webBuilder.ConfigureKestrel(kestrel =>
            {
                kestrel.ConfigureHttpsDefaults(https =>
                {
                    https.ServerCertificate = new X509Certificate2("mycert.pfx", "password");
                });
            });
        });
```

<span data-ttu-id="4272e-180">同样，请务必将文件的密码存储 `.pfx` 在中，并从安全配置源中检索该文件。</span><span class="sxs-lookup"><span data-stu-id="4272e-180">Again, be sure to store the password for the `.pfx` file in, and retrieve it from, a secure configuration source.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="4272e-181">[上一页](grpc-in-production.md)
>[下一页](docker.md)</span><span class="sxs-lookup"><span data-stu-id="4272e-181">[Previous](grpc-in-production.md)
[Next](docker.md)</span></span>
