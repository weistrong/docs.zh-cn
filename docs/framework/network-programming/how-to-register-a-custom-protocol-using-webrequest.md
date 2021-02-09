---
description: 详细了解：操作说明：使用 WebRequest 注册自定义协议
title: 如何：使用 WebRequest 注册自定义协议
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 98ddbdb9-66b1-4080-92ad-51f5c447fcf8
ms.openlocfilehash: 7415017f20c0c6ed80570992e249fb8121907de2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785752"
---
# <a name="how-to-register-a-custom-protocol-using-webrequest"></a>如何：使用 WebRequest 注册自定义协议

此示例演示如何注册在其他位置定义的特定于协议的类。 在此示例中，`CustomWebRequestCreator` 是用户实现对象，它实现返回 `CustomWebRequest` 对象的“Create”方法。 此代码示例假定已编写了实现自定义协议的 `CustomWebRequest` 代码。  
  
## <a name="example"></a>示例  
  
```csharp  
WebRequest.RegisterPrefix("custom", new CustomWebRequestCreator());  
WebRequest req = WebRequest.Create("custom://customHost.contoso.com/");  
```  
  
```vb  
WebRequest.RegisterPrefix("custom", New CustomWebRequestCreator())  
Dim req As WebRequest = WebRequest.Create("custom://customHost.contoso.com/")  
```  
  
## <a name="compiling-the-code"></a>编译代码  

 此示例需要：  
  
 对 <xref:System.Net> 命名空间的引用。  
  
## <a name="see-also"></a>请参阅

- [对可插入协议进行编程](programming-pluggable-protocols.md)
