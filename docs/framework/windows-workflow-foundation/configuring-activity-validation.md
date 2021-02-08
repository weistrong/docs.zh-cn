---
description: 了解详细信息：配置活动验证
title: 配置活动验证
ms.date: 03/30/2017
ms.assetid: 25a4eccb-b8fc-4857-a01d-2683b6341219
ms.openlocfilehash: 9e40842a18dd2afd9a5ec0104d66e8971d691b5f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792747"
---
# <a name="configuring-activity-validation"></a><span data-ttu-id="b5ea4-103">配置活动验证</span><span class="sxs-lookup"><span data-stu-id="b5ea4-103">Configuring Activity Validation</span></span>

<span data-ttu-id="b5ea4-104">通过活动验证，活动作者和用户可以在执行活动配置之前标识和报告此配置中的错误。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-104">Activity validation enables activity authors and users to identify and report errors in an activity’s configuration prior to its execution.</span></span> <span data-ttu-id="b5ea4-105">Windows Workflow Foundation (WF) 提供了以下三种类型的活动验证：</span><span class="sxs-lookup"><span data-stu-id="b5ea4-105">Windows Workflow Foundation (WF) provides the following three types of activity validation:</span></span>  
  
- <span data-ttu-id="b5ea4-106">`RequiredArgument` 和 `OverloadGroup` 特性。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-106">`RequiredArgument` and `OverloadGroup` attributes.</span></span>  
  
- <span data-ttu-id="b5ea4-107">基于命令性代码的验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-107">Imperative code-based validation.</span></span>  
  
- <span data-ttu-id="b5ea4-108">声明性约束。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-108">Declarative constraints.</span></span>  
  
 <span data-ttu-id="b5ea4-109">`RequiredArgument` 和 `OverloadGroup` 特性指示活动中的特定自变量是必需的。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-109">`RequiredArgument` and `OverloadGroup` attributes indicate that certain arguments on an activity are required.</span></span> <span data-ttu-id="b5ea4-110">基于命令性代码的验证为活动提供围绕其自身进行验证的简单方法，声明性约束支持围绕活动及其与包含工作流之间的关系进行验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-110">Imperative code-based validation provides a simple way for an activity to provide validation about itself, and declarative constraints enable validation about the activity and its relationship with the containing workflow.</span></span> <span data-ttu-id="b5ea4-111">如果未根据验证需求正确配置活动，将返回验证错误和警告。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-111">If an activity is not configured properly according to the validation requirements, validation errors and warnings are returned.</span></span> <span data-ttu-id="b5ea4-112">如果包含工作流是使用工作流设计器创建的，则会在设计器中显示所有验证错误和警告。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-112">If the containing workflow is created using the workflow designer, any validation errors and warnings are displayed in the designer.</span></span> <span data-ttu-id="b5ea4-113">如果工作流不是使用工作流设计器创建的，则会在调用工作流时返回任何验证错误。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-113">If the workflow is created outside of the workflow designer any validation errors are returned when the workflow is invoked.</span></span> <span data-ttu-id="b5ea4-114">不管工作流的创建方式如何，绝不允许执行带有验证错误的工作流。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-114">Regardless of how the workflow was created, a workflow with validation errors is never allowed to execute.</span></span> <span data-ttu-id="b5ea4-115">本节概述了这些活动验证类型及其调用方法。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-115">This section provides an overview of these types of activity validation and how activity validation is invoked.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b5ea4-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="b5ea4-116">In This Section</span></span>  

 [<span data-ttu-id="b5ea4-117">必需自变量和重载组</span><span class="sxs-lookup"><span data-stu-id="b5ea4-117">Required Arguments and Overload Groups</span></span>](required-arguments-and-overload-groups.md)  
 <span data-ttu-id="b5ea4-118">介绍如何使用 `RequiredArgument` 和 `OverloadGroup` 特性提供验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-118">Describes how to use the `RequiredArgument` and `OverloadGroup` attributes to provide validation.</span></span>  
  
 [<span data-ttu-id="b5ea4-119">基于命令性代码的验证</span><span class="sxs-lookup"><span data-stu-id="b5ea4-119">Imperative Code-Based Validation</span></span>](imperative-code-based-validation.md)  
 <span data-ttu-id="b5ea4-120">介绍如何对基于 <xref:System.Activities.CodeActivity> 和 <xref:System.Activities.NativeActivity> 的活动使用基于代码的验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-120">Describes how to use code-based validation for <xref:System.Activities.CodeActivity> and <xref:System.Activities.NativeActivity> based activities.</span></span>  
  
 [<span data-ttu-id="b5ea4-121">声明性约束</span><span class="sxs-lookup"><span data-stu-id="b5ea4-121">Declarative Constraints</span></span>](declarative-constraints.md)  
 <span data-ttu-id="b5ea4-122">介绍如何使用声明性约束提供复杂活动验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-122">Describes how to use declarative constraints to provide complex activity validation.</span></span>  
  
 [<span data-ttu-id="b5ea4-123">调用活动验证</span><span class="sxs-lookup"><span data-stu-id="b5ea4-123">Invoking Activity Validation</span></span>](invoking-activity-validation.md)  
 <span data-ttu-id="b5ea4-124">讨论何时自动调用活动验证以及如何显式调用验证。</span><span class="sxs-lookup"><span data-stu-id="b5ea4-124">Discusses when activity validation is invoked automatically and how to explicitly invoke validation.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b5ea4-125">参考</span><span class="sxs-lookup"><span data-stu-id="b5ea4-125">Reference</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="b5ea4-126">相关章节</span><span class="sxs-lookup"><span data-stu-id="b5ea4-126">Related Sections</span></span>
