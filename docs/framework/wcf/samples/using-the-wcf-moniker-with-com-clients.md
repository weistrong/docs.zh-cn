---
description: 了解详细信息：对 COM 客户端使用 WCF 名字对象
title: 对 COM 客户端使用 WCF 标记
ms.date: 03/30/2017
ms.assetid: e2799bfe-88bd-49d7-9d6d-ac16a9b16b04
ms.openlocfilehash: c2888224e36a473773ef6d7fbd72dbae7420fab0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755754"
---
# <a name="using-the-wcf-moniker-with-com-clients"></a><span data-ttu-id="21892-103">对 COM 客户端使用 WCF 标记</span><span class="sxs-lookup"><span data-stu-id="21892-103">Using the WCF Moniker with COM Clients</span></span>

<span data-ttu-id="21892-104">此示例演示如何使用 Windows Communication Foundation (WCF) 服务名字对象将 Web 服务集成到基于 COM 的开发环境中，例如 Microsoft Office Visual Basic for Applications (Office VBA) 或 Visual Basic 6.0。</span><span class="sxs-lookup"><span data-stu-id="21892-104">This sample demonstrates how to use the Windows Communication Foundation (WCF) service moniker to integrate Web services into COM-based development environments, such as Microsoft Office Visual Basic for Applications (Office VBA) or Visual Basic 6.0.</span></span> <span data-ttu-id="21892-105">本示例由 Windows 脚本宿主客户端 (.vbs)、客户端支持库 (.dll) 和 Internet 信息服务 (IIS) 承载的服务库 (.dll) 组成。</span><span class="sxs-lookup"><span data-stu-id="21892-105">This sample consists of a Windows Script Host client (.vbs), a supporting client library (.dll), and a service library (.dll) hosted by Internet Information Services (IIS).</span></span> <span data-ttu-id="21892-106">该服务是一个计算器服务，COM 客户端将对服务调用数学运算（加、减、乘和除）。</span><span class="sxs-lookup"><span data-stu-id="21892-106">The service is a calculator service and the COM client calls math operations—Add, Subtract, Multiply, and Divide—on the service.</span></span> <span data-ttu-id="21892-107">客户端活动显示在消息框窗口中。</span><span class="sxs-lookup"><span data-stu-id="21892-107">Client activity is visible in the message box windows.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="21892-108">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="21892-108">The set-up procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="21892-109">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="21892-109">The samples may already be installed on your computer.</span></span> <span data-ttu-id="21892-110">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="21892-110">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="21892-111">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21892-111">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="21892-112">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="21892-112">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Interop\COM`  
  
 <span data-ttu-id="21892-113">该服务实现一个 `ICalculator` 协定，下面的代码示例对该协定进行了如下定义。</span><span class="sxs-lookup"><span data-stu-id="21892-113">The service implements an `ICalculator` contract defined as shown in the following code example.</span></span>  
  
```csharp
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface ICalculator  
{  
    [OperationContract]  
    double Add(double n1, double n2);  
    [OperationContract]  
    double Subtract(double n1, double n2);  
    [OperationContract]  
    double Multiply(double n1, double n2);  
    [OperationContract]  
    double Divide(double n1, double n2);  
}  
```  
  
 <span data-ttu-id="21892-114">示例演示三种使用标记的备选方法：</span><span class="sxs-lookup"><span data-stu-id="21892-114">The sample demonstrates the three alternative approaches for using the moniker:</span></span>  
  
- <span data-ttu-id="21892-115">类型化协定 - 该协定在客户端计算机上注册为 COM 可见类型。</span><span class="sxs-lookup"><span data-stu-id="21892-115">Typed contract – The contract is registered as a COM visible type on the client computer.</span></span>  
  
- <span data-ttu-id="21892-116">WSDL 协定 - 该协定以 WSDL 文档的形式提供。</span><span class="sxs-lookup"><span data-stu-id="21892-116">WSDL contract – The contract is supplied in the form of a WSDL document.</span></span>  
  
