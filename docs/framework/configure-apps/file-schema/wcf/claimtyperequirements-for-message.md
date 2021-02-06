---
description: 了解详细 <claimTypeRequirements> 信息： <message>
title: 若 <message>，表示集 <claimTypeRequirements>
ms.date: 03/30/2017
ms.assetid: f95c5ecd-abb6-4b77-a6d7-a38727f4a142
ms.openlocfilehash: a393a075c64f4a46e5ac055b3c417514861c9661
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638894"
---
# <a name="claimtyperequirements-for-message"></a><span data-ttu-id="8c72e-103">若 \<message>，表示集 \<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="8c72e-103">\<claimTypeRequirements> for \<message></span></span>

<span data-ttu-id="8c72e-104">指定所需声明类型的集合。</span><span class="sxs-lookup"><span data-stu-id="8c72e-104">Specifies a collection of required claim types.</span></span>  
  
 <span data-ttu-id="8c72e-105">服务使用此集合来指定任何必选和可选声明，这些声明必须位于客户端用于访问服务的已颁发令牌中。</span><span class="sxs-lookup"><span data-stu-id="8c72e-105">The collection is used by the service to specify any required and optional claims which must be in the issued token the client uses to access the service.</span></span> <span data-ttu-id="8c72e-106">如果 WSDL 发布已启用但 WCF 并不要求已颁发的令牌包含指定的声明类型，则服务将会在元数据中公开所需的声明类型。</span><span class="sxs-lookup"><span data-stu-id="8c72e-106">The service exposes the required claim types in metadata if WSDL publishing is enabled but WCF does not require the issued token contain the specified claim types.</span></span> <span data-ttu-id="8c72e-107">希望强制显示所需声明类型的服务应该使用授权策略。</span><span class="sxs-lookup"><span data-stu-id="8c72e-107">Services wishing to enforce required claim types are present should do using authorization policy.</span></span>  
  
 <span data-ttu-id="8c72e-108">在联合客户端上，此集合包含必选和可选声明的列表，该列表将在客户端请求已颁发令牌时发送给安全令牌服务。</span><span class="sxs-lookup"><span data-stu-id="8c72e-108">On federated clients, this collection contains the list of required and optional claims which is sent to the security token service in the client’s request for an issued token.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c72e-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c72e-109">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
