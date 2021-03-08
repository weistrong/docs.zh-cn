---
ms.openlocfilehash: 5a027054024d8429831d73525ab3748c51ae850e
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102255746"
---

<span data-ttu-id="d0ee5-101">使用包管理器进行安装时，将为你安装这些库。</span><span class="sxs-lookup"><span data-stu-id="d0ee5-101">When you install with a package manager, these libraries are installed for you.</span></span> <span data-ttu-id="d0ee5-102">但是，如果手动安装 .NET Core 或发布自包含的应用，则需要确保已安装以下库：</span><span class="sxs-lookup"><span data-stu-id="d0ee5-102">But, if you manually install .NET Core or you publish a self-contained app, you'll need to make sure these libraries are installed:</span></span>

- <span data-ttu-id="d0ee5-103">krb5-libs</span><span class="sxs-lookup"><span data-stu-id="d0ee5-103">krb5-libs</span></span>
- <span data-ttu-id="d0ee5-104">libicu</span><span class="sxs-lookup"><span data-stu-id="d0ee5-104">libicu</span></span>
- <span data-ttu-id="d0ee5-105">openssl-libs</span><span class="sxs-lookup"><span data-stu-id="d0ee5-105">openssl-libs</span></span>
- <span data-ttu-id="d0ee5-106">zlib</span><span class="sxs-lookup"><span data-stu-id="d0ee5-106">zlib</span></span>

<span data-ttu-id="d0ee5-107">如果目标运行时环境的 OpenSSL 版本为1.1 或更高版本，则需要安装 compat-openssl10。</span><span class="sxs-lookup"><span data-stu-id="d0ee5-107">If the target runtime environment's OpenSSL version is 1.1 or newer, you'll need to install **compat-openssl10**.</span></span>

<span data-ttu-id="d0ee5-108">有关依赖项的详细信息，请参阅[独立式 Linux 应用](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="d0ee5-108">For more information about the dependencies, see [Self-contained Linux apps](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md).</span></span>

<span data-ttu-id="d0ee5-109">对于使用 System.Drawing.Common 程序集的 .NET Core 应用，还需要以下依赖项：</span><span class="sxs-lookup"><span data-stu-id="d0ee5-109">For .NET Core apps that use the *System.Drawing.Common* assembly, you'll also need the following dependency:</span></span>

- [<span data-ttu-id="d0ee5-110">libgdiplus（版本 6.0.1 或更高版本）</span><span class="sxs-lookup"><span data-stu-id="d0ee5-110">libgdiplus (version 6.0.1 or later)</span></span>](https://www.mono-project.com/docs/gui/libgdiplus/)

  > [!WARNING]
  > <span data-ttu-id="d0ee5-111">可以通过将 Mono 存储库添加到系统来安装最新版 libgdiplus。</span><span class="sxs-lookup"><span data-stu-id="d0ee5-111">You can install a recent version of *libgdiplus* by adding the Mono repository to your system.</span></span> <span data-ttu-id="d0ee5-112">有关详细信息，请参阅 <https://www.mono-project.com/download/stable/>。</span><span class="sxs-lookup"><span data-stu-id="d0ee5-112">For more information, see <https://www.mono-project.com/download/stable/>.</span></span>
