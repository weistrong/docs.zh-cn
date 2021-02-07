---
description: 了解详细信息： ControlBuilderInterceptor 类
title: ControlBuilderInterceptor 类
ms.date: 08/11/2020
api_name:
- System.Web.Compilation.ControlBuilderInterceptor
api_location:
- System.Web.dll
api_type:
- Assembly
topic_type:
- apiref
ms.openlocfilehash: ac32709bf814d17ac2a02222d4d92edc6cc93337
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664816"
---
# <a name="controlbuilderinterceptor-class"></a><span data-ttu-id="92804-103">ControlBuilderInterceptor 类</span><span class="sxs-lookup"><span data-stu-id="92804-103">ControlBuilderInterceptor class</span></span>

<span data-ttu-id="92804-104">`ControlBuilderInterceptor`类允许自定义或控制编译过程。</span><span class="sxs-lookup"><span data-stu-id="92804-104">The `ControlBuilderInterceptor` class allows the compilation process to be customized or controlled.</span></span>

## <a name="syntax"></a><span data-ttu-id="92804-105">语法</span><span class="sxs-lookup"><span data-stu-id="92804-105">Syntax</span></span>

```csharp
internal class ControlBuilderInterceptor
```

> [!WARNING]
> <span data-ttu-id="92804-106">`ControlBuilderInterceptor`类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="92804-106">The `ControlBuilderInterceptor` class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="92804-107">如 "备注" 部分所述，可以检查是否存在此类型，以确定是否存在侦听器类型支持。</span><span class="sxs-lookup"><span data-stu-id="92804-107">As described in the Remarks section, the existence of this type can be checked to determine whether interceptor type support is present.</span></span> <span data-ttu-id="92804-108">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="92804-108">Microsoft does not support any other use of this class in a production application under any circumstance.</span></span>

## <a name="remarks"></a><span data-ttu-id="92804-109">备注</span><span class="sxs-lookup"><span data-stu-id="92804-109">Remarks</span></span>

