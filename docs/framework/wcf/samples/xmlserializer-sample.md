---
description: 了解有关以下内容的详细信息： XMLSerializer 示例
title: XMLSerializer 示例
ms.date: 03/30/2017
ms.assetid: 7d134453-9a35-4202-ba77-9ca3a65babc3
ms.openlocfilehash: 724eefd2b7d64b2495f1703fa62843dfbc50657b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99676490"
---
# <a name="xmlserializer-sample"></a><span data-ttu-id="f5017-103">XMLSerializer 示例</span><span class="sxs-lookup"><span data-stu-id="f5017-103">XMLSerializer Sample</span></span>

<span data-ttu-id="f5017-104">此示例演示如何序列化和反序列化与 <xref:System.Xml.Serialization.XmlSerializer> 兼容的类型。</span><span class="sxs-lookup"><span data-stu-id="f5017-104">This sample demonstrates how to serialize and deserialize types that are compatible with the <xref:System.Xml.Serialization.XmlSerializer>.</span></span> <span data-ttu-id="f5017-105"> (WCF) 格式化程序的默认 Windows Communication Foundation 为 <xref:System.Runtime.Serialization.DataContractSerializer> 类。</span><span class="sxs-lookup"><span data-stu-id="f5017-105">The default Windows Communication Foundation (WCF) formatter is the <xref:System.Runtime.Serialization.DataContractSerializer> class.</span></span> <span data-ttu-id="f5017-106">当无法使用 <xref:System.Xml.Serialization.XmlSerializer> 类时，可以使用 <xref:System.Runtime.Serialization.DataContractSerializer> 类来序列化和反序列化类型。</span><span class="sxs-lookup"><span data-stu-id="f5017-106">The <xref:System.Xml.Serialization.XmlSerializer> class can be used to serialize and deserialize types when the <xref:System.Runtime.Serialization.DataContractSerializer> class cannot be used.</span></span> <span data-ttu-id="f5017-107">当需要精确控制 XML 时通常会发生这种情况 - 例如，如果某个数据必须是一个 XML 属性，而不能是 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="f5017-107">This is often the case when precise control over the XML is required - for example, if a piece of data must be an XML attribute and not an XML element.</span></span> <span data-ttu-id="f5017-108">此外， <xref:System.Xml.Serialization.XmlSerializer> 在为非 WCF 服务创建客户端时，经常会自动选择。</span><span class="sxs-lookup"><span data-stu-id="f5017-108">Also, the <xref:System.Xml.Serialization.XmlSerializer> often gets automatically selected when creating clients for non-WCF services.</span></span>  
  
 <span data-ttu-id="f5017-109">在此示例中，客户端是一个控制台应用程序 (.exe)，服务是由 Internet 信息服务 (IIS) 承载的。</span><span class="sxs-lookup"><span data-stu-id="f5017-109">In this sample, the client is a console application (.exe) and the service is hosted by Internet Information Services (IIS).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f5017-110">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="f5017-110">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="f5017-111"><xref:System.ServiceModel.ServiceContractAttribute> 和 <xref:System.ServiceModel.XmlSerializerFormatAttribute> 必须应用于该接口，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="f5017-111">The <xref:System.ServiceModel.ServiceContractAttribute> and <xref:System.ServiceModel.XmlSerializerFormatAttribute> must be applied to the interface as shown in the following sample code.</span></span>  
  
```csharp  
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples"), XmlSerializerFormat]  
public interface IXmlSerializerCalculator  
{  
    [OperationContract]  
    ComplexNumber Add(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Subtract(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Multiply(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Divide(ComplexNumber n1, ComplexNumber n2);  
}  
```  
  
 <span data-ttu-id="f5017-112">`ComplexNumber` 类的公共成员被 <xref:System.Xml.Serialization.XmlSerializer> 序列化为 XML 属性。</span><span class="sxs-lookup"><span data-stu-id="f5017-112">The public members of `ComplexNumber` class are serialized by <xref:System.Xml.Serialization.XmlSerializer> as XML attributes.</span></span> <span data-ttu-id="f5017-113"><xref:System.Runtime.Serialization.DataContractSerializer> 不能用于创建此类 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="f5017-113">The <xref:System.Runtime.Serialization.DataContractSerializer> cannot be used to create this kind of XML instance.</span></span>  
  
