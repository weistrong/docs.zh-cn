---
description: 了解详细信息： WS-MetadataExchange 绑定
title: WS-MetadataExchange 绑定
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 3bcea573ad436a85285fab5657e58defa9113d9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643938"
---
# <a name="ws-metadataexchange-bindings"></a>WS-MetadataExchange 绑定

本主题说明如何为各种传输构造默认的元数据交换绑定。  
  
## <a name="the-default-bindings"></a>默认绑定  
  
|默认绑定名称|绑定的构造方式|  
|--------------------------|------------------------------------|  
|mexHttpBinding|一个禁用传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。|  
|mexHttpsBinding|一个支持传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。|  
|mexNamedPipeBinding|一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>。|  
|mexTcpBinding|一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>。|
