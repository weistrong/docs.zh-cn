---
description: 了解详细信息：使用 TryCatch 在 Flowchart 活动中进行错误处理
title: 使用 TryCatch 在 Flowchart 活动中进行错误处理
ms.date: 03/30/2017
ms.assetid: 50922964-bfe0-4ba8-9422-0e7220d514fd
ms.openlocfilehash: 9ab323117e5b26696a07624117e8acc8c0beacff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755325"
---
# <a name="fault-handling-in-a-flowchart-activity-using-trycatch"></a><span data-ttu-id="37036-103">使用 TryCatch 在 Flowchart 活动中进行错误处理</span><span class="sxs-lookup"><span data-stu-id="37036-103">Fault Handling in a Flowchart Activity Using TryCatch</span></span>

<span data-ttu-id="37036-104">此示例演示如何在复杂控制流活动中使用 <xref:System.Activities.Statements.TryCatch> 活动。</span><span class="sxs-lookup"><span data-stu-id="37036-104">This sample shows how the <xref:System.Activities.Statements.TryCatch> activity can be used within a complex control flow activity.</span></span>

<span data-ttu-id="37036-105">在此示例中，将促销代码和孩子数量作为变量传递到 <xref:System.Activities.Statements.Flowchart> 活动，该活动将根据与促销代码相对应的公式计算折扣。</span><span class="sxs-lookup"><span data-stu-id="37036-105">In this sample, a promotion code and number of children are passed as variables to a <xref:System.Activities.Statements.Flowchart> activity that calculates a discount based on formulae that correspond to the promotion code.</span></span> <span data-ttu-id="37036-106">此示例分为命令性代码版本和工作流设计器版本。 </span><span class="sxs-lookup"><span data-stu-id="37036-106">The sample includes imperative code and workflow designer versions of the sample.</span></span>

<span data-ttu-id="37036-107">下表详细描述了 `CreateFlowchartWithFaults` 活动的变量。</span><span class="sxs-lookup"><span data-stu-id="37036-107">The following table details the variables for the `CreateFlowchartWithFaults` activity.</span></span>

|<span data-ttu-id="37036-108">参数</span><span class="sxs-lookup"><span data-stu-id="37036-108">Parameters</span></span>|<span data-ttu-id="37036-109">说明</span><span class="sxs-lookup"><span data-stu-id="37036-109">Description</span></span>|
|----------------|-----------------|
|<span data-ttu-id="37036-110">promoCode</span><span class="sxs-lookup"><span data-stu-id="37036-110">promoCode</span></span>|<span data-ttu-id="37036-111">促销代码。</span><span class="sxs-lookup"><span data-stu-id="37036-111">The promotion code.</span></span> <span data-ttu-id="37036-112">键入：String</span><span class="sxs-lookup"><span data-stu-id="37036-112">Type: String</span></span><br /><br /> <span data-ttu-id="37036-113">可能的值，括号中带有说明：</span><span class="sxs-lookup"><span data-stu-id="37036-113">The possible values with description in parentheses:</span></span><br /><br /> <span data-ttu-id="37036-114">-单一 (单个) </span><span class="sxs-lookup"><span data-stu-id="37036-114">-   Single (Single)</span></span><br /><span data-ttu-id="37036-115">-MNK (结婚，无孩子。 ) </span><span class="sxs-lookup"><span data-stu-id="37036-115">-   MNK (Married with no kids.)</span></span><br /><span data-ttu-id="37036-116">-MWK (结婚。 ) </span><span class="sxs-lookup"><span data-stu-id="37036-116">-   MWK (Married with kids.)</span></span>|
|<span data-ttu-id="37036-117">numKids</span><span class="sxs-lookup"><span data-stu-id="37036-117">numKids</span></span>|<span data-ttu-id="37036-118">孩子数量。</span><span class="sxs-lookup"><span data-stu-id="37036-118">The number of children.</span></span> <span data-ttu-id="37036-119">类型：int</span><span class="sxs-lookup"><span data-stu-id="37036-119">Type: int</span></span>|

