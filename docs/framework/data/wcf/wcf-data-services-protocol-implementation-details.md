---
description: 了解详细信息： WCF Data Services 协议实现详细信息
title: WCF 数据服务协议实现详细信息
ms.date: 03/30/2017
ms.assetid: 712d689b-fada-4cbb-bcdb-d65a3ef83b4c
ms.openlocfilehash: 123f41859fdf579a75bb925a63619e4089577911
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748240"
---
# <a name="wcf-data-services-protocol-implementation-details"></a>WCF 数据服务协议实现详细信息

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

## <a name="odata-protocol-implementation-details"></a>OData 协议实现详细信息  

Open Data Protocol (OData) 要求实现协议的数据服务提供特定的最小功能集。 这些功能在协议文档中用 "应该" 和 "必须" 描述。 其他可选功能将根据 "可能" 进行描述。 本文介绍 WCF Data Services 当前未实现的这些可选功能。
  
### <a name="support-for-the-format-query-option"></a>对 $format 查询选项的支持  

 OData 协议支持 JavaScript 符号 (JSON) 和 Atom 馈送，并且 OData 提供 `$format` 系统查询选项，以允许客户端请求响应源的格式。 此系统查询选项（如果数据服务支持）必须重写请求的 Accept 标头的值。 WCF Data Services 支持同时返回 JSON 和 Atom 源。 但是，默认实现不支持 `$format` 查询选项，它只使用 Accept 标头的值来确定响应的格式。 某些情况下，您的数据服务可能需要支持 `$format` 查询选项，例如，当客户端不能设置 Accept 标头时。 为支持这些情况，您必须扩展您的数据服务以在 URI 中处理此选项。
  
## <a name="wcf-data-services-behaviors"></a>WCF 数据服务行为  

 以下 WCF Data Services 行为未通过 OData 协议显式定义：  
  
### <a name="default-sorting-behavior"></a>默认排序行为  

 当发送到数据服务的查询请求包括 `$top` 或 `$skip` 系统查询选项但不包括 `$orderby` 系统查询选项时，返回的源按键属性升序排序。 这是因为需要顺序以确保结果正确分页。 为此，数据服务向查询中添加排序表达式。 在数据服务中启用服务器驱动的分页时，也会发生此行为。 有关详细信息，请参阅 [配置数据服务](configuring-the-data-service-wcf-data-services.md)。若要控制返回的源的排序，应将包含 `$orderby` 在查询 URI 中。  
  
## <a name="see-also"></a>请参阅

- [定义 WCF 数据服务](defining-wcf-data-services.md)
- [WCF 数据服务客户端库](wcf-data-services-client-library.md)
