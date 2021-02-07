---
description: 了解详细信息： ServiceSecurityAuditBehavior
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
ms.openlocfilehash: 5dfb3a70a80d5dea1ed360dcaf3a0db989bf671b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715465"
---
# <a name="servicesecurityauditbehavior"></a><span data-ttu-id="3eaa4-103">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="3eaa4-103">ServiceSecurityAuditBehavior</span></span>

<span data-ttu-id="3eaa4-104">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="3eaa4-104">ServiceSecurityAuditBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3eaa4-105">语法</span><span class="sxs-lookup"><span data-stu-id="3eaa4-105">Syntax</span></span>  
  
```csharp  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3eaa4-106">方法</span><span class="sxs-lookup"><span data-stu-id="3eaa4-106">Methods</span></span>  

 <span data-ttu-id="3eaa4-107">ServiceSecurityAuditBehavior 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-107">The ServiceSecurityAuditBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3eaa4-108">属性</span><span class="sxs-lookup"><span data-stu-id="3eaa4-108">Properties</span></span>  

 <span data-ttu-id="3eaa4-109">ServiceSecurityAuditBehavior 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="3eaa4-109">The ServiceSecurityAuditBehavior class has the following properties:</span></span>  
  
### <a name="auditloglocation"></a><span data-ttu-id="3eaa4-110">AuditLogLocation</span><span class="sxs-lookup"><span data-stu-id="3eaa4-110">AuditLogLocation</span></span>  

 <span data-ttu-id="3eaa4-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3eaa4-111">Data type: string</span></span>  
  
 <span data-ttu-id="3eaa4-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3eaa4-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3eaa4-113">审核日志的位置。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-113">The location of the audit log.</span></span>  
  
### <a name="messageauthenticationauditlevel"></a><span data-ttu-id="3eaa4-114">MessageAuthenticationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="3eaa4-114">MessageAuthenticationAuditLevel</span></span>  

 <span data-ttu-id="3eaa4-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3eaa4-115">Data type: string</span></span>  
  
 <span data-ttu-id="3eaa4-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3eaa4-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3eaa4-117">用于记录审核事件的消息身份验证级别的类型。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-117">The type of message authentication level that is used to log audit events.</span></span>  
  
### <a name="serviceauthorizationauditlevel"></a><span data-ttu-id="3eaa4-118">ServiceAuthorizationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="3eaa4-118">ServiceAuthorizationAuditLevel</span></span>  

 <span data-ttu-id="3eaa4-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3eaa4-119">Data type: string</span></span>  
  
 <span data-ttu-id="3eaa4-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3eaa4-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3eaa4-121">审核日志中记录的授权事件类型。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-121">The types of authorization events that are recorded in the audit log.</span></span>  
  
### <a name="suppressauditfailure"></a><span data-ttu-id="3eaa4-122">SuppressAuditFailure</span><span class="sxs-lookup"><span data-stu-id="3eaa4-122">SuppressAuditFailure</span></span>  

 <span data-ttu-id="3eaa4-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="3eaa4-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="3eaa4-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3eaa4-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3eaa4-125">一个 boolean 值，指定取消显示审核日志写入失败的行为。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-125">A boolean value that specifies the behavior for suppressing failures of writing to the audit log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3eaa4-126">要求</span><span class="sxs-lookup"><span data-stu-id="3eaa4-126">Requirements</span></span>  
  
|<span data-ttu-id="3eaa4-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3eaa4-127">MOF</span></span>|<span data-ttu-id="3eaa4-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="3eaa4-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3eaa4-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="3eaa4-129">Namespace</span></span>|<span data-ttu-id="3eaa4-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="3eaa4-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3eaa4-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="3eaa4-131">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