- <span data-ttu-id="21892-117">元数据交换协定 - 该协定可在运行时从元数据交换 (MEX) 终结点进行检索。</span><span class="sxs-lookup"><span data-stu-id="21892-117">Metadata Exchange contract – The contract is retrieved at runtime from a Metadata Exchange (MEX) endpoint.</span></span>  
  
## <a name="typed-contract"></a><span data-ttu-id="21892-118">类型化协定</span><span class="sxs-lookup"><span data-stu-id="21892-118">Typed Contract</span></span>  

 <span data-ttu-id="21892-119">若要对类型化协定用法使用标记，必须向 COM 注册服务协定的经适当属性化的类型。</span><span class="sxs-lookup"><span data-stu-id="21892-119">To use the moniker with a typed contract use, appropriately attributed types for the service contract must be registered with COM.</span></span> <span data-ttu-id="21892-120">首先，必须使用 [ ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md)来生成客户端。</span><span class="sxs-lookup"><span data-stu-id="21892-120">First, a client must be generated by using the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="21892-121">在客户端目录中通过命令提示符运行以下命令可以生成该类型化代理。</span><span class="sxs-lookup"><span data-stu-id="21892-121">Run the following command from a command prompt in the client directory to generate the typed proxy.</span></span>  
  
```console  
svcutil.exe /n:http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples http://localhost/servicemodelsamples/service.svc /out:generatedClient.cs  
```  
  
 <span data-ttu-id="21892-122">此类必须包括在项目中，并且应将项目配置为在编译时生成一个 COM 可见的已签名程序集。</span><span class="sxs-lookup"><span data-stu-id="21892-122">This class must be included in a project and the project should be configured to generate a COM-visible, signed assembly when compiled.</span></span> <span data-ttu-id="21892-123">AssemblyInfo.cs 文件中应该包括下面的属性。</span><span class="sxs-lookup"><span data-stu-id="21892-123">The following attribute should be included in the AssemblyInfo.cs file.</span></span>  
  
```csharp
[assembly: ComVisible(true)]  
```  
  
 <span data-ttu-id="21892-124">生成项目以后，通过使用 `regasm` 注册 COM 可见类型，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="21892-124">After building the project, register the COM-visible types by using `regasm` as shown in the following example.</span></span>  
  
```console  
regasm.exe /tlb:CalcProxy.tlb client.dll  
```  
  
 <span data-ttu-id="21892-125">创建的程序集应该添加到全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="21892-125">The assembly that is created should be added to the Global Assembly Cache.</span></span> <span data-ttu-id="21892-126">虽然并不严格要求，但这样做可简化运行时定位程序集的过程。</span><span class="sxs-lookup"><span data-stu-id="21892-126">Though not strictly required, this simplifies the process of the runtime locating the assembly.</span></span> <span data-ttu-id="21892-127">下面的命令将程序集添加到全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="21892-127">The following command adds the assembly to the Global Assembly Cache.</span></span>  
  
```console  
gacutil.exe /i client.dll  
```  
  
> [!NOTE]
> <span data-ttu-id="21892-128">服务标记只要求进行类型注册，并不使用代理与服务通信。</span><span class="sxs-lookup"><span data-stu-id="21892-128">The service moniker requires only the type registration and does not use the proxy to communicate with the service.</span></span>  
  
 <span data-ttu-id="21892-129">ComCalcClient.vbs 客户端应用程序使用 `GetObject` 函数来构造服务的代理，使用服务标记语法指定服务的地址、绑定和协定。</span><span class="sxs-lookup"><span data-stu-id="21892-129">ComCalcClient.vbs client application uses the `GetObject` function to construct a proxy for the service, using the service moniker syntax to specify the address, binding, and contract for the service.</span></span>  
  
```vbscript
Set typedServiceMoniker = GetObject(  
"service4:address=http://localhost/ServiceModelSamples/service.svc, binding=wsHttpBinding,
contractType={9213C6D2-5A6F-3D26-839B-3BA9B82228D3}")  
```  
  
 <span data-ttu-id="21892-130">标记使用的参数将会指定：</span><span class="sxs-lookup"><span data-stu-id="21892-130">The parameters used by the moniker specify:</span></span>  
  
- <span data-ttu-id="21892-131">服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="21892-131">The address of the service endpoint.</span></span>  
  
