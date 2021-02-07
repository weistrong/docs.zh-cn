---
description: 了解详细信息： ClientCredentials
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: 7b0b5a05e5b61de717567de664079f2ed1e20f6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757658"
---
# <a name="clientcredentials"></a><span data-ttu-id="021af-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="021af-103">ClientCredentials</span></span>

<span data-ttu-id="021af-104">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="021af-104">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="021af-105">语法</span><span class="sxs-lookup"><span data-stu-id="021af-105">Syntax</span></span>  
  
```csharp
class ClientCredentials : Behavior  
{  
  string ClientCertificate;  
  string HttpDigest;  
  string IssuedToken;  
  string Peer;  
  string ServiceCertificate;  
  boolean SupportInteractive;  
  string UserName;  
  string Windows;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="021af-106">方法</span><span class="sxs-lookup"><span data-stu-id="021af-106">Methods</span></span>  

 <span data-ttu-id="021af-107">ClientCredentials 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="021af-107">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="021af-108">属性</span><span class="sxs-lookup"><span data-stu-id="021af-108">Properties</span></span>  

 <span data-ttu-id="021af-109">ClientCredentials 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="021af-109">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="021af-110">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="021af-110">ClientCertificate</span></span>  

 <span data-ttu-id="021af-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-111">Data type: string</span></span>  
  
 <span data-ttu-id="021af-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-113">客户端用来向服务验证身份的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="021af-113">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="021af-114">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="021af-114">HttpDigest</span></span>  

 <span data-ttu-id="021af-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-115">Data type: string</span></span>  
  
 <span data-ttu-id="021af-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-117">当前 Http Digest 凭据。</span><span class="sxs-lookup"><span data-stu-id="021af-117">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="021af-118">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="021af-118">IssuedToken</span></span>  

 <span data-ttu-id="021af-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-119">Data type: string</span></span>  
  
 <span data-ttu-id="021af-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-121">用于联系本地安全令牌服务的终结点地址和绑定。</span><span class="sxs-lookup"><span data-stu-id="021af-121">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="021af-122">对等</span><span class="sxs-lookup"><span data-stu-id="021af-122">Peer</span></span>  

 <span data-ttu-id="021af-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-123">Data type: string</span></span>  
  
 <span data-ttu-id="021af-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-125">对等节点用来向网格中的其他节点验证其自身身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="021af-125">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="021af-126">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="021af-126">ServiceCertificate</span></span>  

 <span data-ttu-id="021af-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-127">Data type: string</span></span>  
  
 <span data-ttu-id="021af-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-129">服务的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="021af-129">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="021af-130">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="021af-130">SupportInteractive</span></span>  

 <span data-ttu-id="021af-131">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="021af-131">Data type: boolean</span></span>  
  
 <span data-ttu-id="021af-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-133">一个布尔值，指定凭据是否支持交互式协商。</span><span class="sxs-lookup"><span data-stu-id="021af-133">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="021af-134">UserName</span><span class="sxs-lookup"><span data-stu-id="021af-134">UserName</span></span>  

 <span data-ttu-id="021af-135">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-135">Data type: string</span></span>  
  
 <span data-ttu-id="021af-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-137">客户端用来向服务验证其自身身份的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="021af-137">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="021af-138">Windows</span><span class="sxs-lookup"><span data-stu-id="021af-138">Windows</span></span>  

 <span data-ttu-id="021af-139">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="021af-139">Data type: string</span></span>  
  
 <span data-ttu-id="021af-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="021af-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="021af-141">客户端用来向服务验证其自身身份的 Windows 凭据。</span><span class="sxs-lookup"><span data-stu-id="021af-141">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="021af-142">要求</span><span class="sxs-lookup"><span data-stu-id="021af-142">Requirements</span></span>  
  
|<span data-ttu-id="021af-143">MOF</span><span class="sxs-lookup"><span data-stu-id="021af-143">MOF</span></span>|<span data-ttu-id="021af-144">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="021af-144">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="021af-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="021af-145">Namespace</span></span>|<span data-ttu-id="021af-146">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="021af-146">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="021af-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="021af-147">See also</span></span>

- <xref:System.ServiceModel.Description.ClientCredentials>