<span data-ttu-id="92804-110">在 .NET Framework 2.0 和 .NET Framework 3.5 中， [8 月 2020](https://portal.msrc.microsoft.com/security-guidance/releasenotedetail/2020-Aug) 更新添加了对使用侦听器类型自定义或控制编译过程的支持。</span><span class="sxs-lookup"><span data-stu-id="92804-110">In .NET Framework 2.0 and .NET Framework 3.5, the [August 2020](https://portal.msrc.microsoft.com/security-guidance/releasenotedetail/2020-Aug) updates added support for using an interceptor type to customize or control the compilation process.</span></span> <span data-ttu-id="92804-111">您可以使用检查是否存在该类型来确定是否存在此支持 <xref:System.Type.GetType?displayProperty=nameWithType> `ControlBuilderInterceptor` ，如以下代码所示。</span><span class="sxs-lookup"><span data-stu-id="92804-111">You can determine whether this support is present by using <xref:System.Type.GetType?displayProperty=nameWithType> to check the existence of the `ControlBuilderInterceptor` type, as demonstrated in the following code.</span></span>

```csharp
Type type = Type.GetType("System.Web.Compilation.ControlBuilderInterceptor, System.Web, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a");
```

<span data-ttu-id="92804-112">如果返回值不为 null，则表示侦听器支持。</span><span class="sxs-lookup"><span data-stu-id="92804-112">If the return value is non-null, then interceptor support is present.</span></span> <span data-ttu-id="92804-113">如果返回值为 `null` ，或者引发了异常，则不会安装8月2020的更新，并且不存在侦听器支持。</span><span class="sxs-lookup"><span data-stu-id="92804-113">If the return value is `null`, or if an exception is thrown, then the August 2020 updates have not been installed, and interceptor support is absent.</span></span>

<span data-ttu-id="92804-114">如果提供程序支持，则可以编写并注册与编译过程交互的侦听器类型，就像在 <xref:System.Web.Compilation.ControlBuilderInterceptor> 更高版本的 .NET Framework 上执行的操作一样。</span><span class="sxs-lookup"><span data-stu-id="92804-114">If interceptor support is present, you can write and register an interceptor type that will interact with the compilation process in exactly the same way that <xref:System.Web.Compilation.ControlBuilderInterceptor> does on later versions of .NET Framework.</span></span> <span data-ttu-id="92804-115">在 .NET Framework 2.0 和 .NET Framework 3.5 中，侦听器类型可以是满足以下要求的任何类：</span><span class="sxs-lookup"><span data-stu-id="92804-115">In .NET Framework 2.0 and .NET Framework 3.5, the interceptor type can be any class that meets the following requirements:</span></span>

* <span data-ttu-id="92804-116">具有一个公共的无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="92804-116">Has a public, parameterless constructor.</span></span>
* <span data-ttu-id="92804-117">具有与 `PreControlBuilderInit` `OnProcessGeneratedCode` 和方法相同的、具有与和方法相同的签名和语义的公共非静态方法 <xref:System.Web.Compilation.ControlBuilderInterceptor.PreControlBuilderInit(System.Web.UI.ControlBuilder,System.Web.UI.TemplateParser,System.Web.UI.ControlBuilder,System.Type,System.String,System.String,System.Collections.IDictionary,System.Collections.IDictionary)> <xref:System.Web.Compilation.ControlBuilderInterceptor.OnProcessGeneratedCode(System.Web.UI.ControlBuilder,System.CodeDom.CodeCompileUnit,System.CodeDom.CodeTypeDeclaration,System.CodeDom.CodeTypeDeclaration,System.CodeDom.CodeMemberMethod,System.CodeDom.CodeMemberMethod,System.Collections.IDictionary)> ，这些方法存在于 .NET Framework 的更高版本中。</span><span class="sxs-lookup"><span data-stu-id="92804-117">Has public, non-static methods named `PreControlBuilderInit` and `OnProcessGeneratedCode` that have the same signature and semantics as the <xref:System.Web.Compilation.ControlBuilderInterceptor.PreControlBuilderInit(System.Web.UI.ControlBuilder,System.Web.UI.TemplateParser,System.Web.UI.ControlBuilder,System.Type,System.String,System.String,System.Collections.IDictionary,System.Collections.IDictionary)> and <xref:System.Web.Compilation.ControlBuilderInterceptor.OnProcessGeneratedCode(System.Web.UI.ControlBuilder,System.CodeDom.CodeCompileUnit,System.CodeDom.CodeTypeDeclaration,System.CodeDom.CodeTypeDeclaration,System.CodeDom.CodeMemberMethod,System.CodeDom.CodeMemberMethod,System.Collections.IDictionary)> methods, which exist in later versions of .NET Framework.</span></span>

<span data-ttu-id="92804-118">使用 `aspnet:20ControlBuilderInterceptor` ASP.NET 应用程序设置 () 中的密钥注册侦听器类型 `<appSettings>` 。</span><span class="sxs-lookup"><span data-stu-id="92804-118">Register the interceptor type by using the `aspnet:20ControlBuilderInterceptor` key in ASP.NET application settings (`<appSettings>`).</span></span> <span data-ttu-id="92804-119">此应用程序设置必须在您的计算机或应用程序 *web.config* 文件中列出。</span><span class="sxs-lookup"><span data-stu-id="92804-119">This application setting must be listed in your computer or application *web.config* file.</span></span> <span data-ttu-id="92804-120">使用程序集限定的类型名称指定侦听器类型。</span><span class="sxs-lookup"><span data-stu-id="92804-120">Specify the interceptor type by using its assembly-qualified type name.</span></span> <span data-ttu-id="92804-121">下面的示例演示如何注册名为的侦听器类型 `Fabrikam.Interceptor` 。</span><span class="sxs-lookup"><span data-stu-id="92804-121">The following example shows how to register an interceptor type named `Fabrikam.Interceptor`.</span></span>

```xml
<configuration>
  ...
  <appSettings>
    ...
    <add key="aspnet:20ControlBuilderInterceptor"
         value="Fabrikam.Interceptor, Fabrikam, Version=1.0.0.0, Culture=neutral, PublicKeyToken=2b3831f2f2b744f7" />
  </appSettings>
</configuration>
```

<span data-ttu-id="92804-122">若要检索某个类型的程序集限定名称，请使用 <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType> 属性，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="92804-122">To retrieve the assembly-qualified name of a type, use the <xref:System.Type.AssemblyQualifiedName?displayProperty=nameWithType> property, as demonstrated in the following code.</span></span>

```csharp
string assemblyQualifiedName = typeof(Fabrikam.Interceptor).AssemblyQualifiedName;
```

<span data-ttu-id="92804-123">当存在侦听器支持时，编译过程将按照上述方式与列出的类型进行交互。</span><span class="sxs-lookup"><span data-stu-id="92804-123">When interceptor support is present, the compilation process interacts with the listed type in the manner described above.</span></span> <span data-ttu-id="92804-124">当不存在侦听器支持时，应用程序设置将被忽略且不起作用。</span><span class="sxs-lookup"><span data-stu-id="92804-124">When interceptor support is absent, the application setting is ignored and has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="92804-125">要求</span><span class="sxs-lookup"><span data-stu-id="92804-125">Requirements</span></span>

<span data-ttu-id="92804-126">**命名空间：** System.web. 编译</span><span class="sxs-lookup"><span data-stu-id="92804-126">**Namespace:** System.Web.Compilation</span></span>

<span data-ttu-id="92804-127">**程序集：** System.Web.dll 中的 () </span><span class="sxs-lookup"><span data-stu-id="92804-127">**Assembly:** System.Web (in System.Web.dll)</span></span>

<span data-ttu-id="92804-128">**.NET Framework 版本：** 3.5、2。0</span><span class="sxs-lookup"><span data-stu-id="92804-128">**.NET Framework versions:** 3.5, 2.0</span></span>