- <span data-ttu-id="21892-132">客户端应该用来与该终结点连接的绑定。</span><span class="sxs-lookup"><span data-stu-id="21892-132">The binding that the client should use to connect with that endpoint.</span></span> <span data-ttu-id="21892-133">虽然可以在客户端配置文件中定义自定义绑定，但本例中使用了系统定义的 wsHttpBinding。</span><span class="sxs-lookup"><span data-stu-id="21892-133">In this case, the system-defined wsHttpBinding is used though custom bindings can be defined in client configuration files.</span></span> <span data-ttu-id="21892-134">自定义绑定在与 Cscript.exe 处于同一目录的 Cscript.exe.config 文件中进行定义，以便可以与 Windows 脚本主机一起使用。</span><span class="sxs-lookup"><span data-stu-id="21892-134">For use with the Windows Script Host, the custom binding is defined in a Cscript.exe.config file in the same directory as Cscript.exe.</span></span>  
  
- <span data-ttu-id="21892-135">在终结点受支持的协定的类型。</span><span class="sxs-lookup"><span data-stu-id="21892-135">The type of the contract that is supported at the endpoint.</span></span> <span data-ttu-id="21892-136">此类型是在上面生成并注册的类型。</span><span class="sxs-lookup"><span data-stu-id="21892-136">This is the type that was generated and registered above.</span></span> <span data-ttu-id="21892-137">由于 Visual Basic 脚本不提供强类型 COM 环境，因此必须指定协定的标识符。</span><span class="sxs-lookup"><span data-stu-id="21892-137">Because Visual Basic script does not provide a strongly typed COM environment, an identifier for the contract must be specified.</span></span> <span data-ttu-id="21892-138">此 GUID 是 CalcProxy.tlb 中的 `interfaceID`，可以通过使用 COM 工具（如 OLE/COM 对象查看器 (OleView.exe)）来查看。</span><span class="sxs-lookup"><span data-stu-id="21892-138">This GUID is the `interfaceID` from CalcProxy.tlb, which can be viewed by using COM tools such as the OLE/COM Object Viewer (OleView.exe).</span></span> <span data-ttu-id="21892-139">对于强类型化环境（如 Office VBA 或 Visual Basic 6.0），添加对类型库的显式引用，然后声明代理对象的类型可用于替代协定参数。</span><span class="sxs-lookup"><span data-stu-id="21892-139">For strongly typed environments such as Office VBA or Visual Basic 6.0, adding an explicit reference to the type library and then declaring the type of the proxy object can be used in place of the contract parameter.</span></span> <span data-ttu-id="21892-140">这样还可在客户端应用程序开发过程中提供 IntelliSense 支持。</span><span class="sxs-lookup"><span data-stu-id="21892-140">This also provides IntelliSense support during client application development.</span></span>  
  
 <span data-ttu-id="21892-141">在用服务标记构造代理实例之后，客户端应用程序可以对此代理调用方法，这将生成调用相应服务操作的服务标记基础结构。</span><span class="sxs-lookup"><span data-stu-id="21892-141">Having constructed the proxy instance with the service moniker, the client application can call methods on the proxy, which results in the service moniker infrastructure calling the corresponding service operations.</span></span>  
  
```vbscript  
' Call the service operations using the moniker object  
WScript.Echo "Typed service moniker: 100 + 15.99 = " & typedServiceMoniker.Add(100, 15.99)  
```  
  
 运行示例时，操作响应将显示在 Windows 脚本宿主消息框窗口中。 这说明了使用类型化名字对象发出 COM 调用以便与 WCF 服务进行通信的 COM 客户端。 <span data-ttu-id="21892-144">虽然在客户端应用程序中使用了 COM，但与服务的通信仅由 Web 服务调用组成。</span><span class="sxs-lookup"><span data-stu-id="21892-144">Despite the use of COM in the client application, the communication with the service consists only of Web service calls.</span></span>  
  
