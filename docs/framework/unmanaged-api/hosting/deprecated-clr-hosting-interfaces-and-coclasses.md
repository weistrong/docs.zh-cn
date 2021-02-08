---
description: 了解更多：弃用的 CLR 承载接口和组件类
title: 弃用的 CLR 承载接口和 Coclass
ms.date: 03/30/2017
helpviewer_keywords:
- interfaces [.NET Framework hosting], version 1
- .NET Framework 1.1, hosting interfaces
- hosting interfaces [.NET Framework], version 1
- .NET Framework 1.0, hosting interfaces
ms.assetid: 7b3d2755-cbab-4160-bc69-eb85791e38c7
ms.openlocfilehash: 3d5e8d545dadb4f84c29e2e03a6b23e3729bfe66
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785635"
---
# <a name="deprecated-clr-hosting-interfaces-and-coclasses"></a><span data-ttu-id="32c7a-103">弃用的 CLR 承载接口和 Coclass</span><span class="sxs-lookup"><span data-stu-id="32c7a-103">Deprecated CLR Hosting Interfaces and Coclasses</span></span>

<span data-ttu-id="32c7a-104">本部分介绍了非托管主机可用于将 .NET Framework 版本1.0 和1.1 中的公共语言运行时 (CLR) 集成到其应用程序的接口。</span><span class="sxs-lookup"><span data-stu-id="32c7a-104">This section describes the interfaces that unmanaged hosts can use to integrate the common language runtime (CLR) in the .NET Framework versions 1.0 and 1.1 into their applications.</span></span> <span data-ttu-id="32c7a-105">这些接口为主机提供用于配置运行时并将其加载到进程中的方法。</span><span class="sxs-lookup"><span data-stu-id="32c7a-105">These interfaces provide methods for a host to configure and load the runtime into a process.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="32c7a-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="32c7a-106">In This Section</span></span>  

 <span data-ttu-id="32c7a-107">IAppDomainSetup</span><span class="sxs-lookup"><span data-stu-id="32c7a-107">IAppDomainSetup</span></span>  
 <span data-ttu-id="32c7a-108">为宿主提供用于配置的方法 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="32c7a-108">Provides methods for the host to configure an <xref:System.AppDomain>.</span></span>  
  
 [<span data-ttu-id="32c7a-109">ICeeFileGen 类</span><span class="sxs-lookup"><span data-stu-id="32c7a-109">ICeeFileGen Class</span></span>](iceefilegen-class.md)  
 <span data-ttu-id="32c7a-110"> (弃用) 提供用于创建本机可移植可执行文件 (PE) 文件的功能。</span><span class="sxs-lookup"><span data-stu-id="32c7a-110">(Deprecated) Provides functionality for creating a native portable executable (PE) file.</span></span>  
  
 [<span data-ttu-id="32c7a-111">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="32c7a-111">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)  
 <span data-ttu-id="32c7a-112">为宿主提供用于配置 CLR 设置的方法。</span><span class="sxs-lookup"><span data-stu-id="32c7a-112">Provides methods for the host to configure CLR settings.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="32c7a-113">相关章节</span><span class="sxs-lookup"><span data-stu-id="32c7a-113">Related Sections</span></span>  

 [<span data-ttu-id="32c7a-114">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="32c7a-114">CLR Hosting Interfaces</span></span>](clr-hosting-interfaces.md)  
 <span data-ttu-id="32c7a-115">包含描述随 .NET Framework 版本2.0 及更高版本一起提供的宿主接口的主题。</span><span class="sxs-lookup"><span data-stu-id="32c7a-115">Contains topics that describe the hosting interfaces provided with the .NET Framework version 2.0 and later versions.</span></span>
