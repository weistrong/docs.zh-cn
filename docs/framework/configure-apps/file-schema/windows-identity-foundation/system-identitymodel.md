---
description: 了解详细信息： <System.identitymodel>
title: <system.identityModel>
ms.date: 03/30/2017
ms.assetid: 210ce7e9-d07b-400c-800f-5f525dcf95e8
author: BrucePerlerMS
ms.openlocfilehash: c597f2a849248366f9cf3847c8ef369c13d7a286
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786520"
---
# \<system.identityModel>

<span data-ttu-id="087ae-103">提供用于在应用程序中启用 Windows Identity Foundation (WIF) 选项的配置。</span><span class="sxs-lookup"><span data-stu-id="087ae-103">Provides configuration for enabling Windows Identity Foundation (WIF) options in applications.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.identityModel>**  
  
## <a name="syntax"></a><span data-ttu-id="087ae-104">语法</span><span class="sxs-lookup"><span data-stu-id="087ae-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="087ae-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="087ae-105">Attributes and Elements</span></span>  

 <span data-ttu-id="087ae-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="087ae-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="087ae-107">特性</span><span class="sxs-lookup"><span data-stu-id="087ae-107">Attributes</span></span>  

 <span data-ttu-id="087ae-108">无</span><span class="sxs-lookup"><span data-stu-id="087ae-108">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="087ae-109">子元素</span><span class="sxs-lookup"><span data-stu-id="087ae-109">Child Elements</span></span>  
  
|<span data-ttu-id="087ae-110">元素</span><span class="sxs-lookup"><span data-stu-id="087ae-110">Element</span></span>|<span data-ttu-id="087ae-111">说明</span><span class="sxs-lookup"><span data-stu-id="087ae-111">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="087ae-112">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="087ae-112">Specifies service-level identity settings.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="087ae-113">父元素</span><span class="sxs-lookup"><span data-stu-id="087ae-113">Parent Elements</span></span>  
  
|<span data-ttu-id="087ae-114">元素</span><span class="sxs-lookup"><span data-stu-id="087ae-114">Element</span></span>|<span data-ttu-id="087ae-115">说明</span><span class="sxs-lookup"><span data-stu-id="087ae-115">Description</span></span>|  
|-------------|-----------------|  
|`<configuration>`|<span data-ttu-id="087ae-116">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="087ae-116">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="087ae-117">备注</span><span class="sxs-lookup"><span data-stu-id="087ae-117">Remarks</span></span>  

 <span data-ttu-id="087ae-118">将 `<system.identityModel>` 部分添加到配置文件，以便将服务或应用程序配置为使用 Windows Identity Foundation (WIF) 。</span><span class="sxs-lookup"><span data-stu-id="087ae-118">Add a `<system.identityModel>` section to the configuration file to configure a service or application to use Windows Identity Foundation (WIF).</span></span> <span data-ttu-id="087ae-119">`<system.identityModel>`元素由 <xref:System.IdentityModel.Configuration.SystemIdentityModelSection> 类表示。</span><span class="sxs-lookup"><span data-stu-id="087ae-119">The `<system.identityModel>` element is represented by the <xref:System.IdentityModel.Configuration.SystemIdentityModelSection> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="087ae-120">示例</span><span class="sxs-lookup"><span data-stu-id="087ae-120">Example</span></span>  

 <span data-ttu-id="087ae-121">下面的示例演示如何将节添加 `<system.identityModel>` 到配置文件。</span><span class="sxs-lookup"><span data-stu-id="087ae-121">The following example shows how to add a `<system.identityModel>` section to a configuration file.</span></span> <span data-ttu-id="087ae-122">必须首先在元素下添加配置节和命名空间声明 `<configSections>` 。</span><span class="sxs-lookup"><span data-stu-id="087ae-122">You must first add the configuration section and namespace declaration under the `<configSections>` element.</span></span> <span data-ttu-id="087ae-123">然后，可以将 `<system.IdentityModel>` 元素添加到配置文件中，以指定一个或多个标识配置。</span><span class="sxs-lookup"><span data-stu-id="087ae-123">Then you can add the `<system.IdentityModel>` element to your configuration file to specify one or more identity configurations.</span></span>  
  
```xml  
<configuration>  
  <configSections>  
    <!--WIF 4.5 sections -->  
    <section name="system.identityModel" type="System.IdentityModel.Configuration.SystemIdentityModelSection, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
    <section name="system.identityModel.services" type="System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
  </configSections>  
  
  ...  
  
  <system.identityModel>  
    <identityConfiguration>  
      <audienceUris>  
        <add value="http://localhost/WebApplication1/" />  
      </audienceUris>  
      <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089">  
        <trustedIssuers>  
          <add thumbprint="313D3B … 9106A9EC" name="SelfSTS" />  
        </trustedIssuers>  
      </issuerNameRegistry>  
      <certificateValidation certificateValidationMode="None"/>  
    </identityConfiguration>  
  </system.identityModel>  
  
  ...  
  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="087ae-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="087ae-124">See also</span></span>

- <xref:System.IdentityModel.Configuration.SystemIdentityModelSection>
