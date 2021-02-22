---
title: 如何：检索与 WebRequest 匹配的特定于协议的 WebResponse
description: 了解如何检索与 .NET Framework 中的 WebRequest 匹配的特定于协议的 WebResponse。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: 920704bedce478ed5a4f7906379a634a3b2a4e31
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100584340"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a><span data-ttu-id="c92da-103">如何：检索与 WebRequest 匹配的特定于协议的 WebResponse</span><span class="sxs-lookup"><span data-stu-id="c92da-103">How to: Retrieve a Protocol-Specific WebResponse that Matches a WebRequest</span></span>

<span data-ttu-id="c92da-104">此示例演示如何检索与 WebRequest 匹配的特定于协议的 WebResponse。</span><span class="sxs-lookup"><span data-stu-id="c92da-104">This example shows how to retrieve a protocol-specific WebResponse that matches a WebRequest.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c92da-105">示例</span><span class="sxs-lookup"><span data-stu-id="c92da-105">Example</span></span>  
  
```csharp  
HttpWebRequest req = (HttpWebRequest)WebRequest.Create("http://www.contoso.com/");
HttpWebResponse resp = (HttpWebResponse)req.GetResponse();
```  
  
```vb  
Dim req As HttpWebRequest = CType(WebRequest.Create("http://www.contoso.com"), HttpWebRequest)
Dim resp As HttpWebResponse = CType(req.GetResponse(), HttpWebResponse)
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c92da-106">编译代码</span><span class="sxs-lookup"><span data-stu-id="c92da-106">Compiling the Code</span></span>  

 <span data-ttu-id="c92da-107">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="c92da-107">This example requires:</span></span>  
  
- <span data-ttu-id="c92da-108">引用 System.Net 命名空间。</span><span class="sxs-lookup"><span data-stu-id="c92da-108">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c92da-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="c92da-109">See also</span></span>

- [<span data-ttu-id="c92da-110">请求数据</span><span class="sxs-lookup"><span data-stu-id="c92da-110">Requesting Data</span></span>](requesting-data.md)
