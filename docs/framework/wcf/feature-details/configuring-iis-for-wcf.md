---
description: 了解详细信息：为 Windows Communication Foundation 配置 Internet Information Services 7。0
title: 为 Windows Communication Foundation 配置 Internet Information Services 7.0
ms.date: 03/30/2017
ms.assetid: 1050d395-092e-44d3-b4ba-66be3b039ffb
ms.openlocfilehash: e76918d70a922cb32c9bbacd5779aa4f8e991b2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743260"
---
# <a name="configuring-internet-information-services-70-for-windows-communication-foundation"></a><span data-ttu-id="80f6c-103">为 Windows Communication Foundation 配置 Internet Information Services 7.0</span><span class="sxs-lookup"><span data-stu-id="80f6c-103">Configuring Internet Information Services 7.0 for Windows Communication Foundation</span></span>

<span data-ttu-id="80f6c-104">Internet Information Services (IIS) 7.0 具有模块化设计，允许有选择地安装需要的组件。</span><span class="sxs-lookup"><span data-stu-id="80f6c-104">Internet Information Services (IIS) 7.0 has a modular design that allows you to selectively install components that are required.</span></span> <span data-ttu-id="80f6c-105">此设计基于 Windows Vista 中引入的新的清单驱动组件化技术。</span><span class="sxs-lookup"><span data-stu-id="80f6c-105">This design is based on the new manifest-driven componentization technology introduced in Windows Vista.</span></span> <span data-ttu-id="80f6c-106">IIS 7.0 的40多个独立功能组件可以独立安装。</span><span class="sxs-lookup"><span data-stu-id="80f6c-106">There are more than 40 standalone feature components of IIS 7.0 that can be installed independently.</span></span> <span data-ttu-id="80f6c-107">这使 IT 专业人士能够轻松地按需要自定义安装。</span><span class="sxs-lookup"><span data-stu-id="80f6c-107">This allows IT professionals to easily customize the installation as required.</span></span> <span data-ttu-id="80f6c-108">本主题讨论如何配置 IIS 7.0 以与 Windows Communication Foundation (WCF) 一起使用，并确定所需的组件。</span><span class="sxs-lookup"><span data-stu-id="80f6c-108">This topic discusses how to configure IIS 7.0 for use with Windows Communication Foundation (WCF) and determine which components are required.</span></span>