```csharp  
public class ComplexNumber  
{  
    private double real;  
    private double imaginary;  
  
    [XmlAttribute]  
    public double Real  
    {  
        get { return real; }  
        set { real = value; }  
    }  
  
    [XmlAttribute]  
    public double Imaginary  
    {  
        get { return imaginary; }  
        set { imaginary = value; }  
    }  
  
    public ComplexNumber(double real, double imaginary)  
    {  
        this.Real = real;  
        this.Imaginary = imaginary;  
    }  
    public ComplexNumber()  
    {  
        this.Real = 0;  
        this.Imaginary = 0;  
    }  
  
}  
```  
  
 <span data-ttu-id="f5017-114">服务实现计算并返回相应的结果 - 接受并返回 `ComplexNumber` 类型的值。</span><span class="sxs-lookup"><span data-stu-id="f5017-114">The service implementation calculates and returns the appropriate result—accepting and returning values of the `ComplexNumber` type.</span></span>  
  
```csharp  
public class XmlSerializerCalculatorService : IXmlSerializerCalculator  
{  
    public ComplexNumber Add(ComplexNumber n1, ComplexNumber n2)  
    {  
        return new ComplexNumber(n1.Real + n2.Real, n1.Imaginary +  
                                                      n2.Imaginary);  
    }  
    …  
}  
```  
  
 <span data-ttu-id="f5017-115">客户端实现也使用复数。</span><span class="sxs-lookup"><span data-stu-id="f5017-115">The client implementation also uses complex numbers.</span></span> <span data-ttu-id="f5017-116">服务协定和数据类型都在 generatedClient.cs 源文件中定义，该文件是由 "" 元数据实用工具工具生成的，它从服务元数据中 [ ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 。</span><span class="sxs-lookup"><span data-stu-id="f5017-116">Both the service contract and the data types are defined in the generatedClient.cs source file, which was generated by the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) from service metadata.</span></span> <span data-ttu-id="f5017-117">Svcutil.exe 可以检测何时协定不能由 <xref:System.Runtime.Serialization.DataContractSerializer> 序列化，在这种情况下转而发出 `XmlSerializable` 类型。</span><span class="sxs-lookup"><span data-stu-id="f5017-117">Svcutil.exe can detect when a contract is not serializable by the <xref:System.Runtime.Serialization.DataContractSerializer> and reverts to emitting `XmlSerializable` types in this case.</span></span> <span data-ttu-id="f5017-118">如果要强制使用 <xref:System.Xml.Serialization.XmlSerializer>，可以将 /serializer:XmlSerializer（使用 XmlSerializer）命令选项传递给 Svcutil.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="f5017-118">If you want to force the use of the <xref:System.Xml.Serialization.XmlSerializer>, you can pass the /serializer:XmlSerializer (use XmlSerializer) command option to the Svcutil.exe tool.</span></span>  
  
```csharp  
// Create a client.  
XmlSerializerCalculatorClient client = new  
                         XmlSerializerCalculatorClient();  
  
// Call the Add service operation.  
ComplexNumber value1 = new ComplexNumber();  
value1.Real = 1;  
value1.Imaginary = 2;  
ComplexNumber value2 = new ComplexNumber();  
value2.Real = 3;  
value2.Imaginary = 4;  
ComplexNumber result = client.Add(value1, value2);  
Console.WriteLine("Add({0} + {1}i, {2} + {3}i) = {4} + {5}i",  
    value1.Real, value1.Imaginary, value2.Real, value2.Imaginary,
    result.Real, result.Imaginary);  
    …  
}  
```  
  
 <span data-ttu-id="f5017-119">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="f5017-119">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="f5017-120">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="f5017-120">Press ENTER in the client window to shut down the client.</span></span>  
  
```console  
Add(1 + 2i, 3 + 4i) = 4 + 6i  
Subtract(1 + 2i, 3 + 4i) = -2 + -2i  
Multiply(2 + 3i, 4 + 7i) = -13 + 26i  
Divide(3 + 7i, 5 + -2i) = 0.0344827586206897 + 1.41379310344828i  
  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="f5017-121">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="f5017-121">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="f5017-122">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="f5017-122">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="f5017-123">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="f5017-123">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="f5017-124">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="f5017-124">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="f5017-125">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="f5017-125">The samples may already be installed on your machine.</span></span> <span data-ttu-id="f5017-126">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="f5017-126">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="f5017-127">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5017-127">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="f5017-128">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="f5017-128">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Client\Interop\XmlSerializer`  
