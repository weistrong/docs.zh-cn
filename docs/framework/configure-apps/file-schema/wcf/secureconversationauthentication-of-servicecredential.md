---
description: 了解详细 <secureConversationAuthentication> 信息： <serviceCredential>
title: <secureConversationAuthentication> 的 <serviceCredential>
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: 8f95b4009111996d2a5c1133c9ef762375b4e3e2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683315"
---
# <a name="secureconversationauthentication-of-servicecredential"></a><span data-ttu-id="5c56e-103">\<secureConversationAuthentication> 的 \<serviceCredential></span><span class="sxs-lookup"><span data-stu-id="5c56e-103">\<secureConversationAuthentication> of \<serviceCredential></span></span>

<span data-ttu-id="5c56e-104">指定安全对话服务的设置。</span><span class="sxs-lookup"><span data-stu-id="5c56e-104">Specifies the settings for a secure conversation service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<secureConversationAuthentication>**  
  
## <a name="syntax"></a><span data-ttu-id="5c56e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5c56e-105">Syntax</span></span>  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5c56e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5c56e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5c56e-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c56e-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5c56e-108">特性</span><span class="sxs-lookup"><span data-stu-id="5c56e-108">Attributes</span></span>  
  
|<span data-ttu-id="5c56e-109">属性</span><span class="sxs-lookup"><span data-stu-id="5c56e-109">Attribute</span></span>|<span data-ttu-id="5c56e-110">说明</span><span class="sxs-lookup"><span data-stu-id="5c56e-110">Description</span></span>|  
|---------------|-----------------|  
|`securityStateEncoderType`|<span data-ttu-id="5c56e-111">一个字符串，指定要使用的 <xref:System.ServiceModel.Security.SecurityStateEncoder> 的类型。</span><span class="sxs-lookup"><span data-stu-id="5c56e-111">A string that specifies the type of <xref:System.ServiceModel.Security.SecurityStateEncoder> to be used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5c56e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5c56e-112">Child Elements</span></span>  

 <span data-ttu-id="5c56e-113">无。</span><span class="sxs-lookup"><span data-stu-id="5c56e-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5c56e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5c56e-114">Parent Elements</span></span>  
  
|<span data-ttu-id="5c56e-115">元素</span><span class="sxs-lookup"><span data-stu-id="5c56e-115">Element</span></span>|<span data-ttu-id="5c56e-116">说明</span><span class="sxs-lookup"><span data-stu-id="5c56e-116">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCredentials>](servicecredentials.md)|<span data-ttu-id="5c56e-117">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="5c56e-117">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5c56e-118">备注</span><span class="sxs-lookup"><span data-stu-id="5c56e-118">Remarks</span></span>  

 <span data-ttu-id="5c56e-119">使用此配置元素可指定用于安全上下文令牌 (SCT) Cookie 序列化的已知声明类型的列表和用于编码和保护 Cookie 信息的编码器。</span><span class="sxs-lookup"><span data-stu-id="5c56e-119">Use this configuration element to specify a list of known claim types for the Security Context Token (SCT) cookies serialization, as well as an encoder to encode and secure cookies information.</span></span> <span data-ttu-id="5c56e-120">有关 SCT 的更多信息，请参见 <xref:System.ServiceModel.Security.SecureConversationServiceCredential>。</span><span class="sxs-lookup"><span data-stu-id="5c56e-120">For more information on SCT, see <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c56e-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="5c56e-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
