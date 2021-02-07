---
description: 了解详细信息： <serviceCertificate>
title: <serviceCertificate>
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: d9940fd96667211b1f9fd672b824af84e0d5143a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725319"
---
# \<serviceCertificate>

<span data-ttu-id="43c52-102">配置用于加密和解密令牌的 x.509 证书。</span><span class="sxs-lookup"><span data-stu-id="43c52-102">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel.services>**](system-identitymodel-services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<federationConfiguration>**](federationconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="43c52-103">语法</span><span class="sxs-lookup"><span data-stu-id="43c52-103">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43c52-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="43c52-104">Attributes and Elements</span></span>  

 <span data-ttu-id="43c52-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43c52-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43c52-106">特性</span><span class="sxs-lookup"><span data-stu-id="43c52-106">Attributes</span></span>  

 <span data-ttu-id="43c52-107">无</span><span class="sxs-lookup"><span data-stu-id="43c52-107">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="43c52-108">子元素</span><span class="sxs-lookup"><span data-stu-id="43c52-108">Child Elements</span></span>  
  
|<span data-ttu-id="43c52-109">元素</span><span class="sxs-lookup"><span data-stu-id="43c52-109">Element</span></span>|<span data-ttu-id="43c52-110">说明</span><span class="sxs-lookup"><span data-stu-id="43c52-110">Description</span></span>|  
|-------------|-----------------|  
|[\<certificateReference>](certificatereference.md)|<span data-ttu-id="43c52-111">指定用于在证书存储中查找和验证 x.509 证书的设置。</span><span class="sxs-lookup"><span data-stu-id="43c52-111">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="43c52-112">父元素</span><span class="sxs-lookup"><span data-stu-id="43c52-112">Parent Elements</span></span>  
  
|<span data-ttu-id="43c52-113">元素</span><span class="sxs-lookup"><span data-stu-id="43c52-113">Element</span></span>|<span data-ttu-id="43c52-114">说明</span><span class="sxs-lookup"><span data-stu-id="43c52-114">Description</span></span>|  
|-------------|-----------------|  
|[\<federationConfiguration>](federationconfiguration.md)|<span data-ttu-id="43c52-115">包含配置 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) 和 <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) 的设置。</span><span class="sxs-lookup"><span data-stu-id="43c52-115">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="43c52-116">示例</span><span class="sxs-lookup"><span data-stu-id="43c52-116">Example</span></span>  

 <span data-ttu-id="43c52-117">下面的 XML 演示如何使用 \<serviceCertificate> 元素。</span><span class="sxs-lookup"><span data-stu-id="43c52-117">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="43c52-118">XML 是从示例获取的 `CustomToken` 。</span><span class="sxs-lookup"><span data-stu-id="43c52-118">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
