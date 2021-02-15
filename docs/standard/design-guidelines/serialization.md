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
# <a name="serialization"></a><span data-ttu-id="9c5a3-103">序列化</span><span class="sxs-lookup"><span data-stu-id="9c5a3-103">Serialization</span></span>

<span data-ttu-id="9c5a3-104">序列化是将对象转换为易于持久化或传输的格式的过程。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-104">Serialization is the process of converting an object into a format that can be readily persisted or transported.</span></span> <span data-ttu-id="9c5a3-105">例如，你可以将一个对象序列化，使用 HTTP 通过 Internet 传输该对象，并在目标计算机上对其进行反序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-105">For example, you can serialize an object, transport it over the Internet using HTTP, and deserialized it at the destination machine.</span></span>

 <span data-ttu-id="9c5a3-106">.NET Framework 提供针对各种序列化场景进行了优化的三种主要序列化技术。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-106">The .NET Framework offers three main serialization technologies optimized for various serialization scenarios.</span></span> <span data-ttu-id="9c5a3-107">下表列出了这些技术以及与这些技术相关的主要 Framework 类型。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-107">The following table lists these technologies and the main Framework types related to these technologies.</span></span>

|<span data-ttu-id="9c5a3-108">**技术名称**</span><span class="sxs-lookup"><span data-stu-id="9c5a3-108">**Technology Name**</span></span>|<span data-ttu-id="9c5a3-109">主要类型</span><span class="sxs-lookup"><span data-stu-id="9c5a3-109">**Main Types**</span></span>|<span data-ttu-id="9c5a3-110">**方案**</span><span class="sxs-lookup"><span data-stu-id="9c5a3-110">**Scenarios**</span></span>|
|-------------------------|--------------------|-------------------|
|<span data-ttu-id="9c5a3-111">**数据协定序列化**</span><span class="sxs-lookup"><span data-stu-id="9c5a3-111">**Data Contract Serialization**</span></span>|<xref:System.Runtime.Serialization.DataContractAttribute> <br /> <xref:System.Runtime.Serialization.DataMemberAttribute> <br /> <xref:System.Runtime.Serialization.DataContractSerializer> <br /> <xref:System.Runtime.Serialization.NetDataContractSerializer> <br /> <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> <br /> <xref:System.Runtime.Serialization.ISerializable>|<span data-ttu-id="9c5a3-112">常规持久性</span><span class="sxs-lookup"><span data-stu-id="9c5a3-112">General persistence</span></span><br /><span data-ttu-id="9c5a3-113">Web 服务</span><span class="sxs-lookup"><span data-stu-id="9c5a3-113">Web Services</span></span><br /><span data-ttu-id="9c5a3-114">JSON</span><span class="sxs-lookup"><span data-stu-id="9c5a3-114">JSON</span></span>|
|<span data-ttu-id="9c5a3-115">**XML 序列化**</span><span class="sxs-lookup"><span data-stu-id="9c5a3-115">**XML Serialization**</span></span>|<xref:System.Xml.Serialization.XmlSerializer>|<span data-ttu-id="9c5a3-116">可完全控制 XML 形状的 XML 格式</span><span class="sxs-lookup"><span data-stu-id="9c5a3-116">XML format with full control over the shape of the XML</span></span>|
|<span data-ttu-id="9c5a3-117">运行时序列化（二进制和 SOAP）</span><span class="sxs-lookup"><span data-stu-id="9c5a3-117">**Runtime Serialization (Binary and SOAP)**</span></span>|<xref:System.SerializableAttribute> <br /> <xref:System.Runtime.Serialization.ISerializable> <br /> <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> <br /> <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter>|<span data-ttu-id="9c5a3-118">.NET 远程处理</span><span class="sxs-lookup"><span data-stu-id="9c5a3-118">.NET Remoting</span></span>|

 <span data-ttu-id="9c5a3-119">✔️ 设计新类型时请务必考虑序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-119">✔️ DO think about serialization when you design new types.</span></span>

