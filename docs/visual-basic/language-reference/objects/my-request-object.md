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
# <a name="myrequest-object"></a><span data-ttu-id="821e0-103">My.Request 对象</span><span class="sxs-lookup"><span data-stu-id="821e0-103">My.Request Object</span></span>

<span data-ttu-id="821e0-104">获取所请求的页面的 <xref:System.Web.HttpRequest> 对象。</span><span class="sxs-lookup"><span data-stu-id="821e0-104">Gets the <xref:System.Web.HttpRequest> object for the requested page.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="821e0-105">备注</span><span class="sxs-lookup"><span data-stu-id="821e0-105">Remarks</span></span>  

 <span data-ttu-id="821e0-106">`My.Request` 对象包含当前 HTTP 请求的相关信息。</span><span class="sxs-lookup"><span data-stu-id="821e0-106">The `My.Request` object contains information about the current HTTP request.</span></span>  
  
 <span data-ttu-id="821e0-107">`My.Request` 对象仅适用于 ASP.NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="821e0-107">The `My.Request` object is available only for ASP.NET applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="821e0-108">示例</span><span class="sxs-lookup"><span data-stu-id="821e0-108">Example</span></span>  

 <span data-ttu-id="821e0-109">下面的示例从对象获取标头集合 `My.Request` ，并使用 `My.Response` 对象将其写入到 ASP.NET 页。</span><span class="sxs-lookup"><span data-stu-id="821e0-109">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-aspx-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a><span data-ttu-id="821e0-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="821e0-110">See also</span></span>

- <xref:System.Web.HttpRequest>
- [<span data-ttu-id="821e0-111">My.Response 对象</span><span class="sxs-lookup"><span data-stu-id="821e0-111">My.Response Object</span></span>](my-response-object.md)
