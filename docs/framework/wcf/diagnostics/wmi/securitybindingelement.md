---
description: 了解详细信息： SecurityBindingElement
title: SecurityBindingElement
ms.date: 03/30/2017
ms.assetid: ef93b6e6-3524-48a8-94d3-c8837f1872f9
ms.openlocfilehash: bc9a519978a9cccccd80a58abb8d109fa9bc9337
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743806"
---
# <a name="securitybindingelement"></a><span data-ttu-id="e39e9-103">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="e39e9-103">SecurityBindingElement</span></span>

<span data-ttu-id="e39e9-104">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="e39e9-104">SecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e39e9-105">语法</span><span class="sxs-lookup"><span data-stu-id="e39e9-105">Syntax</span></span>  
  
```csharp
class SecurityBindingElement : BindingElement  
{  
  string DefaultAlgorithmSuite;  
  boolean IncludeTimestamp;  
  string KeyEntropyMode;  
  LocalServiceSecuritySettings LocalServiceSecuritySettings;  
  string MessageSecurityVersion;  
  string SecurityHeaderLayout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e39e9-106">方法</span><span class="sxs-lookup"><span data-stu-id="e39e9-106">Methods</span></span>  

 <span data-ttu-id="e39e9-107">SecurityBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="e39e9-107">The SecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e39e9-108">属性</span><span class="sxs-lookup"><span data-stu-id="e39e9-108">Properties</span></span>  

 <span data-ttu-id="e39e9-109">SecurityBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="e39e9-109">The SecurityBindingElement class has the following properties:</span></span>  
  
### <a name="defaultalgorithmsuite"></a><span data-ttu-id="e39e9-110">DefaultAlgorithmSuite</span><span class="sxs-lookup"><span data-stu-id="e39e9-110">DefaultAlgorithmSuite</span></span>  

 <span data-ttu-id="e39e9-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="e39e9-111">Data type: string</span></span>  
  
 <span data-ttu-id="e39e9-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-113">指定要用于绑定的算法。</span><span class="sxs-lookup"><span data-stu-id="e39e9-113">Specifies the algorithms to use with the binding.</span></span>  
  
### <a name="includetimestamp"></a><span data-ttu-id="e39e9-114">IncludeTimestamp</span><span class="sxs-lookup"><span data-stu-id="e39e9-114">IncludeTimestamp</span></span>  

 <span data-ttu-id="e39e9-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="e39e9-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="e39e9-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-117">一个布尔值，指定是否每个消息都包含时间戳。</span><span class="sxs-lookup"><span data-stu-id="e39e9-117">A Boolean value that specifies whether each message contains a timestamp.</span></span>  
  
### <a name="keyentropymode"></a><span data-ttu-id="e39e9-118">KeyEntropyMode</span><span class="sxs-lookup"><span data-stu-id="e39e9-118">KeyEntropyMode</span></span>  

 <span data-ttu-id="e39e9-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="e39e9-119">Data type: string</span></span>  
  
 <span data-ttu-id="e39e9-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-121">用于创建密钥的熵的来源。</span><span class="sxs-lookup"><span data-stu-id="e39e9-121">The source of entropy used to create keys.</span></span>  
  
### <a name="localservicesecuritysettings"></a><span data-ttu-id="e39e9-122">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="e39e9-122">LocalServiceSecuritySettings</span></span>  

 <span data-ttu-id="e39e9-123">数据类型：LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="e39e9-123">Data type: LocalServiceSecuritySettings</span></span>  
  
 <span data-ttu-id="e39e9-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-125">本地服务的特定于绑定的安全属性。</span><span class="sxs-lookup"><span data-stu-id="e39e9-125">The binding specific security properties for the local service.</span></span>  
  
### <a name="messagesecurityversion"></a><span data-ttu-id="e39e9-126">MessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="e39e9-126">MessageSecurityVersion</span></span>  

 <span data-ttu-id="e39e9-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="e39e9-127">Data type: string</span></span>  
  
 <span data-ttu-id="e39e9-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-129">消息安全使用的版本。</span><span class="sxs-lookup"><span data-stu-id="e39e9-129">The version used for message security.</span></span>  
  
### <a name="securityheaderlayout"></a><span data-ttu-id="e39e9-130">SecurityHeaderLayout</span><span class="sxs-lookup"><span data-stu-id="e39e9-130">SecurityHeaderLayout</span></span>  

 <span data-ttu-id="e39e9-131">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="e39e9-131">Data type: string</span></span>  
  
 <span data-ttu-id="e39e9-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="e39e9-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e39e9-133">此绑定的安全标头中的元素顺序。</span><span class="sxs-lookup"><span data-stu-id="e39e9-133">The order of elements in the security header for this binding.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e39e9-134">要求</span><span class="sxs-lookup"><span data-stu-id="e39e9-134">Requirements</span></span>  
  
|<span data-ttu-id="e39e9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e39e9-135">MOF</span></span>|<span data-ttu-id="e39e9-136">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="e39e9-136">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e39e9-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="e39e9-137">Namespace</span></span>|<span data-ttu-id="e39e9-138">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="e39e9-138">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e39e9-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="e39e9-139">See also</span></span>

- <xref:System.ServiceModel.Channels.SecurityBindingElement>
