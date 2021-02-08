---
description: 了解详细信息： JSON 和 XML 之间的映射
title: JSON 和 XML 之间的映射
ms.date: 03/30/2017
ms.assetid: 22ee1f52-c708-4024-bbf0-572e0dae64af
ms.openlocfilehash: 1d9652d1683446da9946987a31a92906d5e38e55
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793670"
---
# <a name="mapping-between-json-and-xml"></a><span data-ttu-id="49f66-103">JSON 和 XML 之间的映射</span><span class="sxs-lookup"><span data-stu-id="49f66-103">Mapping Between JSON and XML</span></span>

<span data-ttu-id="49f66-104"><xref:System.Runtime.Serialization.Json.JsonReaderWriterFactory> 生成的读取器和编写器通过 JavaScript 对象表示法 (JSON) 内容提供 XML API。</span><span class="sxs-lookup"><span data-stu-id="49f66-104">The readers and writers produced by the <xref:System.Runtime.Serialization.Json.JsonReaderWriterFactory> provide an XML API over JavaScript Object Notation (JSON) content.</span></span> <span data-ttu-id="49f66-105">JSON 使用 JavaScript 的对象文字子集对数据进行编码。</span><span class="sxs-lookup"><span data-stu-id="49f66-105">JSON encodes data using a subset of the object literals of JavaScript.</span></span> <span data-ttu-id="49f66-106">使用或 Windows Communication Foundation (WCF) 应用程序时，也会使用此工厂生成的读取器和编写器来发送或接收 JSON 内容 <xref:System.ServiceModel.Channels.WebMessageEncodingBindingElement> <xref:System.ServiceModel.WebHttpBinding> 。</span><span class="sxs-lookup"><span data-stu-id="49f66-106">The readers and writers produced by this factory are also used when JSON content is being sent or received by Windows Communication Foundation (WCF) applications using the <xref:System.ServiceModel.Channels.WebMessageEncodingBindingElement> or the <xref:System.ServiceModel.WebHttpBinding>.</span></span>

<span data-ttu-id="49f66-107">使用 JSON 内容进行初始化时，JSON 读取器的行为方式与文本 XML 读取器通过 XML 实例执行的方式相同。</span><span class="sxs-lookup"><span data-stu-id="49f66-107">When initialized with JSON content, the JSON reader behaves in the same way that a textual XML reader does over an instance of XML.</span></span> <span data-ttu-id="49f66-108">对文本 XML 读取器的调用序列生成某个 XML 实例时，JSON 编写器写出 JSON 内容。</span><span class="sxs-lookup"><span data-stu-id="49f66-108">The JSON writer, when given a sequence of calls that on a textual XML reader produces a certain XML instance, writes out JSON content.</span></span> <span data-ttu-id="49f66-109">本主题中描述此 XML 实例和 JSON 内容之间的映射以供在高级方案中使用。</span><span class="sxs-lookup"><span data-stu-id="49f66-109">The mapping between this instance of XML and the JSON content is described in this topic for use in advanced scenarios.</span></span>

<span data-ttu-id="49f66-110">在内部，JSON 由 WCF 处理时表示为 XML 信息集。</span><span class="sxs-lookup"><span data-stu-id="49f66-110">Internally, JSON is represented as an XML infoset when processed by WCF.</span></span> <span data-ttu-id="49f66-111">通常，无须关注此内部表示，因为该映射仅仅是逻辑映射：JSON 通常并不物理转换为内存中的 XML 或从 XML 转换为 JSON。</span><span class="sxs-lookup"><span data-stu-id="49f66-111">Normally you do not have to be concerned with this internal representation as the mapping is only a logical one: JSON is normally not physically converted to XML in memory or converted to JSON from XML.</span></span> <span data-ttu-id="49f66-112">该映射意味着 XML API 用于访问 JSON 内容。</span><span class="sxs-lookup"><span data-stu-id="49f66-112">The mapping means that XML APIs are used to access JSON content.</span></span>

<span data-ttu-id="49f66-113">当 WCF 使用 JSON 时，通常情况下，由 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 行为自动插入 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior> ，或在适当的情况下由 <xref:System.ServiceModel.Description.WebHttpBehavior> 行为自动插入。</span><span class="sxs-lookup"><span data-stu-id="49f66-113">When WCF uses JSON, the usual scenario is that the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> is automatically plugged in by the <xref:System.ServiceModel.Description.WebScriptEnablingBehavior> behavior, or by the <xref:System.ServiceModel.Description.WebHttpBehavior> behavior when appropriate.</span></span> <span data-ttu-id="49f66-114"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 了解 JSON 和 XML infoset 之间的映射，其行为就像它直接处理 JSON 那样。</span><span class="sxs-lookup"><span data-stu-id="49f66-114">The <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> understands the mapping between JSON and the XML infoset and acts as if it is dealing with JSON directly.</span></span> <span data-ttu-id="49f66-115">（通过了解 XML 符合下面的映射，可以将 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 与任何 XML 读取器或编写器一起使用。）</span><span class="sxs-lookup"><span data-stu-id="49f66-115">(It is possible to use the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> with any XML reader or writer, with the understanding that the XML conforms to the following mapping.)</span></span>

<span data-ttu-id="49f66-116">在高级方案中，可能需要直接访问下面的映射。</span><span class="sxs-lookup"><span data-stu-id="49f66-116">In advanced scenarios, it may become necessary to directly access the following mapping.</span></span> <span data-ttu-id="49f66-117">希望以自定义方式序列化和反序列化 JSON 而不依赖于 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 时，或者直接为包含 JSON 的消息处理 <xref:System.ServiceModel.Channels.Message> 类型时，会出现这些方案。</span><span class="sxs-lookup"><span data-stu-id="49f66-117">These scenarios occur when you want to serialize and deserialize JSON in custom ways, without relying on the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>, or when dealing with the <xref:System.ServiceModel.Channels.Message> type directly for messages containing JSON.</span></span> <span data-ttu-id="49f66-118">JSON-XML 映射也用于消息日志记录。</span><span class="sxs-lookup"><span data-stu-id="49f66-118">The JSON-XML mapping is also used for message logging.</span></span> <span data-ttu-id="49f66-119">在 WCF 中使用消息日志记录功能时，将根据下一部分中所述的映射，将 JSON 消息作为 XML 记录。</span><span class="sxs-lookup"><span data-stu-id="49f66-119">When using the message logging feature in WCF, JSON messages is logged as XML according to the mapping described in the next section.</span></span>

