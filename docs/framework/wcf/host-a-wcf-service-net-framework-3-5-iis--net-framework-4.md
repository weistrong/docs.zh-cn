---
description: 了解详细信息：如何：托管使用在 .NET Framework 4 下运行的 IIS 中的 .NET Framework 3.5 编写的 WCF 服务
title: 如何：在 .NET Framework 4 环境下运行的 IIS 中承载使用 .NET Framework 3.5 编写的 WCF 服务
ms.date: 03/30/2017
ms.assetid: 9aabc785-068d-4d32-8841-3ef39308d8d6
ms.openlocfilehash: 3ea46b589df293b39369521a133cf9facad97d93
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755962"
---
# <a name="how-to-host-a-wcf-service-written-with-net-framework-35-in-iis-running-under-net-framework-4"></a><span data-ttu-id="208a7-103">如何：在 .NET Framework 4 环境下运行的 IIS 中承载使用 .NET Framework 3.5 编写的 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="208a7-103">How to: Host a WCF Service Written with .NET Framework 3.5 in IIS Running Under .NET Framework 4</span></span>

<span data-ttu-id="208a7-104">在运行 .NET Framework 4 的计算机上承载使用 .NET Framework 3.5 编写的 Windows Communication Foundation (WCF) 服务时，您可能会收到 <xref:System.ServiceModel.ProtocolException> 以下文本。</span><span class="sxs-lookup"><span data-stu-id="208a7-104">When hosting a Windows Communication Foundation (WCF) service written with .NET Framework 3.5 on a machine running .NET Framework 4, you may get a <xref:System.ServiceModel.ProtocolException> with the following text.</span></span>
  
```output  
Unhandled Exception: System.ServiceModel.ProtocolException: The content type text/html; charset=utf-8 of the response message does not match the content type of the binding (application/soap+xml; charset=utf-8). If using a custom encoder, be sure that the IsContentTypeSupported method is implemented properly. The first 1024 bytes of the response were: '<html>    <head>        <title>The application domain or application pool is currently running version 4.0 or later of the .NET Framework. This can occur if IIS settings have been set to 4.0 or later for this Web application, or if you are using version 4.0 or later of the ASP.NET Web Development Server. The <compilation> element in the Web.config file for this Web application does not contain the required 'targetFrameworkMoniker' attribute for this version of the .NET Framework (for example, '<compilation targetFrameworkMoniker=".NETFramework,Version=v4.0">'). Update the Web.config file with this attribute, or configure the Web application to use a different version of the .NET Framework.</title>...  
```  
  
 <span data-ttu-id="208a7-105">或者，如果尝试浏览服务的 .svc 文件，您可能会看到包含以下文本的错误页面。</span><span class="sxs-lookup"><span data-stu-id="208a7-105">Or if you try to browse to the service's .svc file you may see an error page with the following text.</span></span>  
  
```output  
The application domain or application pool is currently running version 4.0 or later of the .NET Framework. This can occur if IIS settings have been set to 4.0 or later for this Web application, or if you are using version 4.0 or later of the ASP.NET Web Development Server. The <compilation> element in the Web.config file for this Web application does not contain the required 'targetFrameworkMoniker' attribute for this version of the .NET Framework (for example, '<compilation targetFrameworkMoniker=".NETFramework,Version=v4.0">'). Update the Web.config file with this attribute, or configure the Web application to use a different version of the .NET Framework.  
```  
  
 <span data-ttu-id="208a7-106">之所以发生这些错误是因为在中运行的应用程序域 IIS 运行 .NET Framework 4，并且 WCF 服务应在 .NET Framework 3.5 下运行。</span><span class="sxs-lookup"><span data-stu-id="208a7-106">These errors occur because the application domain IIS is running within is running .NET Framework 4 and the WCF service is expecting to run under .NET Framework 3.5.</span></span> <span data-ttu-id="208a7-107">本主题说明运行服务所需进行的修改。</span><span class="sxs-lookup"><span data-stu-id="208a7-107">This topic explains the modifications required to get the service to run.</span></span>
  
 <span data-ttu-id="208a7-108">接下来，查找 <`compilers`> 元素，并将 CompilerVersion 提供程序选项更改为具有4.0 的值。</span><span class="sxs-lookup"><span data-stu-id="208a7-108">Next find the <`compilers`> element and change the CompilerVersion provider option to have a value of 4.0.</span></span> <span data-ttu-id="208a7-109">默认情况 `compiler` 下，<> 元素下有两个 <> 元素 `compilers` 。</span><span class="sxs-lookup"><span data-stu-id="208a7-109">By default, there are two <`compiler`> elements under the <`compilers`> element.</span></span> <span data-ttu-id="208a7-110">您必须同时更新这两个元素的 CompilerVersion 提供程序选项，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="208a7-110">You must update the CompilerVersion provider option for both as shown in the following example.</span></span>  
  
