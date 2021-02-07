---
description: 了解更多： VisualStudio. ClientActivityBuilder。ctor
title: Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
ms.date: 03/30/2017
ms.topic: reference
api_name:
- Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
api_location:
- Microsoft.VisualStudio.Activities.dll
api_type:
- Assembly
ms.assetid: 6b44b13c-7a23-4df2-8f9f-45e2b1430002
ms.openlocfilehash: 1a1b436c2b15fdf07f924aa0db2a13598422e988
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739984"
---
# <a name="microsoftvisualstudioactivitiesasrclientactivitybuilderctor"></a><span data-ttu-id="de7a2-103">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor</span><span class="sxs-lookup"><span data-stu-id="de7a2-103">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor</span></span>

<span data-ttu-id="de7a2-104">创建 VisualStudio 的实例。 [ClientActivityBuilder](microsoft-visualstudio-activities-asr-clientactivitybuilder.md) 类的实例。</span><span class="sxs-lookup"><span data-stu-id="de7a2-104">Creates an instance of the [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](microsoft-visualstudio-activities-asr-clientactivitybuilder.md) class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de7a2-105">语法</span><span class="sxs-lookup"><span data-stu-id="de7a2-105">Syntax</span></span>  
  
```csharp  
public ClientActivityBuilder(OperationDescription operationDescription, string configurationName, string proxyNamespace);  
```  
  
## <a name="parameters"></a><span data-ttu-id="de7a2-106">参数</span><span class="sxs-lookup"><span data-stu-id="de7a2-106">Parameters</span></span>  
  
## <a name="parameter-values"></a><span data-ttu-id="de7a2-107">参数值</span><span class="sxs-lookup"><span data-stu-id="de7a2-107">Parameter Values</span></span>  

 <span data-ttu-id="de7a2-108">*operationDescription*</span><span class="sxs-lookup"><span data-stu-id="de7a2-108">*operationDescription*</span></span>  
  
 <span data-ttu-id="de7a2-109">描述要在生成的工作流活动中执行的操作，包括操作名称、返回类型和参数信息。</span><span class="sxs-lookup"><span data-stu-id="de7a2-109">Describes the operation to be performed in the workflow activity that is to be generated, including the operation name, return type, and parameter information.</span></span> <span data-ttu-id="de7a2-110">此参数的值不得为 **null**。</span><span class="sxs-lookup"><span data-stu-id="de7a2-110">The value of this parameter must not be **null**.</span></span> <span data-ttu-id="de7a2-111">它应描述使用消息协定并且取得具有一个消息的参数的同步操作。</span><span class="sxs-lookup"><span data-stu-id="de7a2-111">It should describe a synchronous operation which uses a message contract and takes an argument with one message.</span></span> <span data-ttu-id="de7a2-112">如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。</span><span class="sxs-lookup"><span data-stu-id="de7a2-112">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
 <span data-ttu-id="de7a2-113">*configurationName*</span><span class="sxs-lookup"><span data-stu-id="de7a2-113">*configurationName*</span></span>  
  
 <span data-ttu-id="de7a2-114">指定终结点配置名称。</span><span class="sxs-lookup"><span data-stu-id="de7a2-114">Specifies the endpoint configuration name.</span></span> <span data-ttu-id="de7a2-115">此参数的值不能为 **null** 或为空。</span><span class="sxs-lookup"><span data-stu-id="de7a2-115">The value of this parameter must not be either **null** or empty.</span></span> <span data-ttu-id="de7a2-116">如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。</span><span class="sxs-lookup"><span data-stu-id="de7a2-116">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
 <span data-ttu-id="de7a2-117">*proxyNamespace*</span><span class="sxs-lookup"><span data-stu-id="de7a2-117">*proxyNamespace*</span></span>  
  
 <span data-ttu-id="de7a2-118">指定操作的服务命名空间。</span><span class="sxs-lookup"><span data-stu-id="de7a2-118">Specifies the service namespace for the operation.</span></span> <span data-ttu-id="de7a2-119">此参数的值不能为 **null** 或为空。</span><span class="sxs-lookup"><span data-stu-id="de7a2-119">The value of this parameter must not be either **null** or empty.</span></span> <span data-ttu-id="de7a2-120">如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。</span><span class="sxs-lookup"><span data-stu-id="de7a2-120">If these conditions are not satisfied, the runtime result of using the constructor and the other methods of this class are undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de7a2-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="de7a2-121">See also</span></span>

- [<span data-ttu-id="de7a2-122">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder</span><span class="sxs-lookup"><span data-stu-id="de7a2-122">Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder</span></span>](microsoft-visualstudio-activities-asr-clientactivitybuilder.md)
