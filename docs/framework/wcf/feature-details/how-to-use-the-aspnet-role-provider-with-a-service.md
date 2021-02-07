---
description: 了解详细信息：如何：将 ASP.NET 角色提供程序用于服务
title: 如何：将 ASP.NET 角色提供程序与服务一起使用
ms.date: 03/30/2017
ms.assetid: 88d33a81-8ac7-48de-978c-5c5b1257951e
ms.openlocfilehash: 24bf9ad72d3634baf1d7120e4e60ccde5a4078a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734108"
---
# <a name="how-to-use-the-aspnet-role-provider-with-a-service"></a>如何：将 ASP.NET 角色提供程序与服务一起使用

ASP.NET 角色提供程序 (与 ASP.NET 成员资格提供程序一起使用) 是一项功能，它使 ASP.NET 开发人员能够创建允许用户通过网站创建帐户并为其分配角色进行授权的网站。 借助此功能，任何用户都可以通过网站建立帐户，并登录以获取该网站及其服务的独占访问权。 这与要求用户在 Windows 域中具有帐户的 Windows 安全完全不同。  (提供凭据的任何用户都可以使用该站点及其服务) 用户名/密码组合。  
  
有关示例应用程序，请参阅 [成员身份和角色提供程序](../samples/membership-and-role-provider.md)。 有关 ASP.NET 成员资格提供程序功能的详细信息，请参阅 [如何：使用 ASP.NET 成员资格提供程序](how-to-use-the-aspnet-membership-provider.md)。  
  
角色提供程序功能使用 SQL Server 数据库存储用户信息。 Windows Communication Foundation (WCF) 开发人员可以出于安全目的利用这些功能。 当集成到 WCF 应用程序中时，用户必须为 WCF 客户端应用程序提供用户名/密码组合。 若要使 WCF 能够使用数据库，必须创建类的实例 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior> ，将其 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.PrincipalPermissionMode%2A> 属性设置为 <xref:System.ServiceModel.Description.PrincipalPermissionMode.UseAspNetRoles> ，并将该实例添加到承载服务的的行为集合 <xref:System.ServiceModel.ServiceHost> 。  
  
## <a name="configure-the-role-provider"></a>配置角色提供程序  
  
1. 在 Web.config 文件中的 <`system.web`> 元素下，添加一个 <`roleManager`> 元素，并将其 `enabled` 属性设置为 `true` 。  
  
2. 将 `defaultProvider` 属性设置为 `SqlRoleProvider`。  
  
3. 作为 <> 元素的子 `roleManager` 元素，请添加 <`providers`> 元素。  
  
4. 作为 <> 元素的子 `providers` 元素，添加一个 <> 元素，并将 `add` 以下属性设置为适当的值： `name` 、 `type` 、 `connectionStringName` 和 `applicationName` ，如下面的示例中所示。  
  
    ```xml  
    <!-- Configure the Sql Role Provider. -->  
    <roleManager enabled ="true"
     defaultProvider ="SqlRoleProvider" >  
       <providers>  
         <add name ="SqlRoleProvider"
           type="System.Web.Security.SqlRoleProvider"
           connectionStringName="SqlConn"
           applicationName="MembershipAndRoleProviderSample"/>  
       </providers>  
    </roleManager>  
    ```  
  
## <a name="configure-the-service-to-use-the-role-provider"></a>将服务配置为使用角色提供程序  
  
1. 在 Web.config 文件中，添加一个 [\<system.serviceModel>](../../configure-apps/file-schema/wcf/system-servicemodel.md) 元素。  
  
2. 将 [\<behaviors>](../../configure-apps/file-schema/wcf/behaviors.md) 元素添加到 <`system.ServiceModel`> 元素。  
  
3. 将添加 [\<serviceBehaviors>](../../configure-apps/file-schema/wcf/servicebehaviors.md) 到 <`behaviors`> 元素。  
  
4. 添加 [\<behavior>](../../configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) 元素，并将 `name` 属性设置为合适的值。  
  
5. 将添加 [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) 到 <`behavior`> 元素。  
  
6. 将 `principalPermissionMode` 属性设置为 `UseAspNetRoles`。  
  
7. 将 `roleProviderName` 属性设置为 `SqlRoleProvider`。 下面的示例演示此配置的一个片段。  
  
    ```xml  
    <behaviors>  
     <serviceBehaviors>  
      <behavior name="CalculatorServiceBehavior">  
       <serviceAuthorization principalPermissionMode ="UseAspNetRoles"  
                             roleProviderName ="SqlRoleProvider" />  
      </behavior>  
     </serviceBehaviors>  
    </behaviors>  
    ```  
  
## <a name="see-also"></a>请参阅

- [成员资格和角色提供程序](../samples/membership-and-role-provider.md)
- [如何：使用 ASP.NET 成员资格提供程序](how-to-use-the-aspnet-membership-provider.md)
