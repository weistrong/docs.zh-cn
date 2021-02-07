---
description: 了解详细信息： Customchannelstester.exe
title: CustomChannelsTester
ms.date: 03/30/2017
ms.assetid: ee1fa307-98b1-4647-8860-2e9217ba6082
ms.openlocfilehash: f1b84d8de0a93edf685d63b2bfd3c51f8b3e0420
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755910"
---
# <a name="customchannelstester"></a><span data-ttu-id="d110e-103">CustomChannelsTester</span><span class="sxs-lookup"><span data-stu-id="d110e-103">CustomChannelsTester</span></span>

<span data-ttu-id="d110e-104">`CustomChannelsTester` 是一个可用于依据一组预定义的服务协定测试自定义通道实现的工具。</span><span class="sxs-lookup"><span data-stu-id="d110e-104">The `CustomChannelsTester` is a tool that you can use to test your custom channel implementations against a set of predefined service contracts.</span></span> <span data-ttu-id="d110e-105">可以通过使用 XML 文件选择这组服务协定并将其传递给该工具。</span><span class="sxs-lookup"><span data-stu-id="d110e-105">You can select the set of service contracts and pass it to the tool using an XML file.</span></span> <span data-ttu-id="d110e-106">然后，该工具将生成服务和客户端，该客户端会在消息交换过程中测试您的自定义通道实现。</span><span class="sxs-lookup"><span data-stu-id="d110e-106">The tool then generates the service and client that exercises your custom channel implementations during message exchange.</span></span>  
  
### <a name="to-build-the-tool"></a><span data-ttu-id="d110e-107">生成工具</span><span class="sxs-lookup"><span data-stu-id="d110e-107">To build the tool</span></span>  
  
1. <span data-ttu-id="d110e-108">若要生成解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="d110e-108">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
2. <span data-ttu-id="d110e-109">生成该解决方案将会生成三个文件：CustomChannelsTester.exe、TestSpec.xml 和 SampleRun.cmd。</span><span class="sxs-lookup"><span data-stu-id="d110e-109">Building the solution generates three files: CustomChannelsTester.exe, TestSpec.xml and SampleRun.cmd.</span></span> <span data-ttu-id="d110e-110">文件 Samplerun.cmd 提供了一个示例命令行，说明如何使用此工具来测试 [传输： UDP](transport-udp.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="d110e-110">The file SampleRun.cmd has a sample command line that shows how to use this tool to test the [Transport: UDP](transport-udp.md) sample.</span></span>  
  
### <a name="to-run-the-tool"></a><span data-ttu-id="d110e-111">运行此工具</span><span class="sxs-lookup"><span data-stu-id="d110e-111">To run the tool</span></span>  
  
- <span data-ttu-id="d110e-112">在命令提示符处，键入下列命令：</span><span class="sxs-lookup"><span data-stu-id="d110e-112">At the command prompt type the following command:</span></span>  
  
    ```console  
    CustomChannelsTester.exe /binding:YourCustomBindngName /dll:TheAssemblyWhereThisTypeisDefined /testspec:XmlFileNameWhichContainsTestOptions  
    ```  
  
     <span data-ttu-id="d110e-113">需要使用 `/binding` 选项。</span><span class="sxs-lookup"><span data-stu-id="d110e-113">Using the `/binding` option is required.</span></span>  
  
     <span data-ttu-id="d110e-114">`/dll` 如果 "绑定" 不是由 Windows Communication Foundation (WCF) 提供的系统提供的绑定，则此项是必需的。</span><span class="sxs-lookup"><span data-stu-id="d110e-114">`/dll` is required if "binding" is not a system-provided binding provided by Windows Communication Foundation (WCF).</span></span>  
  
     <span data-ttu-id="d110e-115">`/testspec` 是可选项。</span><span class="sxs-lookup"><span data-stu-id="d110e-115">`/testspec` is optional.</span></span>  
  
     <span data-ttu-id="d110e-116">这将根据测试规范和绑定创建服务器和客户端。</span><span class="sxs-lookup"><span data-stu-id="d110e-116">This creates server and clients based on the test specifications and the binding.</span></span>  
  
     <span data-ttu-id="d110e-117">执行该客户端和服务器并返回结果。</span><span class="sxs-lookup"><span data-stu-id="d110e-117">Executes the client and server and returns the results.</span></span>  
  
     <span data-ttu-id="d110e-118">下面是用于描述测试规范的示例 XML (testspec.xml)：</span><span class="sxs-lookup"><span data-stu-id="d110e-118">The following is the sample XML for the description of the test specifications (testspec.xml):</span></span>  
  
    ```xml  
    <TestSpec xmlns="http://WCF/TestSpec" xmlns:msdata="urn:schemas-microsoft-com:xml-msdata"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" >  
    <ServiceContract>  
    <!-- Test a contract which has oneway / twoway operations. If you set ExpandAll = true, both types of contracts are tested -->    <IsOneWay ExpandAll="true">true</IsOneWay>  
    <!-- Test a contract with Asynchronous / Synchronous Operations-->  
        <IsAsync>false</IsAsync>
    <!-- Test a sessionful / sessionless contract-->
        <IsSession ExpandAll="true">true</IsSession>  
    <!-- If the Service Contract includes a CallBack Contract-->
        <IsCallBack ExpandAll="true">true</IsCallBack>  
    </ServiceContract>  
    <TestDetails>  
    <!-- Name of the machine that runs the server - required if you want to run the test crossmachine-->  
        <ServerName>ReplaceThisWithTheServerMachineName</ServerName>  
    <!-- Port Number - Optional-->  
        <Port>8000</Port>  
    <!--URI for the callBack address for the client. The client will receive the messages from the server on this address in case of a CallBack Contract-->  
        <ClientCallBackAddress/>
    <!-- Duration (in sec) after the server has started, it times out - optional(default = 300sec) -->  
        <ServerTimeout>300</ServerTimeout>  
    <!-- Duration (in sec) before the Client initializes -optional(default = 60sec) -->  
        <ClientTimeout>60</ClientTimeout>  
    <!-- Number of clients for each service - optional(default = 1) -->  
        <NumberOfClients>1</NumberOfClients>  
    <!-- Number of messages each client sends to the service - optional(default = 1) -->  
        <MessagesPerClient>1</MessagesPerClient>  
    </TestDetails>  
    </TestSpec>  
    ```  
