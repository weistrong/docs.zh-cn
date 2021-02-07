---
description: 了解详细信息：如何：创建自定义活动模板
title: 如何：创建自定义活动模板
ms.date: 03/30/2017
ms.assetid: 6760a5cc-6eb8-465f-b4fa-f89b39539429
ms.openlocfilehash: 06fda953110e36e46a91fda8697aadbcd6e6bf59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742103"
---
# <a name="how-to-create-a-custom-activity-template"></a><span data-ttu-id="dfbdb-103">如何：创建自定义活动模板</span><span class="sxs-lookup"><span data-stu-id="dfbdb-103">How to: Create a Custom Activity Template</span></span>

<span data-ttu-id="dfbdb-104">可使用自定义活动模板来自定义活动（包括自定义复合活动）的配置，使用户无需单独创建每个活动并手动配置其属性和其他设置。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-104">Custom activity templates are used to customize the configuration of activities, including custom composite activities, so that users do not have to create each activity individually and configure their properties and other settings manually.</span></span> <span data-ttu-id="dfbdb-105">可在 Windows 工作流设计器上的 " **工具箱** " 中或从重新承载的设计器中使用这些自定义模板，用户可将这些模板拖到预配置的设计图面。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-105">These custom templates can be made available in the **Toolbox** on the Windows Workflow Designer or from a rehosted designer, from which users can drag them onto the preconfigured design surface.</span></span> <span data-ttu-id="dfbdb-106">工作流设计器附带了此类模板的良好示例： "[消息传递活动设计](/visualstudio/workflow-designer/messaging-activity-designers)器" 类别中的[SendAndReceiveReply 模板设计](/visualstudio/workflow-designer/sendandreceivereply-template-designer)器和[ReceiveAndSendReply 模板设计器](/visualstudio/workflow-designer/receiveandsendreply-template-designer)。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-106">Workflow Designer ships with good examples of such templates: the [SendAndReceiveReply Template Designer](/visualstudio/workflow-designer/sendandreceivereply-template-designer) and the [ReceiveAndSendReply Template Designer](/visualstudio/workflow-designer/receiveandsendreply-template-designer) in the [Messaging Activity Designers](/visualstudio/workflow-designer/messaging-activity-designers) category.</span></span>

 <span data-ttu-id="dfbdb-107">本主题中的第一个过程介绍如何为 **Delay** 活动创建自定义活动模板，第二个过程简要介绍了如何在工作流设计器中使用它来验证自定义模板是否正常工作。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-107">The first procedure in this topic describes how to create a custom activity template for a **Delay** activity and the second procedure describes briefly how to make it available in a Workflow Designer to verify that the custom template works.</span></span>

 <span data-ttu-id="dfbdb-108">自定义活动模板必须实现 <xref:System.Activities.Presentation.IActivityTemplateFactory>。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-108">Custom activity templates must implement the <xref:System.Activities.Presentation.IActivityTemplateFactory>.</span></span> <span data-ttu-id="dfbdb-109">此接口具有一个 <xref:System.Activities.Presentation.IActivityTemplateFactory.Create%2A> 方法，可利用此方法创建和配置模板中使用的活动实例。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-109">The interface has a single <xref:System.Activities.Presentation.IActivityTemplateFactory.Create%2A> method with which you can create and configure the activity instances used in the template.</span></span>

## <a name="to-create-a-template-for-the-delay-activity"></a><span data-ttu-id="dfbdb-110">为 Delay 活动创建模板</span><span class="sxs-lookup"><span data-stu-id="dfbdb-110">To create a template for the Delay activity</span></span>

1. <span data-ttu-id="dfbdb-111">启动 Visual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-111">Start Visual Studio 2010.</span></span>

2. <span data-ttu-id="dfbdb-112">在 **“文件”** 菜单上，指向 **“新建”**，然后选择 **“项目”**。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-112">On the **File** menu, point to **New**, and then select **Project**.</span></span>

     <span data-ttu-id="dfbdb-113">**“新建项目”** 对话框随即打开。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-113">The **New Project** dialog box opens.</span></span>

3. <span data-ttu-id="dfbdb-114">在 "**项目类型**" 窗格中，从 **Visual c #** 项目或 **Visual Basic** 分组选择 "**工作流**"，具体取决于你的语言首选项。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-114">In the **Project Types** pane, select **Workflow** from either the **Visual C#** projects or **Visual Basic** groupings depending on your language preference.</span></span>

