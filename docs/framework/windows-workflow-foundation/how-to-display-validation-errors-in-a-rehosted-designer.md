---
description: 了解详细信息：如何：在重新承载设计器中显示验证错误
title: 如何：在重新承载的设计器中显示验证错误
ms.date: 03/30/2017
ms.assetid: 5aa8fb53-8f75-433b-bc06-7c7d33583d5d
ms.openlocfilehash: 75ff45e6e9a81df96a9940ce21d1b160cab1000e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777731"
---
# <a name="how-to-display-validation-errors-in-a-rehosted-designer"></a><span data-ttu-id="9665f-103">如何：在重新承载的设计器中显示验证错误</span><span class="sxs-lookup"><span data-stu-id="9665f-103">How to: Display Validation Errors in a Rehosted Designer</span></span>

<span data-ttu-id="9665f-104">本主题介绍如何在重新承载 Windows 工作流设计器中检索和发布验证错误。</span><span class="sxs-lookup"><span data-stu-id="9665f-104">This topic describes how to retrieve and publish validation errors in a rehosted Windows Workflow Designer.</span></span> <span data-ttu-id="9665f-105">这为我们提供了一个用于确认重新承载的设计器中的工作流是否有效的过程。</span><span class="sxs-lookup"><span data-stu-id="9665f-105">This provides us with a procedure to confirm that a workflow in a rehosted designer is valid.</span></span>  
  
 <span data-ttu-id="9665f-106">此任务包含两个部分。</span><span class="sxs-lookup"><span data-stu-id="9665f-106">This task has two parts.</span></span> <span data-ttu-id="9665f-107">第一部分提供一个实现 <xref:System.Activities.Presentation.Validation.IValidationErrorService>。</span><span class="sxs-lookup"><span data-stu-id="9665f-107">The first is to provide an implementation <xref:System.Activities.Presentation.Validation.IValidationErrorService>.</span></span>  <span data-ttu-id="9665f-108">在此接口上要实现一个关键方法 <xref:System.Activities.Presentation.Validation.IValidationErrorService.ShowValidationErrors%2A>，该方法将一个包含有关错误的信息的 <xref:System.Activities.Presentation.Validation.ValidationErrorInfo> 对象的列表传递给调试日志。</span><span class="sxs-lookup"><span data-stu-id="9665f-108">There is one critical method to implement on this interface, <xref:System.Activities.Presentation.Validation.IValidationErrorService.ShowValidationErrors%2A> which will pass you a list of <xref:System.Activities.Presentation.Validation.ValidationErrorInfo> objects containing information about the errors to the debug log.</span></span>  <span data-ttu-id="9665f-109">实现此接口之后，可通过将该实现的实例发布到编辑上下文来检索错误信息。</span><span class="sxs-lookup"><span data-stu-id="9665f-109">After implementing the interface, you retrieve the error information by publishing an instance of that implementation to the editing context.</span></span>  
  
### <a name="implement-the-ivalidationerrorservice-interface"></a><span data-ttu-id="9665f-110">实现 IValidationErrorService 接口</span><span class="sxs-lookup"><span data-stu-id="9665f-110">Implement the IValidationErrorService Interface</span></span>  
  
1. <span data-ttu-id="9665f-111">下面是一个将验证错误写入调试日志的简单实现的代码示例。</span><span class="sxs-lookup"><span data-stu-id="9665f-111">Here is a code sample for a simple implementation that will write out the validation errors to the debug log.</span></span>  
  
    ```csharp  
    using System.Activities.Presentation.Validation;  
    using System.Collections.Generic;  
    using System.Diagnostics;  
    using System.Linq;  
  
    namespace VariableFinderShell  
    {  
        class DebugValidationErrorService : IValidationErrorService  
        {  
            public void ShowValidationErrors(IList<ValidationErrorInfo> errors)  
            {  
                errors.ToList().ForEach(vei => Debug.WriteLine($"Error: {vei.Message}"));  
            }  
        }  
    }  
    ```  
  
### <a name="publishing-to-the-editing-context"></a><span data-ttu-id="9665f-112">发布到编辑上下文</span><span class="sxs-lookup"><span data-stu-id="9665f-112">Publishing to the Editing Context</span></span>  
  
1. <span data-ttu-id="9665f-113">下面是将此内容发布到编辑上下文的代码。</span><span class="sxs-lookup"><span data-stu-id="9665f-113">Here is the code that will publish this to the editing context.</span></span>  
  
    ```csharp  
    wd.Context.Services.Publish<IValidationErrorService>(new DebugValidationErrorService());  
    ```
