---
description: 了解详细信息：从 XAML 加载
title: 从 XAML 加载
ms.date: 03/30/2017
ms.assetid: 1f103ef6-7bed-4f16-ae52-9e665c5a43d7
ms.openlocfilehash: fd0eca487c0245c7bfa46ca80c06f2adfa577353
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742025"
---
# <a name="load-from-xaml"></a><span data-ttu-id="7bfd4-103">从 XAML 加载</span><span class="sxs-lookup"><span data-stu-id="7bfd4-103">Load From XAML</span></span>

<span data-ttu-id="7bfd4-104">此示例演示如何在不运行 XamlBuildTask 工具的情况下动态加载 XAML 工作流。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-104">This sample demonstrates how to dynamically load a XAML workflow without having to run the XamlBuildTask tool.</span></span> <span data-ttu-id="7bfd4-105">此示例改为调用 <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-105">Instead, the sample calls the <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A> method.</span></span> <span data-ttu-id="7bfd4-106">该示例是一个 Windows Presentation Foundation (WPF) 客户端应用程序，该应用程序使用类加载 XAML 工作流 <xref:System.Activities.XamlIntegration.ActivityXamlServices> 并执行这些工作流。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-106">The sample is a Windows Presentation Foundation (WPF) client application that loads XAML workflows using the <xref:System.Activities.XamlIntegration.ActivityXamlServices> class and executes them.</span></span> <span data-ttu-id="7bfd4-107">在使用 <xref:System.Activities.XamlIntegration.ActivityXamlServices> 类加载完这些工作流后，将返回一个可执行的 <xref:System.Activities.DynamicActivity%601>。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-107">After they have been loaded using the <xref:System.Activities.XamlIntegration.ActivityXamlServices> class, a <xref:System.Activities.DynamicActivity%601> is returned that can be executed.</span></span>

#### <a name="to-use-this-sample"></a><span data-ttu-id="7bfd4-108">使用此示例</span><span class="sxs-lookup"><span data-stu-id="7bfd4-108">To use this sample</span></span>

1. <span data-ttu-id="7bfd4-109">使用 Visual Studio 2010 打开 LoadFromXAML 解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-109">Using Visual Studio 2010, open the LoadFromXAML.sln solution file.</span></span>

2. <span data-ttu-id="7bfd4-110">要生成解决方案，按 Ctrl+Shift+B。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-110">To build the solution, press CTRL+SHIFT+B.</span></span>

3. <span data-ttu-id="7bfd4-111">若要运行解决方案，请按 Ctrl+F5。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-111">To run the solution, press CTRL+F5.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bfd4-112">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="7bfd4-112">The samples may already be installed on your machine.</span></span> <span data-ttu-id="7bfd4-113">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="7bfd4-113">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="7bfd4-114">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7bfd4-114">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="7bfd4-115">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="7bfd4-115">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\DynamicActivity\LoadFromXAML`