<span data-ttu-id="49f66-120">为阐明映射的概念，下面的示例采用一个 JSON 文档。</span><span class="sxs-lookup"><span data-stu-id="49f66-120">To clarify the concept of a mapping, the following example is of a JSON document.</span></span>

```json
{"product":"pencil","price":12}
```

<span data-ttu-id="49f66-121">若要使用前面提到的读取器之一读取此 JSON 文档，请使用与读取以下 XML 文档所用相同的 <xref:System.Xml.XmlDictionaryReader> 调用序列。</span><span class="sxs-lookup"><span data-stu-id="49f66-121">To read this JSON document using one of the readers previously mentioned, use the same sequence of <xref:System.Xml.XmlDictionaryReader> calls as you would to read the following XML document.</span></span>

```xml
<root type="object">
    <product type="string">pencil</product>
    <price type="number">12</price>
</root>
```

<span data-ttu-id="49f66-122">此外，如果该示例中的 JSON 消息由 WCF 接收并记录，则会在前面的日志中看到 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-122">Furthermore, if the JSON message in the example is received by WCF and logged, you would see the XML fragment in the preceding log.</span></span>

## <a name="mapping-between-json-and-the-xml-infoset"></a><span data-ttu-id="49f66-123">JSON 和 XML Infoset 之间的映射</span><span class="sxs-lookup"><span data-stu-id="49f66-123">Mapping Between JSON and the XML Infoset</span></span>

