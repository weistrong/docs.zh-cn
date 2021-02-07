---
description: '了解更多相关信息：自定义数据服务提供程序 (WCF Data Services) '
title: 自定义数据服务提供程序（WCF 数据服务）
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, providers
ms.assetid: e702ecdb-3419-4743-92a9-c3c0e7d44082
ms.openlocfilehash: df0cafae46cfdbd71a96341686a9200f032a9938
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99766148"
---
# <a name="custom-data-service-providers-wcf-data-services"></a>自定义数据服务提供程序（WCF 数据服务）

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

WCF Data Services 包括一组提供程序，使您能够基于后期绑定数据类型定义数据模型。  
  
|提供程序|描述|  
|--------------|-----------------|  
|元数据提供程序|这是核心的自定义数据服务提供程序，用于通过实现 <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> 接口在运行时定义自定义数据模型。|  
|查询提供程序|该提供程序用于对使用 <xref:System.Data.Services.Providers.IDataServiceMetadataProvider> 接口定义的自定义数据模型执行查询。 查询提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceQueryProvider> 接口而创建。|  
|更新提供程序|该提供程序用于更新在自定义数据服务提供程序中公开的类型和管理并发性。 更新提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceUpdateProvider> 接口而创建。|  
|分页提供程序|该提供程序用于与自定义数据服务提供程序一起启用服务器驱动的分页支持。 自定义数据服务的分页提供程序通过实现 <xref:System.Data.Services.Providers.IDataServicePagingProvider> 接口而创建。|  
|流提供程序|此提供程序用于以流形式公开二进制大型对象数据类型。 流提供程序通过实现 <xref:System.Data.Services.Providers.IDataServiceStreamProvider> 接口而创建。 流提供程序还可与实体框架提供程序和反射数据源提供程序一起使用。 有关详细信息，请参阅 [流式处理提供程序](streaming-provider-wcf-data-services.md)。|  
  
## <a name="see-also"></a>请参阅

- [数据服务提供程序](data-services-providers-wcf-data-services.md)
- [实体框架提供程序](entity-framework-provider-wcf-data-services.md)
- [反射提供程序](reflection-provider-wcf-data-services.md)
