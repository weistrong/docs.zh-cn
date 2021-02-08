---
description: 了解更多：可互操作的对象引用
title: 可互操作的对象引用
ms.date: 04/15/2019
ms.assetid: cb8da4c8-08ca-4220-a16b-e04c8f527f1b
ms.openlocfilehash: 27c801fb3954c7ea3f821a6588a2229502702989
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802679"
---
# <a name="interoperable-object-references"></a><span data-ttu-id="df98b-103">可互操作的对象引用</span><span class="sxs-lookup"><span data-stu-id="df98b-103">Interoperable object references</span></span>

<span data-ttu-id="df98b-104">默认情况下， <xref:System.Runtime.Serialization.DataContractSerializer> 按值对对象进行序列化。</span><span class="sxs-lookup"><span data-stu-id="df98b-104">By default, <xref:System.Runtime.Serialization.DataContractSerializer> serializes objects by value.</span></span> <span data-ttu-id="df98b-105">您可以使用 <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> 属性指示数据协定序列化程序在序列化对象时保留对象引用。</span><span class="sxs-lookup"><span data-stu-id="df98b-105">You can use the <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> property to instruct the data contract serializer to preserve object references when serializing objects.</span></span>  
  
## <a name="generated-xml"></a><span data-ttu-id="df98b-106">生成的 XML</span><span class="sxs-lookup"><span data-stu-id="df98b-106">Generated XML</span></span>  

 <span data-ttu-id="df98b-107">例如，请考虑下面的对象：</span><span class="sxs-lookup"><span data-stu-id="df98b-107">As an example, consider the following object:</span></span>  
  
```csharp  
[DataContract]  
public class X  
{  
    SomeClass someInstance = new SomeClass();  
    [DataMember]  
    public SomeClass A = someInstance;  
    [DataMember]  
    public SomeClass B = someInstance;  
}  
  
public class SomeClass
{  
}  
```  
  
 <span data-ttu-id="df98b-108">当 <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> 设置为 `false`（默认值）时，会生成下面的 XML：</span><span class="sxs-lookup"><span data-stu-id="df98b-108">With <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> set to `false` (the default), the following XML is generated:</span></span>  
  
```xml  
<X>  
   <A>contents of someInstance</A>  
   <B>contents of someInstance</B>  
</X>  
```  
  
 <span data-ttu-id="df98b-109">当 <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> 设置为 `true` 时，会生成下面的 XML：</span><span class="sxs-lookup"><span data-stu-id="df98b-109">With <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> set to `true`, the following XML is generated:</span></span>  
  
```xml  
<X>  
   <A id="1">contents of someInstance</A>  
   <B ref="1"></B>  
</X>  
```  
  
 <span data-ttu-id="df98b-110">但是， <xref:System.Runtime.Serialization.XsdDataContractExporter> `id` `ref` 即使属性设置为，也不会在架构中描述和特性 `preserveObjectReferences` `true` 。</span><span class="sxs-lookup"><span data-stu-id="df98b-110">However, <xref:System.Runtime.Serialization.XsdDataContractExporter> doesn't describe the `id` and `ref` attributes in its schema, even when the `preserveObjectReferences` property is set to `true`.</span></span>  
  
## <a name="using-isreference"></a><span data-ttu-id="df98b-111">使用 IsReference</span><span class="sxs-lookup"><span data-stu-id="df98b-111">Using IsReference</span></span>  

 <span data-ttu-id="df98b-112">若要生成根据描述的架构有效的对象引用信息，请将 <xref:System.Runtime.Serialization.DataContractAttribute> 属性应用到类型，并将 <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> 标志设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="df98b-112">To generate object reference information that's valid according to the schema that describes it, apply the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to a type, and set the <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> flag to `true`.</span></span> <span data-ttu-id="df98b-113">下面的示例通过添加以下示例修改 `X` 了上一示例中的类 `IsReference` ：</span><span class="sxs-lookup"><span data-stu-id="df98b-113">The following example modifies class `X` in the previous example by adding `IsReference`:</span></span>  
  
```csharp
[DataContract(IsReference=true)]
public class X
{  
     SomeClass someInstance = new SomeClass();
     [DataMember]
     public SomeClass A = someInstance;
     [DataMember]
     public SomeClass B = someInstance;
}
  
public class SomeClass
{
}  
````

 <span data-ttu-id="df98b-114">生成的 XML 如下：</span><span class="sxs-lookup"><span data-stu-id="df98b-114">The generated XML is as follows:</span></span>  

```xml
<X>  
    <A id="1">
        <Value>contents of A</Value>  
    </A>
    <B ref="1"></B>  
</X>
```  
  
 <span data-ttu-id="df98b-115">使用 `IsReference` 可确保消息往返时遵从架构要求。</span><span class="sxs-lookup"><span data-stu-id="df98b-115">Using `IsReference` ensures compliance on message round-tripping.</span></span> <span data-ttu-id="df98b-116">如果没有此方法，则在从架构生成类型时，该类型的 XML 输出不一定与最初假设的架构兼容。</span><span class="sxs-lookup"><span data-stu-id="df98b-116">Without it, when a type is generated from schema, the XML output for that type isn't necessarily compatible with the schema originally assumed.</span></span> <span data-ttu-id="df98b-117">换言之，虽然 `id` 和 `ref` 属性进行了序列化，但原始架构可能禁止这些属性（或所有属性）在 XML 中出现。</span><span class="sxs-lookup"><span data-stu-id="df98b-117">In other words, although the `id` and `ref` attributes were serialized, the original schema could have barred these attributes (or all attributes) from occurring in the XML.</span></span> <span data-ttu-id="df98b-118">`IsReference`应用于数据成员后，在往返时，将继续将成员识别为 *可引用*。</span><span class="sxs-lookup"><span data-stu-id="df98b-118">With `IsReference` applied to a data member, the member continues to be recognized as *referenceable* when round-tripped.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df98b-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="df98b-119">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute.IsReference?displayProperty=nameWithType>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute.IsReference?displayProperty=nameWithType>
