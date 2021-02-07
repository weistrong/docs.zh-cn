---
description: 了解详细信息： ServiceAuthorizationBehavior
title: ServiceAuthorizationBehavior
ms.date: 03/30/2017
ms.assetid: 77dad8e8-fea4-4d1c-b366-2f01a2a87f78
ms.openlocfilehash: dc398621103774a04934aa23ae3d7208f4389717
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715582"
---
# <a name="serviceauthorizationbehavior"></a><span data-ttu-id="501f5-103">ServiceAuthorizationBehavior</span><span class="sxs-lookup"><span data-stu-id="501f5-103">ServiceAuthorizationBehavior</span></span>

<span data-ttu-id="501f5-104">ServiceAuthorizationBehavior</span><span class="sxs-lookup"><span data-stu-id="501f5-104">ServiceAuthorizationBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="501f5-105">语法</span><span class="sxs-lookup"><span data-stu-id="501f5-105">Syntax</span></span>  
  
```csharp
class ServiceAuthorizationBehavior : Behavior  
{  
  boolean ImpersonateCallerForAllOperations;  
  string PrincipalPermissionMode;  
  string RoleProvider;  
  string ServiceAuthorizationManager;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="501f5-106">方法</span><span class="sxs-lookup"><span data-stu-id="501f5-106">Methods</span></span>  

 <span data-ttu-id="501f5-107">ServiceAuthorizationBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="501f5-107">The ServiceAuthorizationBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="501f5-108">属性</span><span class="sxs-lookup"><span data-stu-id="501f5-108">Properties</span></span>  

 <span data-ttu-id="501f5-109">ServiceAuthorizationBehavior 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="501f5-109">The ServiceAuthorizationBehavior class has the following properties:</span></span>  
  
### <a name="impersonatecallerforalloperations"></a><span data-ttu-id="501f5-110">ImpersonateCallerForAllOperations</span><span class="sxs-lookup"><span data-stu-id="501f5-110">ImpersonateCallerForAllOperations</span></span>  

 <span data-ttu-id="501f5-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="501f5-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="501f5-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="501f5-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="501f5-113">一个值，控制服务是否尝试使用传入消息所提供的凭据进行模拟。</span><span class="sxs-lookup"><span data-stu-id="501f5-113">A value that controls whether the service attempts to impersonate using the credentials provided by the incoming message.</span></span>  
  
### <a name="principalpermissionmode"></a><span data-ttu-id="501f5-114">PrincipalPermissionMode</span><span class="sxs-lookup"><span data-stu-id="501f5-114">PrincipalPermissionMode</span></span>  

 <span data-ttu-id="501f5-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="501f5-115">Data type: string</span></span>  
  
 <span data-ttu-id="501f5-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="501f5-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="501f5-117">用于在服务器上执行操作的主体。</span><span class="sxs-lookup"><span data-stu-id="501f5-117">The principal used to carry out operations on the server.</span></span>  
  
### <a name="roleprovider"></a><span data-ttu-id="501f5-118">RoleProvider</span><span class="sxs-lookup"><span data-stu-id="501f5-118">RoleProvider</span></span>  

 <span data-ttu-id="501f5-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="501f5-119">Data type: string</span></span>  
  
 <span data-ttu-id="501f5-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="501f5-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="501f5-121">ASP.NET 角色提供程序的名称。</span><span class="sxs-lookup"><span data-stu-id="501f5-121">The name of the ASP.NET role provider.</span></span>  
  
### <a name="serviceauthorizationmanager"></a><span data-ttu-id="501f5-122">ServiceAuthorizationManager</span><span class="sxs-lookup"><span data-stu-id="501f5-122">ServiceAuthorizationManager</span></span>  

 <span data-ttu-id="501f5-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="501f5-123">Data type: string</span></span>  
  
 <span data-ttu-id="501f5-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="501f5-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="501f5-125">用于自定义授权的授权管理器。</span><span class="sxs-lookup"><span data-stu-id="501f5-125">The authorization manager used for custom authorization.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="501f5-126">要求</span><span class="sxs-lookup"><span data-stu-id="501f5-126">Requirements</span></span>  
  
|<span data-ttu-id="501f5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="501f5-127">MOF</span></span>|<span data-ttu-id="501f5-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="501f5-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="501f5-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="501f5-129">Namespace</span></span>|<span data-ttu-id="501f5-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="501f5-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="501f5-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="501f5-131">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
