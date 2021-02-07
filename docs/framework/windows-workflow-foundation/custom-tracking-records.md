---
description: 了解详细信息：自定义跟踪记录
title: 自定义跟踪记录
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: 9d6988465fa3afca4302c86e0c2cad2778f2beae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742688"
---
# <a name="custom-tracking-records"></a><span data-ttu-id="2de03-103">自定义跟踪记录</span><span class="sxs-lookup"><span data-stu-id="2de03-103">Custom Tracking Records</span></span>

<span data-ttu-id="2de03-104">本主题演示如何创建自定义跟踪记录并在这些记录中填入将与其一起发出的数据。</span><span class="sxs-lookup"><span data-stu-id="2de03-104">This topic demonstrates how to create custom tracking records and populate them with data to be emitted along with the records.</span></span>

## <a name="emitting-custom-tracking-records"></a><span data-ttu-id="2de03-105">发出自定义跟踪记录</span><span class="sxs-lookup"><span data-stu-id="2de03-105">Emitting Custom Tracking Records</span></span>

<span data-ttu-id="2de03-106">可以从代码活动中发出自定义跟踪记录，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="2de03-106">Custom tracking records can be emitted from a code activity as shown in the following example.</span></span>

```csharp
protected override void Execute(CodeActivityContext context)
{
…
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");
            customRecord.Data.Add("SendTime", sendTime);
            context.Track(customRecord);
}
```

<span data-ttu-id="2de03-107">通过对 <xref:System.Activities.Tracking.CustomTrackingRecord> 调用 <xref:System.Activities.NativeActivityContext.Track%2A> 方法，在代码活动中发出 `ActivityContext`。</span><span class="sxs-lookup"><span data-stu-id="2de03-107">A <xref:System.Activities.Tracking.CustomTrackingRecord> is emitted in a code activity by invoking the <xref:System.Activities.NativeActivityContext.Track%2A> method on the `ActivityContext`.</span></span>

## <a name="see-also"></a><span data-ttu-id="2de03-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="2de03-108">See also</span></span>

- <span data-ttu-id="2de03-109">[Windows Server App Fabric 监视](/previous-versions/appfabric/ee677251(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="2de03-109">[Windows Server App Fabric Monitoring](/previous-versions/appfabric/ee677251(v=azure.10))</span></span>
- <span data-ttu-id="2de03-110">[用 App Fabric 监视应用程序](/previous-versions/appfabric/ee677276(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="2de03-110">[Monitoring Applications with App Fabric](/previous-versions/appfabric/ee677276(v=azure.10))</span></span>
