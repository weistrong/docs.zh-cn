---
description: 了解详细信息：与 COM 应用程序集成
title: 与 COM 应用程序集成
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Communication Foundation, COM integration
- COM [WCF], Windows Communication Foundation integration
- WCF, reusing code
- Windows Communication Foundation, reusing code
- COM [WCF]
- WCF, COM integration
ms.assetid: c98bda3e-6779-419e-8e6d-9aa94053026d
ms.openlocfilehash: 7afee4bed334d7f392b73773f0981022a59170fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802796"
---
# <a name="integrating-with-com-applications"></a><span data-ttu-id="9df18-103">与 COM 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="9df18-103">Integrating with COM Applications</span></span>

<span data-ttu-id="9df18-104">Windows Communication Foundation (WCF) 服务可以使用 WCF 服务名字对象直接集成到现有代码中。</span><span class="sxs-lookup"><span data-stu-id="9df18-104">Windows Communication Foundation (WCF) services can be integrated directly into your existing code by using the WCF service moniker.</span></span> <span data-ttu-id="9df18-105">服务标记可以在众多基于 COM 的开发环境（如 Office VBA、Visual Basic 6.0 或 Visual C++ 6.0）中使用。</span><span class="sxs-lookup"><span data-stu-id="9df18-105">The service moniker can be used from a wide range of COM-based development environments, such as Office VBA, Visual Basic 6.0, or Visual C++ 6.0.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9df18-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="9df18-106">In This Section</span></span>  

 [<span data-ttu-id="9df18-107">COM 应用程序集成概述</span><span class="sxs-lookup"><span data-stu-id="9df18-107">Integrating with COM Applications Overview</span></span>](integrating-with-com-applications-overview.md)  
 <span data-ttu-id="9df18-108">对集成过程的主要部分进行概述。</span><span class="sxs-lookup"><span data-stu-id="9df18-108">Gives an overview of the major parts of the integration process.</span></span>  
  
 [<span data-ttu-id="9df18-109">如何：注册和配置服务名字对象</span><span class="sxs-lookup"><span data-stu-id="9df18-109">How to: Register and Configure a Service Moniker</span></span>](how-to-register-and-configure-a-service-moniker.md)  
 <span data-ttu-id="9df18-110">若要在 COM 应用程序中使用 WCF 服务标记，请将所需的属性化类型注册到 COM，并使用所需的绑定配置来配置 COM 应用程序和标记。</span><span class="sxs-lookup"><span data-stu-id="9df18-110">To use the WCF service moniker within a COM application, register the required attributed types with COM, and configure the COM application and the moniker with the required binding configuration.</span></span>  
  
 [<span data-ttu-id="9df18-111">如何：使用未注册的 Windows Communication Foundation 服务名字对象</span><span class="sxs-lookup"><span data-stu-id="9df18-111">How to: Use the Windows Communication Foundation Service Moniker without Registration</span></span>](use-the-wcf-service-moniker-without-registration.md)  
 <span data-ttu-id="9df18-112">说明如何以 Web 服务定义语言 (WSDL) 文档的形式或者从 WS-MetadataExchange 终结点获取协定的定义。</span><span class="sxs-lookup"><span data-stu-id="9df18-112">Explains how to obtain the definition of the contract in the form of a Web Services Definition Language (WSDL) document or from a WS-MetadataExchange endpoint.</span></span>  
  
 [<span data-ttu-id="9df18-113">如何：将服务名字对象用于 WSDL 协定</span><span class="sxs-lookup"><span data-stu-id="9df18-113">How to: Use a Service Moniker with WSDL Contracts</span></span>](how-to-use-a-service-moniker-with-wsdl-contracts.md)  
 <span data-ttu-id="9df18-114">介绍如何使用 WCF WSDL 名字对象调用 WCF 示例。</span><span class="sxs-lookup"><span data-stu-id="9df18-114">Describes how to call a WCF sample using a WCF WSDL moniker.</span></span>  
  
 [<span data-ttu-id="9df18-115">如何：将服务名字对象与元数据交换协定一起使用</span><span class="sxs-lookup"><span data-stu-id="9df18-115">How to: Use a Service Moniker with Metadata Exchange Contracts</span></span>](how-to-use-a-service-moniker-with-metadata-exchange-contracts.md)  
 <span data-ttu-id="9df18-116">介绍如何使用指定 Mex 终结点的 WCF 名字对象调用 WCF 示例。</span><span class="sxs-lookup"><span data-stu-id="9df18-116">Describes how to call a WCF sample using a WCF moniker that specifies a Mex endpoint.</span></span>  
  
 [<span data-ttu-id="9df18-117">如何：指定通道安全凭据</span><span class="sxs-lookup"><span data-stu-id="9df18-117">How to: Specify Channel Security Credentials</span></span>](how-to-specify-channel-security-credentials.md)  
 <span data-ttu-id="9df18-118">WCF 服务标记支持 `IChannelCredentials` 接口，该接口允许使用一系列替代方法来指定通道凭据。</span><span class="sxs-lookup"><span data-stu-id="9df18-118">The WCF service moniker supports the `IChannelCredentials` interface that allows a range of alternate methods for specifying channel credentials.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="9df18-119">参考</span><span class="sxs-lookup"><span data-stu-id="9df18-119">Reference</span></span>  

 <xref:System.ServiceModel>  
  
## <a name="see-also"></a><span data-ttu-id="9df18-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="9df18-120">See also</span></span>

- [<span data-ttu-id="9df18-121">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="9df18-121">Integrating with COM+ Applications</span></span>](integrating-with-com-plus-applications.md)
