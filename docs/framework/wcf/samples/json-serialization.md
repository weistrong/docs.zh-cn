---
description: 了解详细信息： DataContractJsonSerializer 示例
title: DataContractJsonSerializer 示例
ms.date: 03/30/2017
ms.assetid: 3c2c4747-7510-4bdf-b4fe-64f98428ef4a
ms.openlocfilehash: 258cd38f9ee532e5d750b4cabaa4214366835be7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726346"
---
# <a name="datacontractjsonserializer-sample"></a><span data-ttu-id="73ab6-103">DataContractJsonSerializer 示例</span><span class="sxs-lookup"><span data-stu-id="73ab6-103">DataContractJsonSerializer sample</span></span>

> [!NOTE]
> <span data-ttu-id="73ab6-104">此示例适用于 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 。</span><span class="sxs-lookup"><span data-stu-id="73ab6-104">This sample is for <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer>.</span></span> <span data-ttu-id="73ab6-105">对于涉及序列化和反序列化 JSON 的大多数方案，我们建议在 [System.Text.Js上命名空间](../../../standard/serialization/system-text-json-overview.md)中的 api。</span><span class="sxs-lookup"><span data-stu-id="73ab6-105">For most scenarios that involve serializing and deserializing JSON, we recommend the APIs in the [System.Text.Json namespace](../../../standard/serialization/system-text-json-overview.md).</span></span>

<span data-ttu-id="73ab6-106"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 支持同一类型，如 <xref:System.Runtime.Serialization.DataContractSerializer>。</span><span class="sxs-lookup"><span data-stu-id="73ab6-106"><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> supports the same types as <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span> <span data-ttu-id="73ab6-107">JSON 数据格式在编写异步 JavaScript 和 XML (AJAX) 样式的 Web 应用程序时特别有用。</span><span class="sxs-lookup"><span data-stu-id="73ab6-107">The JSON data format is especially useful when writing Asynchronous JavaScript and XML (AJAX)-style Web applications.</span></span> <span data-ttu-id="73ab6-108">Windows Communication Foundation 中 (WCF) 的 AJAX 支持经过优化，可通过 ScriptManager 控件与 ASP.NET AJAX 一起使用。</span><span class="sxs-lookup"><span data-stu-id="73ab6-108">AJAX support in Windows Communication Foundation (WCF) is optimized for use with ASP.NET AJAX through the ScriptManager control.</span></span> <span data-ttu-id="73ab6-109">有关如何使用 Windows Communication Foundation (WCF) 与 ASP.NET AJAX 一起使用的示例，请参阅 [Ajax 示例](ajax.md)。</span><span class="sxs-lookup"><span data-stu-id="73ab6-109">For examples of how to use Windows Communication Foundation (WCF) with ASP.NET AJAX, see the [AJAX Samples](ajax.md).</span></span>  
  
<span data-ttu-id="73ab6-110">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="73ab6-110">The set-up procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
<span data-ttu-id="73ab6-111">此示例使用 `Person` 数据协定演示序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="73ab6-111">The sample uses a `Person` data contract to demonstrate serialization and deserialization.</span></span>  

```csharp
[DataContract]
class Person
{
    [DataMember]
    internal string name;

    [DataMember]
    internal int age;
}
```

 <span data-ttu-id="73ab6-112">若要将 `Person` 类型的实例序列化为 JSON，首先创建 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 并使用 `WriteObject` 方法将 JSON 数据编写成流。</span><span class="sxs-lookup"><span data-stu-id="73ab6-112">To serialize an instance of the `Person` type to JSON, create the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> first and use the `WriteObject` method to write JSON data to a stream.</span></span>  

```csharp
Person p = new Person();
//Set up Person object...
MemoryStream stream1 = new MemoryStream();
DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));
ser.WriteObject(stream1, p);
```

 <span data-ttu-id="73ab6-113">内存流包含有效的 JSON 数据。</span><span class="sxs-lookup"><span data-stu-id="73ab6-113">The memory stream contains valid JSON data.</span></span>
  
```json  
{"age":42,"name":"John"}  
```  
  
 <span data-ttu-id="73ab6-114">此示例演示从 JSON 数据反序列化为对象。</span><span class="sxs-lookup"><span data-stu-id="73ab6-114">The sample demonstrates deserializing from JSON data into an object.</span></span> <span data-ttu-id="73ab6-115">然后重绕流并调用 `ReadObject`。</span><span class="sxs-lookup"><span data-stu-id="73ab6-115">You then rewind the stream and call `ReadObject`.</span></span>  

```csharp
Person p2 = (Person)ser.ReadObject(stream1);
```

 <span data-ttu-id="73ab6-116">检查 `p2` 对象显示 JSON 数据已正确反序列化。</span><span class="sxs-lookup"><span data-stu-id="73ab6-116">Examining the `p2` object reveals that the JSON data has been deserialized correctly.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="73ab6-117">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="73ab6-117">The samples may already be installed on your machine.</span></span> <span data-ttu-id="73ab6-118">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="73ab6-118">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="73ab6-119">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="73ab6-119">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="73ab6-120">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="73ab6-120">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\JsonSerialization`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="73ab6-121">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="73ab6-121">To set up, build and run the sample</span></span>  
  
1. <span data-ttu-id="73ab6-122">按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中所述生成解决方案 JsonSerialization。</span><span class="sxs-lookup"><span data-stu-id="73ab6-122">Build the solution JsonSerialization.sln as described in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
2. <span data-ttu-id="73ab6-123">运行生成的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="73ab6-123">Run the resulting console application.</span></span>  
