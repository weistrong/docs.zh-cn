---
description: 了解更多：托管异常
title: 承载异常
ms.date: 03/30/2017
ms.assetid: ad9e14f8-fa17-4d59-b365-fe0e7ec17c98
ms.openlocfilehash: ba2ff3d4bd069483ddc620a09bb97eeaddf84a56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686448"
---
# <a name="hosting-exceptions"></a>承载异常

本主题列出了由承载生成的所有异常。  
  
## <a name="exception-list"></a>异常列表  
  
|资源代码|资源字符串|  
|-------------------|---------------------|  
|Hosting_AddressIsAbsoluteUri|不允许完整的 URI。 对于 ServiceHostingEnvironment.EnsureServiceAvailable API，不允许完整的 URI。 对相应的服务使用虚拟路径。|  
|Hosting_BuildProviderCouldNotCreateType|在服务编译期间，无法加载指定的 CLR 类型。 验证此类型是否在应用程序的 \ App_Code 目录中的源文件中定义 \\ ，该文件包含在位于应用程序的 \bin 目录中的已编译程序集中， \\ 或存在于全局程序集缓存中安装的程序集内。 类型名区分大小写。 诸如 \\ \ App_Code 和 \bin 这样的目录 \\ 必须位于应用程序的根目录中。 \\\ App_Code 和 \\ \bin 目录不能嵌套在子目录中。|