## <a name="wsdl-contract"></a><span data-ttu-id="21892-145">WSDL 协定</span><span class="sxs-lookup"><span data-stu-id="21892-145">WSDL Contract</span></span>  

 <span data-ttu-id="21892-146">使用具有 WSDL 协定的标记不需要注册任何客户端库，但必须通过带外机制（如使用浏览器访问服务的 WSDL 终结点）来检索服务的 WSDL 协定。</span><span class="sxs-lookup"><span data-stu-id="21892-146">To use the moniker with a WSDL contract, no client library registration is required but the WSDL contract for the service must be retrieved through an out-of-band mechanism such as using a browser to access the WSDL endpoint for the service.</span></span> <span data-ttu-id="21892-147">标记之后可以在执行时访问该协定。</span><span class="sxs-lookup"><span data-stu-id="21892-147">The moniker can then access that contract at execution time.</span></span>  
  
 <span data-ttu-id="21892-148">ComCalcClient.vbs 客户端应用程序使用 `FileSystemObject` 访问保存在本地的 WSDL 文件，然后再次使用 `GetObject` 函数来构造服务的代理。</span><span class="sxs-lookup"><span data-stu-id="21892-148">The ComCalcClient.vbs client application uses the `FileSystemObject` to access the locally saved WSDL file and then again uses the `GetObject` function to construct a proxy for the service.</span></span>  
  
```vbscript  
' Open the WSDL contract file and read it all into the wsdlContract string  
Const ForReading = 1  
Set objFSO = CreateObject("Scripting.FileSystemObject")  
Set objFile = objFSO.OpenTextFile("serviceWsdl.xml", ForReading)  
wsdlContract = objFile.ReadAll  
objFile.Close  
  
' Create a string for the service moniker including the content of the WSDL contract file  
wsdlMonikerString = "service4:address='http://localhost/ServiceModelSamples/service.svc'"  
wsdlMonikerString = wsdlMonikerString + ", binding=WSHttpBinding_ICalculator, bindingNamespace='http://Microsoft.ServiceModel.Samples'"  
wsdlMonikerString = wsdlMonikerString + ", wsdl='" & wsdlContract & "'"  
wsdlMonikerString = wsdlMonikerString + ", contract=ICalculator, contractNamespace='http://Microsoft.ServiceModel.Samples'"  
  
' Create the service moniker object  
Set wsdlServiceMoniker = GetObject(wsdlMonikerString)  
```  
  
 <span data-ttu-id="21892-149">标记使用的参数将会指定：</span><span class="sxs-lookup"><span data-stu-id="21892-149">The parameters used by the moniker specify:</span></span>  
  
- <span data-ttu-id="21892-150">服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="21892-150">The address of the service endpoint.</span></span>  
  
- <span data-ttu-id="21892-151">客户端用于与该终结点连接的绑定和在其中定义该绑定的命名空间。</span><span class="sxs-lookup"><span data-stu-id="21892-151">The binding that the client should use to connect with that endpoint and the namespace in which that binding is defined.</span></span> <span data-ttu-id="21892-152">在本例中，使用 `wsHttpBinding_ICalculator`。</span><span class="sxs-lookup"><span data-stu-id="21892-152">In this case, the `wsHttpBinding_ICalculator` is used.</span></span>  
  
- <span data-ttu-id="21892-153">定义协定的 WSDL。</span><span class="sxs-lookup"><span data-stu-id="21892-153">The WSDL that defines the contract.</span></span> <span data-ttu-id="21892-154">在本例中是已从 serviceWsdl.xml 文件中读取的字符串。</span><span class="sxs-lookup"><span data-stu-id="21892-154">In this case this is the string that has been read from the serviceWsdl.xml file.</span></span>  
  
