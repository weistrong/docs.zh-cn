---
description: 了解详细信息：尚未指定启动窗体
title: 未指定启动窗体
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_NoStartupForm
ms.assetid: 8e04af49-4bef-49de-a7ec-e407e9873da7
ms.openlocfilehash: 4b00890f07121ef55ce49978842010cc54aba29b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797180"
---
# <a name="a-startup-form-has-not-been-specified"></a>未指定启动窗体

应用程序使用 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> 类，但不指定启动窗体。  
  
 如果在 "项目设计器" 中选择了 " **启用应用程序框架** " 复选框，但未指定 **启动窗体** ，则会发生这种情况。 有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 指定应用程序的启动对象。  
  
     有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。  
  
2. 重写 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> 方法，以将 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> 属性设置为启动窗体。  
  
## <a name="see-also"></a>请参阅

- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A>
- [Visual Basic 应用程序模型概述](../../developing-apps/development-with-my/overview-of-the-visual-basic-application-model.md)
