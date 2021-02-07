---
description: 了解详细信息：终结点：调用出错
title: 终结点：Calls Faulted（出错的调用次数）
ms.date: 03/30/2017
ms.assetid: 271e6284-9c4b-465f-b619-069e1555a5e4
ms.openlocfilehash: c1e65582f39a8512bb62b41044d49d32d9d38743
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759583"
---
# <a name="endpoint-calls-faulted"></a>终结点：Calls Faulted（出错的调用次数）

计数器名称：Calls Faulted（出错的调用次数）。  
  
## <a name="description"></a>说明  

 对此终结点返回错误的调用次数。 在 Windows Communication Foundation (WCF) 应用程序中，服务方法使用 SOAP 错误消息来传递处理错误信息。 SOAP 错误是包括在服务操作元数据中的消息类型，因此会创建一个错误协定，客户端可使用该协定来使执行更加可靠或更具交互性。 由于 SOAP 错误在客户端以 XML 格式表示，因此具有高度的互操作性。  
  
## <a name="see-also"></a>请参阅

- [在协定和服务中指定和处理错误](../../specifying-and-handling-faults-in-contracts-and-services.md)