## <a name="choosing-the-right-serialization-technology-to-support"></a><span data-ttu-id="9c5a3-120">选择要支持的合适的序列化技术</span><span class="sxs-lookup"><span data-stu-id="9c5a3-120">Choosing the Right Serialization Technology to Support</span></span>

 <span data-ttu-id="9c5a3-121">✔️ 如果可能需要在 Web 服务中持久保持或使用类型的实例，则应考虑支持数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-121">✔️ CONSIDER supporting Data Contract Serialization if instances of your type might need to be persisted or used in Web Services.</span></span>

 <span data-ttu-id="9c5a3-122">✔️ 如果需要对序列化类型时生成的 XML 格式具有更多控制，则应考虑改为支持 XML 序列化，或者在支持数据协定序列化之外还支持 XML 序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-122">✔️ CONSIDER supporting the XML Serialization instead of or in addition to Data Contract Serialization if you need more control over the XML format that is produced when the type is serialized.</span></span>

 <span data-ttu-id="9c5a3-123">这对于某些需要使用数据协定序列化所不支持的 XML 构造（例如，用于生成 XML 特性）的互操作性场景可能是必需的。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-123">This may be necessary in some interoperability scenarios where you need to use an XML construct that is not supported by Data Contract Serialization, for example, to produce XML attributes.</span></span>

 <span data-ttu-id="9c5a3-124">✔️ 如果类型的实例需要越过 .NET 远程处理边界传递，则应考虑支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-124">✔️ CONSIDER supporting the Runtime Serialization if instances of your type need to travel across .NET Remoting boundaries.</span></span>

 <span data-ttu-id="9c5a3-125">❌ 请避免仅仅因为常规持久性原因而支持运行时序列化或 XML 序列化，</span><span class="sxs-lookup"><span data-stu-id="9c5a3-125">❌ AVOID supporting Runtime Serialization or XML Serialization just for general persistence reasons.</span></span> <span data-ttu-id="9c5a3-126">而应首选数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-126">Prefer Data Contract Serialization instead.</span></span>

