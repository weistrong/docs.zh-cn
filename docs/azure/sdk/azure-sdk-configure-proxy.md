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
# <a name="configure-a-proxy-server-when-using-the-azure-sdk-for-net"></a><span data-ttu-id="7a56e-103">在使用用于 .NET 的 Azure SDK 时配置代理服务器</span><span class="sxs-lookup"><span data-stu-id="7a56e-103">Configure a proxy server when using the Azure SDK for .NET</span></span>

<span data-ttu-id="7a56e-104">如果你的组织要求使用代理服务器来访问 Internet 资源，你将需要使用代理服务器信息设置环境变量，以便使用用于 .NET 的 Azure SDK。</span><span class="sxs-lookup"><span data-stu-id="7a56e-104">If your organization requires the use of a proxy server to access internet resources, you will need to set an environment variable with the proxy server information to use the Azure SDK for .NET.</span></span>  

## <a name="configuration-using-environment-variables"></a><span data-ttu-id="7a56e-105">使用环境变量进行配置</span><span class="sxs-lookup"><span data-stu-id="7a56e-105">Configuration using environment variables</span></span>

<span data-ttu-id="7a56e-106">根据代理服务器使用的是 HTTP 还是 HTTPS，你将分别设置环境变量 `HTTP_PROXY` 或 `HTTPS_PROXY`。</span><span class="sxs-lookup"><span data-stu-id="7a56e-106">Depending on if your proxy server uses HTTP or HTTPS, you will set either the environment variable `HTTP_PROXY` or `HTTPS_PROXY` respectively.</span></span> <span data-ttu-id="7a56e-107">代理服务器 URL 的格式为 `http[s]://[username:password@]<ip_address_or_hostname>:<port>/`，其中 `username:password` 组合是可选的。</span><span class="sxs-lookup"><span data-stu-id="7a56e-107">The proxy server URL has the form `http[s]://[username:password@]<ip_address_or_hostname>:<port>/` where the `username:password` combination is optional.</span></span> <span data-ttu-id="7a56e-108">若要获取代理服务器的 IP 地址或主机名、端口和凭据，请与网络管理员联系。</span><span class="sxs-lookup"><span data-stu-id="7a56e-108">To get the IP address or hostname, port and credentials for your proxy server, consult your network administrator.</span></span>

<span data-ttu-id="7a56e-109">下面的示例演示如何在命令行界面 (Windows) 和 bash (Linux/Mac) 环境中设置适当的环境变量。</span><span class="sxs-lookup"><span data-stu-id="7a56e-109">The following examples show how to set the appropriate environment variables in command shell (Windows) and bash (Linux/Mac) environments.</span></span>  <span data-ttu-id="7a56e-110">设置适当的环境变量之后，用于 .NET 的 Azure SDK 便会在运行时使用代理服务器。</span><span class="sxs-lookup"><span data-stu-id="7a56e-110">Setting the appropriate environment variable will then cause the Azure SDK for .NET to use the proxy server at runtime.</span></span>

### <a name="cmd"></a>[<span data-ttu-id="7a56e-111">cmd</span><span class="sxs-lookup"><span data-stu-id="7a56e-111">cmd</span></span>](#tab/cmd)

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

### <a name="bash"></a>[<span data-ttu-id="7a56e-112">bash</span><span class="sxs-lookup"><span data-stu-id="7a56e-112">bash</span></span>](#tab/bash)

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
