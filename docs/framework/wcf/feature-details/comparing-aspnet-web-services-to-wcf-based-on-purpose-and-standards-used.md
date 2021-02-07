---
description: 了解详细信息：根据使用的用途和标准将 ASP.NET Web 服务与 WCF 进行比较
title: 基于目标和使用的标准比较 ASP.NET Web 服务与 WCF
ms.date: 03/30/2017
ms.assetid: d3890278-fa9b-4902-91ea-8da73b7143cc
ms.openlocfilehash: debc20f3ab3e8e9f83641eaa7d3b52dabe82055c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743442"
---
# <a name="comparing-aspnet-web-services-to-wcf-based-on-purpose-and-standards-used"></a><span data-ttu-id="25112-103">基于目标和使用的标准比较 ASP.NET Web 服务与 WCF</span><span class="sxs-lookup"><span data-stu-id="25112-103">Comparing ASP.NET Web Services to WCF Based on Purpose and Standards Used</span></span>

<span data-ttu-id="25112-104">开发 ASP.NET Web 服务的目标是生成通过使用 Simple Object Access Protocol (SOAP) over HTTP 来发送和接收消息的应用程序。</span><span class="sxs-lookup"><span data-stu-id="25112-104">ASP.NET Web services was developed for building applications that send and receive messages by using the Simple Object Access Protocol (SOAP) over HTTP.</span></span> <span data-ttu-id="25112-105">消息的结构可使用 XML 架构来定义，并且提供了一种工具，以便将消息序列化为 .NET Framework 对象以及将这种对象反序列化为消息。</span><span class="sxs-lookup"><span data-stu-id="25112-105">The structure of the messages can be defined using an XML Schema, and a tool is provided to facilitate serializing the messages to and from .NET Framework objects.</span></span> <span data-ttu-id="25112-106">该技术可以自动生成元数据，以便用 Web 服务描述语言 (WSDL) 描述 Web 服务，并且提供了另一个工具，用来从 WSDL 生成 Web 服务的客户端。</span><span class="sxs-lookup"><span data-stu-id="25112-106">The technology can automatically generate metadata to describe Web services in the Web Services Description Language (WSDL), and a second tool is provided for generating clients for Web services from the WSDL.</span></span>  
  
 <span data-ttu-id="25112-107">WCF 用于使 .NET Framework 的应用程序能够与其他软件实体交换消息。</span><span class="sxs-lookup"><span data-stu-id="25112-107">WCF is for enabling .NET Framework applications to exchange messages with other software entities.</span></span> <span data-ttu-id="25112-108">默认情况下使用 SOAP，但消息可采用任何格式，并可以使用任何传输协议传递。</span><span class="sxs-lookup"><span data-stu-id="25112-108">SOAP is used by default, but the messages can be in any format, and conveyed by using any transport protocol.</span></span> <span data-ttu-id="25112-109">消息的结构可使用 XML 架构来定义，并且提供多种选项以便将消息序列化为 .NET Framework 对象以及将这种对象反序列化为消息。</span><span class="sxs-lookup"><span data-stu-id="25112-109">The structure of the messages can be defined using an XML Schema, and there are various options for serializing the messages to and from .NET Framework objects.</span></span> <span data-ttu-id="25112-110">WCF 可以自动生成元数据来描述使用 WSDL 中的技术生成的应用程序，此外还提供了一个工具，用于为这些应用程序从 WSDL 生成客户端。</span><span class="sxs-lookup"><span data-stu-id="25112-110">WCF can automatically generate metadata to describe applications built using the technology in WSDL, and it also provides a tool for generating clients for those applications from the WSDL.</span></span>  
  
 <span data-ttu-id="25112-111">[使用 ASP.NET 创建的 XML Web services 的优点](/previous-versions/dotnet/netframework-4.0/0859ebft(v=vs.100))介绍了 ASP.NET Web 服务支持的标准。</span><span class="sxs-lookup"><span data-stu-id="25112-111">The standards supported by ASP.NET Web services are documented in [Benefits of XML Web Services Created Using ASP.NET](/previous-versions/dotnet/netframework-4.0/0859ebft(v=vs.100)).</span></span> <span data-ttu-id="25112-112">在 [System-Provided 互操作性绑定支持的 Web 服务协议](web-services-protocols-supported-by-system-provided-interoperability-bindings.md)中列出了 WCF 支持的更广泛的标准列表。</span><span class="sxs-lookup"><span data-stu-id="25112-112">The more extensive list of standards supported by WCF are listed at [Web Services Protocols Supported by System-Provided Interoperability Bindings](web-services-protocols-supported-by-system-provided-interoperability-bindings.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25112-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="25112-113">See also</span></span>

- [<span data-ttu-id="25112-114">从开发的角度比较 ASP.NET Web 服务与 WCF</span><span class="sxs-lookup"><span data-stu-id="25112-114">Comparing ASP.NET Web Services to WCF Based on Development</span></span>](comparing-aspnet-web-services-to-wcf-based-on-development.md)
