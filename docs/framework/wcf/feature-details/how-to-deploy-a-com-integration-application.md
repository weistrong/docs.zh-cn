---
description: 了解有关详细信息，请参阅如何：部署 COM + 集成应用程序
title: 如何：部署 COM+ 集成应用程序
ms.date: 03/30/2017
ms.assetid: 2e5a0510-db3c-4988-a09c-696285836650
ms.openlocfilehash: 4bf9e72a631c97f3b791ecd01abb5cb74365772d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734381"
---
# <a name="how-to-deploy-a-com-integration-application"></a><span data-ttu-id="7f804-103">如何：部署 COM+ 集成应用程序</span><span class="sxs-lookup"><span data-stu-id="7f804-103">How to: Deploy a COM+ Integration Application</span></span>

<span data-ttu-id="7f804-104">编写了 COM+ 集成应用程序后，您可能要将它部署在另一台计算机上。</span><span class="sxs-lookup"><span data-stu-id="7f804-104">Once you have written a COM+ integration application, you may want to deploy it on another machine.</span></span> <span data-ttu-id="7f804-105">本主题说明如何将 COM+ 集成应用程序从一台计算机移动到另一台计算机。</span><span class="sxs-lookup"><span data-stu-id="7f804-105">This topic describes how to move a COM+ integration application from one machine to another.</span></span>  
  
### <a name="moving-a-com-hosted-integration-app"></a><span data-ttu-id="7f804-106">移动 COM+ 承载的集成应用程序</span><span class="sxs-lookup"><span data-stu-id="7f804-106">Moving a COM+ hosted Integration App</span></span>  
  
1. <span data-ttu-id="7f804-107">确保两台计算机上都安装了 WCF。</span><span class="sxs-lookup"><span data-stu-id="7f804-107">Ensure that WCF is installed on both machines.</span></span>  
  
2. <span data-ttu-id="7f804-108">从计算机 A 中导出应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f804-108">Export the application from machine A.</span></span>  
  
3. <span data-ttu-id="7f804-109">在计算机 B 上导入应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f804-109">Import the application on machine B.</span></span>  
  
4. <span data-ttu-id="7f804-110">设置应用程序根目录。</span><span class="sxs-lookup"><span data-stu-id="7f804-110">Set the Application Root Directory.</span></span> <span data-ttu-id="7f804-111">按照约定，此目录为 %PROGRAMFILES%/ComPlus Applications/{AppGUID}。</span><span class="sxs-lookup"><span data-stu-id="7f804-111">By convention, this is %PROGRAMFILES%/ComPlus Applications/{AppGUID}.</span></span>  
  
5. <span data-ttu-id="7f804-112">将计算机 A 上应用程序根目录中的 Application.config 和 Application.manifest 文件复制到计算机 B 上的应用程序根目录。</span><span class="sxs-lookup"><span data-stu-id="7f804-112">Copy the Application.config and Application.manifest files from the application root directory on machine A to the application root directory on machine B.</span></span>  
  
6. <span data-ttu-id="7f804-113">在计算机 B 的 Application.config 文件中编辑服务终结点地址以标识相应计算机。</span><span class="sxs-lookup"><span data-stu-id="7f804-113">Edit the service endpoint addresses in the Application.config file on machine B to identify the appropriate machine.</span></span> <span data-ttu-id="7f804-114">例如，将 `http://machineA/MyService` 更改为 `http://machineB/MyService`。</span><span class="sxs-lookup"><span data-stu-id="7f804-114">For example, change `http://machineA/MyService` to `http://machineB/MyService`.</span></span>  
  
### <a name="moving-a-web-hosted-integration-application"></a><span data-ttu-id="7f804-115">移动 Web 承载的集成应用程序</span><span class="sxs-lookup"><span data-stu-id="7f804-115">Moving a Web-hosted integration application</span></span>  
  
1. <span data-ttu-id="7f804-116">确保两台计算机上都安装了 WCF。</span><span class="sxs-lookup"><span data-stu-id="7f804-116">Ensure that WCF is installed on both machines.</span></span>  
  
2. <span data-ttu-id="7f804-117">从计算机 A 中导出应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f804-117">Export the application from machine A.</span></span>  
  
3. <span data-ttu-id="7f804-118">在计算机 B 上导入应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f804-118">Import the application on machine B.</span></span>  
  
4. <span data-ttu-id="7f804-119">在计算机 B 上创建 IIS 虚拟根目录。</span><span class="sxs-lookup"><span data-stu-id="7f804-119">Create an IIS vroot on machine B.</span></span>  
  
5. <span data-ttu-id="7f804-120">将计算机 A 上虚拟根目录中的 .svc 文件 (componentName.svc) 和 Web.config 文件复制到计算机 B 上新创建的虚拟根目录。</span><span class="sxs-lookup"><span data-stu-id="7f804-120">Copy the .svc file (componentName.svc) and the Web.config file from the vroot on machine A to the newly created vroot on machine B.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f804-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f804-121">See also</span></span>

- [<span data-ttu-id="7f804-122">与 COM + 应用程序集成概述</span><span class="sxs-lookup"><span data-stu-id="7f804-122">Integrating with COM+ Applications Overview</span></span>](integrating-with-com-plus-applications-overview.md)
- [<span data-ttu-id="7f804-123">如何：配置 COM+ 服务设置</span><span class="sxs-lookup"><span data-stu-id="7f804-123">How to: Configure COM+ Service Settings</span></span>](how-to-configure-com-service-settings.md)
- [<span data-ttu-id="7f804-124">如何：使用 COM+ 服务模型配置工具</span><span class="sxs-lookup"><span data-stu-id="7f804-124">How to: Use the COM+ Service Model Configuration Tool</span></span>](how-to-use-the-com-service-model-configuration-tool.md)
