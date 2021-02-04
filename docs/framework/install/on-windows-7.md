---
title: 在 Windows 7 SP1 上安装 .NET Framework
description: 了解如何在 Windows 7 SP1 上安装 .NET Framework。
ms.date: 04/18/2019
ms.openlocfilehash: 900b38110626a93f37829045a8676ea87101d7e9
ms.sourcegitcommit: 8299abfbd5c49b596d61f1e4d09bc6b8ba055b36
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "98899082"
---
# <a name="install-the-net-framework-on-windows-7-sp1-and-windows-server-2008-r2"></a><span data-ttu-id="657f1-103">在 Windows 7 SP1 和 Windows Server 2008 R2 上安装 .NET Framework</span><span class="sxs-lookup"><span data-stu-id="657f1-103">Install the .NET Framework on Windows 7 SP1 and Windows Server 2008 R2</span></span>

<span data-ttu-id="657f1-104">在 Windows 上运行许多应用程序需要 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="657f1-104">The .NET Framework is required to run many applications on Windows.</span></span> <span data-ttu-id="657f1-105">可以按照以下说明进行安装。</span><span class="sxs-lookup"><span data-stu-id="657f1-105">You can use the following instructions to install it.</span></span> <span data-ttu-id="657f1-106">在尝试运行应用程序后，可能转到了此页并在计算机上看到以下对话框：</span><span class="sxs-lookup"><span data-stu-id="657f1-106">You may have arrived on this page after trying to run an application and seeing the following dialog on your machine.</span></span>

![无法启动此应用程序](./media/this-application-could-not-be-started.png)

<span data-ttu-id="657f1-108">这些说明可帮助安装所需的 .NET Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="657f1-108">These instructions will help you install the .NET Framework versions you need.</span></span> <span data-ttu-id="657f1-109">[.NET Framework 4.8](https://github.com/Microsoft/dotnet/tree/master/releases/net48) 是最新版本。</span><span class="sxs-lookup"><span data-stu-id="657f1-109">The [.NET Framework 4.8](https://github.com/Microsoft/dotnet/tree/master/releases/net48) is the latest version.</span></span> <span data-ttu-id="657f1-110">Windows 7 SP1 和 Windows Server 2008 R2 支持它，且它包含在 [Windows 10 2019 年 5 月更新](https://support.microsoft.com/help/4028685/windows-10-get-the-update)中。</span><span class="sxs-lookup"><span data-stu-id="657f1-110">It is supported on Windows 7 SP1 and Windows Server 2008 R2 and is included with [Windows 10 May 2019 Update](https://support.microsoft.com/help/4028685/windows-10-get-the-update).</span></span>

## <a name="net-framework-48"></a><span data-ttu-id="657f1-111">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="657f1-111">.NET Framework 4.8</span></span>

> [!div class="button"]
> [<span data-ttu-id="657f1-112">下载 .NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="657f1-112">Download .NET Framework 4.8</span></span>](https://dotnet.microsoft.com/download/dotnet-framework/net48)

<span data-ttu-id="657f1-113">[.NET Framework 4.8](https://github.com/Microsoft/dotnet/tree/master/releases/net48) 可用于运行针对 .NET Framework 4.0 或更高版本生成的应用程序。</span><span class="sxs-lookup"><span data-stu-id="657f1-113">The [.NET Framework 4.8](https://github.com/Microsoft/dotnet/tree/master/releases/net48) can be used to run applications built for .NET Framework 4.0 or later.</span></span>

### <a name="offline-installer"></a><span data-ttu-id="657f1-114">脱机安装程序</span><span class="sxs-lookup"><span data-stu-id="657f1-114">Offline installer</span></span>

<span data-ttu-id="657f1-115">在 Windows 7 上执行 .NET Framework 的脱机安装时，首先需要确保目标计算机上已安装最新的 [Microsoft 根证书颁发机构 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm)。</span><span class="sxs-lookup"><span data-stu-id="657f1-115">When doing an offline install for .NET Framework on Windows 7, you'll first need to make sure that the latest [Microsoft Root Certificate Authority 2011](https://www.microsoft.com/pkiops/Docs/Repository.htm) has been installed on the target machine.</span></span>

<span data-ttu-id="657f1-116">certmgr.exe 工具可以自动安装证书，并从 Visual Studio 或 Windows SDK 获取该证书。</span><span class="sxs-lookup"><span data-stu-id="657f1-116">The _certmgr.exe_ tool can automate installing a certificate and is obtained from Visual Studio or the Windows SDK.</span></span> <span data-ttu-id="657f1-117">以下命令用于在运行 .NET Framework 安装程序之前安装证书：</span><span class="sxs-lookup"><span data-stu-id="657f1-117">The following command is used to install the certificate before running the .NET Framework installer:</span></span>

```console
certmgr.exe /add MicRooCerAut2011_2011_03_22.crt /s /r localMachine root
```

## <a name="net-framework-35"></a><span data-ttu-id="657f1-118">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="657f1-118">.NET Framework 3.5</span></span>

<span data-ttu-id="657f1-119">[.NET Framework 3.5](https://dotnet.microsoft.com/download/dotnet-framework/net35-sp1) 包含在 Windows 7 中。</span><span class="sxs-lookup"><span data-stu-id="657f1-119">The [.NET Framework 3.5](https://dotnet.microsoft.com/download/dotnet-framework/net35-sp1) is included with Windows 7.</span></span>

<span data-ttu-id="657f1-120">.NET Framework 3.5 支持为 .NET Framework 1.0 到 3.5 生成的应用。</span><span class="sxs-lookup"><span data-stu-id="657f1-120">The .NET Framework 3.5 supports apps built for .NET Framework 1.0 through 3.5.</span></span>

## <a name="help"></a><span data-ttu-id="657f1-121">帮助</span><span class="sxs-lookup"><span data-stu-id="657f1-121">Help</span></span>

<span data-ttu-id="657f1-122">如果无法确定已安装 .NET Framework 的正确版本，可以[联系 Microsoft 获取帮助](mailto:dotnet-install-help@service.microsoft.com?subject=Install-Help)。</span><span class="sxs-lookup"><span data-stu-id="657f1-122">You can [contact Microsoft for help](mailto:dotnet-install-help@service.microsoft.com?subject=Install-Help) if you cannot get the correct version of the .NET Framework installed.</span></span>

## <a name="see-also"></a><span data-ttu-id="657f1-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="657f1-123">See also</span></span>

- [<span data-ttu-id="657f1-124">下载 .NET Framework</span><span class="sxs-lookup"><span data-stu-id="657f1-124">Download the .NET Framework</span></span>](https://dotnet.microsoft.com/download)
- [<span data-ttu-id="657f1-125">安装和卸载 .NET Framework 受阻疑难解答</span><span class="sxs-lookup"><span data-stu-id="657f1-125">Troubleshoot blocked .NET Framework installations and uninstallations</span></span>](troubleshoot-blocked-installations-and-uninstallations.md)
- [<span data-ttu-id="657f1-126">安装面向开发人员的 .NET Framework</span><span class="sxs-lookup"><span data-stu-id="657f1-126">Install the .NET Framework for developers</span></span>](guide-for-developers.md)