- <span data-ttu-id="21892-155">协定的名称和命名空间。</span><span class="sxs-lookup"><span data-stu-id="21892-155">The name and namespace of the contract.</span></span> <span data-ttu-id="21892-156">由于 WSDL 可能包含多个协定，因此需要此标识。</span><span class="sxs-lookup"><span data-stu-id="21892-156">This identification is required because the WSDL may contain more than one contract.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="21892-157">默认情况下，WCF 服务为使用的每个命名空间生成单独的 WSDL 文件。</span><span class="sxs-lookup"><span data-stu-id="21892-157">By default, WCF services generate separate WSDL files for each namespace that the use.</span></span> <span data-ttu-id="21892-158">这些文件通过使用 WSDL 导入构造连接。</span><span class="sxs-lookup"><span data-stu-id="21892-158">These are linked with the use of the WSDL import construct.</span></span> <span data-ttu-id="21892-159">由于标记需要单个 WSDL 定义，因此服务必须使用单个命名空间（如本示例中的演示），或者必须手动合并单独的文件。</span><span class="sxs-lookup"><span data-stu-id="21892-159">Because the moniker expects a single WSDL definition, the service must either use a single namespace as demonstrated in this sample or the separate files must be manually merged.</span></span>  
  
 <span data-ttu-id="21892-160">在用服务标记构造代理实例之后，客户端应用程序可以对此代理调用方法，这将生成调用相应服务操作的服务标记基础结构。</span><span class="sxs-lookup"><span data-stu-id="21892-160">Having constructed the proxy instance with the service moniker, the client application can call methods on the proxy, which results in the service moniker infrastructure calling the corresponding service operations.</span></span>  
  
```vbscript  
' Call the service operations using the moniker object  
WScript.Echo "WSDL service moniker: 145 - 76.54 = " & wsdlServiceMoniker.Subtract(145, 76.54)  
```  
  
 运行示例时，操作响应将显示在 Windows 脚本宿主消息框窗口中。 <span data-ttu-id="21892-162">这说明了使用带有 WSDL 协定的名字对象进行 COM 调用以便与 WCF 服务进行通信的 COM 客户端。</span><span class="sxs-lookup"><span data-stu-id="21892-162">This demonstrates a COM client making COM calls using the moniker with a WSDL contract to communicate with a WCF service.</span></span>  
  
## <a name="metadata-exchange-contract"></a><span data-ttu-id="21892-163">元数据交换协定</span><span class="sxs-lookup"><span data-stu-id="21892-163">Metadata Exchange Contract</span></span>  

 <span data-ttu-id="21892-164">和 WSDL 协定一样，使用具有 MEX 协定的标记不需要注册任何客户端。</span><span class="sxs-lookup"><span data-stu-id="21892-164">To use the moniker with a MEX contract, as with the WSDL contract, no client registration is required.</span></span> <span data-ttu-id="21892-165">服务的协定通过内部使用元数据交换在执行时进行检索。</span><span class="sxs-lookup"><span data-stu-id="21892-165">The contract for the service is retrieved at execution time through the internal use of Metadata Exchange.</span></span>  
  
 <span data-ttu-id="21892-166">ComCalcClient.vbs 客户端应用程序也使用 `GetObject` 函数来构造服务的代理。</span><span class="sxs-lookup"><span data-stu-id="21892-166">The ComCalcClient.vbs client application again uses the `GetObject` function to construct a proxy for the service.</span></span>  
  
```vbscript  
' Create a string for the service moniker specifying the address to retrieve the service metadata from  
mexMonikerString = "service4:mexAddress='http://localhost/servicemodelsamples/service.svc/mex'"  
mexMonikerString = mexMonikerString + ", address='http://localhost/ServiceModelSamples/service.svc'"  
mexMonikerString = mexMonikerString + ", binding=WSHttpBinding_ICalculator, bindingNamespace='http://Microsoft.ServiceModel.Samples'"  
mexMonikerString = mexMonikerString + ", contract=ICalculator, contractNamespace='http://Microsoft.ServiceModel.Samples'"  
  
' Create the service moniker object  
Set mexServiceMoniker = GetObject(mexMonikerString)  
```  
  
 <span data-ttu-id="21892-167">标记使用的参数将会指定：</span><span class="sxs-lookup"><span data-stu-id="21892-167">The parameters used by the moniker specify:</span></span>  
  
- <span data-ttu-id="21892-168">服务元数据交换终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="21892-168">The address of the service metadata exchange endpoint.</span></span>  
  
- <span data-ttu-id="21892-169">服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="21892-169">The address of the service endpoint.</span></span>  
  
