---
description: 了解更多：消息安全窗口
title: Windows 消息安全
ms.date: 03/30/2017
helpviewer_keywords:
- WS Security
ms.assetid: d2221d1c-c9cb-48d1-b044-a3b4445c7f05
ms.openlocfilehash: 6b181e1bb835ea3129e99eb45baa6669bf8c09a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752270"
---
# <a name="message-security-windows"></a><span data-ttu-id="7449b-103">Windows 消息安全</span><span class="sxs-lookup"><span data-stu-id="7449b-103">Message Security Windows</span></span>

<span data-ttu-id="7449b-104">本示例演示如何将 <xref:System.ServiceModel.WSHttpBinding> 绑定配置为使用具有 Windows 身份验证的消息级安全性。</span><span class="sxs-lookup"><span data-stu-id="7449b-104">This sample demonstrates how to configure a <xref:System.ServiceModel.WSHttpBinding> binding to use message-level security with Windows authentication.</span></span> <span data-ttu-id="7449b-105">此示例基于 [入门](getting-started-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="7449b-105">This sample is based on the [Getting Started](getting-started-sample.md).</span></span> <span data-ttu-id="7449b-106">在此示例中，服务由 Internet 信息服务 (IIS) 承载，客户端是一个控制台应用程序 (.exe)。</span><span class="sxs-lookup"><span data-stu-id="7449b-106">In this sample, the service is hosted in Internet Information Services (IIS) and the client is a console application (.exe).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7449b-107">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="7449b-107">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="7449b-108">的默认安全性 [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md) 是使用 Windows 身份验证的消息安全。</span><span class="sxs-lookup"><span data-stu-id="7449b-108">The default security for the [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md) is message security using Windows authentication.</span></span> <span data-ttu-id="7449b-109">此示例中的配置文件将的属性显式设置为 `mode` [\<security>](../../configure-apps/file-schema/wcf/security-of-wshttpbinding.md) `Message` ，并将 `clientCredentialType` 特性设置为 `Windows` 。</span><span class="sxs-lookup"><span data-stu-id="7449b-109">The configuration files in this sample explicitly set the `mode` attribute of the [\<security>](../../configure-apps/file-schema/wcf/security-of-wshttpbinding.md) to `Message` and the `clientCredentialType` attribute to `Windows`.</span></span> <span data-ttu-id="7449b-110">这些值是此绑定的默认值，但为了演示其用法，已对这些值进行了显式配置，如下面的示例配置所示。</span><span class="sxs-lookup"><span data-stu-id="7449b-110">These values are the default values for this binding, but they have been explicitly configured, as shown in the following sample configuration to demonstrate their use.</span></span>  
  
```xml  
<bindings>  
    <wsHttpBinding>  
        <binding>  
            <security mode="Message">  
                <message clientCredentialType="Windows"/>  
            </security>  
        </binding>  
    </wsHttpBinding>  
</bindings>  
```  
  
 <span data-ttu-id="7449b-111">客户端终结点配置由服务终结点的绝对地址、绑定和协定组成。</span><span class="sxs-lookup"><span data-stu-id="7449b-111">The client endpoint configuration consists of an absolute address for the service endpoint, the binding, and the contract.</span></span> <span data-ttu-id="7449b-112">该客户端绑定是使用相应的 `securityMode` 和 `authenticationMode` 配置的。</span><span class="sxs-lookup"><span data-stu-id="7449b-112">The client binding is configured with the appropriate `securityMode` and `authenticationMode`.</span></span>  
  
```xml  
<system.serviceModel>  
  <client>  
    <endpoint address=  
            "http://localhost/servicemodelsamples/service.svc"
            binding="wsHttpBinding"
            bindingConfiguration="Binding1"
            contract="Microsoft.ServiceModel.Samples.ICalculator" />  
  </client>  
  
  <bindings>  
    <wsHttpBinding>  
      <!-- The default security for the WSHttpBinding is -->  
      <!-- Message security using Windows authentication. -->  
      <!-- This configuration explicitly defines the security mode -->  
      <!-- as Message and the clientCredentialType as Windows -->  
      <!-- for demonstration purposes. -->  
      <binding name="Binding1">  
        <security mode="Message">  
          <message clientCredentialType="Windows"/>  
        </security>  
      </binding>  
    </wsHttpBinding>  
  </bindings>  
</system.serviceModel>  
```  
  
 <span data-ttu-id="7449b-113">为了演示如何使用 <xref:System.ServiceModel.OperationContext.ServiceSecurityContext%2A> 来访问调用方的标识，服务源代码已进行了修改。</span><span class="sxs-lookup"><span data-stu-id="7449b-113">The service source code has been modified to demonstrate how the <xref:System.ServiceModel.OperationContext.ServiceSecurityContext%2A> can be used to access the identity of the caller.</span></span>  

```csharp
public string GetCallerIdentity()  
{  
    // The Windows identity of the caller can be accessed on the ServiceSecurityContext.WindowsIdentity.  
    return OperationContext.Current.ServiceSecurityContext.WindowsIdentity.Name;  
}  
```

 <span data-ttu-id="7449b-114">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="7449b-114">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="7449b-115">调用的第一个方法 `GetCallerIdentity` 将调用方标识的名称返回给客户端。</span><span class="sxs-lookup"><span data-stu-id="7449b-115">The first method called - `GetCallerIdentity` - returns the name of the caller identity back to the client.</span></span> <span data-ttu-id="7449b-116">在控制台窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="7449b-116">Press ENTER in the console window to shut down the client.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="7449b-117">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="7449b-117">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="7449b-118">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="7449b-118">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="7449b-119">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="7449b-119">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="7449b-120">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="7449b-120">To run the sample in a single- or cross-computer configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
