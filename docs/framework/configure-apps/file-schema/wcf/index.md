---
description: 了解详细信息： WCF 配置架构
title: WCF 配置架构
ms.date: 03/30/2017
ms.assetid: c282aeb5-91f0-4522-8e2f-704c1ef3651f
ms.openlocfilehash: 31307fd299cc1e0b63d92b43b33aabafa28858f0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725761"
---
# <a name="wcf-configuration-schema"></a><span data-ttu-id="5fc8d-103">WCF 配置架构</span><span class="sxs-lookup"><span data-stu-id="5fc8d-103">WCF Configuration Schema</span></span>

<span data-ttu-id="5fc8d-104">Windows Communication Foundation (WCF) 配置元素，你可以配置 WCF 服务和客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-104">Windows Communication Foundation (WCF) configuration elements enable you to configure WCF service and client applications.</span></span> <span data-ttu-id="5fc8d-105">可以使用[配置编辑器工具 (SvcConfigEditor.exe)](../../../wcf/configuration-editor-tool-svcconfigeditor-exe.md) 创建和修改客户端和服务的配置文件。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-105">You can use the [Configuration Editor Tool (SvcConfigEditor.exe)](../../../wcf/configuration-editor-tool-svcconfigeditor-exe.md) to create and modify configuration files for clients and services.</span></span> <span data-ttu-id="5fc8d-106">由于配置文件的格式都是以 XML 形式设置的，因此，如果要使用文本编辑器手动编辑这些文件，则您必须熟悉 XML。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-106">Since the configuration files are formatted as XML, you must be familiar with XML if you want to manually edit them using a text editor.</span></span> <span data-ttu-id="5fc8d-107">否则，您可能会遇到一些问题，如找不到某个 XML 元素标记或特性。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-107">Otherwise, you may run into issues such as an unfound XML element tag or attribute.</span></span> <span data-ttu-id="5fc8d-108">这是因为 XML 元素标记和特性是区分大小写的。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-108">This is because XML element tags and attributes are case-sensitive.</span></span>  
  
 <span data-ttu-id="5fc8d-109">WCF 配置系统基于 <xref:System.Configuration> 命名空间。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-109">The WCF configuration system is based on the <xref:System.Configuration> namespace.</span></span> <span data-ttu-id="5fc8d-110">因此，您可以使用 <xref:System.Configuration> 命名空间提供的所有标准功能（如配置锁定、加密和合并）以提高应用程序及其配置的安全性。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-110">Therefore, you can use all the standard features provided by the <xref:System.Configuration> namespace, such as configuration locking, encryption and merging to increase the security of your application and its configuration.</span></span> <span data-ttu-id="5fc8d-111">有关这些概念的更多信息，请参见下列主题。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-111">For more information on these concepts, see the following topics.</span></span>  
  
 <span data-ttu-id="5fc8d-112">[加密配置信息](/previous-versions/aspnet/53tyfkaw(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5fc8d-112">[Encrypting Configuration Information](/previous-versions/aspnet/53tyfkaw(v=vs.100))</span></span>  
  
 <span data-ttu-id="5fc8d-113">[锁定配置设置](/previous-versions/aspnet/55th21y4(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5fc8d-113">[Locking Configuration Settings](/previous-versions/aspnet/55th21y4(v=vs.100))</span></span>  
  
 <span data-ttu-id="5fc8d-114">本节描述每个配置项的所有可能的值，以及它如何与其他 WCF 配置元素进行交互。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-114">This section describes all possible values of each configuration item, and how it interacts with other WCF configuration elements.</span></span> <span data-ttu-id="5fc8d-115">下图说明了 WCF 配置架构：</span><span class="sxs-lookup"><span data-stu-id="5fc8d-115">The following map illustrates the WCF configuration schema:</span></span>

:::image type="content" source="./media/index/windows-communication-foundation-configuration-schema.gif" alt-text="显示 WCF 配置架构的关系图。" lightbox="./media/index/windows-communication-foundation-configuration-schema.gif":::
  
> [!CAUTION]
> <span data-ttu-id="5fc8d-117">使用适当的访问控制)  (列表 ( # A0) 保护应用程序配置文件中的 WCF 配置节，以避免任何潜在的安全威胁。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-117">Protect WCF configuration sections in your application configuration files (app.config) with appropriate Access Control Lists (ACL) to prevent any potential security threats.</span></span> <span data-ttu-id="5fc8d-118">例如，确保只有适当的人员可以访问或修改应用程序绑定的安全设置或服务的配置文件的服务模型部分。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-118">For example, make sure that only the appropriate people can access or modify the security settings on application bindings, or the service model section of the configuration file for a service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5fc8d-119">本节内容</span><span class="sxs-lookup"><span data-stu-id="5fc8d-119">In This Section</span></span>  

 [\<system.serviceModel>](system-servicemodel.md)  
 <span data-ttu-id="5fc8d-120">描述 `ServiceModel` 元素。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-120">Describes the `ServiceModel` element.</span></span>  
  
 [\<system.serviceModel.activation>](system-servicemodel-activation.md)  
 <span data-ttu-id="5fc8d-121">配置 SMSvcHost.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-121">Configures the SMSvcHost.exe tool.</span></span>  
  
 [\<system.runtime.serialization>](system-runtime-serialization.md)  
 <span data-ttu-id="5fc8d-122">当使用序列化程序（如 <xref:System.Runtime.Serialization.DataContractSerializer>）时，用于设置选项的顶级元素。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-122">The top-level element for setting options when using serializers such as the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="5fc8d-123">相关章节</span><span class="sxs-lookup"><span data-stu-id="5fc8d-123">Related Sections</span></span>  

 [<span data-ttu-id="5fc8d-124">配置 Windows Communication Foundation 应用程序</span><span class="sxs-lookup"><span data-stu-id="5fc8d-124">Configuring Windows Communication Foundation Applications</span></span>](../../../wcf/configuring-services.md)  
 <span data-ttu-id="5fc8d-125">介绍如何配置 WCF 服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="5fc8d-125">Describes how to configure WCF services and clients.</span></span>
