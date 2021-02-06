---
description: 了解有关以下内容的详细信息：部署 WCF 库项目
title: 部署 WCF 库项目
ms.date: 03/30/2017
ms.assetid: 9f9222fe-d358-443c-9a49-12c5498e35e7
ms.openlocfilehash: 1476f564e3e341c77ab9ba4e4281d6f242a735cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646096"
---
# <a name="deploying-a-wcf-library-project"></a><span data-ttu-id="6c8a8-103">部署 WCF 库项目</span><span class="sxs-lookup"><span data-stu-id="6c8a8-103">Deploying a WCF Library Project</span></span>

<span data-ttu-id="6c8a8-104">本主题介绍如何部署 Windows Communication Foundation (WCF) 服务库项目。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-104">This topic describes how you can deploy a Windows Communication Foundation (WCF) Service Library Project.</span></span>  
  
## <a name="deploying-a-wcf-service-library"></a><span data-ttu-id="6c8a8-105">部署 WCF 服务库</span><span class="sxs-lookup"><span data-stu-id="6c8a8-105">Deploying a WCF Service Library</span></span>  

 <span data-ttu-id="6c8a8-106">WCF 服务库是 (DLL) 的动态链接库。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-106">A WCF service library is a dynamic-link library (DLL).</span></span> <span data-ttu-id="6c8a8-107">因此，它不能自己运行。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-107">As such, it cannot be executed on its own.</span></span> <span data-ttu-id="6c8a8-108">必须将其部署到宿主环境中。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-108">It needs to be deployed into a hosting environment.</span></span> <span data-ttu-id="6c8a8-109">有关此过程的详细信息，请参阅 [托管和使用 WCF 服务](/previous-versions/dotnet/articles/bb332338(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-109">For more information about this process, see [Hosting and Consuming WCF Services](/previous-versions/dotnet/articles/bb332338(v=msdn.10)).</span></span>  
  
 <span data-ttu-id="6c8a8-110">WCF 服务库可以像任何其他 WCF 服务一样部署。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-110">A WCF service library can be deployed like any other WCF service.</span></span> <span data-ttu-id="6c8a8-111">但请注意，.NET Framework 不支持 Dll 的配置。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-111">However, be aware that .NET Framework does not support configuration for DLLs.</span></span> <span data-ttu-id="6c8a8-112"><xref:System.Configuration> 支持每个应用程序域一个配置文件。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-112"><xref:System.Configuration> supports one configuration file per app-domain.</span></span> <span data-ttu-id="6c8a8-113">WCF 服务库项目在开发期间为库提供了一个 App.config 文件，从而减轻了这一限制。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-113">The WCF service library project alleviates this limitation by providing an App.config file for the library during development.</span></span> <span data-ttu-id="6c8a8-114">但在部署之后不能识别 App.config 文件。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-114">However, the App.config file is not recognized after deployment.</span></span>  
  
 <span data-ttu-id="6c8a8-115">必须将配置代码移动到主机环境所识别的配置文件中。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-115">You have to move your configuration code into the configuration file recognized by your hosting environment.</span></span> <span data-ttu-id="6c8a8-116">对于自承载，您应将 App.config 文件的内容复制到宿主可执行文件的 App.config 文件中。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-116">For self-hosting, you should copy the contents of the App.config file into the App.config file of the hosting executable.</span></span> <span data-ttu-id="6c8a8-117">如果使用 IIS 承载服务，则应将 App.config 文件的内容复制到虚拟目录的 Web.config 文件中。</span><span class="sxs-lookup"><span data-stu-id="6c8a8-117">If you use IIS to host your service, you should copy the contents of the App.config file into the Web.config file of the virtual directory.</span></span>
