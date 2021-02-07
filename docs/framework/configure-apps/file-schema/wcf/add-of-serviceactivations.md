---
description: 了解详细 <add> 信息： <serviceActivations>
title: <add> 的 <serviceActivations>
ms.date: 03/30/2017
ms.assetid: e5b01fc8-ee84-48b7-95fd-95ab54fa871f
ms.openlocfilehash: 53c89321c8cde1966a04870c62fa0777610ff547
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750138"
---
# <a name="add-of-serviceactivations"></a><span data-ttu-id="33139-103">\<add> 的 \<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="33139-103">\<add> of \<serviceActivations></span></span>

<span data-ttu-id="33139-104">一个配置元素，可用于定义虚拟服务激活设置，这些设置映射到 Windows Communication Foundation (WCF) 服务类型。</span><span class="sxs-lookup"><span data-stu-id="33139-104">A configuration element that allows you to define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="33139-105">使用此配置元素可以在不使用 .svc 文件的情况下激活承载在 WAS/IIS 中的服务。</span><span class="sxs-lookup"><span data-stu-id="33139-105">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceActivations>**](serviceactivations.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  

## <a name="syntax"></a><span data-ttu-id="33139-106">语法</span><span class="sxs-lookup"><span data-stu-id="33139-106">Syntax</span></span>

```xml
<serviceHostingEnvironment>
    <serviceActivations>
      <add factory="String"
           service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="33139-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="33139-107">Attributes and Elements</span></span>

<span data-ttu-id="33139-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33139-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="33139-109">特性</span><span class="sxs-lookup"><span data-stu-id="33139-109">Attributes</span></span>

|<span data-ttu-id="33139-110">属性</span><span class="sxs-lookup"><span data-stu-id="33139-110">Attribute</span></span>|<span data-ttu-id="33139-111">说明</span><span class="sxs-lookup"><span data-stu-id="33139-111">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="33139-112">工厂</span><span class="sxs-lookup"><span data-stu-id="33139-112">factory</span></span>|<span data-ttu-id="33139-113">一个字符串，指定生成服务激活元素的工厂的 CLR 类型名称。</span><span class="sxs-lookup"><span data-stu-id="33139-113">A string that specifies the CLR type name of the factory that generates a service activation element.</span></span>|
|<span data-ttu-id="33139-114">服务</span><span class="sxs-lookup"><span data-stu-id="33139-114">service</span></span>|<span data-ttu-id="33139-115">实现服务的 ServiceType（完全限定的 Typename 或短的 Typename（将它置于 App_Code 文件夹中时））。</span><span class="sxs-lookup"><span data-stu-id="33139-115">The ServiceType that implements the service (either the full qualified Typename or the short Typename (when it is placed in the App_Code folder).</span></span>|
|<span data-ttu-id="33139-116">relativeAddress</span><span class="sxs-lookup"><span data-stu-id="33139-116">relativeAddress</span></span>|<span data-ttu-id="33139-117">当前 IIS 应用程序内的相对地址，例如“Service.svc”。</span><span class="sxs-lookup"><span data-stu-id="33139-117">The relative address within the current IIS application - for example "Service.svc".</span></span> <span data-ttu-id="33139-118">在 WCF 4.0 中，此相对地址必须包含一个已知文件扩展名 ( .xamlx，... ) 。RelativeUrl 不存在物理文件</span><span class="sxs-lookup"><span data-stu-id="33139-118">In WCF 4.0 this relative address has to contain one of the known file extensions (.svc, .xamlx, ...). No physical file has to exist for the relativeUrl</span></span>|

### <a name="child-elements"></a><span data-ttu-id="33139-119">子元素</span><span class="sxs-lookup"><span data-stu-id="33139-119">Child Elements</span></span>

<span data-ttu-id="33139-120">无。</span><span class="sxs-lookup"><span data-stu-id="33139-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="33139-121">父元素</span><span class="sxs-lookup"><span data-stu-id="33139-121">Parent Elements</span></span>

|<span data-ttu-id="33139-122">元素</span><span class="sxs-lookup"><span data-stu-id="33139-122">Element</span></span>|<span data-ttu-id="33139-123">说明</span><span class="sxs-lookup"><span data-stu-id="33139-123">Description</span></span>|
|-------------|-----------------|
|[\<serviceHostingEnvironment>](servicehostingenvironment.md)|<span data-ttu-id="33139-124">一个描述激活设置的配置节。</span><span class="sxs-lookup"><span data-stu-id="33139-124">A configuration section that describes activation settings.</span></span>|

## <a name="remarks"></a><span data-ttu-id="33139-125">备注</span><span class="sxs-lookup"><span data-stu-id="33139-125">Remarks</span></span>

<span data-ttu-id="33139-126">下面的示例演示如何在 web.config 文件中配置激活设置。</span><span class="sxs-lookup"><span data-stu-id="33139-126">The following example shows how to configure activation settings within your web.config file.</span></span>

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

<span data-ttu-id="33139-127">使用此配置，您可以在不使用 .svc 文件的情况下激活 GreetingService。</span><span class="sxs-lookup"><span data-stu-id="33139-127">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>

<span data-ttu-id="33139-128">请注意，`<serviceHostingEnvironment>` 是应用程序级配置。</span><span class="sxs-lookup"><span data-stu-id="33139-128">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="33139-129">必须将包含此配置的 `web.config` 放置到虚拟应用程序的根目录下。</span><span class="sxs-lookup"><span data-stu-id="33139-129">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="33139-130">此外， `serviceHostingEnvironment` 是 machineToApplication 可继承部分。</span><span class="sxs-lookup"><span data-stu-id="33139-130">In addition, `serviceHostingEnvironment` is a machineToApplication inheritable section.</span></span> <span data-ttu-id="33139-131">如果在计算机的根目录中注册了一个服务，应用程序中的每个服务都将继承此服务。</span><span class="sxs-lookup"><span data-stu-id="33139-131">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>

<span data-ttu-id="33139-132">基于配置的激活支持通过 http 协议和非 http 协议进行激活。</span><span class="sxs-lookup"><span data-stu-id="33139-132">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="33139-133">它需要 relativeAddress 中的扩展，即 xoml 或 .xamlx。</span><span class="sxs-lookup"><span data-stu-id="33139-133">It requires extensions in the relativeAddress, i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="33139-134">您可以将自己的扩展名映射到已知的 buildProviders，然后就可以通过任意扩展名激活服务。</span><span class="sxs-lookup"><span data-stu-id="33139-134">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="33139-135">如果发生冲突，`<serviceActivations>` 节将重写 .svc 注册。</span><span class="sxs-lookup"><span data-stu-id="33139-135">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>

## <a name="see-also"></a><span data-ttu-id="33139-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="33139-136">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceActivationElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