## <a name="supporting-data-contract-serialization"></a><span data-ttu-id="9c5a3-127">支持数据协定序列化</span><span class="sxs-lookup"><span data-stu-id="9c5a3-127">Supporting Data Contract Serialization</span></span>

 <span data-ttu-id="9c5a3-128">通过将 <xref:System.Runtime.Serialization.DataContractAttribute> 应用到类型，并将 <xref:System.Runtime.Serialization.DataMemberAttribute> 应用到类型的成员（字段和属性），类型可支持数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-128">Types can support Data Contract Serialization by applying the <xref:System.Runtime.Serialization.DataContractAttribute> to the type and the <xref:System.Runtime.Serialization.DataMemberAttribute> to the members (fields and properties) of the type.</span></span>

 <span data-ttu-id="9c5a3-129">✔️ 如果可以在部分信任模式下使用类型，则考虑将类型的数据成员标记为公共的。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-129">✔️ CONSIDER marking data members of your type public if the type can be used in partial trust.</span></span>

 <span data-ttu-id="9c5a3-130">在完全信任模式下，数据协定序列化程序可对非公共类型和成员进行序列化和反序列化，但在部分信任模式下，仅可对公共成员进行序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-130">In full trust, Data Contract serializers can serialize and deserialize nonpublic types and members, but only public members can be serialized and deserialized in partial trust.</span></span>

 <span data-ttu-id="9c5a3-131">✔️ 请务必在包含 <xref:System.Runtime.Serialization.DataMemberAttribute> 的所有属性上实现 getter 和 setter。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-131">✔️ DO implement a getter and setter on all properties that have <xref:System.Runtime.Serialization.DataMemberAttribute>.</span></span> <span data-ttu-id="9c5a3-132">数据协定序列化程序要求该类型的 getter 和 setter 都被视为是可序列化的。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-132">Data Contract serializers require both the getter and the setter for the type to be considered serializable.</span></span> <span data-ttu-id="9c5a3-133">（在 .NET Framework 3.5 SP1 中，某些集合属性可以为仅限获取属性。）如果不会在部分信任模式下使用类型，则这两个属性访问器中的一个或两个都可以是非公共的。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-133">(In .NET Framework 3.5 SP1, some collection properties can be get-only.) If the type won’t be used in partial trust, one or both of the property accessors can be nonpublic.</span></span>

 <span data-ttu-id="9c5a3-134">✔️ 对于反序列化实例的初始化，应考虑使用序列化回调。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-134">✔️ CONSIDER using the serialization callbacks for initialization of deserialized instances.</span></span>

 <span data-ttu-id="9c5a3-135">反序列化对象时，不调用任何构造函数。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-135">Constructors are not called when objects are deserialized.</span></span> <span data-ttu-id="9c5a3-136">（该规则存在例外情况。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-136">(There are exceptions to the rule.</span></span> <span data-ttu-id="9c5a3-137">在反序列化期间，调用标记为 <xref:System.Runtime.Serialization.CollectionDataContractAttribute> 的集合的构造函数。）因此，在正常构造期间执行的任何逻辑都需要作为一个序列化回调实现。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-137">Constructors of collections marked with <xref:System.Runtime.Serialization.CollectionDataContractAttribute> are called during deserialization.) Therefore, any logic that executes during normal construction needs to be implemented as one of the serialization callbacks.</span></span>

 <span data-ttu-id="9c5a3-138">`OnDeserializedAttribute` 是最常用的回调属性。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-138">`OnDeserializedAttribute` is the most commonly used callback attribute.</span></span> <span data-ttu-id="9c5a3-139">此系列中的其他属性还有 <xref:System.Runtime.Serialization.OnDeserializingAttribute>、<xref:System.Runtime.Serialization.OnSerializingAttribute> 和 <xref:System.Runtime.Serialization.OnSerializedAttribute>。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-139">The other attributes in the family are <xref:System.Runtime.Serialization.OnDeserializingAttribute>,  <xref:System.Runtime.Serialization.OnSerializingAttribute>, and <xref:System.Runtime.Serialization.OnSerializedAttribute>.</span></span> <span data-ttu-id="9c5a3-140">这些属性可分别用来标记在反序列化之前、序列化之前以及序列化之后执行的回调。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-140">They can be used to mark callbacks that get executed before deserialization, before serialization, and finally, after serialization, respectively.</span></span>

 <span data-ttu-id="9c5a3-141">✔️ 请考虑使用 <xref:System.Runtime.Serialization.KnownTypeAttribute> 指示在反序列化复杂对象图时应使用的具体类型。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-141">✔️ CONSIDER using the <xref:System.Runtime.Serialization.KnownTypeAttribute> to indicate concrete types that should be used when deserializing a complex object graph.</span></span>

 <span data-ttu-id="9c5a3-142">✔️ 创建或更改可序列化的类型时，请务必考虑后向兼容性和前向兼容性。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-142">✔️ DO consider backward and forward compatibility when creating or changing serializable types.</span></span>

 <span data-ttu-id="9c5a3-143">请记住，类型的未来版本的序列化流可反序列化到类型的当前版本，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-143">Keep in mind that serialized streams of future versions of your type can be deserialized into the current version of the type, and vice versa.</span></span>

 <span data-ttu-id="9c5a3-144">你一定要清楚，数据成员（甚至是私有成员和内部成员）不能更改其名称和类型，甚至不能更改其在类型的未来版本中的顺序，除非特别留意将使用显式参数的协定保存到数据协定属性。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-144">Make sure you understand that data members, even private and internal, cannot change their names, types, or even their order in future versions of the type unless special care is taken to preserve the contract using explicit parameters to the data contract attributes.</span></span>

 <span data-ttu-id="9c5a3-145">在对可序列化的类型进行更改时，测试序列化的兼容性。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-145">Test compatibility of serialization when making changes to serializable types.</span></span> <span data-ttu-id="9c5a3-146">尝试将新版本反序列化为旧版本，以及将旧版本反序列化为新版本。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-146">Try deserializing the new version into an old version, and vice versa.</span></span>

 <span data-ttu-id="9c5a3-147">✔️ 考虑实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 以允许在类型的两个不同版本之间进行往返。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-147">✔️ CONSIDER implementing <xref:System.Runtime.Serialization.IExtensibleDataObject> to allow round-tripping between different versions of the type.</span></span>

 <span data-ttu-id="9c5a3-148">序列化程序可通过此接口确保在往返期间不丢失任何数据。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-148">The interface allows the serializer to ensure that no data is lost during round-tripping.</span></span> <span data-ttu-id="9c5a3-149">使用 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType> 属性存储来自当前版本未知的类型的未来版本的任何数据，因此该属性不能将这些数据存储在其数据成员中。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-149">The <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType> property is used to store any data from the future version of the type that is unknown to the current version, and so it cannot store it in its data members.</span></span> <span data-ttu-id="9c5a3-150">在随后序列化当前版本并将其反序列化为未来版本时，可在序列化流中使用附加数据。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-150">When the current version is subsequently serialized and deserialized into a future version, the additional data will be available in the serialized stream.</span></span>

## <a name="supporting-xml-serialization"></a><span data-ttu-id="9c5a3-151">支持 XML 序列化</span><span class="sxs-lookup"><span data-stu-id="9c5a3-151">Supporting XML Serialization</span></span>

 <span data-ttu-id="9c5a3-152">数据协定序列化是 .NET Framework 中的主要（默认）序列化技术，但也存在数据协定序列化不支持的序列化场景。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-152">Data Contract Serialization is the main (default) serialization technology in the .NET Framework, but there are serialization scenarios that Data Contract Serialization does not support.</span></span> <span data-ttu-id="9c5a3-153">例如，数据协定序列化无法让您完全控制序列化程序生成或使用的 XML 的形状。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-153">For example, it does not give you full control over the shape of XML produced or consumed by the serializer.</span></span> <span data-ttu-id="9c5a3-154">如果要求此类精细控制，则必须使用 XML 序列化，而且需要设计类型以支持此序列化技术。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-154">If such fine control is required, XML Serialization has to be used, and you need to design your types to support this serialization technology.</span></span>

 <span data-ttu-id="9c5a3-155">❌ 请避免专门针对 XML 序列化设计类型，除非你有很充分的理由要控制所生成的 XML 的形状。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-155">❌ AVOID designing your types specifically for XML Serialization, unless you have a very strong reason to control the shape of the XML produced.</span></span> <span data-ttu-id="9c5a3-156">此序列化技术已由上一节讨论的数据协定序列化所取代。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-156">This serialization technology has been superseded by the Data Contract Serialization discussed in the previous section.</span></span>

 <span data-ttu-id="9c5a3-157">✔️ 如果通过应用 XML 序列化属性所提供的对于序列化 XML 的形状的控制还无法满足你的需要，则可考虑实现 <xref:System.Xml.Serialization.IXmlSerializable> 接口。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-157">✔️ CONSIDER implementing the <xref:System.Xml.Serialization.IXmlSerializable> interface if you want even more control over the shape of the serialized XML than what’s offered by applying the XML Serialization attributes.</span></span> <span data-ttu-id="9c5a3-158">利用此接口的两种方法（<xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> 和 <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>），你可以完全控制序列化的 XML 流。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-158">Two methods of the interface, <xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> and <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>, allow you to fully control the serialized XML stream.</span></span> <span data-ttu-id="9c5a3-159">还可以通过应用 `XmlSchemaProviderAttribute` 来控制为类型生成的 XML 架构。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-159">You can also control the XML schema that gets generated for the type by applying the `XmlSchemaProviderAttribute`.</span></span>

## <a name="supporting-runtime-serialization"></a><span data-ttu-id="9c5a3-160">支持运行时序列化</span><span class="sxs-lookup"><span data-stu-id="9c5a3-160">Supporting Runtime Serialization</span></span>

 <span data-ttu-id="9c5a3-161">运行时序列化是 .NET 远程处理所使用的一项技术。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-161">Runtime Serialization is a technology used by .NET Remoting.</span></span> <span data-ttu-id="9c5a3-162">如果你认为将会使用 .NET 远程处理传输类型，则需要确保类型支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-162">If you think your types will be transported using .NET Remoting, you need to make sure they support Runtime Serialization.</span></span>

 <span data-ttu-id="9c5a3-163">可通过应用 <xref:System.SerializableAttribute> 来提供对运行时序列化的基本支持，更高级的场景涉及实现一个简单的运行时可序列化模式（实现 <xref:System.Runtime.Serialization.ISerializable> 并提供序列化构造函数）。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-163">The basic support for Runtime Serialization can be provided by applying the <xref:System.SerializableAttribute>, and more advanced scenarios involve implementing a simple Runtime Serializable Pattern (implement <xref:System.Runtime.Serialization.ISerializable> and provide serialization constructor).</span></span>

 <span data-ttu-id="9c5a3-164">✔️ 如果你的类型将要用于 .NET 远程处理，则应考虑支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-164">✔️ CONSIDER supporting Runtime Serialization if your types will be used with .NET Remoting.</span></span> <span data-ttu-id="9c5a3-165">例如，<xref:System.AddIn?displayProperty=nameWithType> 命名空间使用 .NET 远程处理，因此在 `System.AddIn` 加载项之间交换的所有类型都需要支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-165">For example, the <xref:System.AddIn?displayProperty=nameWithType> namespace uses .NET Remoting, and so all types exchanged between `System.AddIn` add-ins need to support Runtime Serialization.</span></span>

 <span data-ttu-id="9c5a3-166">✔️ 如果需要完全控制序列化过程，则应考虑实现运行时可序列化模式。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-166">✔️ CONSIDER implementing the Runtime Serializable Pattern if you want complete control over the serialization process.</span></span> <span data-ttu-id="9c5a3-167">例如，如果您需要在对数据进行序列化或反序列化时转换数据。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-167">For example, if you want to transform data as it gets serialized or deserialized.</span></span>

 <span data-ttu-id="9c5a3-168">此模式非常简单。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-168">The pattern is very simple.</span></span> <span data-ttu-id="9c5a3-169">您需要执行的全部操作就是实现 <xref:System.Runtime.Serialization.ISerializable> 接口，并提供在反序列化对象时使用的特殊构造函数。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-169">All you need to do is implement the <xref:System.Runtime.Serialization.ISerializable> interface and provide a special constructor that is used when the object is deserialized.</span></span>

 <span data-ttu-id="9c5a3-170">✔️ 请务必保护序列化构造函数，并提供完全按照此处示例中所示类型化和命名的两个参数。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-170">✔️ DO make the serialization constructor protected and provide two parameters typed and named exactly as shown in the sample here.</span></span>

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

 <span data-ttu-id="9c5a3-171">✔️ 请务必显式实现 <xref:System.Runtime.Serialization.ISerializable> 成员。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-171">✔️ DO implement the <xref:System.Runtime.Serialization.ISerializable> members explicitly.</span></span>

 <span data-ttu-id="9c5a3-172">✔️ 请务必将链接要求应用到 <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> 实现。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-172">✔️ DO apply a link demand to <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> implementation.</span></span> <span data-ttu-id="9c5a3-173">这可确保只有完全受信任的核心和运行时序列化程序才有权访问成员。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-173">This ensures that only fully trusted core and the Runtime Serializer have access to the member.</span></span>

 <span data-ttu-id="9c5a3-174">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="9c5a3-174">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="9c5a3-175">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="9c5a3-175">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="9c5a3-176">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c5a3-176">See also</span></span>

- [<span data-ttu-id="9c5a3-177">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="9c5a3-177">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="9c5a3-178">使用准则</span><span class="sxs-lookup"><span data-stu-id="9c5a3-178">Usage Guidelines</span></span>](usage-guidelines.md)