4. <span data-ttu-id="dfbdb-115">在 " **模板** " 窗格中选择 " **活动库**"。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-115">In the **Templates** pane, select **Activity Library**.</span></span>

5. <span data-ttu-id="dfbdb-116">在“名称”框中，输入 `DelayActivityTemplate`。 </span><span class="sxs-lookup"><span data-stu-id="dfbdb-116">In the **Name** box, enter `DelayActivityTemplate`.</span></span>

6. <span data-ttu-id="dfbdb-117">接受 " **位置** " 和 " **解决方案名称** " 文本框中的默认值，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-117">Accept the defaults in the **Location** and **Solution name** text boxes, and then click **OK**.</span></span>

7. <span data-ttu-id="dfbdb-118">在 **解决方案资源管理器** 中右键单击 "DelayActivityTemplate" 项目的 "引用" 目录，然后选择 " **添加引用** " 以打开 " **添加引用** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-118">Right-click the References directory of the DelayActivityTemplate project in **Solution Explorer** and choose **Add Reference** to open the **Add Reference** dialog box.</span></span>

8. <span data-ttu-id="dfbdb-119">使用 " **.net** " 选项卡，从左侧的 "**组件名称**" 列中选择 " **PresentationFramework** "，然后单击 **"确定"** 以添加对 PresentationFramework.dll 文件的引用。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-119">Go to the **.NET** tab and select **PresentationFramework** from the **Component Name** column on the left and click **OK** to add a reference to the PresentationFramework.dll file.</span></span>

9. <span data-ttu-id="dfbdb-120">重复此过程以添加对 System.Activities.Presentation.dll 文件和 WindowsBase.dll 文件的引用。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-120">Repeat this procedure to add references to the System.Activities.Presentation.dll and the WindowsBase.dll files.</span></span>

10. <span data-ttu-id="dfbdb-121">在 **解决方案资源管理器** 中右键单击 "DelayActivityTemplate" 项目，然后依次选择 " **添加** " 和 " **新建项** " 以打开 " **添加新项** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-121">Right-click the DelayActivityTemplate project in **Solution Explorer** and choose **Add** and then **New Item** to open the **Add New Item** dialog box.</span></span>

11. <span data-ttu-id="dfbdb-122">选择 " **类** " 模板，将其命名为 "MyDelayTemplate"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-122">Select the **Class** template, name it MyDelayTemplate, and then click **OK**.</span></span>

12. <span data-ttu-id="dfbdb-123">打开 MyDelayTemplate.cs 文件并添加下面的语句。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-123">Open the MyDelayTemplate.cs file and add the following statements.</span></span>

    ```csharp
    //Namespaces added
    using System.Activities;
    using System.Activities.Statements;
    using System.Activities.Presentation;
    using System.Windows;
    ```

13. <span data-ttu-id="dfbdb-124">使用带有以下代码的 <xref:System.Activities.Presentation.IActivityTemplateFactory> 类来实现 `MyDelayActivity`。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-124">Implement the <xref:System.Activities.Presentation.IActivityTemplateFactory> with the `MyDelayActivity` class with the following code.</span></span> <span data-ttu-id="dfbdb-125">这会将延迟时间配置为 10 秒。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-125">This configures the delay to have a duration of 10 seconds.</span></span>

    ```csharp
    public sealed class MyDelayActivity : IActivityTemplateFactory
    {
        public Activity Create(System.Windows.DependencyObject target)
        {
            return new System.Activities.Statements.Delay
            {
                DisplayName = "DelayActivityTemplate",
                Duration = new TimeSpan(0, 0, 10)

            };
        }
    }
    ```

14. <span data-ttu-id="dfbdb-126">从 "**生成**" 菜单中选择 "**生成解决方案**"，生成 DelayActivityTemplate.dll 文件。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-126">Select **Build Solution** from the **Build** menu to generate the DelayActivityTemplate.dll file.</span></span>

### <a name="to-make-the-template-available-in-a-workflow-designer"></a><span data-ttu-id="dfbdb-127">使模板在工作流设计器中可用</span><span class="sxs-lookup"><span data-stu-id="dfbdb-127">To make the template available in a Workflow Designer</span></span>

1. <span data-ttu-id="dfbdb-128">在 **解决方案资源管理器** 中右键单击 "DelayActivityTemplate" 解决方案，然后依次选择 " **添加** "、" **新建项目** "，以打开 " **添加新项目** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-128">Right-click the DelayActivityTemplate solution in **Solution Explorer** and choose **Add** and then **New Project** to open the **Add New Project** dialog box.</span></span>

