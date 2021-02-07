---
description: 了解详细信息： <serviceActivations>
title: <serviceActivations>
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 726514af4e42cc387daf61b688d528f690ec8ee8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683016"
---
# \<serviceActivations>

<span data-ttu-id="e5f97-102">一个配置元素，允许您添加用于定义虚拟服务激活设置的设置，这些设置将映射到 Windows Communication Foundation (WCF) 服务类型。</span><span class="sxs-lookup"><span data-stu-id="e5f97-102">A configuration element that allows you to add settings that define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="e5f97-103">使用此配置元素可以在不使用 .svc 文件的情况下激活承载在 WAS/IIS 中的服务。</span><span class="sxs-lookup"><span data-stu-id="e5f97-103">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceActivations>**  

## <a name="syntax"></a><span data-ttu-id="e5f97-104">语法</span><span class="sxs-lookup"><span data-stu-id="e5f97-104">Syntax</span></span>

```xml
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e5f97-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e5f97-105">Attributes and Elements</span></span>

<span data-ttu-id="e5f97-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e5f97-106">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="e5f97-107">特性</span><span class="sxs-lookup"><span data-stu-id="e5f97-107">Attributes</span></span>

<span data-ttu-id="e5f97-108">无。</span><span class="sxs-lookup"><span data-stu-id="e5f97-108">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="e5f97-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e5f97-109">Child Elements</span></span>

|<span data-ttu-id="e5f97-110">元素</span><span class="sxs-lookup"><span data-stu-id="e5f97-110">Element</span></span>|<span data-ttu-id="e5f97-111">说明</span><span class="sxs-lookup"><span data-stu-id="e5f97-111">Description</span></span>|
|-------------|-----------------|
|[\<add>](add-of-serviceactivations.md)|<span data-ttu-id="e5f97-112">添加一个指定激活服务应用程序的配置元素。</span><span class="sxs-lookup"><span data-stu-id="e5f97-112">Adds a configuration element that specifies the activation of a service application.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="e5f97-113">父元素</span><span class="sxs-lookup"><span data-stu-id="e5f97-113">Parent Elements</span></span>

|<span data-ttu-id="e5f97-114">元素</span><span class="sxs-lookup"><span data-stu-id="e5f97-114">Element</span></span>|<span data-ttu-id="e5f97-115">说明</span><span class="sxs-lookup"><span data-stu-id="e5f97-115">Description</span></span>|
|-------------|-----------------|
|[\<serviceHostingEnvironment>](servicehostingenvironment.md)|<span data-ttu-id="e5f97-116">定义服务承载环境要为特定传输实例化的类型。</span><span class="sxs-lookup"><span data-stu-id="e5f97-116">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e5f97-117">备注</span><span class="sxs-lookup"><span data-stu-id="e5f97-117">Remarks</span></span>

<span data-ttu-id="e5f97-118">下面的示例演示如何在 web.config 文件中配置激活设置。</span><span class="sxs-lookup"><span data-stu-id="e5f97-118">The following example shows how to configure activation settings within your web.config file.</span></span>

```xml
<configuration>
  <system.serviceModel>
    <serviceHostingEnvironment>
      <serviceActivations>
        <add service="GreetingService" />
      </serviceActivations>
    </serviceHostingEnvironment>
  </system.serviceModel>
</configuration>
```

<span data-ttu-id="e5f97-119">使用此配置，您可以在不使用 .svc 文件的情况下激活 GreetingService。</span><span class="sxs-lookup"><span data-stu-id="e5f97-119">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>

<span data-ttu-id="e5f97-120">请注意，`<serviceHostingEnvironment>` 是应用程序级配置。</span><span class="sxs-lookup"><span data-stu-id="e5f97-120">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="e5f97-121">必须将包含此配置的 `web.config` 放置到虚拟应用程序的根目录下。</span><span class="sxs-lookup"><span data-stu-id="e5f97-121">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="e5f97-122">此外， `serviceHostingEnvironment` 是 machineToApplication 可继承部分。</span><span class="sxs-lookup"><span data-stu-id="e5f97-122">In addition, `serviceHostingEnvironment` is a machineToApplication inheritable section.</span></span> <span data-ttu-id="e5f97-123">如果在计算机的根目录中注册了一个服务，应用程序中的每个服务都将继承此服务。</span><span class="sxs-lookup"><span data-stu-id="e5f97-123">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>

<span data-ttu-id="e5f97-124">基于配置的激活支持通过 http 协议和非 http 协议进行激活。</span><span class="sxs-lookup"><span data-stu-id="e5f97-124">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="e5f97-125">它需要 relativeAddress 中的扩展，如 xoml 或 .xamlx。</span><span class="sxs-lookup"><span data-stu-id="e5f97-125">It requires extensions in the relativeAddress i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="e5f97-126">您可以将自己的扩展名映射到已知的 buildProviders，然后就可以通过任意扩展名激活服务。</span><span class="sxs-lookup"><span data-stu-id="e5f97-126">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="e5f97-127">如果发生冲突，`<serviceActivations>` 节将重写 .svc 注册。</span><span class="sxs-lookup"><span data-stu-id="e5f97-127">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5f97-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5f97-128">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
