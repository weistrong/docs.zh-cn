---
description: 了解详细信息： ServiceCredentials
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: bfd025a8f671a3c5aea537059cde0e751cfa9bb9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715543"
---
# <a name="servicecredentials"></a><span data-ttu-id="897ed-103">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="897ed-103">ServiceCredentials</span></span>

<span data-ttu-id="897ed-104">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="897ed-104">ServiceCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="897ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="897ed-105">Syntax</span></span>  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="897ed-106">方法</span><span class="sxs-lookup"><span data-stu-id="897ed-106">Methods</span></span>  

 <span data-ttu-id="897ed-107">ServiceCredentials 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="897ed-107">The ServiceCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="897ed-108">属性</span><span class="sxs-lookup"><span data-stu-id="897ed-108">Properties</span></span>  

 <span data-ttu-id="897ed-109">ServiceCredentials 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="897ed-109">The ServiceCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="897ed-110">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="897ed-110">ClientCertificate</span></span>  

 <span data-ttu-id="897ed-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-111">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-113">此服务的客户端证书身份验证和配置设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-113">The client certificate authentication and provisioning settings for this service.</span></span>  
  
### <a name="issuedtokenauthentication"></a><span data-ttu-id="897ed-114">IssuedTokenAuthentication</span><span class="sxs-lookup"><span data-stu-id="897ed-114">IssuedTokenAuthentication</span></span>  

 <span data-ttu-id="897ed-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-115">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-117">当前颁发的此服务的令牌身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-117">The current issued token authentication settings for this service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="897ed-118">对等</span><span class="sxs-lookup"><span data-stu-id="897ed-118">Peer</span></span>  

 <span data-ttu-id="897ed-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-119">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-121">对等传输终结点要使用的当前凭据身份验证和配置设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-121">The current credential authentication and provisioning settings to be used by peer transport endpoints.</span></span>  
  
### <a name="secureconversationauthentication"></a><span data-ttu-id="897ed-122">SecureConversationAuthentication</span><span class="sxs-lookup"><span data-stu-id="897ed-122">SecureConversationAuthentication</span></span>  

 <span data-ttu-id="897ed-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-123">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-125">指定当前安全对话设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-125">Specifies the current secure conversation settings.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="897ed-126">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="897ed-126">ServiceCertificate</span></span>  

 <span data-ttu-id="897ed-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-127">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-129">与此服务关联的证书。</span><span class="sxs-lookup"><span data-stu-id="897ed-129">The certificate associated with this service.</span></span>  
  
### <a name="usernameauthentication"></a><span data-ttu-id="897ed-130">UserNameAuthentication</span><span class="sxs-lookup"><span data-stu-id="897ed-130">UserNameAuthentication</span></span>  

 <span data-ttu-id="897ed-131">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-131">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-133">此服务的用户名/密码设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-133">The username/password settings for this service.</span></span>  
  
### <a name="windowsauthentication"></a><span data-ttu-id="897ed-134">WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="897ed-134">WindowsAuthentication</span></span>  

 <span data-ttu-id="897ed-135">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="897ed-135">Data type: string</span></span>  
  
 <span data-ttu-id="897ed-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="897ed-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="897ed-137">此服务的 Windows 身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="897ed-137">The Windows authentication settings for this service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="897ed-138">要求</span><span class="sxs-lookup"><span data-stu-id="897ed-138">Requirements</span></span>  
  
|<span data-ttu-id="897ed-139">MOF</span><span class="sxs-lookup"><span data-stu-id="897ed-139">MOF</span></span>|<span data-ttu-id="897ed-140">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="897ed-140">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="897ed-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="897ed-141">Namespace</span></span>|<span data-ttu-id="897ed-142">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="897ed-142">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="897ed-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="897ed-143">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceCredentials>
