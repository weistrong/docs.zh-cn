---
ms.openlocfilehash: 3275865cf7f4669ba7deaacea320136d02f64dda
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804207"
---

<span data-ttu-id="41d04-101">如果收到类似于“找不到包 {dotnet-package}”或“无法安装某些包”的错误消息，请运行以下命令 。</span><span class="sxs-lookup"><span data-stu-id="41d04-101">If you receive an error message similar to **Unable to locate package {dotnet-package}** or **Some packages could not be installed**, run the following commands.</span></span>

<span data-ttu-id="41d04-102">以下命令组中有两个占位符。</span><span class="sxs-lookup"><span data-stu-id="41d04-102">There are two placeholders in the following set of commands.</span></span>

- `{dotnet-package}`\
<span data-ttu-id="41d04-103">此项表示要安装的 .NET 包，如 `aspnetcore-runtime-3.1`。</span><span class="sxs-lookup"><span data-stu-id="41d04-103">This represents the .NET package you're installing, such as `aspnetcore-runtime-3.1`.</span></span> <span data-ttu-id="41d04-104">它在以下 `sudo apt-get install` 命令中使用。</span><span class="sxs-lookup"><span data-stu-id="41d04-104">This is used in the following `sudo apt-get install` command.</span></span>

- `{os-version}`\
<span data-ttu-id="41d04-105">这表示你正在使用的发行版。</span><span class="sxs-lookup"><span data-stu-id="41d04-105">This represents the distribution version you're on.</span></span> <span data-ttu-id="41d04-106">此项在以下 `wget` 命令中使用。</span><span class="sxs-lookup"><span data-stu-id="41d04-106">This is used in the `wget` command below.</span></span> <span data-ttu-id="41d04-107">发行版是数值，如 Ubuntu 上的 `20.04` 或 Debian 上的 `10`。</span><span class="sxs-lookup"><span data-stu-id="41d04-107">The distribution version is the numerical value, such as `20.04` on Ubuntu or `10` on Debian.</span></span>

<span data-ttu-id="41d04-108">首先，尝试清除包列表：</span><span class="sxs-lookup"><span data-stu-id="41d04-108">First, try purging the package list:</span></span>

```bash
sudo dpkg --purge packages-microsoft-prod && sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update
```

<span data-ttu-id="41d04-109">然后，再次尝试安装 .NET。</span><span class="sxs-lookup"><span data-stu-id="41d04-109">Then, try to install .NET again.</span></span> <span data-ttu-id="41d04-110">如果这不起作用，可使用以下命令运行手动安装：</span><span class="sxs-lookup"><span data-stu-id="41d04-110">If that doesn't work, you can run a manual install with the following commands:</span></span>