<span data-ttu-id="49f66-124">正式地说，根据 [RFC 4627](https://www.ietf.org/rfc/rfc4627.txt) (中所述，在 JSON 中进行映射，但某些限制是宽松的，某些其他) 限制 (而不是文本 xml) ，如 [xml 信息集中](https://www.w3.org/TR/2004/REC-xml-infoset-20040204/)所述。</span><span class="sxs-lookup"><span data-stu-id="49f66-124">Formally, the mapping is between JSON as described in [RFC 4627](https://www.ietf.org/rfc/rfc4627.txt) (except with certain restrictions relaxed and certain other restrictions added) and the XML infoset (and not textual XML) as described in [XML Information Set](https://www.w3.org/TR/2004/REC-xml-infoset-20040204/).</span></span> <span data-ttu-id="49f66-125">请参阅本主题，了解 [方括号] 中的 *信息项* 和字段的定义。</span><span class="sxs-lookup"><span data-stu-id="49f66-125">See this topic for the definitions of *information items* and fields in [square brackets].</span></span>

<span data-ttu-id="49f66-126">空白 JSON 文档映射到空白 XML 文档，空白 XML 文档映射到空白 JSON 文档。</span><span class="sxs-lookup"><span data-stu-id="49f66-126">A blank JSON document maps to a blank XML document, and a blank XML document maps to a blank JSON document.</span></span> <span data-ttu-id="49f66-127">在 XML 到 JSON 的映射上，不允许在文档后出现空格和尾随空格。</span><span class="sxs-lookup"><span data-stu-id="49f66-127">On the XML to JSON mapping, preceding white space and trailing white space after the document are not allowed.</span></span>

<span data-ttu-id="49f66-128">映射是在文档信息项 (DII) 或元素信息项 (EII) 和 JSON 之间定义的。</span><span class="sxs-lookup"><span data-stu-id="49f66-128">The mapping is defined between either a Document Information Item (DII) or an Element Information Item (EII) and JSON.</span></span> <span data-ttu-id="49f66-129">EII 或 DII 的 [文档元素] 属性称为根 JSON 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-129">The EII, or the DII’s [document element] property, is referred to as the Root JSON Element.</span></span> <span data-ttu-id="49f66-130">请注意此映射不支持文档片段（具有多个根元素的 XML）。</span><span class="sxs-lookup"><span data-stu-id="49f66-130">Note that document fragments (XML with multiple root elements) are not supported in this mapping.</span></span>

<span data-ttu-id="49f66-131">示例：下面的文档：</span><span class="sxs-lookup"><span data-stu-id="49f66-131">Example: The following document:</span></span>

```xml
<?xml version="1.0"?>
<root type="number">42</root>
```

<span data-ttu-id="49f66-132">和下面的元素：</span><span class="sxs-lookup"><span data-stu-id="49f66-132">And the following element:</span></span>

```xml
<root type="number">42</root>
```

<span data-ttu-id="49f66-133">都具有到 JSON 的映射。</span><span class="sxs-lookup"><span data-stu-id="49f66-133">Both have a mapping to JSON.</span></span> <span data-ttu-id="49f66-134">`root`在这两种情况下，<> 元素都是根 JSON 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-134">The <`root`> element is the Root JSON Element in both cases.</span></span>

<span data-ttu-id="49f66-135">此外，在使用 DII 的情况下，应该考虑以下内容：</span><span class="sxs-lookup"><span data-stu-id="49f66-135">Furthermore, in the case of a DII, the following should be considered:</span></span>

- <span data-ttu-id="49f66-136">[子级] 列表中的某些项不得存在。</span><span class="sxs-lookup"><span data-stu-id="49f66-136">Some items in the [children] list must not be present.</span></span> <span data-ttu-id="49f66-137">读取从 JSON 映射的 XML 时，不要依赖于此事实。</span><span class="sxs-lookup"><span data-stu-id="49f66-137">Do not rely on this fact when reading XML mapped from JSON.</span></span>

- <span data-ttu-id="49f66-138">[子级] 列表不包含注释信息项。</span><span class="sxs-lookup"><span data-stu-id="49f66-138">The [children] list holds no comment information items.</span></span>

- <span data-ttu-id="49f66-139">[子级] 列表不包含 DTD 信息项。</span><span class="sxs-lookup"><span data-stu-id="49f66-139">The [children] list holds no DTD information items.</span></span>

- <span data-ttu-id="49f66-140">[子级] 列表不包含任何个人信息 (PI) 信息项 (`<?xml…>` 声明不被视为 PI 信息项) </span><span class="sxs-lookup"><span data-stu-id="49f66-140">The [children] list holds no personal Information (PI) information items (the `<?xml…>` declaration is not considered a PI information item)</span></span>

- <span data-ttu-id="49f66-141">[符号] 集为空。</span><span class="sxs-lookup"><span data-stu-id="49f66-141">The [notations] set is empty.</span></span>

- <span data-ttu-id="49f66-142">[未分析的实体] 集为空。</span><span class="sxs-lookup"><span data-stu-id="49f66-142">The [unparsed entities] set is empty.</span></span>

<span data-ttu-id="49f66-143">示例：下面的文档没有到 JSON 的映射，因为 [子级] 包含 PI 和注释。</span><span class="sxs-lookup"><span data-stu-id="49f66-143">Example: The following document has no mapping to JSON because [children] holds a PI and a comment.</span></span>

```xml
<?xml version="1.0"?>
<!--comment--><?pi?>
<root type="number">42</root>
```

<span data-ttu-id="49f66-144">根 JSON 元素的 EII 具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="49f66-144">The EII for the Root JSON Element has the following characteristics:</span></span>

- <span data-ttu-id="49f66-145">[本地名称] 具有值“root”。</span><span class="sxs-lookup"><span data-stu-id="49f66-145">[local name] has the value "root".</span></span>

- <span data-ttu-id="49f66-146">[命名空间名称] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-146">[namespace name] has no value.</span></span>

- <span data-ttu-id="49f66-147">[前缀] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-147">[prefix] has no value.</span></span>

- <span data-ttu-id="49f66-148">[子级] 可能包含 EII（表示内部元素，将进一步描述）或 CII（字符信息项，将进一步描述）或这两者都不包含，但不能同时包含这两者。</span><span class="sxs-lookup"><span data-stu-id="49f66-148">[children] may either contain EIIs (which represent Inner Elements as described further) or CIIs (Character Information Items as described further) or none of these, but not both.</span></span>

- <span data-ttu-id="49f66-149">[属性] 可能包含以下可选的属性信息项 (AII)</span><span class="sxs-lookup"><span data-stu-id="49f66-149">[attributes] may contain the following optional attribute information items (AIIs)</span></span>

- <span data-ttu-id="49f66-150">JSON 类型属性（“type”），将进一步描述。</span><span class="sxs-lookup"><span data-stu-id="49f66-150">The JSON Type Attribute ("type") as described further.</span></span> <span data-ttu-id="49f66-151">此属性用于保留已映射 XML 中的 JSON 类型（字符串、数字、boolean、对象、数组或 null）。</span><span class="sxs-lookup"><span data-stu-id="49f66-151">This attribute is used to preserve the JSON type (string, number, boolean, object, array or null) in the mapped XML.</span></span>

- <span data-ttu-id="49f66-152">数据协定名称属性 ( " \_ \_ type" ) ，如下面所述。</span><span class="sxs-lookup"><span data-stu-id="49f66-152">The Data Contract Name Attribute ("\_\_type") as described further.</span></span> <span data-ttu-id="49f66-153">仅当 JSON 类型属性也存在且其 [正常化值] 为“object”时，此属性才能存在。</span><span class="sxs-lookup"><span data-stu-id="49f66-153">This attribute is can only be present if the JSON type attribute is also present and its [normalized value] is "object".</span></span> <span data-ttu-id="49f66-154">此属性由 `DataContractJsonSerializer` 用来保留数据协定类型信息 - 例如，在序列化派生类型和期望基类型的多态情况下。</span><span class="sxs-lookup"><span data-stu-id="49f66-154">This attribute is used by the `DataContractJsonSerializer` to preserve data contract type information - for example, in polymorphic cases where a derived type is serialized and where a base type is expected.</span></span> <span data-ttu-id="49f66-155">如果未使用 `DataContractJsonSerializer`，则大多数情况下忽略此属性。</span><span class="sxs-lookup"><span data-stu-id="49f66-155">If you are not working with the `DataContractJsonSerializer`, in most cases, this attribute is ignored.</span></span>

- <span data-ttu-id="49f66-156">[范围内命名空间] 包含将 "xml" 绑定到的 `http://www.w3.org/XML/1998/namespace` 信息集规范要求的绑定。</span><span class="sxs-lookup"><span data-stu-id="49f66-156">[in-scope namespaces] contains the binding of "xml" to `http://www.w3.org/XML/1998/namespace` as mandated by the infoset specification.</span></span>

- <span data-ttu-id="49f66-157">[子级]、[属性] 和 [范围内命名空间] 不得具有除前面指定的之外的任何项，[命名空间属性] 不得具有成员，但是在读取从 JSON 映射的 XML 时不依赖于这些事实。</span><span class="sxs-lookup"><span data-stu-id="49f66-157">[children], [attributes] and [in-scope namespaces] must not have any items other than as specified previously and [namespace attributes] must have no members, but do not rely on these facts when reading XML mapped from JSON.</span></span>

<span data-ttu-id="49f66-158">示例：下面的文档没有到 JSON 的映射，因为 [命名空间属性] 不为空。</span><span class="sxs-lookup"><span data-stu-id="49f66-158">Example: The following document has no mapping to JSON because [namespace attributes] is not empty.</span></span>

```xml
<?xml version="1.0"?>
<root xmlns:a="myattributevalue">42</root>
```

<span data-ttu-id="49f66-159">JSON 类型属性的 AII 具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="49f66-159">The AII for the JSON Type Attribute has the following characteristics:</span></span>

- <span data-ttu-id="49f66-160">[命名空间名称] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-160">[namespace name] has no value.</span></span>
- <span data-ttu-id="49f66-161">[前缀] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-161">[prefix] has no value.</span></span>
- <span data-ttu-id="49f66-162">[本地名称] 为“type”。</span><span class="sxs-lookup"><span data-stu-id="49f66-162">[local name] is "type".</span></span>
- <span data-ttu-id="49f66-163">[正常化值] 是下面部分中描述的可能类型值之一。</span><span class="sxs-lookup"><span data-stu-id="49f66-163">[normalized value] is one of the possible type values described in the following section.</span></span>
- <span data-ttu-id="49f66-164">[已指定] 为 `true`。</span><span class="sxs-lookup"><span data-stu-id="49f66-164">[specified] is `true`.</span></span>
- <span data-ttu-id="49f66-165">[属性类型] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-165">[attribute type] has no value.</span></span>
- <span data-ttu-id="49f66-166">[引用] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-166">[references] has no value.</span></span>

<span data-ttu-id="49f66-167">数据协定名称属性的 AII 具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="49f66-167">The AII for the Data Contract Name Attribute has the following characteristics:</span></span>

- <span data-ttu-id="49f66-168">[命名空间名称] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-168">[namespace name] has no value.</span></span>
- <span data-ttu-id="49f66-169">[前缀] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-169">[prefix] has no value.</span></span>
- <span data-ttu-id="49f66-170">[local name] 是 " \_ \_ type" (两个下划线，然后 "type" ) 。</span><span class="sxs-lookup"><span data-stu-id="49f66-170">[local name] is "\_\_type" (two underscores and then "type").</span></span>
- <span data-ttu-id="49f66-171">[正常化值] 是任何有效的 Unicode 字符串 – 此字符串到 JSON 的映射将在下面的部分中进行描述。</span><span class="sxs-lookup"><span data-stu-id="49f66-171">[normalized value] is any valid Unicode string – the mapping of this string to JSON is described in the following section.</span></span>
- <span data-ttu-id="49f66-172">[已指定] 为 `true`。</span><span class="sxs-lookup"><span data-stu-id="49f66-172">[specified] is `true`.</span></span>
- <span data-ttu-id="49f66-173">[属性类型] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-173">[attribute type] has no value.</span></span>
- <span data-ttu-id="49f66-174">[引用] 没有值。</span><span class="sxs-lookup"><span data-stu-id="49f66-174">[references] has no value.</span></span>

<span data-ttu-id="49f66-175">根 JSON 元素中包含的内部元素或其他内部元素具有以下特征：</span><span class="sxs-lookup"><span data-stu-id="49f66-175">Inner elements contained within the Root JSON Element or other inner elements have the following characteristics:</span></span>

- <span data-ttu-id="49f66-176">[本地名称] 可以具有任何值，如前面所述。</span><span class="sxs-lookup"><span data-stu-id="49f66-176">[local name] may have any value as described further.</span></span>
- <span data-ttu-id="49f66-177">[命名空间名称]、[前缀]、[子级]、[属性]、[命名空间属性] 和 [范围内命名空间] 遵循与根 JSON 元素相同的规则。</span><span class="sxs-lookup"><span data-stu-id="49f66-177">[namespace name], [prefix], [children], [attributes], [namespace attributes], and [in-scope namespaces] are subject to the same rules as the Root JSON Element.</span></span>

<span data-ttu-id="49f66-178">在根 JSON 元素和内部元素中，JSON 类型属性定义到 JSON 的映射和可能的 [子级] 及其解释。</span><span class="sxs-lookup"><span data-stu-id="49f66-178">In both the Root JSON Element and the inner elements, the JSON Type Attribute defines the mapping to JSON and the possible [children] and their interpretation.</span></span> <span data-ttu-id="49f66-179">属性的 [正常化值] 区分大小写，并且必须是小写，且不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="49f66-179">The attribute’s [normalized value] is case-sensitive and must be lowercase, and cannot contain white space.</span></span>

|<span data-ttu-id="49f66-180">JSON 类型属性的 AII 的 [规范化值]</span><span class="sxs-lookup"><span data-stu-id="49f66-180">[normalized value] of JSON Type Attribute’s AII</span></span>|<span data-ttu-id="49f66-181">对应 EII 的已允许 [子级]</span><span class="sxs-lookup"><span data-stu-id="49f66-181">Allowed [children] of the corresponding EII</span></span>|<span data-ttu-id="49f66-182">映射到 JSON</span><span class="sxs-lookup"><span data-stu-id="49f66-182">Mapping to JSON</span></span>|
|---------------------------------------------------------|---------------------------------------------------|---------------------|
|<span data-ttu-id="49f66-183">`string`（或缺少 JSON 类型 AII）</span><span class="sxs-lookup"><span data-stu-id="49f66-183">`string` (or absence of the JSON type AII)</span></span><br /><br /> <span data-ttu-id="49f66-184">`string` 与缺少 JSON 类型 AII 相同，使 `string` 成为默认值。</span><span class="sxs-lookup"><span data-stu-id="49f66-184">A `string` and the absence of the JSON type AII are the same makes `string` the default.</span></span><br /><br /> <span data-ttu-id="49f66-185">因此，`<root> string1</root>` 映射到 JSON `string`“string1”。</span><span class="sxs-lookup"><span data-stu-id="49f66-185">So, `<root> string1</root>` maps to the JSON `string` "string1".</span></span>|<span data-ttu-id="49f66-186">0个或多个个 cii</span><span class="sxs-lookup"><span data-stu-id="49f66-186">0 or more CIIs</span></span>|<span data-ttu-id="49f66-187">JSON `string`（JSON RFC，第 2.5 节）。</span><span class="sxs-lookup"><span data-stu-id="49f66-187">A JSON `string` (JSON RFC, section 2.5).</span></span> <span data-ttu-id="49f66-188">每个 `char` 是对应于来自 CII 的 [字符代码] 的字符。</span><span class="sxs-lookup"><span data-stu-id="49f66-188">Each `char` is a character that corresponds to the [character code] from the CII.</span></span> <span data-ttu-id="49f66-189">如果没有 CII，则它映射到空 JSON `string`。</span><span class="sxs-lookup"><span data-stu-id="49f66-189">If there are no CIIs, it maps to an empty JSON `string`.</span></span><br /><br /> <span data-ttu-id="49f66-190">示例：下面的元素映射到 JSON 片段：</span><span class="sxs-lookup"><span data-stu-id="49f66-190">Example: The following element maps to a JSON fragment:</span></span><br /><br /> `<root type="string">42</root>`<br /><br /> <span data-ttu-id="49f66-191">JSON 片段是“42”。</span><span class="sxs-lookup"><span data-stu-id="49f66-191">The JSON fragment is "42".</span></span><br /><br /> <span data-ttu-id="49f66-192">在 XML 到 JSON 的映射上，必须转义的字符映射到转义符，所有其他字符都映射到未转义的字符。</span><span class="sxs-lookup"><span data-stu-id="49f66-192">On XML to JSON mapping, characters that must be escaped map to escaped characters, all others map to characters that are not escaped.</span></span> <span data-ttu-id="49f66-193">"/" 字符是特殊字符–即使它不必 (写出为 "/" ) ，它也会被转义 \\ 。</span><span class="sxs-lookup"><span data-stu-id="49f66-193">The "/" character is special – it is escaped even though it does not have to be (written out as "\\/").</span></span><br /><br /> <span data-ttu-id="49f66-194">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-194">Example: The following element maps to a JSON fragment.</span></span><br /><br /> `<root type="string">the "da/ta"</root>`<br /><br /> <span data-ttu-id="49f66-195">JSON 片段是 "/ta" \\ \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="49f66-195">The JSON fragment is "the \\"da\\/ta\\"".</span></span><br /><br /> <span data-ttu-id="49f66-196">在 JSON 到 XML 的映射上，任何转义符和未转义的字符都正确映射到对应的 [字符代码]。</span><span class="sxs-lookup"><span data-stu-id="49f66-196">On JSON to XML mapping, any escaped characters and characters that are not escaped map correctly to the corresponding [character code].</span></span><br /><br /> <span data-ttu-id="49f66-197">示例：JSON 片段“\u0041BC”映射到下面的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-197">Example: The JSON fragment "\u0041BC", maps to the following XML element.</span></span><br /><br /> `<root type="string">ABC</root>`<br /><br /> <span data-ttu-id="49f66-198">该字符串可在 JSON RFC) 的第2部分中的空白 ( "ws" 的周围，而不会映射到 XML。</span><span class="sxs-lookup"><span data-stu-id="49f66-198">The string can be surrounded by white space ('ws' in section 2 of the JSON RFC) that does not get mapped to XML.</span></span><br /><br /> <span data-ttu-id="49f66-199">示例：JSON 片段           "ABC"（在第一个双引号之前存在空格）映射到下面的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-199">Example: The JSON fragment           "ABC", (there are spaces before the first double quote), maps to the following XML element.</span></span><br /><br /> `<root type="string">ABC</root>`<br /><br /> <span data-ttu-id="49f66-200">XML 中的任何空白都映射到 JSON 中的空白区域。</span><span class="sxs-lookup"><span data-stu-id="49f66-200">Any white space in XML maps to white space in JSON.</span></span><br /><br /> <span data-ttu-id="49f66-201">示例：下面的 XML 元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-201">Example: The following XML element maps to a JSON fragment.</span></span><br /><br /> `<root type="string">  A BC      </root>`<br /><br /> <span data-ttu-id="49f66-202">JSON 片段是“ A BC ”。</span><span class="sxs-lookup"><span data-stu-id="49f66-202">The JSON fragment is " A BC ".</span></span>|
|`number`|<span data-ttu-id="49f66-203">1 个或多个 CII</span><span class="sxs-lookup"><span data-stu-id="49f66-203">1 or more CIIs</span></span>|<span data-ttu-id="49f66-204">JSON `number` (JSON RFC，2.4) ，可能由空格括起来。</span><span class="sxs-lookup"><span data-stu-id="49f66-204">A JSON `number` (JSON RFC, section 2.4), possibly surrounded by white space.</span></span> <span data-ttu-id="49f66-205">Number/空格组合中的每个字符都是对应于 CII 中 [字符代码] 的字符。</span><span class="sxs-lookup"><span data-stu-id="49f66-205">Each character in the number/white space combination is a character that corresponds to the [character code] from the CII.</span></span><br /><br /> <span data-ttu-id="49f66-206">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-206">Example: The following element maps to a JSON fragment.</span></span><br /><br /> `<root type="number">    42</root>`<br /><br /> <span data-ttu-id="49f66-207">JSON 片段是    42</span><span class="sxs-lookup"><span data-stu-id="49f66-207">The JSON fragment is    42</span></span><br /><br /> <span data-ttu-id="49f66-208">)  (保留空白。</span><span class="sxs-lookup"><span data-stu-id="49f66-208">(White space is preserved).</span></span>|
|`boolean`|<span data-ttu-id="49f66-209">4或 5 (个 cii，它对应于 `true` 或 `false`) ，可能括在额外的空白个 cii 中。</span><span class="sxs-lookup"><span data-stu-id="49f66-209">4 or 5 CIIs (which corresponds to `true` or `false`), possibly surrounded by additional white-space CIIs.</span></span>|<span data-ttu-id="49f66-210">对应于字符串“true”的 CII 序列被映射到文字 `true`，而对应于字符串“false”的 CII 序列被映射到文字 `false`。</span><span class="sxs-lookup"><span data-stu-id="49f66-210">A CII sequence that corresponds to the string "true" is mapped to the literal `true`, and a CII sequence that corresponds to the string "false" is mapped to the literal `false`.</span></span> <span data-ttu-id="49f66-211">将保留周围的空白区域。</span><span class="sxs-lookup"><span data-stu-id="49f66-211">Surrounding white space is preserved.</span></span><br /><br /> <span data-ttu-id="49f66-212">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-212">Example: The following element maps to a JSON fragment.</span></span><br /><br /> `<root type="boolean"> false</root>`<br /><br /> <span data-ttu-id="49f66-213">JSON 片段是 `false`。</span><span class="sxs-lookup"><span data-stu-id="49f66-213">The JSON fragment is `false`.</span></span>|
|`null`|<span data-ttu-id="49f66-214">都不允许。</span><span class="sxs-lookup"><span data-stu-id="49f66-214">None allowed.</span></span>|<span data-ttu-id="49f66-215">文字 `null`。</span><span class="sxs-lookup"><span data-stu-id="49f66-215">The literal `null`.</span></span> <span data-ttu-id="49f66-216">在 JSON 到 XML 的映射上， `null` 可能会将空格括在第2部分中的空白 ( "ws") ，而不会映射到 xml。</span><span class="sxs-lookup"><span data-stu-id="49f66-216">On JSON to XML mapping, the `null` may be surrounded by white space (‘ws’ in section 2) that does not get mapped to XML.</span></span><br /><br /> <span data-ttu-id="49f66-217">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-217">Example: The following element maps to a JSON fragment.</span></span><br /><br /> `<root type="null"/>`<br /><br /> <span data-ttu-id="49f66-218">或</span><span class="sxs-lookup"><span data-stu-id="49f66-218">or</span></span><br /><br /> `<root type="null"></root>`<br /><br /> <span data-ttu-id="49f66-219">:</span><span class="sxs-lookup"><span data-stu-id="49f66-219">:</span></span><br /><br /> <span data-ttu-id="49f66-220">在这两种情况下 JSON 片段都是 `Null`。</span><span class="sxs-lookup"><span data-stu-id="49f66-220">The JSON fragment in both cases is `Null`.</span></span>|
|`object`|<span data-ttu-id="49f66-221">0 个或多个 EII。</span><span class="sxs-lookup"><span data-stu-id="49f66-221">0 or more EIIs.</span></span>|<span data-ttu-id="49f66-222">如 JSON RFC 第 2.2 节中的 `begin-object`（左花括号），后跟每个 EII 的成员记录，将进一步说明。</span><span class="sxs-lookup"><span data-stu-id="49f66-222">A `begin-object` (left curly brace) as in section 2.2 of the JSON RFC, followed by a member record for each EII as described further.</span></span> <span data-ttu-id="49f66-223">如果存在多个 EII，则在成员记录之间存在值分隔符（逗号）。</span><span class="sxs-lookup"><span data-stu-id="49f66-223">If there is more than one EII, there are value-separators (commas) between the member records.</span></span> <span data-ttu-id="49f66-224">所有这一切后跟 end-object（右花括号）。</span><span class="sxs-lookup"><span data-stu-id="49f66-224">All this is followed by an end-object (right curly brace).</span></span><br /><br /> <span data-ttu-id="49f66-225">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-225">Example: The following element maps to the JSON fragment.</span></span><br /><br /> `<root type="object">`<br /><br /> `<type1 type="string">aaa\</type1>`<br /><br /> `<type2 type="string">bbb\</type2>`<br /><br /> `</root >`<br /><br /> <span data-ttu-id="49f66-226">JSON 片段是 `{"type1":"aaa","type2":"bbb"}`。</span><span class="sxs-lookup"><span data-stu-id="49f66-226">The JSON fragment is `{"type1":"aaa","type2":"bbb"}`.</span></span><br /><br /> <span data-ttu-id="49f66-227">如果在 XML 到 JSON 的映射上存在数据协定类型属性，则在开头插入其他成员记录。</span><span class="sxs-lookup"><span data-stu-id="49f66-227">If the Data Contract Type Attribute is present on XML to JSON mapping, then an additional Member Record is inserted at the beginning.</span></span> <span data-ttu-id="49f66-228">其名称是数据协定类型属性的 [本地名称] ( " \_ \_ Type" ) ，其值为属性的 "规范化值"。</span><span class="sxs-lookup"><span data-stu-id="49f66-228">Its name is the [local name] of the Data Contract Type Attribute ("\_\_type"), and its value is the attribute's [normalized value].</span></span> <span data-ttu-id="49f66-229">相反，在 JSON 到 XML 的映射中，如果第一个成员记录的名称是数据协定类型属性的 [local name] (即 " \_ \_ Type" ) ，则映射的 XML 中将显示相应的数据协定类型属性，但不存在相应的 EII。</span><span class="sxs-lookup"><span data-stu-id="49f66-229">Conversely, on JSON to XML mapping, if the first member-record’s name is the [local name] of the Data Contract Type Attribute (that is, "\_\_type"), a corresponding Data Contract Type Attribute is present in the mapped XML, but a corresponding EII is not present.</span></span> <span data-ttu-id="49f66-230">请注意，此成员记录必须首先出现在 JSON 对象中才能应用此特殊映射。</span><span class="sxs-lookup"><span data-stu-id="49f66-230">Note that this member record must occur first in the JSON object for this special mapping to apply.</span></span> <span data-ttu-id="49f66-231">这与通常的 JSON 处理（成员记录的顺序是不重要的）相背离。</span><span class="sxs-lookup"><span data-stu-id="49f66-231">This represents a departure from usual JSON processing, where the order of member records is not significant.</span></span><br /><br /> <span data-ttu-id="49f66-232">例如：</span><span class="sxs-lookup"><span data-stu-id="49f66-232">Example:</span></span><br /><br /> <span data-ttu-id="49f66-233">下面的 JSON 片段映射到 XML。</span><span class="sxs-lookup"><span data-stu-id="49f66-233">The following JSON fragment maps to XML.</span></span><br /><br /> `{"__type":"Person","name":"John"}`<br /><br /> <span data-ttu-id="49f66-234">XML 是下面的代码。</span><span class="sxs-lookup"><span data-stu-id="49f66-234">The XML is the following code.</span></span><br /><br /> `<root type="object" __type="Person">   <name type="string">John</name> </root>`<br /><br /> <span data-ttu-id="49f66-235">请注意， \_ \_ 类型 AII 存在，但没有 \_ \_ 类型为 EII。</span><span class="sxs-lookup"><span data-stu-id="49f66-235">Notice that the \_\_type AII is present, but there is no \_\_type EII.</span></span><br /><br /> <span data-ttu-id="49f66-236">但是，如果保留 JSON 中的顺序，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="49f66-236">However, if the order in the JSON is reversed as shown in the following example.</span></span><br /><br /> `{"name":"John","\_\_type":"Person"}`<br /><br /> <span data-ttu-id="49f66-237">则显示对应的 XML。</span><span class="sxs-lookup"><span data-stu-id="49f66-237">The corresponding XML is shown.</span></span><br /><br /> `<root type="object">   <name type="string">John</name>   <__type type="string">Person</__type> </root>`<br /><br /> <span data-ttu-id="49f66-238">也就是说， \_ _type 停止具有特殊意义，并像平常一样（而非 AII）映射到 EII。</span><span class="sxs-lookup"><span data-stu-id="49f66-238">That is, \__type ceases to have special meaning and maps to an EII as usual, not AII.</span></span><br /><br /> <span data-ttu-id="49f66-239">映射到 JSON 值时，AII 的 [正常化值] 的转义/未转义规则与在此表的“string”行中指定的 JSON 字符串的相同。</span><span class="sxs-lookup"><span data-stu-id="49f66-239">Escaping/unescaping rules for the AII’s [normalized value] when mapped to a JSON value are the same as for JSON strings, specified in the "string" row of this table.</span></span><br /><br /> <span data-ttu-id="49f66-240">例如：</span><span class="sxs-lookup"><span data-stu-id="49f66-240">Example:</span></span><br /><br /> `<root type="object" __type="\abc" />`<br /><br /> <span data-ttu-id="49f66-241">前面的示例可以映射到下面的 JSON。</span><span class="sxs-lookup"><span data-stu-id="49f66-241">to the previous example can be mapped to the following JSON.</span></span><br /><br /> `{"__type":"\\abc"}`<br /><br /> <span data-ttu-id="49f66-242">在 XML 到 JSON 的映射中，第一个 EII 的 [本地名称] 不得为 " \_ \_ type"。</span><span class="sxs-lookup"><span data-stu-id="49f66-242">On an XML to JSON mapping, the first EII’s [local name] must not be "\_\_type".</span></span><br /><br /> <span data-ttu-id="49f66-243">`ws`在 xml 到 json 的映射上从不生成空白 () ，在 json 到 XML 的映射上将忽略空格。</span><span class="sxs-lookup"><span data-stu-id="49f66-243">White space (`ws`) is never generated on XML to JSON mapping for objects and is ignored on JSON to XML mapping.</span></span><br /><br /> <span data-ttu-id="49f66-244">示例：下面的 JSON 片段映射到 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-244">Example: The following JSON fragment maps to an XML element.</span></span><br /><br /> `{ "ccc" : "aaa", "ddd" :"bbb"}`<br /><br /> <span data-ttu-id="49f66-245">在下面的代码中显示了 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-245">The XML element is shown in the following code.</span></span><br /><br /> `<root type="object">    <ccc type="string">aaa</ccc>    <ddd type="string">bbb</bar> </root >`|
|<span data-ttu-id="49f66-246">array</span><span class="sxs-lookup"><span data-stu-id="49f66-246">array</span></span>|<span data-ttu-id="49f66-247">0 个或多个 EII</span><span class="sxs-lookup"><span data-stu-id="49f66-247">0 or more EIIs</span></span>|<span data-ttu-id="49f66-248">如 JSON RFC 第 2.3 节中的 begin-array（左花括号），后跟每个 EII 的数组记录，将进一步描述。</span><span class="sxs-lookup"><span data-stu-id="49f66-248">A begin-array (left square bracket) as in section 2.3 of the JSON RFC, followed by an array record for each EII as described further.</span></span> <span data-ttu-id="49f66-249">如果存在多个 EII，则在数组记录之间存在值分隔符（逗号）。</span><span class="sxs-lookup"><span data-stu-id="49f66-249">If there is more than one EII, there are value-separators (commas) between the array records.</span></span> <span data-ttu-id="49f66-250">所有这一切后跟 end-array。</span><span class="sxs-lookup"><span data-stu-id="49f66-250">All this is followed by an end-array.</span></span><br /><br /> <span data-ttu-id="49f66-251">示例：下面的 XML 元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-251">Example: The following XML element maps to a JSON fragment.</span></span><br /><br /> `<root type="array"/>    <item type="string">aaa</item>    <item type="string">bbb</item> </root >`<br /><br /> <span data-ttu-id="49f66-252">JSON 片段是 `["aaa","bbb"]`</span><span class="sxs-lookup"><span data-stu-id="49f66-252">The JSON fragment is `["aaa","bbb"]`</span></span><br /><br /> <span data-ttu-id="49f66-253">`ws`在 xml 到 json 的映射上从不生成空白 () ，且在 json 到 XML 的映射上将忽略空格。</span><span class="sxs-lookup"><span data-stu-id="49f66-253">White space (`ws`) is never generated on XML to JSON mapping for arrays and is ignored on JSON to XML mapping.</span></span><br /><br /> <span data-ttu-id="49f66-254">示例： JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-254">Example: A JSON fragment.</span></span><br /><br />`["aaa", "bbb"]`<br /><br /> <span data-ttu-id="49f66-255">它映射到的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="49f66-255">The XML element that it maps to.</span></span><br /><br /> `<root type="array"/>    <item type="string">aaa</item>    <item type="string">bbb</item> </root >`|

<span data-ttu-id="49f66-256">成员记录的工作原理如下：</span><span class="sxs-lookup"><span data-stu-id="49f66-256">Member Records work as follows:</span></span>

- <span data-ttu-id="49f66-257">内部元素的 [本地名称] 映射到 `string` 的 `member` 部分，如 JSON RFC 第 2.2 节所定义。</span><span class="sxs-lookup"><span data-stu-id="49f66-257">Inner element’s [local name] maps to the `string` part of the `member` as defined in section 2.2 of the JSON RFC.</span></span>

<span data-ttu-id="49f66-258">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-258">Example: The following element maps to a JSON fragment.</span></span>

```xml
<root type="object">
    <myLocalName type="string">aaa</myLocalName>
</root>
```

<span data-ttu-id="49f66-259">将显示下面的 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-259">The following JSON fragment is displayed.</span></span>

```json
{"myLocalName":"aaa"}
```

- <span data-ttu-id="49f66-260">在 XML 到 JSON 的映射上，对必须在 JSON 中转义的字符进行转义，而不对其他字符进行转义。</span><span class="sxs-lookup"><span data-stu-id="49f66-260">On the XML to JSON mapping, the characters that must be escaped in JSON are escaped, and the others are not escaped.</span></span> <span data-ttu-id="49f66-261">但是，对“/”字符进行转义，尽管它不是必须转义的字符（在 JSON 到 XML 的映射上不必对它进行转义）。</span><span class="sxs-lookup"><span data-stu-id="49f66-261">The "/" character, even though it is not a character that must be escaped, is escaped nevertheless (it does not have to be escaped on JSON to XML mapping).</span></span> <span data-ttu-id="49f66-262">这是支持 JSON 中 `DateTime` 数据的 ASP.NET AJAX 格式所必需的。</span><span class="sxs-lookup"><span data-stu-id="49f66-262">This is required to support the ASP.NET AJAX format for `DateTime` data in JSON.</span></span>

- <span data-ttu-id="49f66-263">在 JSON 到 XML 的映射上，提取所有字符（如有必要，则包括未转义的字符）以构成一个生成 [本地名称] 的 `string`。</span><span class="sxs-lookup"><span data-stu-id="49f66-263">On the JSON to XML mapping, all characters (including the not escaped characters, if necessary) are taken to form a `string` that produces a [local name].</span></span>

- <span data-ttu-id="49f66-264">按照 `JSON Type Attribute`，内部元素 [子级] 映射到第 2.2 节中的值，就像 `Root JSON Element` 那样。</span><span class="sxs-lookup"><span data-stu-id="49f66-264">Inner elements [children] map to the value in section 2.2, according to the `JSON Type Attribute` just like for the `Root JSON Element`.</span></span> <span data-ttu-id="49f66-265">允许 EII 的多级嵌套（包括数组中的嵌套）。</span><span class="sxs-lookup"><span data-stu-id="49f66-265">Multiple levels of nesting of EIIs (including nesting within arrays) are allowed.</span></span>

<span data-ttu-id="49f66-266">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-266">Example: The following element maps to a JSON fragment.</span></span>

```xml
<root type="object">
    <myLocalName1 type="string">myValue1</myLocalName1>
    <myLocalName2 type="number">2</myLocalName2>
    <myLocalName3 type="object">
        <myNestedName1 type="boolean">true</myNestedName1>
        <myNestedName2 type="null"/>
    </myLocalName3>
</root >
```

<span data-ttu-id="49f66-267">下面的 JSON 片段是它映射到的内容。</span><span class="sxs-lookup"><span data-stu-id="49f66-267">The following JSON fragment is what it maps to.</span></span>

```json
{"myLocalName1":"myValue1","myLocalName2":2,"myLocalName3":{"myNestedName1":true,"myNestedName2":null}}
```

> [!NOTE]
> <span data-ttu-id="49f66-268">在前面的映射中没有 XML 编码步骤。</span><span class="sxs-lookup"><span data-stu-id="49f66-268">There is no XML encoding step in the preceding mapping.</span></span> <span data-ttu-id="49f66-269">因此，WCF 仅支持 JSON 文档，其中键名称中的所有字符都是 XML 元素名称中的有效字符。</span><span class="sxs-lookup"><span data-stu-id="49f66-269">Therefore, WCF only supports JSON documents where all characters in key names are valid characters in XML element names.</span></span> <span data-ttu-id="49f66-270">例如，不支持 JSON 文档 {"<"： "a"}，因为 < 不是 XML 元素的有效名称。</span><span class="sxs-lookup"><span data-stu-id="49f66-270">For example, the JSON document {"<":"a"} is not supported because < is not a valid name for an XML element.</span></span>

<span data-ttu-id="49f66-271">相反的情况（字符在 XML 中有效而在 JSON 中无效）不会导致任何问题，因为上述映射包括 JSON 转义/取消转义步骤。</span><span class="sxs-lookup"><span data-stu-id="49f66-271">The reverse situation (characters valid in XML but not in JSON) does not cause any problems because the preceding mapping includes JSON escaping/unescaping steps.</span></span>

<span data-ttu-id="49f66-272">数组记录的工作原理如下：</span><span class="sxs-lookup"><span data-stu-id="49f66-272">Array Records work as follows:</span></span>

- <span data-ttu-id="49f66-273">内部元素的 [本地名称] 是“item”。</span><span class="sxs-lookup"><span data-stu-id="49f66-273">Inner element’s [local name] is "item".</span></span>

- <span data-ttu-id="49f66-274">按照 JSON 类型属性，内部元素的 [子级] 映射到第 2.3 节中的值，Root JSON 元素也是这样。</span><span class="sxs-lookup"><span data-stu-id="49f66-274">Inner element’s [children] map to the value in section 2.3, according to the JSON Type Attribute as is does for the Root JSON Element.</span></span> <span data-ttu-id="49f66-275">允许 EII 的多级嵌套（包括对象内的嵌套）。</span><span class="sxs-lookup"><span data-stu-id="49f66-275">Multiple levels of nesting of EIIs (including nesting within objects) are allowed.</span></span>

<span data-ttu-id="49f66-276">示例：下面的元素映射到 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-276">Example: The following element maps to a JSON fragment.</span></span>

```xml
<root type="array">
    <item type="string">myValue1</item>
    <item type="number">2</item>
    <item type="array">
    <item type="boolean">true</item>
    <item type="null"/></item>
</root>
```

<span data-ttu-id="49f66-277">下面是 JSON 片段。</span><span class="sxs-lookup"><span data-stu-id="49f66-277">The following is the JSON fragment.</span></span>

```json
["myValue1",2,[true,null]]
```

## <a name="see-also"></a><span data-ttu-id="49f66-278">请参阅</span><span class="sxs-lookup"><span data-stu-id="49f66-278">See also</span></span>

- <xref:System.Runtime.Serialization.Json.JsonReaderWriterFactory>
- <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>
- [<span data-ttu-id="49f66-279">独立 JSON 序列化</span><span class="sxs-lookup"><span data-stu-id="49f66-279">Stand-Alone JSON Serialization</span></span>](stand-alone-json-serialization.md)
