---
description: 了解详细信息：部分信任
title: 部分信任
ms.date: 03/30/2017
ms.assetid: 489b1587-9909-4d0e-8c1a-5e83c8f8292b
ms.openlocfilehash: 89d714a57c4662958689e536b7bff2d0bfd67e2b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733510"
---
# <a name="partial-trust"></a><span data-ttu-id="a5e84-103">部分信任</span><span class="sxs-lookup"><span data-stu-id="a5e84-103">Partial Trust</span></span>

<span data-ttu-id="a5e84-104">从 .NET Framework 3.5 开始，部分受信任的调用方可以访问在、和中实现的公共类型和方法 <xref:System.ServiceModel> <xref:System.Runtime.Serialization> <xref:System.ServiceModel.Web> 。</span><span class="sxs-lookup"><span data-stu-id="a5e84-104">Starting with the .NET Framework 3.5, partially trusted callers can access public types and methods implemented in <xref:System.ServiceModel>, <xref:System.Runtime.Serialization>, and <xref:System.ServiceModel.Web>.</span></span> <span data-ttu-id="a5e84-105">本部分介绍了在部分受信任的应用程序中使用 Windows Communication Foundation (WCF) 的受支持方案，以及使用降低了代码访问安全 (CA) 权限的应用程序可使用的 WCF 功能的有限子集。</span><span class="sxs-lookup"><span data-stu-id="a5e84-105">This section describes supported scenarios for using Windows Communication Foundation (WCF) within a partially trusted application as well as the limited subset of WCF functionality available to applications running with reduced code access security (CAS) permissions.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a5e84-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="a5e84-106">In This Section</span></span>  

 [<span data-ttu-id="a5e84-107">支持的部署方案</span><span class="sxs-lookup"><span data-stu-id="a5e84-107">Supported Deployment Scenarios</span></span>](supported-deployment-scenarios.md)  
 <span data-ttu-id="a5e84-108">介绍运行 WCF 的主要部分信任方案。</span><span class="sxs-lookup"><span data-stu-id="a5e84-108">Describes the main partial trust scenarios for running WCF.</span></span>  
  
 [<span data-ttu-id="a5e84-109">部分信任功能兼容性</span><span class="sxs-lookup"><span data-stu-id="a5e84-109">Partial Trust Feature Compatibility</span></span>](partial-trust-feature-compatibility.md)  
 <span data-ttu-id="a5e84-110">介绍不能用于部分信任的 WCF 功能。</span><span class="sxs-lookup"><span data-stu-id="a5e84-110">Describes the WCF features that cannot be used with partial trust.</span></span>  
  
 [<span data-ttu-id="a5e84-111">部分信任最佳实践</span><span class="sxs-lookup"><span data-stu-id="a5e84-111">Partial Trust Best Practices</span></span>](partial-trust-best-practices.md)  
 <span data-ttu-id="a5e84-112">包含在部分受信任的应用程序中使用 WCF 的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="a5e84-112">Contains best practices for using WCF in partially trusted applications.</span></span>
