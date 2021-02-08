---
description: 了解详细信息：重命名 WCF 服务
title: 重命名 WCF 服务
ms.date: 03/30/2017
ms.assetid: 14235a65-b1c5-409d-b6cc-a979acd54bbd
ms.openlocfilehash: 8d75e43f4bda97e8ee6de34b039eb1236d6c4a6d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779161"
---
# <a name="renaming-a-wcf-service"></a><span data-ttu-id="3876d-103">重命名 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="3876d-103">Renaming a WCF Service</span></span>

<span data-ttu-id="3876d-104">本主题介绍如何重命名 WCF) 服务 (Windows Communication Foundation。</span><span class="sxs-lookup"><span data-stu-id="3876d-104">This topic describes how you can rename a Windows Communication Foundation (WCF) service.</span></span>  
  
## <a name="renaming-a-wcf-service"></a><span data-ttu-id="3876d-105">重命名 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="3876d-105">Renaming a WCF Service</span></span>  

 <span data-ttu-id="3876d-106">执行以下步骤以重命名 Windows Communication Foundation (WCF) 模板中的服务。</span><span class="sxs-lookup"><span data-stu-id="3876d-106">Perform the following steps to rename a service in a Windows Communication Foundation (WCF) template,</span></span>  
  
- <span data-ttu-id="3876d-107">更改实现该服务的类的名称。</span><span class="sxs-lookup"><span data-stu-id="3876d-107">Change the name of the class that implements the service.</span></span>  
  
- <span data-ttu-id="3876d-108">在该服务的配置文件中，将服务的名称更改为选定的新名称，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="3876d-108">In the configuration file of the service, change the name of the service to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="3876d-109">配置文件可以是 app.config 或 web.config 文件，具体取决于宿主模型。</span><span class="sxs-lookup"><span data-stu-id="3876d-109">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service name="WcfService.NewName">  
      </service>  
   </services>  
</system.servicemodel>  
```  
  
- <span data-ttu-id="3876d-110">如果服务已 webhosted，则它将使用 *\* .svc* 文件。</span><span class="sxs-lookup"><span data-stu-id="3876d-110">If your service is webhosted, it uses an *\*.svc* file.</span></span> <span data-ttu-id="3876d-111">打开 svc 文件并修改服务的名称，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="3876d-111">Open the svc file and modify the name of your service as indicated in the following example.</span></span> <span data-ttu-id="3876d-112">由于没有 svc 文件，因此对于自承载的应用程序来说，此步骤不是必需的。</span><span class="sxs-lookup"><span data-stu-id="3876d-112">This step is not necessary for self-hosted applications, as there is no svc file.</span></span>  
  
```aspx-csharp
<%@ ServiceHost Service="WcfService.NewName">  
```  
  
## <a name="renaming-a-wcf-service-contract"></a><span data-ttu-id="3876d-113">重命名 WCF 服务协定</span><span class="sxs-lookup"><span data-stu-id="3876d-113">Renaming a WCF Service Contract</span></span>  
  
- <span data-ttu-id="3876d-114">若要重命名服务协定，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="3876d-114">Perform the following steps to rename the service contract,</span></span>  
  
- <span data-ttu-id="3876d-115">更改服务协定的名称。</span><span class="sxs-lookup"><span data-stu-id="3876d-115">Change the name of the service contract.</span></span>  
  
- <span data-ttu-id="3876d-116">在该服务的配置文件中，将服务协定的名称更改为选定的新名称，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="3876d-116">In the configuration file of the service, change the name of the service contract to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="3876d-117">配置文件可以是 app.config 或 web.config 文件，具体取决于宿主模型。</span><span class="sxs-lookup"><span data-stu-id="3876d-117">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service>  
         <endpoint contract="WcfService.NewContractName" />  
      </service>  
   </services>  
</system.servicemodel>  
```
