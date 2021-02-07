---
description: 了解详细信息：受限并行 ForEach
title: 限制并行 ForEach
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: 2c1d1386f0b8c5b3c68d60bc83386ccfdf5e7875
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741674"
---
# <a name="throttled-parallel-foreach"></a>限制并行 ForEach

`ThrottleParallelForEach` 活动类似于 <xref:System.Activities.Statements.ParallelForEach%601> 活动，不同之处在于前者允许设置并发系数来限制要执行的并发分支的数目。 `ThrottleParallelForEach` 活动派生自 <xref:System.Activities.NativeActivity>，因为该活动需要对其他活动（子活动）进行计划，并且只有通过 <xref:System.Activities.NativeActivityContext> 类才能对此进行访问。

## <a name="projects"></a>项目

|**ProjectName**|**说明**|**主要文件**|
|-|-|-|
|ThrottledParallelForEach|包含 `ThrottledParallelForEach` 活动及其设计器。|ThrottledParallelForEach.cs<br /><br /> `ThrottledParallelForEach` 活动定义。|
|CodeTestClient|示例客户端应用程序，通过使用命令性代码的 `ThrottledParallelForEach` 来配置和运行工作流。|Program.cs<br /><br /> 定义和运行示例工作流的实例。|

## <a name="to-use-this-sample"></a>使用此示例

1. 使用 Visual Studio 2010 打开 ThrottledParallelForEach 文件。

2. 要生成解决方案，按 Ctrl+Shift+B。

3. 若要运行解决方案，请按 F5。

> [!IMPORTANT]
> 您的计算机上可能已安装这些示例。 在继续操作之前，请先检查以下（默认）目录：
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> 如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)] 此示例位于以下目录：
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`
