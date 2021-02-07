---
description: 了解详细信息：任务1：创建新的 Windows Presentation Foundation 应用程序
title: 任务 1：创建一个新的 Windows Presentation Foundation 应用程序
ms.date: 03/30/2017
ms.assetid: 270eaeba-9492-4532-af9f-403ce5c9935b
ms.openlocfilehash: 7bbb49e3d663d1878b2b3e150a24f775eeca0135
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755234"
---
# <a name="task-1-create-a-new-windows-presentation-foundation-application"></a><span data-ttu-id="2b682-103">任务 1：创建一个新的 Windows Presentation Foundation 应用程序</span><span class="sxs-lookup"><span data-stu-id="2b682-103">Task 1: Create a New Windows Presentation Foundation Application</span></span>

<span data-ttu-id="2b682-104">在此任务中，您将使用 WPF 应用程序 Visual Studio 模板创建一个空的 Windows Presentation Foundation (WPF) 应用程序，并添加对相应 [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] 工作流程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="2b682-104">In this task, you will create an empty Windows Presentation Foundation (WPF) application by using the WPF Application Visual Studio template and add references to the appropriate [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] workflow assemblies.</span></span>  
  
## <a name="to-create-the-wpf-application-project"></a><span data-ttu-id="2b682-105">创建 WPF 应用程序项目</span><span class="sxs-lookup"><span data-stu-id="2b682-105">To create the WPF Application project</span></span>

1. <span data-ttu-id="2b682-106">打开 Visual Studio，在 " **文件** " 菜单上，指向 " **新建**"，然后单击 " **项目**"。</span><span class="sxs-lookup"><span data-stu-id="2b682-106">Open Visual Studio and on the **File** menu, point to **New**, and then click **Project**.</span></span>

2. <span data-ttu-id="2b682-107">在 "**新建项目**" 对话框中，从框左侧的 "**已安装的模板**" 窗格中选择 " **Visual c #** " 或 " **Visual Basic** "。</span><span class="sxs-lookup"><span data-stu-id="2b682-107">In the **New Project** dialog box, select either **Visual C#** or **Visual Basic** from the **Installed Templates** pane on the left side of the box.</span></span> <span data-ttu-id="2b682-108">如果你选择的语言未显示，请在 " **其他语言**" 下查看。</span><span class="sxs-lookup"><span data-stu-id="2b682-108">If the language of your choice does not appear, look under **Other Languages**.</span></span>

3. <span data-ttu-id="2b682-109">在 "**已安装的模板**" 窗格中选择 "**窗口**"。</span><span class="sxs-lookup"><span data-stu-id="2b682-109">Select **Windows** in the **Installed Templates** pane.</span></span>

4. <span data-ttu-id="2b682-110">在顶部窗格中，确认已在下拉列表框中选择了 " (默认值) **.NET Framework 4** "，然后选择 " **WPF 应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="2b682-110">In the top pane, confirm that (the default value) **.NET Framework 4** has been selected in the drop-down list box, and then select **WPF Application**.</span></span>

5. <span data-ttu-id="2b682-111">在窗口底部，将项目的名称设置为 **HostingApplication** 。</span><span class="sxs-lookup"><span data-stu-id="2b682-111">Set the name of the project to **HostingApplication** at the bottom of the window.</span></span>

6. <span data-ttu-id="2b682-112">将解决方案名称设置为 **RehostingTheDesigner**。</span><span class="sxs-lookup"><span data-stu-id="2b682-112">Set the solution name to **RehostingTheDesigner**.</span></span>

7. <span data-ttu-id="2b682-113">单击 **"确定"** 以创建应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="2b682-113">Click **OK** to create the application project.</span></span> <span data-ttu-id="2b682-114">Visual Studio 为应用程序创建一个基本 WPF UI，并包含相应的 XAML 和代码隐藏文件。</span><span class="sxs-lookup"><span data-stu-id="2b682-114">Visual Studio creates a basic WPF UI for your application and includes the appropriate XAML and code-behind files.</span></span>

8. <span data-ttu-id="2b682-115">添加对 **WorkflowModel** 程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="2b682-115">Add references to **WorkflowModel** assemblies.</span></span> <span data-ttu-id="2b682-116">为此，请在 **解决方案资源管理器** 中，右键单击 **HostingApplication** 项目，然后选择 " **添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="2b682-116">To do this, in **Solution Explorer**, right-click the **HostingApplication** project and select **Add Reference**.</span></span>

9. <span data-ttu-id="2b682-117">在 " **添加引用** " 对话框中，单击 " **.net** " 选项卡，按住 CTRL 键，选择以下程序集，然后单击 **"确定"**：</span><span class="sxs-lookup"><span data-stu-id="2b682-117">In the **Add Reference** dialog box, click the **.NET** tab, hold down the CTRL key, select the following assemblies, and then click **OK**:</span></span>

    - <span data-ttu-id="2b682-118">System.Activities</span><span class="sxs-lookup"><span data-stu-id="2b682-118">System.Activities</span></span>
    - <span data-ttu-id="2b682-119">System.Activities.Presentation</span><span class="sxs-lookup"><span data-stu-id="2b682-119">System.Activities.Presentation</span></span>
    - <span data-ttu-id="2b682-120">System.Activities.Core.Presentation</span><span class="sxs-lookup"><span data-stu-id="2b682-120">System.Activities.Core.Presentation</span></span>

10. <span data-ttu-id="2b682-121">请参阅 [任务2：宿主工作流设计器](task-2-host-the-workflow-designer.md) 以了解如何承载工作流设计器设计画布。</span><span class="sxs-lookup"><span data-stu-id="2b682-121">See [Task 2: Host the Workflow Designer](task-2-host-the-workflow-designer.md) to learn how to host the workflow designer design canvas.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b682-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b682-122">See also</span></span>

- [<span data-ttu-id="2b682-123">重新承载工作流设计器</span><span class="sxs-lookup"><span data-stu-id="2b682-123">Rehosting the Workflow Designer</span></span>](rehosting-the-workflow-designer.md)
- [<span data-ttu-id="2b682-124">任务 2：承载工作流设计器</span><span class="sxs-lookup"><span data-stu-id="2b682-124">Task 2: Host the Workflow Designer</span></span>](task-2-host-the-workflow-designer.md)
