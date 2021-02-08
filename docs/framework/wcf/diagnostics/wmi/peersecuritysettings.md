---
description: 了解详细信息： PeerSecuritySettings
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: a8b5b8c88e71cb46110fa35186599c0f9c366d17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803004"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="7e986-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="7e986-103">PeerSecuritySettings</span></span>

<span data-ttu-id="7e986-104">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="7e986-104">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e986-105">语法</span><span class="sxs-lookup"><span data-stu-id="7e986-105">Syntax</span></span>  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="7e986-106">方法</span><span class="sxs-lookup"><span data-stu-id="7e986-106">Methods</span></span>  

 <span data-ttu-id="7e986-107">PeerSecuritySettings 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="7e986-107">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7e986-108">属性</span><span class="sxs-lookup"><span data-stu-id="7e986-108">Properties</span></span>  

 <span data-ttu-id="7e986-109">PeerSecuritySettings 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="7e986-109">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="7e986-110">模型</span><span class="sxs-lookup"><span data-stu-id="7e986-110">Mode</span></span>  

 <span data-ttu-id="7e986-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="7e986-111">Data type: string</span></span>  
  
 <span data-ttu-id="7e986-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7e986-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7e986-113">配置有绑定的终结点是否使用消息级别和传输级别安全。</span><span class="sxs-lookup"><span data-stu-id="7e986-113">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="7e986-114">Transport</span><span class="sxs-lookup"><span data-stu-id="7e986-114">Transport</span></span>  

 <span data-ttu-id="7e986-115">数据类型：PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="7e986-115">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="7e986-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="7e986-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7e986-117">传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="7e986-117">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e986-118">要求</span><span class="sxs-lookup"><span data-stu-id="7e986-118">Requirements</span></span>  
  
|<span data-ttu-id="7e986-119">MOF</span><span class="sxs-lookup"><span data-stu-id="7e986-119">MOF</span></span>|<span data-ttu-id="7e986-120">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="7e986-120">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7e986-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e986-121">Namespace</span></span>|<span data-ttu-id="7e986-122">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="7e986-122">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7e986-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="7e986-123">See also</span></span>

- <xref:System.ServiceModel.PeerSecuritySettings>