## <a name="minimal-installation-installing-was"></a><span data-ttu-id="80f6c-109">最小安装：安装 WAS</span><span class="sxs-lookup"><span data-stu-id="80f6c-109">Minimal Installation: Installing WAS</span></span>

 <span data-ttu-id="80f6c-110">整个 IIS 7.0 包的最小安装是安装) 的 Windows 进程激活服务 (。</span><span class="sxs-lookup"><span data-stu-id="80f6c-110">The minimal installation of the whole IIS 7.0 package is to install the Windows Process Activation Service (WAS).</span></span> <span data-ttu-id="80f6c-111">WAS 是一项独立功能，并且是 IIS 7.0 中唯一适用于所有 Windows Vista 操作系统的功能， (Home Basic、Home Premium、Business 和旗舰版和企业版) 。</span><span class="sxs-lookup"><span data-stu-id="80f6c-111">WAS is a standalone feature and it is the only feature from the IIS 7.0 that is available for all Windows Vista operating systems (Home Basic, Home Premium, Business, and Ultimate and Enterprise).</span></span>

 <span data-ttu-id="80f6c-112">在 "控制面板" 中，单击 "**程序**"，然后单击 "**程序和功能**" 下的 "**打开或关闭 Windows 功能**"，WAS 组件显示在列表中，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="80f6c-112">From the Control Panel, click **Programs** and then click **Turn Windows features on or off** which is listed under **Programs and Features**, the WAS component is shown in the list as in the following illustration.</span></span>

 <span data-ttu-id="80f6c-113">![打开或关闭功能对话框](media/wcfc-turnfeaturesonoroffs.gif "wcfc_TurnFeaturesOnOrOffs")</span><span class="sxs-lookup"><span data-stu-id="80f6c-113">![Turn Features On or Off Dialog](media/wcfc-turnfeaturesonoroffs.gif "wcfc_TurnFeaturesOnOrOffs")</span></span>

 <span data-ttu-id="80f6c-114">此功能具有下列子组件：</span><span class="sxs-lookup"><span data-stu-id="80f6c-114">This feature has the following sub-components:</span></span>

- <span data-ttu-id="80f6c-115">.NET 环境</span><span class="sxs-lookup"><span data-stu-id="80f6c-115">.NET Environment</span></span>

- <span data-ttu-id="80f6c-116">配置 API</span><span class="sxs-lookup"><span data-stu-id="80f6c-116">Configuration APIs</span></span>

- <span data-ttu-id="80f6c-117">进程模型</span><span class="sxs-lookup"><span data-stu-id="80f6c-117">Process Model</span></span>

 <span data-ttu-id="80f6c-118">如果选择的根节点为，则默认情况下仅检查 " **进程模型** " 子节点。</span><span class="sxs-lookup"><span data-stu-id="80f6c-118">If you select the root node of WAS, only the **Process Model** sub-node is checked by default.</span></span> <span data-ttu-id="80f6c-119">请注意，使用此安装时，你将只安装 WAS，因为没有用于 Web 服务器的支持功能。</span><span class="sxs-lookup"><span data-stu-id="80f6c-119">Please note that with this installation you are only installing WAS, because there is no support for a Web server.</span></span>

 <span data-ttu-id="80f6c-120">若要使 WCF 或任何 ASP.NET 应用程序正常工作，请选中 " **.Net 环境** " 复选框。</span><span class="sxs-lookup"><span data-stu-id="80f6c-120">To make WCF or any ASP.NET application work, check the **.NET Environment** checkbox.</span></span> <span data-ttu-id="80f6c-121">这意味着，所有 WAS 组件都需要使 WCF 和 ASP.NET 能够正常运行。</span><span class="sxs-lookup"><span data-stu-id="80f6c-121">This means that all of WAS components are required to make WCF and ASP.NET to work well.</span></span> <span data-ttu-id="80f6c-122">您安装其中任何组件后，会自动选中这些组件。</span><span class="sxs-lookup"><span data-stu-id="80f6c-122">These are automatically checked once you install any of those components.</span></span>

## <a name="iis-70-default-installation"></a><span data-ttu-id="80f6c-123">IIS 7.0：默认安装</span><span class="sxs-lookup"><span data-stu-id="80f6c-123">IIS 7.0: Default Installation</span></span>

 <span data-ttu-id="80f6c-124">通过检查 **Internet Information Services** 功能，会自动检查某些子节点，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="80f6c-124">By checking the **Internet Information Services** feature, some of the sub-nodes are automatically checked as shown in the following illustration.</span></span>

 <span data-ttu-id="80f6c-125">![IIS 7.0 功能的默认设置](media/wcfc-turningfeaturesonoroff2.gif "wcfc_TurningFeaturesOnOrOff2")</span><span class="sxs-lookup"><span data-stu-id="80f6c-125">![Default settings for IIS 7.0 features](media/wcfc-turningfeaturesonoroff2.gif "wcfc_TurningFeaturesOnOrOff2")</span></span>

 <span data-ttu-id="80f6c-126">这是 IIS 7.0 的默认安装。</span><span class="sxs-lookup"><span data-stu-id="80f6c-126">This is the default installation of IIS 7.0.</span></span> <span data-ttu-id="80f6c-127">使用此安装，你可以使用 IIS 7.0 来为静态内容提供服务 (如 HTML 页面和其他内容) 。</span><span class="sxs-lookup"><span data-stu-id="80f6c-127">With this installation, you can use IIS 7.0 to service static content (such as HTML pages and other content).</span></span> <span data-ttu-id="80f6c-128">但是，不能运行 ASP.NET 或 CGI 应用程序，也不能托管 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="80f6c-128">However, you cannot run ASP.NET or CGI applications or host WCF services.</span></span>

## <a name="iis-70-installation-with-aspnet-support"></a><span data-ttu-id="80f6c-129">IIS 7.0：带 ASP.NET 支持的安装</span><span class="sxs-lookup"><span data-stu-id="80f6c-129">IIS 7.0: Installation with ASP.NET Support</span></span>

 <span data-ttu-id="80f6c-130">必须安装 ASP.NET 才能在 IIS 7.0 上进行 ASP.NET 工作。</span><span class="sxs-lookup"><span data-stu-id="80f6c-130">You must install ASP.NET to make ASP.NET work on IIS 7.0.</span></span> <span data-ttu-id="80f6c-131">检查 **ASP.NET** 后，屏幕应如下图所示。</span><span class="sxs-lookup"><span data-stu-id="80f6c-131">After checking **ASP.NET**, your screen should look like the following illustration.</span></span>

 <span data-ttu-id="80f6c-132">![Asp.NET 需要的设置](media/wcfc-trunfeaturesonoroff3s.gif "wcfc_TrunFeaturesOnOrOFf3s")</span><span class="sxs-lookup"><span data-stu-id="80f6c-132">![Asp.NET required settings](media/wcfc-trunfeaturesonoroff3s.gif "wcfc_TrunFeaturesOnOrOFf3s")</span></span>

 <span data-ttu-id="80f6c-133">这是 WCF 和 ASP.NET 应用程序在 IIS 7.0 中工作的最小环境。</span><span class="sxs-lookup"><span data-stu-id="80f6c-133">This is the minimal environment for both WCF and ASP.NET applications to work in IIS 7.0.</span></span>

## <a name="iis-70-installation-with-iis-60-compatibility-components"></a><span data-ttu-id="80f6c-134">IIS 7.0：带 IIS 6.0 兼容组件的安装</span><span class="sxs-lookup"><span data-stu-id="80f6c-134">IIS 7.0: Installation with IIS 6.0 Compatibility Components</span></span>

 <span data-ttu-id="80f6c-135">当使用 Visual Studio 2005 或其他一些自动化脚本或工具在系统上安装 IIS 7.0 时 (例如 Adsutil.vbs) 配置使用 IIS 6.0 元数据库 API 的虚拟应用程序时，请确保检查 IIS 6.0 **脚本编写工具**。</span><span class="sxs-lookup"><span data-stu-id="80f6c-135">When installing IIS 7.0 on a system with Visual Studio 2005 or some other automation scripts or tools (such as Adsutil.vbs) that configure virtual applications that use IIS 6.0 Metabase API, ensure that you check the IIS 6.0 **Scripting Tools**.</span></span> <span data-ttu-id="80f6c-136">这会自动检查 IIS 6.0 **管理兼容性** 的其他子节点。</span><span class="sxs-lookup"><span data-stu-id="80f6c-136">This automatically checks the other sub-nodes of IIS 6.0 **Management Compatibility**.</span></span> <span data-ttu-id="80f6c-137">下图显示了完成此操作后的屏幕：</span><span class="sxs-lookup"><span data-stu-id="80f6c-137">The following illustration shows the screen after this is done:</span></span>

 <span data-ttu-id="80f6c-138">![IIS 6.0 管理兼容性设置](media/scfc-turnfeaturesonoroff5s.gif "scfc_TurnFeaturesOnOrOff5s")</span><span class="sxs-lookup"><span data-stu-id="80f6c-138">![IIS 6.0 Management Compatibility Settings](media/scfc-turnfeaturesonoroff5s.gif "scfc_TurnFeaturesOnOrOff5s")</span></span>

 <span data-ttu-id="80f6c-139">通过此安装，你可以使用 Web 上提供的 IIS 7.0、ASP.NET 和 WCF 功能和示例所需的一切。</span><span class="sxs-lookup"><span data-stu-id="80f6c-139">With this installation, you have everything required to use IIS 7.0, ASP.NET and WCF features and samples available on the Web.</span></span>

## <a name="request-limits"></a><span data-ttu-id="80f6c-140">请求限制</span><span class="sxs-lookup"><span data-stu-id="80f6c-140">Request Limits</span></span>

 <span data-ttu-id="80f6c-141">在带有 IIS 7 的 Windows Vista 上，和设置的默认值已 `maxUri` `maxQueryStringSize` 更改。</span><span class="sxs-lookup"><span data-stu-id="80f6c-141">On Windows Vista with IIS 7 the default value of the `maxUri` and `maxQueryStringSize` settings have been changed.</span></span> <span data-ttu-id="80f6c-142">默认情况下，IIS 7.0 中的请求筛选功能允许 URL 的长度为 4096 个字符，查询字符串的长度为 2048 个字符。</span><span class="sxs-lookup"><span data-stu-id="80f6c-142">By default, request filtering in IIS 7.0 allows a URL length of 4096 characters and a query string length of 2048 characters.</span></span> <span data-ttu-id="80f6c-143">更改这些默认值，可将以下 XML 添加到 App.config 文件中。</span><span class="sxs-lookup"><span data-stu-id="80f6c-143">To change these defaults add the following XML to your App.config file.</span></span>

```xml
 <system.webServer>
    <security>
        <requestFiltering>
            <requestLimits maxUrl="8192" maxQueryString="8192" />
        </requestFiltering>
    </security>
 </system.webServer>
 ```

## <a name="see-also"></a><span data-ttu-id="80f6c-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="80f6c-144">See also</span></span>

- [<span data-ttu-id="80f6c-145">WAS 激活体系结构</span><span class="sxs-lookup"><span data-stu-id="80f6c-145">WAS Activation Architecture</span></span>](was-activation-architecture.md)
- [<span data-ttu-id="80f6c-146">配置 WAS 以用于 WCF</span><span class="sxs-lookup"><span data-stu-id="80f6c-146">Configuring WAS for Use with WCF</span></span>](configuring-the-wpa--service-for-use-with-wcf.md)
- [<span data-ttu-id="80f6c-147">如何：安装和配置 WCF 激活组件</span><span class="sxs-lookup"><span data-stu-id="80f6c-147">How to: Install and Configure WCF Activation Components</span></span>](how-to-install-and-configure-wcf-activation-components.md)
- <span data-ttu-id="80f6c-148">[Windows Server App Fabric 承载功能](/previous-versions/appfabric/ee677189(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="80f6c-148">[Windows Server App Fabric Hosting Features](/previous-versions/appfabric/ee677189(v=azure.10))</span></span>
