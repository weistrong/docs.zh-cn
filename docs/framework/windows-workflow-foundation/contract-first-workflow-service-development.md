---
description: 了解详细信息：约定优先工作流服务开发
title: 协定优先的工作流服务开发
ms.date: 03/30/2017
ms.assetid: e5dbaa7b-005f-4330-848d-58ac4f42f093
ms.openlocfilehash: 54f6c0c5de45187bd65e45d22978e6e9b105f3e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792708"
---
# <a name="contract-first-workflow-service-development"></a>协定优先的工作流服务开发

从 .NET Framework 4.5 开始，Windows Workflow Foundation (WF) 功能以协定优先的工作流开发的形式，更好地集成 web 服务和工作流。 通过协定优先的工作流开发工具，可以在代码中优先设计协定。 然后该工具在工具箱中为协定中的操作自动生成活动模板。 本主题概述工作流服务中的活动和属性如何映射到服务协定的特性。 有关创建协定优先工作流服务的分步示例，请参阅 [如何：创建使用现有服务协定的工作流服务](how-to-create-a-workflow-service-that-consumes-an-existing-service-contract.md)。

## <a name="in-this-topic"></a>本主题内容

- [将服务协定特性映射到工作流特性](contract-first-workflow-service-development.md#MappingAttributes)

  - [服务协定特性](contract-first-workflow-service-development.md#ServiceContract)

  - [操作协定特性](contract-first-workflow-service-development.md#OperationContract)

  - [消息协定特性](contract-first-workflow-service-development.md#MessageContract)

  - [数据协定特性](contract-first-workflow-service-development.md#DataContract)

  - [错误协定特性](contract-first-workflow-service-development.md#FaultContract)

- [其他支持和实现信息](contract-first-workflow-service-development.md#AdditionalSupport)

  - [不支持的服务协定功能](contract-first-workflow-service-development.md#UnsupportedFeatures)

  - [配置消息活动的生成](contract-first-workflow-service-development.md#ActivityGeneration)

## <a name="mapping-service-contract-attributes-to-workflow-attributes"></a><a name="MappingAttributes"></a> 将服务协定特性映射到工作流属性

下面几节中的表指定不同 WCF 特性和属性，以及它们如何映射到协定优先工作流中的消息活动和属性。

- [服务协定特性](contract-first-workflow-service-development.md#ServiceContract)

- [操作协定特性](contract-first-workflow-service-development.md#OperationContract)

- [消息协定特性](contract-first-workflow-service-development.md#MessageContract)

- [数据协定特性](contract-first-workflow-service-development.md#DataContract)

- [错误协定特性](contract-first-workflow-service-development.md#FaultContract)

### <a name="service-contract-attributes"></a><a name="ServiceContract"></a> 服务协定特性

|属性名称|支持|说明|WF 验证|
|-------------------|---------------|-----------------|-------------------|
|CallbackContract|否|获取或设置当协定为双工协定时的回调协定类型。|(N/A)|
|ConfigurationName|否|获取或设置用于查找应用程序配置文件中的服务的名称。|(N/A)|
|HasProtectionLevel|是|获取一个值，该值指示是否对成员分配保护级别。|Receive.ProtectionLevel 不应为 null。|
|名称|是|获取或设置 Web 服务描述语言 (WSDL) 中的 \<portType> 元素的名称。|Receive.ServiceContractName.LocalName 应当匹配。|
|命名空间|是|获取或设置 Web 服务描述语言 (WSDL) 中的 \<portType> 元素的命名空间。|Receive.ServiceContractName.NameSpace 应当匹配|
|ProtectionLevel|是|指定协定的绑定是否必须支持 ProtectionLevel 属性的值。|Receive.ProtectionLevel 应当匹配。|
|SessionMode|否|获取或设置是否允许、不允许或要求会话。|(N/A)|
|TypeId|否|在派生类中实现时，获取此特性的唯一标识符。 （从特性继承。）|(N/A)|

在此处插入小节正文。

### <a name="operation-contract-attributes"></a><a name="OperationContract"></a> 操作协定属性

|属性名称|支持|说明|WF 验证|
|-------------------|---------------|-----------------|-------------------|
|操作|是|获取或设置请求消息的 WS-Addressing 操作。|Receive.Action 应当匹配。|
|AsyncPattern|否|指示操作是使用 \<methodName> 服务协定中的 Begin 和 End 方法对异步实现的 \<methodName> 。|(N/A)|
|HasProtectionLevel|是|获取一个值，该值指示是否必须对此操作的消息进行加密和/或签名。|Receive.ProtectionLevel 不应为 null。|
|IsInitiating|否|获取或设置一个值，该值指示方法是否实现可在服务器上启动会话（如果存在会话）的操作。|(N/A)|
|IsOneWay|是|获取或设置一个值，该值指示操作是否返回答复消息。|(此 Receive 无对应 SendReply 或此 Send 无对应 ReceiveReply）。|
|IsTerminating|否|获取或设置一个值，该值指示服务操作在发送答复消息（如果存在）后，是否会导致服务器关闭会话。|(N/A)|
|名称|是|获取或设置操作的名称。|Receive.OperationName 应当匹配。|
|ProtectionLevel|是|获取或设置一个值，该值指定是否必须对操作的消息进行加密和/或签名。|Receive.ProtectionLevel 应当匹配。|
|ReplyAction|是|获取或设置用于该操作答复消息的 SOAP 操作的值。|SendReply.Action 应当匹配。|
|TypeId|否|在派生类中实现时，获取此特性的唯一标识符。 （从特性继承。）|(N/A)|

### <a name="message-contract-attributes"></a><a name="MessageContract"></a> 消息协定属性

|属性名称|支持|说明|WF 验证|
|-------------------|---------------|-----------------|-------------------|
|HasProtectionLevel|是|获取一个值，该值指示消息是否有保护级别。|无验证（Receive.Content 和 SendReply.Content 必须匹配消息协定类型）。|
|IsWrapped|是|获取或设置一个值，该值指定消息正文是否有包装元素。|无验证（Receive.Content 和 Sendreply.Content 必须匹配消息协定类型）。|
|ProtectionLevel|否|获取或设置一个值，该值指定是否对消息进行加密、签名或同时执行这两种操作。|(N/A)|
|TypeId|是|在派生类中实现时，获取此特性的唯一标识符。 （从特性继承。）|无验证（Receive.Content 和 SendReply.Content 必须匹配消息协定类型）。|
|WrapperName|是|获取或设置消息正文的包装元素名称。|无验证（Receive.Content 和 SendReply.Content 必须匹配消息协定类型）。|
|WrapperNamespace|否|获取或设置消息正文包装元素的命名空间。|(N/A)|

### <a name="data-contract-attributes"></a><a name="DataContract"></a> 数据协定属性

|属性名称|支持|说明|WF 验证|
|-------------------|---------------|-----------------|-------------------|
|IsReference|否|获取或设置一个值，该值指示是否保留对象引用数据。|(N/A)|
|名称|是|获取或设置类型的数据协定的名称。|无验证（Receive.Content 和 SendReply.Content 必须匹配消息协定类型）。|
|命名空间|是|获取或设置类型的数据协定的命名空间。|无验证（Receive.Content 和 SendReply.Content 必须匹配消息协定类型）。|
|TypeId|否|在派生类中实现时，获取此特性的唯一标识符。 （从特性继承。）|(N/A)|

### <a name="fault-contract-attributes"></a><a name="FaultContract"></a> 错误协定属性

|属性名称|支持|说明|WF 验证|
|-------------------|---------------|-----------------|-------------------|
|操作|是|获取或设置已指定作为操作协定一部分的 SOAP 错误消息的操作。|SendReply.Action 应当匹配。|
|DetailType|是|获取包含错误信息的可序列化对象的类型。|SendReply.Content 应匹配该类型|
|HasProtectionLevel|否|获取一个值，该值指示 SOAP 错误消息是否分配有保护级别。|(N/A)|
|名称|否|获取或设置 Web 服务描述语言 (WSDL) 中的错误消息的名称。|(N/A)|
|命名空间|否|获取或设置 SOAP 错误的命名空间。|(N/A)|
|ProtectionLevel|否|指定 SOAP 错误要求的绑定的保护级别。|(N/A)|
|TypeId|否|在派生类中实现时，获取此特性的唯一标识符。 （从特性继承。）|(N/A)|

## <a name="additional-support-and-implementation-information"></a><a name="AdditionalSupport"></a> 其他支持和实现信息

- [不支持的服务协定功能](contract-first-workflow-service-development.md#UnsupportedFeatures)

- [配置消息活动的生成](contract-first-workflow-service-development.md#ActivityGeneration)

### <a name="unsupported-service-contract-features"></a><a name="UnsupportedFeatures"></a> 不支持的服务协定功能

- 不支持在协定中用 TPL（任务并行库）任务。

- 不支持服务协定的继承。

### <a name="generation-of-configured-messaging-activities"></a><a name="ActivityGeneration"></a> 生成已配置的消息传递活动

向 <xref:System.ServiceModel.Activities.Receive> 和 <xref:System.ServiceModel.Activities.SendReply> 活动加入两个公共静态方法，以支持在使用协定优先工作流服务时生成预配置消息活动。

- <xref:System.ServiceModel.Activities.Receive.FromOperationDescription%2A?displayProperty=nameWithType>

- <xref:System.ServiceModel.Activities.SendReply.FromOperationDescription%2A?displayProperty=nameWithType>

由这些方法生成的活动应当通过协定验证，因此这些方法在内部用作 <xref:System.ServiceModel.Activities.Receive> 和 <xref:System.ServiceModel.Activities.SendReply> 的验证逻辑。 <xref:System.ServiceModel.Activities.Receive.OperationName%2A>、<xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A>、<xref:System.ServiceModel.Activities.Receive.Action%2A>、<xref:System.ServiceModel.Activities.Receive.SerializerOption%2A>、<xref:System.ServiceModel.Activities.Receive.ProtectionLevel%2A> 和 <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A> 都进行了预配置，以匹配导入的协定。 在工作流设计器中的活动的内容属性页中，还将对 **消息** 或 **参数** 部分进行预配置，使其与协定匹配。

还可以通过 <xref:System.ServiceModel.Activities.SendReply> 为中显示的每个错误返回一组单独的已配置活动来处理 WCF 故障协定 <xref:System.ServiceModel.Description.OperationDescription.Faults%2A> <xref:System.ServiceModel.Description.FaultDescriptionCollection> 。

对于 <xref:System.ServiceModel.Description.OperationDescription> 当前不受 WF 服务支持的其他部分 (例如 WebGet/WebInvoke 行为，或自定义操作行为) ，API 将在生成和配置过程中忽略这些值。 不会引发任何异常。
