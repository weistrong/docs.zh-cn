---
description: 了解详细信息： <httpDigest> 元素
title: <httpDigest> 元素
ms.date: 03/30/2017
ms.assetid: 3da4f276-dfd9-4247-8c07-01d83618727c
ms.openlocfilehash: 2b11edcaab88ff3a2b437b1e886997e08b8c9fee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749657"
---
# <a name="httpdigest-element"></a><span data-ttu-id="7e67a-103">\<httpDigest> 元素</span><span class="sxs-lookup"><span data-stu-id="7e67a-103">\<httpDigest> Element</span></span>

<span data-ttu-id="7e67a-104">指定一个在向服务证明客户端身份时使用的摘要类型凭据。</span><span class="sxs-lookup"><span data-stu-id="7e67a-104">Specifies a digest type credential used when authenticating the client to a service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<httpDigest>**  
  
## <a name="syntax"></a><span data-ttu-id="7e67a-105">语法</span><span class="sxs-lookup"><span data-stu-id="7e67a-105">Syntax</span></span>  
  
```xml  
<httpDigest impersonationLevel="Identification/Impersonation/Delegation/Anonymous/None" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7e67a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7e67a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="7e67a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e67a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7e67a-108">特性</span><span class="sxs-lookup"><span data-stu-id="7e67a-108">Attributes</span></span>  
  
|<span data-ttu-id="7e67a-109">属性</span><span class="sxs-lookup"><span data-stu-id="7e67a-109">Attribute</span></span>|<span data-ttu-id="7e67a-110">说明</span><span class="sxs-lookup"><span data-stu-id="7e67a-110">Description</span></span>|  
|---------------|-----------------|  
|`impersonationLevel`|<span data-ttu-id="7e67a-111">设置客户端用于与服务器进行通信的模拟首选项。</span><span class="sxs-lookup"><span data-stu-id="7e67a-111">Sets the impersonation preference that the client communicates to the server.</span></span> <span data-ttu-id="7e67a-112">服务器上不强制使用客户端所选择的模拟模式。</span><span class="sxs-lookup"><span data-stu-id="7e67a-112">The impersonation mode that the client selects is not enforced on the server.</span></span> <span data-ttu-id="7e67a-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="7e67a-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="7e67a-114">-标识：服务器可以获取客户端的标识和特权，但不能模拟客户端。</span><span class="sxs-lookup"><span data-stu-id="7e67a-114">-   Identification: The server can get the identity and privileges of the client, but cannot impersonate the client.</span></span><br /><span data-ttu-id="7e67a-115">-模拟：服务器可以在本地系统上模拟客户端的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="7e67a-115">-   Impersonation: The server can impersonate the client's security context on the local system.</span></span><br /><span data-ttu-id="7e67a-116">-委派：服务器可以在远程系统上模拟客户端的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="7e67a-116">-   Delegation: The server can impersonate the client's security context on remote systems.</span></span><br /><span data-ttu-id="7e67a-117">-Anonymous：服务器无法模拟或标识客户端。</span><span class="sxs-lookup"><span data-stu-id="7e67a-117">-   Anonymous: The server cannot impersonate or identify the client.</span></span><br /><span data-ttu-id="7e67a-118">-None：不分配模拟级别。</span><span class="sxs-lookup"><span data-stu-id="7e67a-118">-   None: An impersonation level is not assigned.</span></span><br /><br /> <span data-ttu-id="7e67a-119">默认值为 Identification。</span><span class="sxs-lookup"><span data-stu-id="7e67a-119">The default is Identification.</span></span> <span data-ttu-id="7e67a-120">此属性的类型为 <xref:System.Security.Principal.TokenImpersonationLevel>。</span><span class="sxs-lookup"><span data-stu-id="7e67a-120">This attribute is of type <xref:System.Security.Principal.TokenImpersonationLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7e67a-121">子元素</span><span class="sxs-lookup"><span data-stu-id="7e67a-121">Child Elements</span></span>  

 <span data-ttu-id="7e67a-122">无</span><span class="sxs-lookup"><span data-stu-id="7e67a-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7e67a-123">父元素</span><span class="sxs-lookup"><span data-stu-id="7e67a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="7e67a-124">元素</span><span class="sxs-lookup"><span data-stu-id="7e67a-124">Element</span></span>|<span data-ttu-id="7e67a-125">说明</span><span class="sxs-lookup"><span data-stu-id="7e67a-125">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="7e67a-126">指定用于向服务验证客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="7e67a-126">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7e67a-127">备注</span><span class="sxs-lookup"><span data-stu-id="7e67a-127">Remarks</span></span>  

 <span data-ttu-id="7e67a-128">摘要是使用算法和一组输入确定的哈希。</span><span class="sxs-lookup"><span data-stu-id="7e67a-128">A digest is a hash determined by using an algorithm and a set of inputs.</span></span> <span data-ttu-id="7e67a-129">身份验证器和被验证方一致同意某种算法并交换用作输入的数据。</span><span class="sxs-lookup"><span data-stu-id="7e67a-129">The authenticator and the authenticated agree upon an algorithm and exchange the data used as inputs.</span></span> <span data-ttu-id="7e67a-130">客户端可以计算哈希并将其发送给服务。</span><span class="sxs-lookup"><span data-stu-id="7e67a-130">The client can calculate the hash and send it to the service.</span></span> <span data-ttu-id="7e67a-131">服务也可以计算哈希并比较值。</span><span class="sxs-lookup"><span data-stu-id="7e67a-131">The service also calculates the hash and compares the values.</span></span> <span data-ttu-id="7e67a-132">如果匹配，则客户端将通过验证。</span><span class="sxs-lookup"><span data-stu-id="7e67a-132">A match validates the client.</span></span>  
  
 <span data-ttu-id="7e67a-133">必须使用 Windows 上的 Active Directory 和 Internet 信息服务 (IIS) 启用此功能。</span><span class="sxs-lookup"><span data-stu-id="7e67a-133">This feature must be enabled with Active Directory on Windows and Internet Information Services (IIS).</span></span> <span data-ttu-id="7e67a-134">有关详细信息，请参阅 [IIS 6.0 中的摘要式身份验证](/previous-versions/windows/it-pro/windows-server-2003/cc782661(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="7e67a-134">For more information, see [Digest Authentication in IIS 6.0](/previous-versions/windows/it-pro/windows-server-2003/cc782661(v=ws.10)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e67a-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e67a-135">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.HttpDigest%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.HttpDigest%2A>
- <xref:System.ServiceModel.Configuration.HttpDigestClientElement>
- <xref:System.ServiceModel.Security.HttpDigestClientCredential>
- [<span data-ttu-id="7e67a-136">安全行为</span><span class="sxs-lookup"><span data-stu-id="7e67a-136">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="7e67a-137">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="7e67a-137">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="7e67a-138">使用证书</span><span class="sxs-lookup"><span data-stu-id="7e67a-138">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="7e67a-139">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="7e67a-139">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