- <span data-ttu-id="21892-170">客户端用于与该终结点连接的绑定和在其中定义该绑定的命名空间。</span><span class="sxs-lookup"><span data-stu-id="21892-170">The binding that the client should use to connect with that endpoint and the namespace in which that binding is defined.</span></span> <span data-ttu-id="21892-171">在本例中，使用 `wsHttpBinding_ICalculator`。</span><span class="sxs-lookup"><span data-stu-id="21892-171">In this case, the `wsHttpBinding_ICalculator` is used.</span></span>  
  
- <span data-ttu-id="21892-172">协定的名称和命名空间。</span><span class="sxs-lookup"><span data-stu-id="21892-172">The name and namespace of the contract.</span></span> <span data-ttu-id="21892-173">由于 WSDL 可能包含多个协定，因此需要此标识。</span><span class="sxs-lookup"><span data-stu-id="21892-173">This identification is required because the WSDL may contain more than one contract.</span></span>  
  
 <span data-ttu-id="21892-174">在用服务标记构造代理实例之后，客户端应用程序可以对此代理调用方法，这将生成调用相应服务操作的服务标记基础结构。</span><span class="sxs-lookup"><span data-stu-id="21892-174">Having constructed the proxy instance with the service moniker, the client application can call methods on the proxy, which results in the service moniker infrastructure calling the corresponding service operations.</span></span>  
  
```vbscript  
' Call the service operations using the moniker object  
WScript.Echo "MEX service moniker: 9 * 81.25 = " & mexServiceMoniker.Multiply(9, 81.25)  
```  
  
 运行示例时，操作响应将显示在 Windows 脚本宿主消息框窗口中。 <span data-ttu-id="21892-176">这表明，COM 客户端使用名字对象和 MEX 协定进行 COM 调用，以便与 WCF 服务进行通信。</span><span class="sxs-lookup"><span data-stu-id="21892-176">This demonstrates a COM client making COM calls using the moniker with a MEX contract to communicate with a WCF service.</span></span>  
  
#### <a name="to-set-up-and-build-the-sample"></a><span data-ttu-id="21892-177">设置和生成示例</span><span class="sxs-lookup"><span data-stu-id="21892-177">To set up and build the sample</span></span>  
  
1. <span data-ttu-id="21892-178">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="21892-178">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="21892-179">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="21892-179">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="21892-180">在 Visual Studio 开发人员命令提示中，打开语言特定文件夹下的 \client\bin 文件夹。</span><span class="sxs-lookup"><span data-stu-id="21892-180">From a Developer Command Prompt for Visual Studio, open the \client\bin folder, under the language-specific folder.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="21892-181">如果使用的是 Windows Vista、Windows Server 2008、Windows 7 或 Windows Server 2008 R2，请确保使用管理员权限运行命令提示符。</span><span class="sxs-lookup"><span data-stu-id="21892-181">If you are using Windows Vista, Windows Server 2008, Windows 7, or Windows Server 2008 R2, make sure that you run the command prompt with administrator privileges.</span></span>  
  
4. <span data-ttu-id="21892-182">键入以 `tlbexp.exe client.dll /out:CalcProxy.tlb` 将 dll 导出到 tlb 文件中。</span><span class="sxs-lookup"><span data-stu-id="21892-182">Type in `tlbexp.exe client.dll /out:CalcProxy.tlb` to export the dll to a tlb file.</span></span> <span data-ttu-id="21892-183">预期会出现“Type library exporter warning”（类型库导出程序警告），但由于不需要泛型类型，因此这不是问题。</span><span class="sxs-lookup"><span data-stu-id="21892-183">A "Type library exporter warning" is expected but is not an issue because the generic type is not required.</span></span>  
  
5. <span data-ttu-id="21892-184">键入 `regasm.exe /tlb:CalcProxy.tlb client.dll` 以向 COM 注册类型。</span><span class="sxs-lookup"><span data-stu-id="21892-184">Type in `regasm.exe /tlb:CalcProxy.tlb client.dll` to register the types with COM.</span></span> <span data-ttu-id="21892-185">预期会出现“Type library exporter warning”（类型库导出程序警告），但由于不需要泛型类型，因此这不是问题。</span><span class="sxs-lookup"><span data-stu-id="21892-185">A "Type library exporter warning" is expected but is not an issue because the generic type is not required.</span></span>  
  
