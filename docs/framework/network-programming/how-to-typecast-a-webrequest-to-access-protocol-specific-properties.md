---
description: 详细了解：操作说明：转换 WebRequest 以访问协议特定属性
title: 如何：转换 WebRequest 以访问特定于协议的属性
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d9a8eae2-7454-46f9-b43b-c98477c5bcde
ms.openlocfilehash: 24c07a3f2d77dec180476dec3c58f07b40e00c8f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662736"
---
# <a name="how-to-typecast-a-webrequest-to-access-protocol-specific-properties"></a>如何：转换 WebRequest 以访问协议特定属性

此示例演示如何类型转换 WebRequest 以访问特定于协议的属性。  
  
## <a name="example"></a>示例  
  
```csharp  
HttpWebRequest httpreq =
   (HttpWebRequest) WebRequest.Create("http://www.contoso.com/");  
```  
  
```vb  
Dim httpreq As HttpWebRequest = _  
   CType(WebRequest.Create("http://www.contoso.com/"), HttpWebRequest)  
```  
  
## <a name="see-also"></a>请参阅

- [对可插入协议进行编程](programming-pluggable-protocols.md)
