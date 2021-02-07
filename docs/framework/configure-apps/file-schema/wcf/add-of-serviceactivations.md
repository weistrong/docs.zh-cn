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
# <a name="add-of-serviceactivations"></a>\<add> 的 \<serviceActivations>

一个配置元素，可用于定义虚拟服务激活设置，这些设置映射到 Windows Communication Foundation (WCF) 服务类型。 使用此配置元素可以在不使用 .svc 文件的情况下激活承载在 WAS/IIS 中的服务。

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceActivations>**](serviceactivations.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  

## <a name="syntax"></a>语法

```xml
<serviceHostingEnvironment>
    <serviceActivations>
      <add factory="String"
           service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```

## <a name="attributes-and-elements"></a>特性和元素

下列各节描述了特性、子元素和父元素。

### <a name="attributes"></a>特性

|属性|说明|
|---------------|-----------------|
|工厂|一个字符串，指定生成服务激活元素的工厂的 CLR 类型名称。|
|服务|实现服务的 ServiceType（完全限定的 Typename 或短的 Typename（将它置于 App_Code 文件夹中时））。|
|relativeAddress|当前 IIS 应用程序内的相对地址，例如“Service.svc”。 在 WCF 4.0 中，此相对地址必须包含一个已知文件扩展名 ( .xamlx，... ) 。RelativeUrl 不存在物理文件|

### <a name="child-elements"></a>子元素

无。

### <a name="parent-elements"></a>父元素

|元素|说明|
|-------------|-----------------|
|[\<serviceHostingEnvironment>](servicehostingenvironment.md)|一个描述激活设置的配置节。|

## <a name="remarks"></a>备注

下面的示例演示如何在 web.config 文件中配置激活设置。

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

使用此配置，您可以在不使用 .svc 文件的情况下激活 GreetingService。

请注意，`<serviceHostingEnvironment>` 是应用程序级配置。 必须将包含此配置的 `web.config` 放置到虚拟应用程序的根目录下。 此外， `serviceHostingEnvironment` 是 machineToApplication 可继承部分。 如果在计算机的根目录中注册了一个服务，应用程序中的每个服务都将继承此服务。

基于配置的激活支持通过 http 协议和非 http 协议进行激活。 它需要 relativeAddress 中的扩展，即 xoml 或 .xamlx。 您可以将自己的扩展名映射到已知的 buildProviders，然后就可以通过任意扩展名激活服务。 如果发生冲突，`<serviceActivations>` 节将重写 .svc 注册。

## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Configuration.ServiceActivationElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
