---
description: 了解详细信息： My. Request 对象
title: My.Request 对象
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Request
- My.Request
helpviewer_keywords:
- My.Request object
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
ms.openlocfilehash: 0b72252e261cd033bfc35c546de5c53a4f3cfe2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640649"
---
# <a name="myrequest-object"></a>My.Request 对象

获取所请求的页面的 <xref:System.Web.HttpRequest> 对象。  
  
## <a name="remarks"></a>备注  

 `My.Request` 对象包含当前 HTTP 请求的相关信息。  
  
 `My.Request` 对象仅适用于 ASP.NET 应用程序。  
  
## <a name="example"></a>示例  

 下面的示例从对象获取标头集合 `My.Request` ，并使用 `My.Response` 对象将其写入到 ASP.NET 页。  
  
 [!code-aspx-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.Web.HttpRequest>
- [My.Response 对象](my-response-object.md)
