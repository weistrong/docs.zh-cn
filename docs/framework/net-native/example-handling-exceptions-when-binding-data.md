---
description: 了解详细信息：示例：绑定数据时处理异常
title: 示例：处理绑定数据时出现的异常
ms.date: 03/30/2017
ms.assetid: bd63ed96-9853-46dc-ade5-7bd1b0f39110
ms.openlocfilehash: 434520e42afa3e1ab7c453c3ddf41863ceb62eb6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747889"
---
# <a name="example-handling-exceptions-when-binding-data"></a><span data-ttu-id="54e6b-103">示例：处理绑定数据时出现的异常</span><span class="sxs-lookup"><span data-stu-id="54e6b-103">Example: Handling Exceptions When Binding Data</span></span>

> [!NOTE]
> <span data-ttu-id="54e6b-104">该主题是指 .NET Native 开发者预览版这款预发布软件。</span><span class="sxs-lookup"><span data-stu-id="54e6b-104">This topic refers to the .NET Native Developer Preview, which is pre-release software.</span></span> <span data-ttu-id="54e6b-105">可从 [Microsoft Connect 网站](https://go.microsoft.com/fwlink/?LinkId=394611)（需要注册）下载该预览版。</span><span class="sxs-lookup"><span data-stu-id="54e6b-105">You can download the preview from the [Microsoft Connect website](https://go.microsoft.com/fwlink/?LinkId=394611) (requires registration).</span></span>  
  
 <span data-ttu-id="54e6b-106">下面的示例演示如何解决在使用 .NET Native 工具链编译的应用尝试绑定数据时引发的 [MissingMetadataException](missingmetadataexception-class-net-native.md) 异常。</span><span class="sxs-lookup"><span data-stu-id="54e6b-106">The following example shows how to resolve a [MissingMetadataException](missingmetadataexception-class-net-native.md) exception that is thrown when an app compiled with the .NET Native tool chain tries to bind data.</span></span> <span data-ttu-id="54e6b-107">以下是有关异常的信息：</span><span class="sxs-lookup"><span data-stu-id="54e6b-107">Here’s the exception information:</span></span>  
  
```output
This operation cannot be carried out as metadata for the following type was removed for performance reasons:
App.ViewModels.MainPageVM  
```  
  
 <span data-ttu-id="54e6b-108">以下是相关的调用堆栈：</span><span class="sxs-lookup"><span data-stu-id="54e6b-108">Here's the associated call stack:</span></span>  
  
```output
Reflection::Execution::ReflectionDomainSetupImplementation.CreateNonInvokabilityException+0x238  
Reflection::Core::ReflectionDomain.CreateNonInvokabilityException+0x2e  
Reflection::Core::Execution::ExecutionEnvironment.+0x316  
System::Reflection::Runtime::PropertyInfos::RuntimePropertyInfo.GetValue+0x1cb  
System::Reflection::PropertyInfo.GetValue+0x22  
System::Runtime::InteropServices::WindowsRuntime::CustomPropertyImpl.GetValue+0x42  
App!$66_Interop::McgNative.Func_IInspectable_IInspectable+0x158  
App!$66_Interop::McgNative::__vtable_Windows_UI_Xaml_Data__ICustomProperty.GetValue__STUB+0x46  
Windows_UI_Xaml!DirectUI::PropertyProviderPropertyAccess::GetValue+0x3f
Windows_UI_Xaml!DirectUI::PropertyAccessPathStep::GetValue+0x31
Windows_UI_Xaml!DirectUI::PropertyPathListener::ConnectPathStep+0x113  
```  
  
## <a name="what-was-the-app-doing"></a><span data-ttu-id="54e6b-109">该应用在执行什么操作？</span><span class="sxs-lookup"><span data-stu-id="54e6b-109">What was the app doing?</span></span>  

 <span data-ttu-id="54e6b-110">在堆栈的基础上，命名空间中的帧 <xref:Windows.UI.Xaml?displayProperty=nameWithType> 指示 XAML 呈现引擎正在运行。</span><span class="sxs-lookup"><span data-stu-id="54e6b-110">At the base of the stack, frames from the <xref:Windows.UI.Xaml?displayProperty=nameWithType> namespace indicate that the XAML rendering engine was running.</span></span>   <span data-ttu-id="54e6b-111">对 <xref:System.Reflection.PropertyInfo.GetValue%2A?displayProperty=nameWithType> 方法的显示了属性值的基于反射的查找，该值位于元数据遭到删除的类型上。</span><span class="sxs-lookup"><span data-stu-id="54e6b-111">The use of the <xref:System.Reflection.PropertyInfo.GetValue%2A?displayProperty=nameWithType> method indicates a reflection-based lookup of a property’s value on the type whose metadata was removed.</span></span>  
  
 <span data-ttu-id="54e6b-112">第一步是提供一个元数据指令，将其添加到该类型的 `serialize` 元数据，使其所有属性都可访问：</span><span class="sxs-lookup"><span data-stu-id="54e6b-112">The first step in providing a metadata directive would be to add `serialize` metadata for the type so that its properties are all accessible:</span></span>  
  
```xml  
<Type Name="App.ViewModels.MainPageVM" Serialize="Required Public" />  
```  
  
## <a name="is-this-an-isolated-case"></a><span data-ttu-id="54e6b-113">这是一个孤立情形吗？</span><span class="sxs-lookup"><span data-stu-id="54e6b-113">Is this an isolated case?</span></span>  

 <span data-ttu-id="54e6b-114">在此情况下，如果数据绑定拥有一个 `ViewModel` 的不完整元数据，它对于其他模型可能也是如此。</span><span class="sxs-lookup"><span data-stu-id="54e6b-114">In this scenario, if data binding has incomplete metadata for one `ViewModel`, it may for others, too.</span></span>  <span data-ttu-id="54e6b-115">如果代码的结构方式使得该应用的查看模型都位于 `App.ViewModels` 命名空间，你可以使用一个更一般的运行时指令：</span><span class="sxs-lookup"><span data-stu-id="54e6b-115">If the code is structured in a way that the app’s view models are all in the `App.ViewModels` namespace, you could use a more general runtime directive:</span></span>  
  
```xml  
<Namespace Name="App.ViewModels " Serialize="Required Public" />  
```  
  
## <a name="could-the-code-be-rewritten-to-not-use-reflection"></a><span data-ttu-id="54e6b-116">代码能够重新，改为不使用反射吗？</span><span class="sxs-lookup"><span data-stu-id="54e6b-116">Could the code be rewritten to not use reflection?</span></span>  

 <span data-ttu-id="54e6b-117">因为数据绑定是反射密集型的，更改代码以避免反射是不可行的。</span><span class="sxs-lookup"><span data-stu-id="54e6b-117">Because data binding is reflection-intensive, changing the code to avoid reflection isn’t feasible.</span></span>  
  
 <span data-ttu-id="54e6b-118">然而，有几种方法可以指定 `ViewModel` 到 XAML 页面，从而让工具链在汇编时间可以将属性绑定与正确的类型关联起来并保存元数据，而不必使用运行时指令。</span><span class="sxs-lookup"><span data-stu-id="54e6b-118">However, there are ways to specify the `ViewModel` to the XAML page so that the tool chain can associate property bindings with the correct type at compile time and keep the metadata without using a runtime directive.</span></span>  <span data-ttu-id="54e6b-119">例如，可以 <xref:Windows.UI.Xaml.Data.BindableAttribute?displayProperty=nameWithType> 在属性上应用特性。</span><span class="sxs-lookup"><span data-stu-id="54e6b-119">For example, you could apply the <xref:Windows.UI.Xaml.Data.BindableAttribute?displayProperty=nameWithType> attribute on properties.</span></span> <span data-ttu-id="54e6b-120">这会使得 XAML 编译器生成所需的查找信息并避免在 Default.rd.xml 文件中要求一个运行时指令。</span><span class="sxs-lookup"><span data-stu-id="54e6b-120">This causes the XAML compiler to generate the required lookup information and avoids requiring a runtime directive in the Default.rd.xml file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54e6b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="54e6b-121">See also</span></span>

- [<span data-ttu-id="54e6b-122">入门</span><span class="sxs-lookup"><span data-stu-id="54e6b-122">Getting Started</span></span>](getting-started-with-net-native.md)
- [<span data-ttu-id="54e6b-123">示例：动态编程疑难解答</span><span class="sxs-lookup"><span data-stu-id="54e6b-123">Example: Troubleshooting Dynamic Programming</span></span>](example-troubleshooting-dynamic-programming.md)
