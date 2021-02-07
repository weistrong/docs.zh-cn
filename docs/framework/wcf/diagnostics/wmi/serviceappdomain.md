---
description: 了解详细信息： ServiceAppDomain
title: ServiceAppDomain
ms.date: 03/30/2017
ms.assetid: f28e5186-a66d-46c1-abe9-b50e07f8cb4f
ms.openlocfilehash: 1ac32b1fbd88518ffb260be9dd3ed2adb88d211c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715634"
---
# <a name="serviceappdomain"></a><span data-ttu-id="bdcc9-103">ServiceAppDomain</span><span class="sxs-lookup"><span data-stu-id="bdcc9-103">ServiceAppDomain</span></span>

<span data-ttu-id="bdcc9-104">将服务映射到应用程序域。</span><span class="sxs-lookup"><span data-stu-id="bdcc9-104">Maps a service to an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdcc9-105">语法</span><span class="sxs-lookup"><span data-stu-id="bdcc9-105">Syntax</span></span>  
  
```csharp
class ServiceAppDomain  
{  
  Service ref;  
  AppDomainInfo ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="bdcc9-106">方法</span><span class="sxs-lookup"><span data-stu-id="bdcc9-106">Methods</span></span>  

 <span data-ttu-id="bdcc9-107">ServiceAppDomain 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="bdcc9-107">The ServiceAppDomain class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="bdcc9-108">属性</span><span class="sxs-lookup"><span data-stu-id="bdcc9-108">Properties</span></span>  

 <span data-ttu-id="bdcc9-109">ServiceAppDomain 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="bdcc9-109">The ServiceAppDomain class has the following properties:</span></span>  
  
### <a name="ref"></a><span data-ttu-id="bdcc9-110">ref</span><span class="sxs-lookup"><span data-stu-id="bdcc9-110">ref</span></span>  

 <span data-ttu-id="bdcc9-111">数据类型：Service</span><span class="sxs-lookup"><span data-stu-id="bdcc9-111">Data type: Service</span></span>  
<span data-ttu-id="bdcc9-112">限定符：键</span><span class="sxs-lookup"><span data-stu-id="bdcc9-112">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="bdcc9-113">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bdcc9-113">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bdcc9-114">此应用程序域的服务。</span><span class="sxs-lookup"><span data-stu-id="bdcc9-114">The service of this application domain.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="bdcc9-115">ref</span><span class="sxs-lookup"><span data-stu-id="bdcc9-115">ref</span></span>  

 <span data-ttu-id="bdcc9-116">数据类型：AppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="bdcc9-116">Data type: AppDomainInfo</span></span>  
<span data-ttu-id="bdcc9-117">限定符：键</span><span class="sxs-lookup"><span data-stu-id="bdcc9-117">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="bdcc9-118">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bdcc9-118">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bdcc9-119">包含应用程序域的属性。</span><span class="sxs-lookup"><span data-stu-id="bdcc9-119">Contains properties of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdcc9-120">要求</span><span class="sxs-lookup"><span data-stu-id="bdcc9-120">Requirements</span></span>  
  
|<span data-ttu-id="bdcc9-121">MOF</span><span class="sxs-lookup"><span data-stu-id="bdcc9-121">MOF</span></span>|<span data-ttu-id="bdcc9-122">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="bdcc9-122">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="bdcc9-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="bdcc9-123">Namespace</span></span>|<span data-ttu-id="bdcc9-124">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="bdcc9-124">Defined in root\ServiceModel</span></span>|
