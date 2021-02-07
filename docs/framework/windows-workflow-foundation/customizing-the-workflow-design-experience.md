---
description: 了解详细信息：自定义工作流设计体验
title: 自定义工作流设计体验
ms.date: 03/30/2017
helpviewer_keywords:
- extending [WF], Workflow Designer
ms.assetid: 98135077-0f5d-4d16-9337-01094e843537
ms.openlocfilehash: 02049f8b42de3de6e4dfdfe8a4151be1500bcca9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742649"
---
# <a name="customizing-the-workflow-design-experience"></a><span data-ttu-id="1dc73-103">自定义工作流设计体验</span><span class="sxs-lookup"><span data-stu-id="1dc73-103">Customizing the Workflow Design Experience</span></span>

<span data-ttu-id="1dc73-104">用于设计自定义活动和重新承载 Windows 工作流设计器的方案在 .NET Framework 4 中已大大简化。</span><span class="sxs-lookup"><span data-stu-id="1dc73-104">The scenarios for designing custom activities and for rehosting the Windows Workflow Designer have been greatly simplified in .NET Framework 4.</span></span> <span data-ttu-id="1dc73-105">现在，开发和部署工作变得更轻松、更灵活。</span><span class="sxs-lookup"><span data-stu-id="1dc73-105">Development and deployment are now both easier and more flexible.</span></span> <span data-ttu-id="1dc73-106">关键的基础结构变化在于，新的活动设计器编程模型是基于 Windows Presentation Foundation (WPF) 生成的。</span><span class="sxs-lookup"><span data-stu-id="1dc73-106">The key infrastructural change is that the new activity designer programming model is built upon Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="1dc73-107">这使你能够以声明方式定义活动设计器，并在比较轻松的其他应用程序中 rehost 工作流设计器。</span><span class="sxs-lookup"><span data-stu-id="1dc73-107">This gives you the ability to define activity designers declaratively and to rehost the Workflow Designer in other applications with comparative easy.</span></span> <span data-ttu-id="1dc73-108">在重新承载时，可以开发自定义表达式编辑器来支持 IntelliSense 或简化的表达式域。</span><span class="sxs-lookup"><span data-stu-id="1dc73-108">When rehosting, a custom expression editor can be developed to support IntelliSense or a simplified expression domain.</span></span> <span data-ttu-id="1dc73-109">使用工作流服务，与 Windows Communication Foundation (WCF) 的集成变得更加顺畅。</span><span class="sxs-lookup"><span data-stu-id="1dc73-109">The integration with Windows Communication Foundation (WCF) has become more seamless with use of workflow services.</span></span> <span data-ttu-id="1dc73-110">可使用自定义活动设计器和模型项树来增强重新承载的工作流设计器中的设计时体验。</span><span class="sxs-lookup"><span data-stu-id="1dc73-110">Custom activity designers and the Model Item Tree can be used to enhance design time experiences in rehosted workflow designers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1dc73-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="1dc73-111">In This Section</span></span>

 [<span data-ttu-id="1dc73-112">使用自定义活动设计器和模板</span><span class="sxs-lookup"><span data-stu-id="1dc73-112">Using Custom Activity Designers and Templates</span></span>](using-custom-activity-designers-and-templates.md)

 <span data-ttu-id="1dc73-113">介绍如何创建新的自定义活动设计器和模板。</span><span class="sxs-lookup"><span data-stu-id="1dc73-113">Describes how to create new custom activity designers and templates.</span></span>

 [<span data-ttu-id="1dc73-114">重新承载工作流设计器</span><span class="sxs-lookup"><span data-stu-id="1dc73-114">Rehosting the Workflow Designer</span></span>](rehosting-the-workflow-designer.md)

 <span data-ttu-id="1dc73-115">介绍如何在 Visual Studio 外部重新托管 Windows 工作流设计器以及如何显示验证错误。</span><span class="sxs-lookup"><span data-stu-id="1dc73-115">Describes how to re-host the Windows Workflow Designer outside of Visual Studio and how to display validation errors.</span></span>

 [<span data-ttu-id="1dc73-116">使用自定义表达式编辑器</span><span class="sxs-lookup"><span data-stu-id="1dc73-116">Using a Custom Expression Editor</span></span>](using-a-custom-expression-editor.md)

 <span data-ttu-id="1dc73-117">介绍如何实现自定义表达式编辑器，以便在 Visual Studio 2010 之外的重新承载工作流设计器中使用。</span><span class="sxs-lookup"><span data-stu-id="1dc73-117">Describes how to implement a custom expression editor to use with workflow designers rehosted outside of Visual Studio 2010.</span></span>

## <a name="reference"></a><span data-ttu-id="1dc73-118">参考</span><span class="sxs-lookup"><span data-stu-id="1dc73-118">Reference</span></span>

<xref:System.Activities.Presentation.ActivityDesigner>

## <a name="see-also"></a><span data-ttu-id="1dc73-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="1dc73-119">See also</span></span>

- [<span data-ttu-id="1dc73-120">扩展 Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="1dc73-120">Extending Windows Workflow Foundation</span></span>](extend.md)
- [<span data-ttu-id="1dc73-121">Designer</span><span class="sxs-lookup"><span data-stu-id="1dc73-121">Designer</span></span>](./samples/designer.md)
- [<span data-ttu-id="1dc73-122">自定义活动设计器</span><span class="sxs-lookup"><span data-stu-id="1dc73-122">Custom Activity Designers</span></span>](./samples/custom-activity-designers.md)
- [<span data-ttu-id="1dc73-123">设计器重新承载</span><span class="sxs-lookup"><span data-stu-id="1dc73-123">Designer ReHosting</span></span>](./samples/designer-rehosting.md)
