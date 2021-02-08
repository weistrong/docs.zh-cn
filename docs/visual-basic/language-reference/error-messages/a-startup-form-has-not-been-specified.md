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
# <a name="a-startup-form-has-not-been-specified"></a><span data-ttu-id="836e2-103">未指定启动窗体</span><span class="sxs-lookup"><span data-stu-id="836e2-103">A startup form has not been specified</span></span>

<span data-ttu-id="836e2-104">应用程序使用 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> 类，但不指定启动窗体。</span><span class="sxs-lookup"><span data-stu-id="836e2-104">The application uses the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> class but does not specify the startup form.</span></span>  
  
 <span data-ttu-id="836e2-105">如果在 "项目设计器" 中选择了 " **启用应用程序框架** " 复选框，但未指定 **启动窗体** ，则会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="836e2-105">This can occur if the **Enable application framework** check box is selected in the project designer but the **Startup form** is not specified.</span></span> <span data-ttu-id="836e2-106">有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。</span><span class="sxs-lookup"><span data-stu-id="836e2-106">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="836e2-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="836e2-107">To correct this error</span></span>  
  
1. <span data-ttu-id="836e2-108">指定应用程序的启动对象。</span><span class="sxs-lookup"><span data-stu-id="836e2-108">Specify a startup object for the application.</span></span>  
  
     <span data-ttu-id="836e2-109">有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。</span><span class="sxs-lookup"><span data-stu-id="836e2-109">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
2. <span data-ttu-id="836e2-110">重写 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> 方法，以将 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> 属性设置为启动窗体。</span><span class="sxs-lookup"><span data-stu-id="836e2-110">Override the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> method to set the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> property to the startup form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="836e2-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="836e2-111">See also</span></span>

- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A>
- [<span data-ttu-id="836e2-112">Visual Basic 应用程序模型概述</span><span class="sxs-lookup"><span data-stu-id="836e2-112">Overview of the Visual Basic Application Model</span></span>](../../developing-apps/development-with-my/overview-of-the-visual-basic-application-model.md)
