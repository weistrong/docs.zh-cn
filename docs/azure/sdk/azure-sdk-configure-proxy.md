---
title: 在使用用于 .NET 的 Azure SDK 时配置代理服务器
description: 使用 HTTP[S]_PROXY 环境变量为用于 .NET 的 Azure SDK 定义代理
ms.date: 12/10/2020
ms.topic: conceptual
ms.custom: devx-track-dotnet
ms.openlocfilehash: 64d525f8a6c277a5ac383dfded828f2fd3cfd744
ms.sourcegitcommit: 3d6d6595a03915f617349781f455f838a44b0f44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "97700889"
---
# <a name="configure-a-proxy-server-when-using-the-azure-sdk-for-net"></a>在使用用于 .NET 的 Azure SDK 时配置代理服务器

如果你的组织要求使用代理服务器来访问 Internet 资源，你将需要使用代理服务器信息设置环境变量，以便使用用于 .NET 的 Azure SDK。  

## <a name="configuration-using-environment-variables"></a>使用环境变量进行配置

根据代理服务器使用的是 HTTP 还是 HTTPS，你将分别设置环境变量 `HTTP_PROXY` 或 `HTTPS_PROXY`。 代理服务器 URL 的格式为 `http[s]://[username:password@]<ip_address_or_hostname>:<port>/`，其中 `username:password` 组合是可选的。 若要获取代理服务器的 IP 地址或主机名、端口和凭据，请与网络管理员联系。

下面的示例演示如何在命令行界面 (Windows) 和 bash (Linux/Mac) 环境中设置适当的环境变量。  设置适当的环境变量之后，用于 .NET 的 Azure SDK 便会在运行时使用代理服务器。

### <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
rem Non-authenticated HTTP server:
set HTTP_PROXY=http://10.10.1.10:1180

rem Authenticated HTTP server:
set HTTP_PROXY=http://username:password@10.10.1.10:1180

rem Non-authenticated HTTPS server:
set HTTPS_PROXY=http://10.10.1.10:1180

rem Authenticated HTTPS server:
set HTTPS_PROXY=http://username:password@10.10.1.10:1180
```

### <a name="bash"></a>[bash](#tab/bash)

```bash
# Non-authenticated HTTP server:
HTTP_PROXY=http://10.10.1.10:1180

# Authenticated HTTP server:
HTTP_PROXY=http://username:password@10.10.1.10:1180

# Non-authenticated HTTPS server:
HTTPS_PROXY=http://10.10.1.10:1180

# Authenticated HTTPS server:
HTTPS_PROXY=http://username:password@10.10.1.10:1180
```

---