6. <span data-ttu-id="21892-186">键入以 `gacutil.exe /i client.dll` 将程序集添加到全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="21892-186">Type in `gacutil.exe /i client.dll` to add the assembly to the Global Assembly Cache.</span></span>  
  
#### <a name="to-run-the-sample-on-the-same-computer"></a><span data-ttu-id="21892-187">在同一计算机上运行示例</span><span class="sxs-lookup"><span data-stu-id="21892-187">To run the sample on the same computer</span></span>  
  
1. <span data-ttu-id="21892-188">通过键入以下地址来测试是否可以使用浏览器访问服务： `http://localhost/servicemodelsamples/service.svc` 。</span><span class="sxs-lookup"><span data-stu-id="21892-188">Test that you can access the service using a browser by typing in the following address: `http://localhost/servicemodelsamples/service.svc`.</span></span> <span data-ttu-id="21892-189">在响应中应显示确认页。</span><span class="sxs-lookup"><span data-stu-id="21892-189">A confirmation page should be displayed in response.</span></span>  
  
2. <span data-ttu-id="21892-190">运行 \client（在语言特定文件夹内）中的 ComCalcClient.vbs。</span><span class="sxs-lookup"><span data-stu-id="21892-190">Run ComCalcClient.vbs from \client, from under the language-specific folder.</span></span> <span data-ttu-id="21892-191">客户端活动将显示在消息框窗口中。</span><span class="sxs-lookup"><span data-stu-id="21892-191">Client activity is displayed in message box windows.</span></span>  
  
