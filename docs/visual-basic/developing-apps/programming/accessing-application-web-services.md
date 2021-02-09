---
description: 详细了解：访问应用程序 Web 服务 (Visual Basic)
title: 访问应用程序 Web 服务
ms.date: 07/20/2015
helpviewer_keywords:
- Web services [Visual Basic], My.WebServices object
- My.WebServices object
- applications [Visual Basic], Web services
ms.assetid: 8ad5405b-e771-42b1-82d3-ce97af2cea9e
ms.openlocfilehash: 4efd35ed7c8f4251a749b85a45242af299a51e6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797882"
---
# <a name="accessing-application-web-services-visual-basic"></a><span data-ttu-id="96466-103">访问应用程序 Web 服务 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="96466-103">Accessing Application Web Services (Visual Basic)</span></span>

<span data-ttu-id="96466-104">`My.WebServices` 对象提供当前项目所引用的每个 Web 服务的实例。</span><span class="sxs-lookup"><span data-stu-id="96466-104">The `My.WebServices` object provides an instance of each Web service referenced by the current project.</span></span> <span data-ttu-id="96466-105">按需实例化每个实例。</span><span class="sxs-lookup"><span data-stu-id="96466-105">Each instance is instantiated on demand.</span></span> <span data-ttu-id="96466-106">可以通过 `My.WebServices` 对象的属性访问这些 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="96466-106">You can access these Web services through the properties of the `My.WebServices` object.</span></span> <span data-ttu-id="96466-107">该属性的名称与该属性所访问的 Web 服务的名称相同。</span><span class="sxs-lookup"><span data-stu-id="96466-107">The name of the property is the same as the name of the Web service that the property accesses.</span></span> <span data-ttu-id="96466-108">任何自 <xref:System.Web.Services.Protocols.SoapHttpClientProtocol> 继承的类均为 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="96466-108">Any class that inherits from <xref:System.Web.Services.Protocols.SoapHttpClientProtocol> is a Web service.</span></span>

## <a name="tasks"></a><span data-ttu-id="96466-109">任务</span><span class="sxs-lookup"><span data-stu-id="96466-109">Tasks</span></span>

<span data-ttu-id="96466-110">下表列出了访问应用程序所引用的 Web 服务的可能方法。</span><span class="sxs-lookup"><span data-stu-id="96466-110">The following table lists possible ways to access Web services referenced by an application.</span></span>

|<span data-ttu-id="96466-111">功能</span><span class="sxs-lookup"><span data-stu-id="96466-111">To</span></span>|<span data-ttu-id="96466-112">查看</span><span class="sxs-lookup"><span data-stu-id="96466-112">See</span></span>|
|---|---|
|<span data-ttu-id="96466-113">调用 Web 服务</span><span class="sxs-lookup"><span data-stu-id="96466-113">Call a Web service</span></span>|[<span data-ttu-id="96466-114">My.WebServices 对象</span><span class="sxs-lookup"><span data-stu-id="96466-114">My.WebServices Object</span></span>](../../language-reference/objects/my-webservices-object.md)|
|<span data-ttu-id="96466-115">以异步方式调用 Web 服务，并在事件完成时处理该事件</span><span class="sxs-lookup"><span data-stu-id="96466-115">Call a Web service asynchronously and handle an event when it completes</span></span>|[<span data-ttu-id="96466-116">如何：以异步方式调用 Web 服务</span><span class="sxs-lookup"><span data-stu-id="96466-116">How to: Call a Web Service Asynchronously</span></span>](how-to-call-a-web-service-asynchronously.md)|

## <a name="see-also"></a><span data-ttu-id="96466-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96466-117">See also</span></span>

- [<span data-ttu-id="96466-118">My.WebServices 对象</span><span class="sxs-lookup"><span data-stu-id="96466-118">My.WebServices Object</span></span>](../../language-reference/objects/my-webservices-object.md)
