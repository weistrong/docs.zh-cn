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
# <a name="custom-tracking-records"></a>自定义跟踪记录

本主题演示如何创建自定义跟踪记录并在这些记录中填入将与其一起发出的数据。

## <a name="emitting-custom-tracking-records"></a>发出自定义跟踪记录

可以从代码活动中发出自定义跟踪记录，如下面的示例所示。

```csharp
protected override void Execute(CodeActivityContext context)
{
…
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");
            customRecord.Data.Add("SendTime", sendTime);
            context.Track(customRecord);
}
```

通过对 <xref:System.Activities.Tracking.CustomTrackingRecord> 调用 <xref:System.Activities.NativeActivityContext.Track%2A> 方法，在代码活动中发出 `ActivityContext`。

## <a name="see-also"></a>请参阅

- [Windows Server App Fabric 监视](/previous-versions/appfabric/ee677251(v=azure.10))
- [用 App Fabric 监视应用程序](/previous-versions/appfabric/ee677276(v=azure.10))