```xml  
<system.codedom>  
      <compilers>  
        <compiler language="c#;cs;csharp" extension=".cs" warningLevel="4"  
                  type="Microsoft.CSharp.CSharpCodeProvider, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
          <providerOption name="CompilerVersion" value="v3.5"/>  
          <providerOption name="WarnAsError" value="false"/>  
        </compiler>  
        <compiler language="vb;vbs;visualbasic;vbscript" extension=".vb" warningLevel="4"  
                  type="Microsoft.VisualBasic.VBCodeProvider, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
          <providerOption name="CompilerVersion" value="v3.5"/>  
          <providerOption name="OptionInfer" value="true"/>  
          <providerOption name="WarnAsError" value="false"/>  
        </compiler>  
      </compilers>  
    </system.codedom>  
```  
  
### <a name="add-the-required-targetframework-attribute"></a><span data-ttu-id="208a7-111">添加所需的 targetFramework 特性</span><span class="sxs-lookup"><span data-stu-id="208a7-111">Add the required targetFramework attribute</span></span>  
  
1. <span data-ttu-id="208a7-112">打开服务的 Web.config 文件，查找 <`compilation`> 元素。</span><span class="sxs-lookup"><span data-stu-id="208a7-112">Open the service's Web.config file and look for the <`compilation`> element.</span></span>  
  
2. <span data-ttu-id="208a7-113">将 `targetFramework` 特性添加到 <`compilation`> 元素，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="208a7-113">Add the `targetFramework` attribute to the <`compilation`> element as shown in the following example.</span></span>  
  
    ```xml  
    <compilation debug="false"  
            targetFramework="4.0">  
  
            <assemblies>  
              <add assembly="System.Core, Version=3.5.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
              <add assembly="System.Xml.Linq, Version=3.5.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
              <add assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31BF3856AD364E35"/>  
              <add assembly="System.Data.DataSetExtensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089"/>  
            </assemblies>  
  
          </compilation>  
    ```  
  
3. <span data-ttu-id="208a7-114">查找 <`compilers`> 元素，并更改 CompilerVersion 提供程序选项的值为4.0。</span><span class="sxs-lookup"><span data-stu-id="208a7-114">Find the <`compilers`> element and change the CompilerVersion provider option to have a value of 4.0.</span></span> <span data-ttu-id="208a7-115">默认情况 `compiler` 下，<> 元素下有两个 <> 元素 `compilers` 。</span><span class="sxs-lookup"><span data-stu-id="208a7-115">By default, there are two <`compiler`> elements under the <`compilers`> element.</span></span> <span data-ttu-id="208a7-116">您必须同时更新这两个元素的 CompilerVersion 提供程序选项，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="208a7-116">You must update the CompilerVersion provider option for both as shown in the following example.</span></span>  
  
    ```xml  
    <system.codedom>  
          <compilers>  
            <compiler language="c#;cs;csharp" extension=".cs" warningLevel="4"  
                      type="Microsoft.CSharp.CSharpCodeProvider, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
              <providerOption name="CompilerVersion" value="v3.5"/>  
              <providerOption name="WarnAsError" value="false"/>  
            </compiler>  
            <compiler language="vb;vbs;visualbasic;vbscript" extension=".vb" warningLevel="4"  
                      type="Microsoft.VisualBasic.VBCodeProvider, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
              <providerOption name="CompilerVersion" value="v3.5"/>  
              <providerOption name="OptionInfer" value="true"/>  
              <providerOption name="WarnAsError" value="false"/>  
            </compiler>  
          </compilers>  
        </system.codedom>  
    ```
