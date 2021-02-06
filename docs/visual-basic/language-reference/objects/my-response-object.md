---
description: 了解详细信息： My Response 对象
title: My.Response 对象
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 551528356040539994251cb66a905d0249f482da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640610"
---
# <a name="myresponse-object"></a>My.Response 对象

获取 <xref:System.Web.HttpResponse> 与关联的对象 <xref:System.Web.UI.Page> 。 使用此对象，可以将 HTTP 响应数据发送到客户端，并包含此响应的相关信息。  
  
## <a name="remarks"></a>备注  

 `My.Response`对象包含 <xref:System.Web.HttpResponse> 与页关联的当前对象。  
  
 `My.Response`对象仅适用于 ASP.NET 应用程序。  
  
## <a name="example"></a>示例  

 下面的示例从对象获取标头集合 `My.Request` ，并使用 `My.Response` 对象将其写入到 ASP.NET 页。  
  
 [!code-aspx-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.Web.HttpResponse>
- [My.Request 对象](my-request-object.md)