2. <span data-ttu-id="dfbdb-129">选择 " **工作流控制台应用程序** " 模板，将其命名为 `CustomActivityTemplateApp` ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-129">Select the **Workflow Console Application** template, name it `CustomActivityTemplateApp`, and then click **OK**.</span></span>

3. <span data-ttu-id="dfbdb-130">在 **解决方案资源管理器** 中右键单击 "右击 customactivitytemplateapp" 项目的 "引用" 目录，然后选择 " **添加引用** " 以打开 " **添加引用** " 对话框。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-130">Right-click the References directory of the CustomActivityTemplateApp project in **Solution Explorer** and choose **Add Reference** to open the **Add Reference** dialog box.</span></span>

4. <span data-ttu-id="dfbdb-131">中转到 "**项目**" 选项卡，从左侧的 "**项目名称**" 列中选择 " **DelayActivityTemplate** "，然后单击 **"确定"** 以添加对您在第一个过程中创建的 DelayActivityTemplate.dll 文件的引用。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-131">Go to the **Projects** tab and select **DelayActivityTemplate** from the **Project Name** column on the left and click **OK** to add a reference to the DelayActivityTemplate.dll file that you created in the first procedure.</span></span>

5. <span data-ttu-id="dfbdb-132">在 **解决方案资源管理器** 中右键单击 "右击 customactivitytemplateapp" 项目，然后选择 " **生成** " 以编译该应用程序。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-132">Right-click the CustomActivityTemplateApp project in **Solution Explorer** and choose **Build** to compile the application.</span></span>

6. <span data-ttu-id="dfbdb-133">在 **解决方案资源管理器** 中右键单击 "右击 customactivitytemplateapp" 项目，然后选择 " **设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-133">Right-click the CustomActivityTemplateApp project in **Solution Explorer** and choose **Set as Startup Project**.</span></span>

7. <span data-ttu-id="dfbdb-134">从 "**调试**" 菜单中选择 "**启动（不调试**）"，然后在出现 cmd.exe 窗口中的提示时，按任意键继续。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-134">Select **Start Without Debugging** from the **Debug** menu and press any key to continue when prompted from the cmd.exe window.</span></span>

8. <span data-ttu-id="dfbdb-135">打开 Workflow1.xaml 文件并打开 " **工具箱**"。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-135">Open the Workflow1.xaml file and open the **Toolbox**.</span></span>

9. <span data-ttu-id="dfbdb-136">在 **DelayActivityTemplate** 类别中找到 **MyDelayActivity** 模板。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-136">Locate the **MyDelayActivity** template in the **DelayActivityTemplate** category.</span></span> <span data-ttu-id="dfbdb-137">将此模板拖动到设计图面上。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-137">Drag it onto the design surface.</span></span> <span data-ttu-id="dfbdb-138">在 " **属性** " 窗口中确认 `Duration` 属性已设置为10秒。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-138">Confirm in the **Properties** window that the `Duration` property has been set to 10 seconds.</span></span>

## <a name="example"></a><span data-ttu-id="dfbdb-139">示例</span><span class="sxs-lookup"><span data-stu-id="dfbdb-139">Example</span></span>

 <span data-ttu-id="dfbdb-140">MyDelayActivity.cs 文件应包含以下代码。</span><span class="sxs-lookup"><span data-stu-id="dfbdb-140">The MyDelayActivity.cs file should contain the following code.</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

//Namespaces added
using System.Activities;
using System.Activities.Statements;
using System.Activities.Presentation;
using System.Windows;

namespace DelayActivityTemplate
{
    public sealed class MyDelayActivity : IActivityTemplateFactory
    {
        public Activity Create(System.Windows.DependencyObject target)
        {
            return new System.Activities.Statements.Delay
            {
                DisplayName = "DelayActivityTemplate",
                Duration = new TimeSpan(0, 0, 10)

            };
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dfbdb-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="dfbdb-141">See also</span></span>

- <xref:System.Activities.Presentation.IActivityTemplateFactory>
- [<span data-ttu-id="dfbdb-142">自定义工作流设计体验</span><span class="sxs-lookup"><span data-stu-id="dfbdb-142">Customizing the Workflow Design Experience</span></span>](customizing-the-workflow-design-experience.md)
