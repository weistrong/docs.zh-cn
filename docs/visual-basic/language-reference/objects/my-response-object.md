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
# <a name="myresponse-object"></a><span data-ttu-id="9af57-103">My.Response 对象</span><span class="sxs-lookup"><span data-stu-id="9af57-103">My.Response Object</span></span>

<span data-ttu-id="9af57-104">获取 <xref:System.Web.HttpResponse> 与关联的对象 <xref:System.Web.UI.Page> 。</span><span class="sxs-lookup"><span data-stu-id="9af57-104">Gets the <xref:System.Web.HttpResponse> object associated with the <xref:System.Web.UI.Page>.</span></span> <span data-ttu-id="9af57-105">使用此对象，可以将 HTTP 响应数据发送到客户端，并包含此响应的相关信息。</span><span class="sxs-lookup"><span data-stu-id="9af57-105">This object allows you to send HTTP response data to a client and contains information about that response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9af57-106">备注</span><span class="sxs-lookup"><span data-stu-id="9af57-106">Remarks</span></span>  

 <span data-ttu-id="9af57-107">`My.Response`对象包含 <xref:System.Web.HttpResponse> 与页关联的当前对象。</span><span class="sxs-lookup"><span data-stu-id="9af57-107">The `My.Response` object contains the current <xref:System.Web.HttpResponse> object associated with the page.</span></span>  
  
 <span data-ttu-id="9af57-108">`My.Response`对象仅适用于 ASP.NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="9af57-108">The `My.Response` object is only available for ASP.NET applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9af57-109">示例</span><span class="sxs-lookup"><span data-stu-id="9af57-109">Example</span></span>  

 <span data-ttu-id="9af57-110">下面的示例从对象获取标头集合 `My.Request` ，并使用 `My.Response` 对象将其写入到 ASP.NET 页。</span><span class="sxs-lookup"><span data-stu-id="9af57-110">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-aspx-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a><span data-ttu-id="9af57-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="9af57-111">See also</span></span>

- <xref:System.Web.HttpResponse>
- [<span data-ttu-id="9af57-112">My.Request 对象</span><span class="sxs-lookup"><span data-stu-id="9af57-112">My.Request Object</span></span>](my-request-object.md)
