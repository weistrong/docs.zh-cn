---
ms.openlocfilehash: 5a027054024d8429831d73525ab3748c51ae850e
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102255746"
---

使用包管理器进行安装时，将为你安装这些库。 但是，如果手动安装 .NET Core 或发布自包含的应用，则需要确保已安装以下库：

- krb5-libs
- libicu
- openssl-libs
- zlib

如果目标运行时环境的 OpenSSL 版本为1.1 或更高版本，则需要安装 compat-openssl10。

有关依赖项的详细信息，请参阅[独立式 Linux 应用](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)。

对于使用 System.Drawing.Common 程序集的 .NET Core 应用，还需要以下依赖项：

- [libgdiplus（版本 6.0.1 或更高版本）](https://www.mono-project.com/docs/gui/libgdiplus/)

  > [!WARNING]
  > 可以通过将 Mono 存储库添加到系统来安装最新版 libgdiplus。 有关详细信息，请参阅 <https://www.mono-project.com/download/stable/>。