3. <span data-ttu-id="21892-192">如果客户端和服务无法进行通信，请参阅 [WCF 示例的故障排除提示](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="21892-192">If the client and service are not able to communicate, see [Troubleshooting Tips for WCF Samples](/previous-versions/dotnet/netframework-3.5/ms751511(v=vs.90)).</span></span>  
  
#### <a name="to-run-the-sample-across-computers"></a><span data-ttu-id="21892-193">跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="21892-193">To run the sample across computers</span></span>  
  
1. <span data-ttu-id="21892-194">在服务计算机上创建一个名为 ServiceModelSamples 的虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="21892-194">On the service computer, create a virtual directory named ServiceModelSamples.</span></span> <span data-ttu-id="21892-195">可以使用示例中附带的 Setupvroot.bat 脚本来创建磁盘目录和虚拟目录。</span><span class="sxs-lookup"><span data-stu-id="21892-195">The Setupvroot.bat script included with the sample can be used to create the disk directory and virtual directory.</span></span>  
  
2. <span data-ttu-id="21892-196">从 %SystemDrive%\Inetpub\wwwroot\servicemodelsamples 中将服务程序文件复制到服务计算机上的 ServiceModelSamples 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21892-196">Copy the service program files from %SystemDrive%\Inetpub\wwwroot\servicemodelsamples to the ServiceModelSamples virtual directory on the service computer.</span></span> <span data-ttu-id="21892-197">确保在 \bin 目录中包括这些文件。</span><span class="sxs-lookup"><span data-stu-id="21892-197">Be sure to include the files in the \bin directory.</span></span>  
  
3. <span data-ttu-id="21892-198">将 \client 文件夹（在语言特定文件夹内）中的客户端脚本文件复制到客户端计算机上。</span><span class="sxs-lookup"><span data-stu-id="21892-198">Copy the client script file from the \client folder, under the language-specific folder, to the client computer.</span></span>  
  
4. <span data-ttu-id="21892-199">在该脚本文件中，更改终结点定义的地址值以与服务的新地址相匹配。</span><span class="sxs-lookup"><span data-stu-id="21892-199">In the script file, change the address value of the endpoint definition to match the new address of your service.</span></span> <span data-ttu-id="21892-200">在地址中将任何对“localhost”的引用替换为一个完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="21892-200">Replace any references to "localhost" with a fully-qualified domain name in the address.</span></span>  
  
5. <span data-ttu-id="21892-201">将 WSDL 文件复制到客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="21892-201">Copy the WSDL file to the client computer.</span></span> <span data-ttu-id="21892-202">在 WSDL 文件 serviceWsdl.xml 中，将地址中任何对“localhost”的引用替换为一个完全限定的域名。</span><span class="sxs-lookup"><span data-stu-id="21892-202">In the WSDL file, serviceWsdl.xml, replace any references to "localhost" with a fully-qualified domain name in the address.</span></span>  
  
6. <span data-ttu-id="21892-203">将 \client\bin\ 文件夹（在语言特定文件夹内）中的 Client.dll 库复制到客户端计算机上的一个目录中。</span><span class="sxs-lookup"><span data-stu-id="21892-203">Copy the Client.dll library from the \client\bin folder, under the language-specific folder, to a directory on the client computer.</span></span>  
  
7. <span data-ttu-id="21892-204">在命令提示符下，定位到客户端计算机上的目标目录。</span><span class="sxs-lookup"><span data-stu-id="21892-204">From a command prompt, navigate to that destination directory on the client computer.</span></span> <span data-ttu-id="21892-205">如果使用的是 Windows Vista 或 Windows Server 2008，请确保以管理员身份运行命令提示符。</span><span class="sxs-lookup"><span data-stu-id="21892-205">If using Windows Vista or Windows Server 2008, make sure to run the command prompt as Administrator.</span></span>  
  
8. <span data-ttu-id="21892-206">键入以 `tlbexp.exe client.dll /out:CalcProxy.tlb` 将 dll 导出到 tlb 文件中。</span><span class="sxs-lookup"><span data-stu-id="21892-206">Type in `tlbexp.exe client.dll /out:CalcProxy.tlb` to export the dll to a tlb file.</span></span> <span data-ttu-id="21892-207">预期会出现“Type library exporter warning”（类型库导出程序警告），但由于不需要泛型类型，因此这不是问题。</span><span class="sxs-lookup"><span data-stu-id="21892-207">A "Type library exporter warning" is expected but is not an issue because the generic type is not required.</span></span>  
  
9. <span data-ttu-id="21892-208">键入 `regasm.exe /tlb:CalcProxy.tlb client.dll` 以向 COM 注册类型。</span><span class="sxs-lookup"><span data-stu-id="21892-208">Type in `regasm.exe /tlb:CalcProxy.tlb client.dll` to register the types with COM.</span></span> <span data-ttu-id="21892-209">在运行命令之前，请确保已将路径设置为包含的文件夹 `regasm.exe` 。</span><span class="sxs-lookup"><span data-stu-id="21892-209">Ensure that path has been set to the folder that contains `regasm.exe` before you run the command.</span></span>  
  
10. <span data-ttu-id="21892-210">键入以 `gacutil.exe /i client.dll` 将程序集添加到全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="21892-210">Type in `gacutil.exe /i client.dll` to add the assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="21892-211">在运行命令之前，请确保已将路径设置为包含的文件夹 `gacutil.exe` 。</span><span class="sxs-lookup"><span data-stu-id="21892-211">Ensure that path has been set to the folder that contains `gacutil.exe` before you run the command.</span></span>  
  
11. <span data-ttu-id="21892-212">测试是否可使用浏览器从客户端计算机访问服务。</span><span class="sxs-lookup"><span data-stu-id="21892-212">Test that you can access the service from the client computer using a browser.</span></span>  
  
12. <span data-ttu-id="21892-213">在客户端计算机上，启动 ComCalcClient.vbs。</span><span class="sxs-lookup"><span data-stu-id="21892-213">On the client computer, launch ComCalcClient.vbs.</span></span>  
  
#### <a name="to-clean-up-after-the-sample"></a><span data-ttu-id="21892-214">运行示例后进行清理</span><span class="sxs-lookup"><span data-stu-id="21892-214">To clean up after the sample</span></span>  
  
- <span data-ttu-id="21892-215">出于安全目的，请在示例结束后删除虚拟目录定义和在安装步骤中授予的权限。</span><span class="sxs-lookup"><span data-stu-id="21892-215">For security purposes, remove the virtual directory definition and permissions granted in the setup steps when you are finished with the samples.</span></span>
