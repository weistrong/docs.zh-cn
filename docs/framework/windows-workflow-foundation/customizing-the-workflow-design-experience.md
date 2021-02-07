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
# <a name="customizing-the-workflow-design-experience"></a>自定义工作流设计体验

用于设计自定义活动和重新承载 Windows 工作流设计器的方案在 .NET Framework 4 中已大大简化。 现在，开发和部署工作变得更轻松、更灵活。 关键的基础结构变化在于，新的活动设计器编程模型是基于 Windows Presentation Foundation (WPF) 生成的。 这使你能够以声明方式定义活动设计器，并在比较轻松的其他应用程序中 rehost 工作流设计器。 在重新承载时，可以开发自定义表达式编辑器来支持 IntelliSense 或简化的表达式域。 使用工作流服务，与 Windows Communication Foundation (WCF) 的集成变得更加顺畅。 可使用自定义活动设计器和模型项树来增强重新承载的工作流设计器中的设计时体验。

## <a name="in-this-section"></a>本节内容

 [使用自定义活动设计器和模板](using-custom-activity-designers-and-templates.md)

 介绍如何创建新的自定义活动设计器和模板。

 [重新承载工作流设计器](rehosting-the-workflow-designer.md)

 介绍如何在 Visual Studio 外部重新托管 Windows 工作流设计器以及如何显示验证错误。

 [使用自定义表达式编辑器](using-a-custom-expression-editor.md)

 介绍如何实现自定义表达式编辑器，以便在 Visual Studio 2010 之外的重新承载工作流设计器中使用。

## <a name="reference"></a>参考

<xref:System.Activities.Presentation.ActivityDesigner>

## <a name="see-also"></a>请参阅

- [扩展 Windows Workflow Foundation](extend.md)
- [Designer](./samples/designer.md)
- [自定义活动设计器](./samples/custom-activity-designers.md)
- [设计器重新承载](./samples/designer-rehosting.md)
