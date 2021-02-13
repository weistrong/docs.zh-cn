---
ms.openlocfilehash: 3275865cf7f4669ba7deaacea320136d02f64dda
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804207"
---

如果收到类似于“找不到包 {dotnet-package}”或“无法安装某些包”的错误消息，请运行以下命令 。

以下命令组中有两个占位符。

- `{dotnet-package}`\
此项表示要安装的 .NET 包，如 `aspnetcore-runtime-3.1`。 它在以下 `sudo apt-get install` 命令中使用。

- `{os-version}`\
这表示你正在使用的发行版。 此项在以下 `wget` 命令中使用。 发行版是数值，如 Ubuntu 上的 `20.04` 或 Debian 上的 `10`。

首先，尝试清除包列表：

```bash
sudo dpkg --purge packages-microsoft-prod && sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update
```

然后，再次尝试安装 .NET。 如果这不起作用，可使用以下命令运行手动安装：
