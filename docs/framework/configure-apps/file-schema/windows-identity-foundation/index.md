---
description: 了解更多相关信息： Windows Identity Foundation 配置架构
title: Windows Identity Foundation 配置架构
ms.date: 03/30/2017
ms.assetid: 4d4f6d76-49a5-4bad-b345-097b2e2844e9
author: BrucePerlerMS
ms.openlocfilehash: 926b2dbe25359ebc789c95f75a59090c7e5a52e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725332"
---
# <a name="windows-identity-foundation-configuration-schema"></a><span data-ttu-id="13556-103">Windows Identity Foundation 配置架构</span><span class="sxs-lookup"><span data-stu-id="13556-103">Windows Identity Foundation Configuration Schema</span></span>

<span data-ttu-id="13556-104">本节中的主题介绍了 Windows Identity Foundation (WIF) 配置架构。</span><span class="sxs-lookup"><span data-stu-id="13556-104">The topics in this section provide information about the Windows Identity Foundation (WIF) configuration schema.</span></span> <span data-ttu-id="13556-105">你还可以将应用程序配置为通过框架公开的类使用 WIF。</span><span class="sxs-lookup"><span data-stu-id="13556-105">You can also configure an application to use WIF through classes exposed by the framework.</span></span> <span data-ttu-id="13556-106">在处理架构中相关元素的几节中提到了这些类。</span><span class="sxs-lookup"><span data-stu-id="13556-106">These classes are noted in the sections that treat relevant elements in the schema.</span></span> <span data-ttu-id="13556-107">以下显示由 WIF 配置架构公开的基本 XML 标记结构。</span><span class="sxs-lookup"><span data-stu-id="13556-107">The following shows the basic XML tag structure exposed by the WIF configuration schema.</span></span> <span data-ttu-id="13556-108">系统会省略属性。</span><span class="sxs-lookup"><span data-stu-id="13556-108">Attributes are omitted.</span></span> <span data-ttu-id="13556-109">突出显示的注释描述架构的主要组件。</span><span class="sxs-lookup"><span data-stu-id="13556-109">Highlighted comments indicate major components of the schema.</span></span>  
  
```xml  
<configuration>  
    <system.identityModel>  
        <!-- Service Configuration -->  
        <identityConfiguration>  
            <caches>  
                <sessionSecurityTokenCache />  
                <tokenReplayCache />  
            </caches>  

            <certificateValidation>  
                <certificateValidator />
            </certificateValidation>  

            <claimsAuthenticationManager />  

            <claimsAuthorizationManager>  
                <optionalConfigurationElement>  
            </claimsAuthorizationManager>  

            <claimTypeRequired>  
                <claimType />
            </claimTypeRequired>  

            <tokenReplayDetection />  

            <!-- Security Token Handler Collection Configuration -->  
            <securityTokenHandlers>  
                <add>  
                    <!-- Can take an optional configuration element which can be one of  
                         the following or a custom element -->  
                    <samlSecurityTokenHandlerRequirement>  
                        <nameClaimType>  
                        <roleClaimType>
                    </samlSecurityTokenHandlerRequirement>  

                    <sessionSecurityTokenHandlerRequirement />  
                    <x509SecurityTokenHandlerRequirement />  
                    <userNameSecurityTokenHandlerRequirement />  
                </add>  
                <clear />  
                <remove />  
                <securityTokenHandlerConfiguration>  
                    <audienceUris>  
                        <add>  
                        <clear>  
                        <remove>  
                    </audienceUris>  

                    <caches>  
                        <sessionSecurityTokenCache />  
                        <tokenReplayCache />  
                    </caches>  

                    <certificateValidation>  
                        <certificateValidator>
                    </certificateValidation>  

                    <issuerNameRegistry>  
                        <!-- Can take an optional configuration element which can be   
                             the <trustedIssuers> element to configure a configuration-based  
                             issuer name registry or can be a custom element -->  
                        <trustedIssuers>  
                            <add>  
                            <clear>  
                            <remove>  
                        </trustedIssuers>  
                    </issuerNameRegistry>  

                    <issuerTokenResolver />  
                    <serviceTokenResolver />  
                    <tokenReplayDetection />  
                </securityTokenHandlerConfiguration>  
            </securityTokenHandlers>  
        </identityConfiguration>  
    </system.identityModel>  

    <system.identityModel.services>  
        <!-- Federation Authentication Configuration -->  
        <federatedAuthentication>  
            <cookieHandler>  
                <chunkedCookieHandler />  
                <customCookieHandler />  
            </cookieHandler>  

            <serviceCertificate>  
                <certificateReference>  
            </serviceCertificate>  

            <wsFederation />  
        </federatedAuthentication>  
    </system.identityModel.services>  
</configuration>  
```  
  
## <a name="in-this-section"></a><span data-ttu-id="13556-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="13556-110">In This Section</span></span>  

<span data-ttu-id="13556-111">[\<system.identityModel>](system-identitymodel.md) 为在应用程序中启用 WIF 选项提供配置。</span><span class="sxs-lookup"><span data-stu-id="13556-111">[\<system.identityModel>](system-identitymodel.md) Provides configuration for enabling WIF options in applications.</span></span>  
  
<span data-ttu-id="13556-112">[\<system.identityModel.services>](system-identitymodel-services.md) 为使用 WIF 的被动联合提供配置。</span><span class="sxs-lookup"><span data-stu-id="13556-112">[\<system.identityModel.services>](system-identitymodel-services.md) Provides configuration for passive federation using WIF.</span></span> <span data-ttu-id="13556-113">配置会话身份验证模块 (SAM) 和联合身份验证模块 (WSFAM)。</span><span class="sxs-lookup"><span data-stu-id="13556-113">Configures the Session Authentication Module (SAM) and the Federated Authentication Module (WSFAM).</span></span>
