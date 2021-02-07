---
description: 了解详细信息：授权访问服务操作
title: 授予对服务操作的访问权限
ms.date: 03/30/2017
helpviewer_keywords:
- service behaviors, authorizing access sample
- Authorizing Access To Service Operations Sample [Windows Communication Foundation]
- authorization, Windows Communication Foundation sample
ms.assetid: ddcfdaa5-8b2e-4e13-bd85-887209dc6328
ms.openlocfilehash: 052adc6104b75884c90c266e2e0e7a045032c457
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732691"
---
# <a name="authorizing-access-to-service-operations"></a><span data-ttu-id="f137d-103">授予对服务操作的访问权限</span><span class="sxs-lookup"><span data-stu-id="f137d-103">Authorizing Access to Service Operations</span></span>

<span data-ttu-id="f137d-104">此示例演示如何使用 [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) 来允许使用 <xref:System.Security.Permissions.PrincipalPermissionAttribute> 属性来授予对服务操作的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f137d-104">This sample demonstrates how to use the [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) to enable use of the <xref:System.Security.Permissions.PrincipalPermissionAttribute> attribute to authorize access to service operations.</span></span> <span data-ttu-id="f137d-105">此示例基于 [入门](getting-started-sample.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="f137d-105">This sample is based on the [Getting Started](getting-started-sample.md) sample.</span></span> <span data-ttu-id="f137d-106">使用配置服务和客户端 [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="f137d-106">The service and client are configured using the [\<wsHttpBinding>](../../configure-apps/file-schema/wcf/wshttpbinding.md).</span></span> <span data-ttu-id="f137d-107">`mode`的特性已 [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) 设置为 `Message` ，并且已 `clientCredentialType` 设置为 `Windows` 。</span><span class="sxs-lookup"><span data-stu-id="f137d-107">The `mode` attribute of the [\<security>](../../configure-apps/file-schema/wcf/security-of-custombinding.md) has been set to `Message` and `clientCredentialType` has been set to `Windows`.</span></span> <span data-ttu-id="f137d-108"><xref:System.Security.Permissions.PrincipalPermissionAttribute> 应用到每个服务方法并用于限制对每个操作的访问。</span><span class="sxs-lookup"><span data-stu-id="f137d-108">The <xref:System.Security.Permissions.PrincipalPermissionAttribute> is applied to each service method and used to restrict access to each operation.</span></span> <span data-ttu-id="f137d-109">调用方必须是 Windows 管理员才能访问每项操作。</span><span class="sxs-lookup"><span data-stu-id="f137d-109">The caller must be a Windows administrator to access each operation.</span></span>  
  
 <span data-ttu-id="f137d-110">在此示例中，客户端是一个控制台应用程序 (.exe)，服务是由 Internet 信息服务 (IIS) 承载的。</span><span class="sxs-lookup"><span data-stu-id="f137d-110">In this sample, the client is a console application (.exe) and the service is hosted by Internet Information Services (IIS).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f137d-111">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="f137d-111">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="f137d-112">服务配置文件使用 [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) 来设置 `principalPermissionMode` 属性：</span><span class="sxs-lookup"><span data-stu-id="f137d-112">The service configuration file uses the [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) to set the `principalPermissionMode` attribute:</span></span>  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
    <behavior>
      <!-- The serviceAuthorization behavior sets the  
           principalPermissionMode to UseWindowsGroups.  
           This puts a WindowsPrincipal on the current thread when a   
           service is invoked. -->  
      <serviceAuthorization principalPermissionMode="UseWindowsGroups" />  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
 <span data-ttu-id="f137d-113">将 `principalPermissionMode` 设置为 `UseWindowsGroups` 可使用基于 Windows 组名的 <xref:System.Security.Permissions.PrincipalPermissionAttribute>。</span><span class="sxs-lookup"><span data-stu-id="f137d-113">Setting the `principalPermissionMode` to `UseWindowsGroups` enables the use of <xref:System.Security.Permissions.PrincipalPermissionAttribute> based on Windows group names.</span></span>  
  
 <span data-ttu-id="f137d-114">将 <xref:System.Security.Permissions.PrincipalPermissionAttribute> 应用于每个操作以要求调用方是 Windows 管理员组的成员，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="f137d-114">The <xref:System.Security.Permissions.PrincipalPermissionAttribute> is applied to each operation to require the caller to be part of the Windows administrators group, as shown in the following sample code.</span></span>  
  
```csharp
[PrincipalPermission(SecurityAction.Demand,
                             Role = "Builtin\\Administrators")]  
public double Add(double n1, double n2)  
{  
    double result = n1 + n2;  
    return result;  
}  
```  
  
 <span data-ttu-id="f137d-115">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="f137d-115">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="f137d-116">如果客户端在管理员组成员的账户下运行，客户端可与每个操作成功通信；否则访问被拒绝。</span><span class="sxs-lookup"><span data-stu-id="f137d-116">The client successfully communicates with each operation if it is running under an account that is part of the Administrators group; otherwise, access is denied.</span></span> <span data-ttu-id="f137d-117">若要体验授权失败，请在不是管理员组成员的账户下运行客户端。</span><span class="sxs-lookup"><span data-stu-id="f137d-117">To experiment with authorization failure, run the client under an account that is not part of the Administrators group.</span></span> <span data-ttu-id="f137d-118">在控制台窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="f137d-118">Press ENTER in the console window to shut down the client.</span></span>  
  
 <span data-ttu-id="f137d-119">通过实现 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 可以通知服务授权失败。</span><span class="sxs-lookup"><span data-stu-id="f137d-119">A service can be notified of authorization failures by implementing an <xref:System.ServiceModel.Dispatcher.IErrorHandler>.</span></span> <span data-ttu-id="f137d-120">有关实现的信息，请参阅 [扩展对错误处理和报告的控制](extending-control-over-error-handling-and-reporting.md) `IErrorHandler` 。</span><span class="sxs-lookup"><span data-stu-id="f137d-120">See [Extending Control Over Error Handling and Reporting](extending-control-over-error-handling-and-reporting.md) for information about implementing `IErrorHandler`.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="f137d-121">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="f137d-121">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="f137d-122">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="f137d-122">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="f137d-123">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="f137d-123">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="f137d-124">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="f137d-124">To run the sample in a single- or cross-computer configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
