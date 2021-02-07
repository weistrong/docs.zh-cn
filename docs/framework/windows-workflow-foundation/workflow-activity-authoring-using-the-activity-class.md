---
description: 了解详细信息：使用活动类创作工作流活动
title: 使用 Activity 类的工作流活动创作
ms.date: 03/30/2017
ms.assetid: 7b7b1c66-f093-43c3-b4d1-7173b46516da
ms.openlocfilehash: 0d3ffc88bacfd941dfa0c853991bf72045468323
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754935"
---
# <a name="workflow-activity-authoring-using-the-activity-class"></a><span data-ttu-id="ee2b6-103">使用 Activity 类的工作流活动创作</span><span class="sxs-lookup"><span data-stu-id="ee2b6-103">Workflow Activity Authoring Using the Activity Class</span></span>

<span data-ttu-id="ee2b6-104">使用 Windows Workflow Foundation (WF) 创建活动的最基本方法 [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] 是创建一个继承自的类，该类 <xref:System.Activities.Activity> 通过从 [内置活动库](net-framework-4-5-built-in-activity-library.md)中组合自定义活动或活动来创建功能。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-104">The most basic way to create an activity using Windows Workflow Foundation (WF) in [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] is to create a class that inherits from <xref:System.Activities.Activity> that creates functionality by assembling custom activities or activities from the [Built-In Activity Library](net-framework-4-5-built-in-activity-library.md).</span></span> <span data-ttu-id="ee2b6-105">本主题演示如何创建向控制台写入两个消息的活动。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-105">This topic demonstrates how to create an activity that writes two messages to the console.</span></span>

### <a name="to-create-a-custom-activity-using-the-activity-designer"></a><span data-ttu-id="ee2b6-106">使用活动设计器创建自定义活动</span><span class="sxs-lookup"><span data-stu-id="ee2b6-106">To create a custom Activity using the activity designer</span></span>

1. <span data-ttu-id="ee2b6-107">打开 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-107">Open Visual Studio 2012.</span></span>

2. <span data-ttu-id="ee2b6-108">依次选择“文件”、“新建”和“项目”。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-108">Select File, New, Project.</span></span> <span data-ttu-id="ee2b6-109">在 "**项目类型**" 窗口中的 " **Visual c #** " 下选择 " **Workflow 4.0** "，然后选择 " **v2010** " 节点。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-109">Select **Workflow 4.0** under **Visual C#** in the **Project Types** window, and select the **v2010** node.</span></span> <span data-ttu-id="ee2b6-110">在 "**模板**" 窗口中选择 "**活动库**"。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-110">Select **Activity Library** in the **Templates** window.</span></span> <span data-ttu-id="ee2b6-111">将新项目命名为 HelloActivity。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-111">Name the new project HelloActivity.</span></span>

3. <span data-ttu-id="ee2b6-112">打开新的活动。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-112">Open the new activity.</span></span>  <span data-ttu-id="ee2b6-113">将 <xref:System.Activities.Statements.Sequence> 活动从工具箱拖到设计器图面。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-113">Drag a <xref:System.Activities.Statements.Sequence> activity from the toolbox onto the designer surface.</span></span>

4. <span data-ttu-id="ee2b6-114">将 <xref:System.Activities.Statements.WriteLine> 活动拖到 <xref:System.Activities.Statements.Sequence> 活动中。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-114">Drag a <xref:System.Activities.Statements.WriteLine> activity into the <xref:System.Activities.Statements.Sequence> activity.</span></span> <span data-ttu-id="ee2b6-115">`"Hello World"`在 "**文本**" 字段中输入引号)  (。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-115">Enter `"Hello World"` (with quotes) into the **Text** field.</span></span>

5. <span data-ttu-id="ee2b6-116">将第二个 <xref:System.Activities.Statements.WriteLine> 活动拖到 <xref:System.Activities.Statements.Sequence> 活动中并将其放置在第一个活动的下面。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-116">Drag a second <xref:System.Activities.Statements.WriteLine> activity into the <xref:System.Activities.Statements.Sequence> activity, below the first one.</span></span> <span data-ttu-id="ee2b6-117">`"Goodbye"`在 "**文本**" 字段中输入引号)  (。</span><span class="sxs-lookup"><span data-stu-id="ee2b6-117">Enter `"Goodbye"` (with quotes) into the **Text** field.</span></span>
