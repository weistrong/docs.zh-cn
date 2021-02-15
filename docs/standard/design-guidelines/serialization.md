---
description: 详细了解：序列化
title: 序列化
ms.date: 10/22/2008
ms.assetid: bebb27ac-9712-4196-9931-de19fc04dbac
ms.openlocfilehash: a12163c01da2f9eed19de05b0434c02d05ca99b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713294"
---
# <a name="serialization"></a>序列化

序列化是将对象转换为易于持久化或传输的格式的过程。 例如，你可以将一个对象序列化，使用 HTTP 通过 Internet 传输该对象，并在目标计算机上对其进行反序列化。

 .NET Framework 提供针对各种序列化场景进行了优化的三种主要序列化技术。 下表列出了这些技术以及与这些技术相关的主要 Framework 类型。

|**技术名称**|主要类型|**方案**|
|-------------------------|--------------------|-------------------|
|**数据协定序列化**|<xref:System.Runtime.Serialization.DataContractAttribute> <br /> <xref:System.Runtime.Serialization.DataMemberAttribute> <br /> <xref:System.Runtime.Serialization.DataContractSerializer> <br /> <xref:System.Runtime.Serialization.NetDataContractSerializer> <br /> <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> <br /> <xref:System.Runtime.Serialization.ISerializable>|常规持久性<br />Web 服务<br />JSON|
|**XML 序列化**|<xref:System.Xml.Serialization.XmlSerializer>|可完全控制 XML 形状的 XML 格式|
|运行时序列化（二进制和 SOAP）|<xref:System.SerializableAttribute> <br /> <xref:System.Runtime.Serialization.ISerializable> <br /> <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> <br /> <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter>|.NET 远程处理|

 ✔️ 设计新类型时请务必考虑序列化。

## <a name="choosing-the-right-serialization-technology-to-support"></a>选择要支持的合适的序列化技术

 ✔️ 如果可能需要在 Web 服务中持久保持或使用类型的实例，则应考虑支持数据协定序列化。

 ✔️ 如果需要对序列化类型时生成的 XML 格式具有更多控制，则应考虑改为支持 XML 序列化，或者在支持数据协定序列化之外还支持 XML 序列化。

 这对于某些需要使用数据协定序列化所不支持的 XML 构造（例如，用于生成 XML 特性）的互操作性场景可能是必需的。

 ✔️ 如果类型的实例需要越过 .NET 远程处理边界传递，则应考虑支持运行时序列化。

 ❌ 请避免仅仅因为常规持久性原因而支持运行时序列化或 XML 序列化， 而应首选数据协定序列化。

## <a name="supporting-data-contract-serialization"></a>支持数据协定序列化

 通过将 <xref:System.Runtime.Serialization.DataContractAttribute> 应用到类型，并将 <xref:System.Runtime.Serialization.DataMemberAttribute> 应用到类型的成员（字段和属性），类型可支持数据协定序列化。

 ✔️ 如果可以在部分信任模式下使用类型，则考虑将类型的数据成员标记为公共的。

 在完全信任模式下，数据协定序列化程序可对非公共类型和成员进行序列化和反序列化，但在部分信任模式下，仅可对公共成员进行序列化和反序列化。

 ✔️ 请务必在包含 <xref:System.Runtime.Serialization.DataMemberAttribute> 的所有属性上实现 getter 和 setter。 数据协定序列化程序要求该类型的 getter 和 setter 都被视为是可序列化的。 （在 .NET Framework 3.5 SP1 中，某些集合属性可以为仅限获取属性。）如果不会在部分信任模式下使用类型，则这两个属性访问器中的一个或两个都可以是非公共的。

 ✔️ 对于反序列化实例的初始化，应考虑使用序列化回调。

 反序列化对象时，不调用任何构造函数。 （该规则存在例外情况。 在反序列化期间，调用标记为 <xref:System.Runtime.Serialization.CollectionDataContractAttribute> 的集合的构造函数。）因此，在正常构造期间执行的任何逻辑都需要作为一个序列化回调实现。

 `OnDeserializedAttribute` 是最常用的回调属性。 此系列中的其他属性还有 <xref:System.Runtime.Serialization.OnDeserializingAttribute>、<xref:System.Runtime.Serialization.OnSerializingAttribute> 和 <xref:System.Runtime.Serialization.OnSerializedAttribute>。 这些属性可分别用来标记在反序列化之前、序列化之前以及序列化之后执行的回调。

 ✔️ 请考虑使用 <xref:System.Runtime.Serialization.KnownTypeAttribute> 指示在反序列化复杂对象图时应使用的具体类型。

 ✔️ 创建或更改可序列化的类型时，请务必考虑后向兼容性和前向兼容性。

 请记住，类型的未来版本的序列化流可反序列化到类型的当前版本，反之亦然。

 你一定要清楚，数据成员（甚至是私有成员和内部成员）不能更改其名称和类型，甚至不能更改其在类型的未来版本中的顺序，除非特别留意将使用显式参数的协定保存到数据协定属性。

 在对可序列化的类型进行更改时，测试序列化的兼容性。 尝试将新版本反序列化为旧版本，以及将旧版本反序列化为新版本。

 ✔️ 考虑实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 以允许在类型的两个不同版本之间进行往返。

 序列化程序可通过此接口确保在往返期间不丢失任何数据。 使用 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType> 属性存储来自当前版本未知的类型的未来版本的任何数据，因此该属性不能将这些数据存储在其数据成员中。 在随后序列化当前版本并将其反序列化为未来版本时，可在序列化流中使用附加数据。

