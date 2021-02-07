---
description: 了解有关 <windows> 元素的详细 <clientCredentials> 信息
title: <windows> of <clientCredentials> 元素
ms.date: 03/30/2017
ms.assetid: 793e41c2-31ea-4159-abbc-2123bf097233
ms.openlocfilehash: d693ad914dfa02ef12a7c8520ca84be3a9595e73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682418"
---
# <a name="windows-of-clientcredentials-element"></a><span data-ttu-id="5a0ab-103">\<windows> of \<clientCredentials> 元素</span><span class="sxs-lookup"><span data-stu-id="5a0ab-103">\<windows> of \<clientCredentials> Element</span></span>

<span data-ttu-id="5a0ab-104">指定用于表示客户端的 Windows 凭据的设置。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-104">Specifies the settings for a Windows credential to be used to represent the client.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<windows>**  
  
## <a name="syntax"></a><span data-ttu-id="5a0ab-105">语法</span><span class="sxs-lookup"><span data-stu-id="5a0ab-105">Syntax</span></span>  
  
```xml  
<windows allowedImpersonationLevel="Identification/Impersonation/Delegation/Anonymous/None"
         allowNtlm="Boolean" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5a0ab-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5a0ab-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5a0ab-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5a0ab-108">特性</span><span class="sxs-lookup"><span data-stu-id="5a0ab-108">Attributes</span></span>  
  
|<span data-ttu-id="5a0ab-109">属性</span><span class="sxs-lookup"><span data-stu-id="5a0ab-109">Attribute</span></span>|<span data-ttu-id="5a0ab-110">说明</span><span class="sxs-lookup"><span data-stu-id="5a0ab-110">Description</span></span>|  
|---------------|-----------------|  
|`allowedImpersonationLevel`|<span data-ttu-id="5a0ab-111">设置客户端用于与服务器进行通信的模拟首选项。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-111">Sets the impersonation preference that the client communicates to the server.</span></span> <span data-ttu-id="5a0ab-112">服务器上不强制使用客户端所选择的模拟模式。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-112">The impersonation mode that the client selects is not enforced on the server.</span></span> <span data-ttu-id="5a0ab-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="5a0ab-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="5a0ab-114">-标识：服务器可以获取客户端的标识和特权，但不能模拟客户端。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-114">-   Identification: The server can get the identity and privileges of the client, but cannot impersonate the client.</span></span><br /><span data-ttu-id="5a0ab-115">-模拟：服务器可以在本地系统上模拟客户端的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-115">-   Impersonation: The server can impersonate the client's security context on the local system.</span></span><br /><span data-ttu-id="5a0ab-116">-委派：服务器可以在远程系统上模拟客户端的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-116">-   Delegation: The server can impersonate the client's security context on remote systems.</span></span><br /><span data-ttu-id="5a0ab-117">-Anonymous：服务器无法模拟或标识客户端。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-117">-   Anonymous: The server cannot impersonate or identify the client.</span></span><br /><span data-ttu-id="5a0ab-118">-None：不分配模拟级别。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-118">-   None: An impersonation level is not assigned.</span></span><br /><br /> <span data-ttu-id="5a0ab-119">默认值为 Identification。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-119">The default is Identification.</span></span> <span data-ttu-id="5a0ab-120">此属性的类型为 <xref:System.Security.Principal.TokenImpersonationLevel>。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-120">This attribute is of type <xref:System.Security.Principal.TokenImpersonationLevel>.</span></span>|  
|`allowNtlm`|<span data-ttu-id="5a0ab-121">如果 Kerberos 不可用，则将此属性设置为 `true` 可令身份验证降级到 NTLM。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-121">Setting this property to `true` allows authentication to downgrade to NTLM if Kerberos is not available.</span></span><br /><br /> <span data-ttu-id="5a0ab-122">如果将此属性设置为，则 `false` Windows Communication Foundation (WCF) 以便在使用 NTLM 时尽力引发异常。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-122">Setting this property to `false` causes Windows Communication Foundation (WCF) to make a best-effort to throw an exception if NTLM is used.</span></span> <span data-ttu-id="5a0ab-123">请注意，将此属性设置为 `false` 可能不阻止通过网络发送 NTLM 凭据。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-123">Note that setting this property to `false` may not prevent NTLM credentials from being sent over the wire.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5a0ab-124">子元素</span><span class="sxs-lookup"><span data-stu-id="5a0ab-124">Child Elements</span></span>  

 <span data-ttu-id="5a0ab-125">无。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5a0ab-126">父元素</span><span class="sxs-lookup"><span data-stu-id="5a0ab-126">Parent Elements</span></span>  
  
|<span data-ttu-id="5a0ab-127">元素</span><span class="sxs-lookup"><span data-stu-id="5a0ab-127">Element</span></span>|<span data-ttu-id="5a0ab-128">说明</span><span class="sxs-lookup"><span data-stu-id="5a0ab-128">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="5a0ab-129">指定用于向服务证明客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="5a0ab-129">Specifies the credentials used to authenticate the client to the service.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5a0ab-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a0ab-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.WindowsClientElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Windows%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Windows%2A>
- <xref:System.ServiceModel.Security.WindowsClientCredential>
- [<span data-ttu-id="5a0ab-131">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="5a0ab-131">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="5a0ab-132">使用证书</span><span class="sxs-lookup"><span data-stu-id="5a0ab-132">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="5a0ab-133">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="5a0ab-133">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
