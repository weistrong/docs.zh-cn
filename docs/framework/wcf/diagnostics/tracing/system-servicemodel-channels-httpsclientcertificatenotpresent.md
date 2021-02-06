---
description: 了解有关以下方面的详细信息： HttpsClientCertificateNotPresent
title: System.ServiceModel.Channels.HttpsClientCertificateNotPresent
ms.date: 03/30/2017
ms.assetid: b13ef1b6-e340-401d-93ca-2710c3842205
ms.openlocfilehash: 1bca23915a55561c76b73c6b96750f324cb0e4dd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99654481"
---
# <a name="systemservicemodelchannelshttpsclientcertificatenotpresent"></a><span data-ttu-id="88107-103">System.ServiceModel.Channels.HttpsClientCertificateNotPresent</span><span class="sxs-lookup"><span data-stu-id="88107-103">System.ServiceModel.Channels.HttpsClientCertificateNotPresent</span></span>

<span data-ttu-id="88107-104">需要客户端证书。</span><span class="sxs-lookup"><span data-stu-id="88107-104">Client certificate is required.</span></span> <span data-ttu-id="88107-105">在请求中未找到任何证书。</span><span class="sxs-lookup"><span data-stu-id="88107-105">No certificate was found in the request.</span></span>  
  
## <a name="description"></a><span data-ttu-id="88107-106">说明</span><span class="sxs-lookup"><span data-stu-id="88107-106">Description</span></span>  

 <span data-ttu-id="88107-107">此跟踪指示 HTTPS 侦听器收到与客户端证书无关的 HTTPS 请求。</span><span class="sxs-lookup"><span data-stu-id="88107-107">This trace indicates that the HTTPS listener received an HTTPS request that was not associated with a client certificate.</span></span> <span data-ttu-id="88107-108">因为侦听器被配置为对所有 HTTPS 请求都要求提供客户端证书，所以侦听器未能验证该客户端的真实性。</span><span class="sxs-lookup"><span data-stu-id="88107-108">Since the listener was configured to require client certificates on all HTTPS requests, the listener failed to validate the client’s authenticity.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88107-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="88107-109">See also</span></span>

- [<span data-ttu-id="88107-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="88107-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="88107-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="88107-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="88107-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="88107-112">Administration and Diagnostics</span></span>](../index.md)