<span data-ttu-id="37036-120">`CreateFlowchartWithFaults` 活动使用 <xref:System.Activities.Statements.FlowSwitch%601> 活动，后者根据 `promoCode` 参数进行切换并使用以下公式计算折扣。</span><span class="sxs-lookup"><span data-stu-id="37036-120">The `CreateFlowchartWithFaults` activity uses a <xref:System.Activities.Statements.FlowSwitch%601> activity that switches on the `promoCode` argument and calculates the discount using the following formula.</span></span>

|<span data-ttu-id="37036-121">`promoCode` 的值</span><span class="sxs-lookup"><span data-stu-id="37036-121">Value of `promoCode`</span></span>|<span data-ttu-id="37036-122">折扣 (%)</span><span class="sxs-lookup"><span data-stu-id="37036-122">Discount (%)</span></span>|
|--------------------------|--------------------|
|<span data-ttu-id="37036-123">Single</span><span class="sxs-lookup"><span data-stu-id="37036-123">Single</span></span>|<span data-ttu-id="37036-124">10</span><span class="sxs-lookup"><span data-stu-id="37036-124">10</span></span>|
|<span data-ttu-id="37036-125">MNK</span><span class="sxs-lookup"><span data-stu-id="37036-125">MNK</span></span>|<span data-ttu-id="37036-126">15</span><span class="sxs-lookup"><span data-stu-id="37036-126">15</span></span>|
|<span data-ttu-id="37036-127">MWK</span><span class="sxs-lookup"><span data-stu-id="37036-127">MWK</span></span>|<span data-ttu-id="37036-128">15 + (1 – 1/ `numberOfKids`) \* 10 **注意：**  此计算可能会引发 <xref:System.DivideByZeroException> 。</span><span class="sxs-lookup"><span data-stu-id="37036-128">15 + (1 – 1/`numberOfKids`)\*10 **Note:**  Potentially, this calculation can throw a <xref:System.DivideByZeroException>.</span></span> <span data-ttu-id="37036-129">因此，将折扣计算包装在 <xref:System.Activities.Statements.TryCatch> 活动中，该活动可捕获 <xref:System.DivideByZeroException> 异常并将折扣设置为零。</span><span class="sxs-lookup"><span data-stu-id="37036-129">So, the discount calculation is wrapped in a <xref:System.Activities.Statements.TryCatch> activity that catches the <xref:System.DivideByZeroException> exception and sets the discount to zero.</span></span>|

#### <a name="to-use-this-sample"></a><span data-ttu-id="37036-130">使用此示例</span><span class="sxs-lookup"><span data-stu-id="37036-130">To use this sample</span></span>

1. <span data-ttu-id="37036-131">使用 Visual Studio 2010 打开 FlowchartWithFaultHandling 解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="37036-131">Using Visual Studio 2010, open the FlowchartWithFaultHandling.sln solution file.</span></span>

2. <span data-ttu-id="37036-132">要生成解决方案，按 Ctrl+Shift+B。</span><span class="sxs-lookup"><span data-stu-id="37036-132">To build the solution, press CTRL+SHIFT+B.</span></span>

3. <span data-ttu-id="37036-133">若要运行解决方案，请按 F5。</span><span class="sxs-lookup"><span data-stu-id="37036-133">To run the solution, press F5.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37036-134">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="37036-134">The samples may already be installed on your computer.</span></span> <span data-ttu-id="37036-135">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="37036-135">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="37036-136">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="37036-136">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="37036-137">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="37036-137">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\FlowChartWithFaultHandling`

## <a name="see-also"></a><span data-ttu-id="37036-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="37036-138">See also</span></span>

- [<span data-ttu-id="37036-139">流程图工作流</span><span class="sxs-lookup"><span data-stu-id="37036-139">Flowchart Workflows</span></span>](../flowchart-workflows.md)
- [<span data-ttu-id="37036-140">异常</span><span class="sxs-lookup"><span data-stu-id="37036-140">Exceptions</span></span>](../exceptions.md)
