---
description: 了解详细信息： Internet Explorer 和 WCF 完成的服务证书验证之间的差异
title: Internet Explorer 完成的与 WCF 完成的服务证书验证之间的差异
ms.date: 03/30/2017
helpviewer_keywords:
- service certificate validation [WCF]
- certificates [WCF], service certificate validation
ms.assetid: 9dffcab2-70a9-40f0-99fd-d3a0b296028f
ms.openlocfilehash: 2d635aec0949ec4e65cd965089206bbf6d6815a6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756352"
---
# <a name="differences-between-service-certificate-validation-done-by-internet-explorer-and-wcf"></a>Internet Explorer 完成的与 WCF 完成的服务证书验证之间的差异

由于 Internet Explorer 和 Windows Communication Foundation (WCF) 在使用 HTTPS 时验证服务证书的方式不同，因此 Internet Explorer 将无法访问帮助页或服务的 Web 服务描述语言 (WSDL) ，即使 WCF 客户端可以成功地将消息发送到服务终结点也是如此。 这是因为 Internet Explorer 会检查服务证书是否在 `ServerAuthentication` 增强使用标志中 (OID) 了对象标识符，而 WCF 不会强制实施此类约束。 如果 Internet Explorer 无法访问服务帮助页或服务的 WSDL，请使用 "服务 [元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 访问服务元数据。  
  
## <a name="see-also"></a>请参阅

- [HTTPS、通过 TCP 的 SSL 与 SOAP 安全之间的证书验证差异](cert-val-diff-https-ssl-over-tcp-and-soap.md)
- [如何：检索元数据并实现兼容服务](how-to-retrieve-metadata-and-implement-a-compliant-service.md)
