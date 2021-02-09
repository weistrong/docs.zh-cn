---
description: 详细了解：操作说明：当应用程序启动或关闭时记录消息 (Visual Basic)
title: 如何：在应用程序启动或关闭时记录消息
ms.date: 07/20/2015
helpviewer_keywords:
- event logs, shutdown
- My.Application.Log object, logging
- Startup event [Visual Basic]
- event logs, startup
- Shutdown event [Visual Basic]
- My.Log object, logging
ms.assetid: 67624d05-cddf-48b7-8c36-5c99baa4c621
ms.openlocfilehash: 545a57c3666aa12e3763961d05067face9fe324a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99775183"
---
# <a name="how-to-log-messages-when-the-application-starts-or-shuts-down-visual-basic"></a><span data-ttu-id="8c972-103">如何：当应用程序启动或关闭时记录消息 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8c972-103">How to: Log Messages When the Application Starts or Shuts Down (Visual Basic)</span></span>

<span data-ttu-id="8c972-104">可以使用 `My.Application.Log` 和 `My.Log` 对象来记录有关应用程序中所发生事件的信息。</span><span class="sxs-lookup"><span data-stu-id="8c972-104">You can use the `My.Application.Log` and `My.Log` objects to log information about events that occur in your application.</span></span> <span data-ttu-id="8c972-105">本示例将演示如何结合使用 `My.Application.Log.WriteEntry` 方法与 `Startup` 和 `Shutdown` 事件来写入跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="8c972-105">This example shows how to use the `My.Application.Log.WriteEntry` method with the `Startup` and `Shutdown` events to write tracing information.</span></span>  
  
### <a name="to-access-the-applications-event-handler-code"></a><span data-ttu-id="8c972-106">访问应用程序的事件处理程序代码</span><span class="sxs-lookup"><span data-stu-id="8c972-106">To access the application's event-handler code</span></span>  
  
1. <span data-ttu-id="8c972-107">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="8c972-107">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="8c972-108">在 **“项目”** 菜单上，选择 **“属性”** 。</span><span class="sxs-lookup"><span data-stu-id="8c972-108">On the **Project** menu, choose **Properties**.</span></span>  
  
2. <span data-ttu-id="8c972-109">单击“应用程序”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="8c972-109">Click the **Application** tab.</span></span>  
  
3. <span data-ttu-id="8c972-110">单击“查看应用程序事件”  按钮，打开“代码编辑器”。</span><span class="sxs-lookup"><span data-stu-id="8c972-110">Click the **View Application Events** button to open the Code Editor.</span></span>  
  
     <span data-ttu-id="8c972-111">此时将打开 ApplicationEvents.vb 文件。</span><span class="sxs-lookup"><span data-stu-id="8c972-111">This opens the ApplicationEvents.vb file.</span></span>  
  
### <a name="to-log-messages-when-the-application-starts"></a><span data-ttu-id="8c972-112">在应用程序启动时记录消息</span><span class="sxs-lookup"><span data-stu-id="8c972-112">To log messages when the application starts</span></span>  
  
1. <span data-ttu-id="8c972-113">在“代码编辑器”中打开 ApplicationEvents.vb 文件。</span><span class="sxs-lookup"><span data-stu-id="8c972-113">Have the ApplicationEvents.vb file open in the Code Editor.</span></span> <span data-ttu-id="8c972-114">在“常规”  菜单上，选择“MyApplication 事件” 。</span><span class="sxs-lookup"><span data-stu-id="8c972-114">On the **General** menu, choose **MyApplication Events**.</span></span>  
  
2. <span data-ttu-id="8c972-115">在“声明”  菜单上，选择“启动” 。</span><span class="sxs-lookup"><span data-stu-id="8c972-115">On the **Declarations** menu, choose **Startup**.</span></span>  
  
     <span data-ttu-id="8c972-116">在主应用程序运行之前，应用程序将引发 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> 事件。</span><span class="sxs-lookup"><span data-stu-id="8c972-116">The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> event before the main application runs.</span></span>  
  
3. <span data-ttu-id="8c972-117">将 `My.Application.Log.WriteEntry` 方法添加到 `Startup` 事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="8c972-117">Add the `My.Application.Log.WriteEntry` method to the `Startup` event handler.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#1)]  
  
### <a name="to-log-messages-when-the-application-shuts-down"></a><span data-ttu-id="8c972-118">在应用程序关闭时记录消息</span><span class="sxs-lookup"><span data-stu-id="8c972-118">To log messages when the application shuts down</span></span>  
  
1. <span data-ttu-id="8c972-119">在“代码编辑器”中打开 ApplicationEvents.vb 文件。</span><span class="sxs-lookup"><span data-stu-id="8c972-119">Have the ApplicationEvents.vb file open in the Code Editor.</span></span> <span data-ttu-id="8c972-120">在“常规”  菜单上，选择“MyApplication 事件” 。</span><span class="sxs-lookup"><span data-stu-id="8c972-120">On the **General** menu, choose **MyApplication Events**.</span></span>  
  
2. <span data-ttu-id="8c972-121">在“声明”  菜单上，选择“关闭” 。</span><span class="sxs-lookup"><span data-stu-id="8c972-121">On the **Declarations** menu, choose **Shutdown**.</span></span>  
  
     <span data-ttu-id="8c972-122">在主应用程序运行之后、关闭之前，应用程序将引发 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> 事件。</span><span class="sxs-lookup"><span data-stu-id="8c972-122">The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> event after the main application runs, but before it shuts down.</span></span>  
  
3. <span data-ttu-id="8c972-123">将 `My.Application.Log.WriteEntry` 方法添加到 `Shutdown` 事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="8c972-123">Add the `My.Application.Log.WriteEntry` method to the `Shutdown` event handler.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#2)]  
  
## <a name="example"></a><span data-ttu-id="8c972-124">示例</span><span class="sxs-lookup"><span data-stu-id="8c972-124">Example</span></span>  

 <span data-ttu-id="8c972-125">可以通过“项目设计器”  访问“代码编辑器”中的应用程序事件。</span><span class="sxs-lookup"><span data-stu-id="8c972-125">You can use the **Project Designer** to access the application events in the Code Editor.</span></span> <span data-ttu-id="8c972-126">有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。</span><span class="sxs-lookup"><span data-stu-id="8c972-126">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
 [!code-vb[VbVbalrMyApplicationLog#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="8c972-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c972-127">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [<span data-ttu-id="8c972-128">“项目设计器”->“应用程序”页 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8c972-128">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [<span data-ttu-id="8c972-129">使用应用程序日志</span><span class="sxs-lookup"><span data-stu-id="8c972-129">Working with Application Logs</span></span>](working-with-application-logs.md)