## <a name="supporting-xml-serialization"></a>支持 XML 序列化

 数据协定序列化是 .NET Framework 中的主要（默认）序列化技术，但也存在数据协定序列化不支持的序列化场景。 例如，数据协定序列化无法让您完全控制序列化程序生成或使用的 XML 的形状。 如果要求此类精细控制，则必须使用 XML 序列化，而且需要设计类型以支持此序列化技术。

 ❌ 请避免专门针对 XML 序列化设计类型，除非你有很充分的理由要控制所生成的 XML 的形状。 此序列化技术已由上一节讨论的数据协定序列化所取代。

 ✔️ 如果通过应用 XML 序列化属性所提供的对于序列化 XML 的形状的控制还无法满足你的需要，则可考虑实现 <xref:System.Xml.Serialization.IXmlSerializable> 接口。 利用此接口的两种方法（<xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> 和 <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>），你可以完全控制序列化的 XML 流。 还可以通过应用 `XmlSchemaProviderAttribute` 来控制为类型生成的 XML 架构。

## <a name="supporting-runtime-serialization"></a>支持运行时序列化

 运行时序列化是 .NET 远程处理所使用的一项技术。 如果你认为将会使用 .NET 远程处理传输类型，则需要确保类型支持运行时序列化。

 可通过应用 <xref:System.SerializableAttribute> 来提供对运行时序列化的基本支持，更高级的场景涉及实现一个简单的运行时可序列化模式（实现 <xref:System.Runtime.Serialization.ISerializable> 并提供序列化构造函数）。

 ✔️ 如果你的类型将要用于 .NET 远程处理，则应考虑支持运行时序列化。 例如，<xref:System.AddIn?displayProperty=nameWithType> 命名空间使用 .NET 远程处理，因此在 `System.AddIn` 加载项之间交换的所有类型都需要支持运行时序列化。

 ✔️ 如果需要完全控制序列化过程，则应考虑实现运行时可序列化模式。 例如，如果您需要在对数据进行序列化或反序列化时转换数据。

 此模式非常简单。 您需要执行的全部操作就是实现 <xref:System.Runtime.Serialization.ISerializable> 接口，并提供在反序列化对象时使用的特殊构造函数。

 ✔️ 请务必保护序列化构造函数，并提供完全按照此处示例中所示类型化和命名的两个参数。

```csharp
[Serializable]
public class Person : ISerializable
{
    protected Person(SerializationInfo info, StreamingContext context)
    {
        // ...
    }
}
```

 ✔️ 请务必显式实现 <xref:System.Runtime.Serialization.ISerializable> 成员。

 ✔️ 请务必将链接要求应用到 <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> 实现。 这可确保只有完全受信任的核心和运行时序列化程序才有权访问成员。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [使用准则](usage-guidelines.md)
