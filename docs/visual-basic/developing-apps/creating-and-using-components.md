---
description: 详细了解：创建和使用组件 (Visual Basic)
title: 创建和使用组件
ms.date: 07/20/2015
helpviewer_keywords:
- components [Visual Basic]
ms.assetid: ee6a4156-73f7-4e9b-8e01-c74c4798b65c
ms.openlocfilehash: f59b4774556d95dcbc1befb16409d68a51c50535
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666584"
---
# <a name="creating-and-using-components-in-visual-basic"></a><span data-ttu-id="93f63-103">创建和使用组件 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="93f63-103">Creating and Using Components in Visual Basic</span></span>

<span data-ttu-id="93f63-104">组件  是一个类，该类实现 <xref:System.ComponentModel.IComponent?displayProperty=nameWithType> 接口或直接/间接派生自实现 <xref:System.ComponentModel.IComponent> 的类。</span><span class="sxs-lookup"><span data-stu-id="93f63-104">A *component* is a class that implements the <xref:System.ComponentModel.IComponent?displayProperty=nameWithType> interface or that derives directly or indirectly from a class that implements <xref:System.ComponentModel.IComponent>.</span></span> <span data-ttu-id="93f63-105">NET 组件是可重复使用的对象，可以和其他对象进行交互，并提供对外部资源和设计时支持的控制。</span><span class="sxs-lookup"><span data-stu-id="93f63-105">A .NET component is an object that is reusable, can interact with other objects, and provides control over external resources and design-time support.</span></span>  
  
 <span data-ttu-id="93f63-106">组件的一个重要特性在于它们是可设计的，这意味着可在 Visual Studio 集成开发环境中使用作为组件的类。</span><span class="sxs-lookup"><span data-stu-id="93f63-106">An important feature of components is that they are designable, which means that a class that is a component can be used in the Visual Studio Integrated Development Environment.</span></span> <span data-ttu-id="93f63-107">可以将组件添加到“工具箱”、拖放到窗体以及在设计图面上操作。</span><span class="sxs-lookup"><span data-stu-id="93f63-107">A component can be added to the Toolbox, dragged and dropped onto a form, and manipulated on a design surface.</span></span> <span data-ttu-id="93f63-108">对组件的基本设计时支持已内置于 .NET 中。</span><span class="sxs-lookup"><span data-stu-id="93f63-108">Base design-time support for components is built into .NET.</span></span> <span data-ttu-id="93f63-109">组件开发人员不必执行任何附加工作便可利用基本设计时功能。</span><span class="sxs-lookup"><span data-stu-id="93f63-109">A component developer does not have to do any additional work to take advantage of the base design-time functionality.</span></span>  
  
 <span data-ttu-id="93f63-110">控件与组件类似，二者都是可设计的。 </span><span class="sxs-lookup"><span data-stu-id="93f63-110">A *control* is similar to a component, as both are designable.</span></span> <span data-ttu-id="93f63-111">不过，控件提供用户界面，而组件不提供。</span><span class="sxs-lookup"><span data-stu-id="93f63-111">However, a control provides a user interface, while a component does not.</span></span> <span data-ttu-id="93f63-112">控件必须派生自基控件类之一：<xref:System.Windows.Forms.Control> 或 <xref:System.Web.UI.Control>。</span><span class="sxs-lookup"><span data-stu-id="93f63-112">A control must derive from one of the base control classes: <xref:System.Windows.Forms.Control> or <xref:System.Web.UI.Control>.</span></span>  
  
## <a name="when-to-create-a-component"></a><span data-ttu-id="93f63-113">创建组件的时间</span><span class="sxs-lookup"><span data-stu-id="93f63-113">When to Create a Component</span></span>  

 <span data-ttu-id="93f63-114">如果类将在设计图面（如 Windows 窗体设计器或 Web 窗体设计器）上使用，但没有用户界面，此类应该是一个组件并实现 <xref:System.ComponentModel.IComponent>，或者是从直接或间接实现 <xref:System.ComponentModel.IComponent> 的类派生的。</span><span class="sxs-lookup"><span data-stu-id="93f63-114">If your class will be used on a design surface (such as the Windows Forms or Web Forms Designer) but has no user interface, it should be a component and implement <xref:System.ComponentModel.IComponent>, or derive from a class that directly or indirectly implements <xref:System.ComponentModel.IComponent>.</span></span>  
  
 <span data-ttu-id="93f63-115"><xref:System.ComponentModel.Component> 和 <xref:System.ComponentModel.MarshalByValueComponent> 类是 <xref:System.ComponentModel.IComponent> 接口的基实现。</span><span class="sxs-lookup"><span data-stu-id="93f63-115">The <xref:System.ComponentModel.Component> and <xref:System.ComponentModel.MarshalByValueComponent> classes are base implementations of the <xref:System.ComponentModel.IComponent> interface.</span></span> <span data-ttu-id="93f63-116">这些类之间的主要区别在于 <xref:System.ComponentModel.Component> 类由引用封送，而 <xref:System.ComponentModel.IComponent> 由值封送。</span><span class="sxs-lookup"><span data-stu-id="93f63-116">The main difference between these classes is that the <xref:System.ComponentModel.Component> class is marshaled by reference, while <xref:System.ComponentModel.IComponent> is marshaled by value.</span></span> <span data-ttu-id="93f63-117">以下列表为实施者提供了全面的指南。</span><span class="sxs-lookup"><span data-stu-id="93f63-117">The following list provides broad guidelines for implementers.</span></span>  
  
- <span data-ttu-id="93f63-118">如果组件需要由引用封送，请从 <xref:System.ComponentModel.Component> 派生。</span><span class="sxs-lookup"><span data-stu-id="93f63-118">If your component needs to be marshaled by reference, derive from <xref:System.ComponentModel.Component>.</span></span>  
  
- <span data-ttu-id="93f63-119">如果组件需要由值封送，请从 <xref:System.ComponentModel.MarshalByValueComponent> 派生。</span><span class="sxs-lookup"><span data-stu-id="93f63-119">If your component needs to be marshaled by value, derive from <xref:System.ComponentModel.MarshalByValueComponent>.</span></span>  
  
- <span data-ttu-id="93f63-120">如果因单一继承导致无法从其中一个基实现派生组件，则请实现 <xref:System.ComponentModel.IComponent>。</span><span class="sxs-lookup"><span data-stu-id="93f63-120">If your component cannot derive from one of the base implementations due to single inheritance, implement <xref:System.ComponentModel.IComponent>.</span></span>  
  
## <a name="component-classes"></a><span data-ttu-id="93f63-121">组件类</span><span class="sxs-lookup"><span data-stu-id="93f63-121">Component Classes</span></span>  

 <span data-ttu-id="93f63-122"><xref:System.ComponentModel> 命名空间提供用于实现组件和控件的运行时和设计时行为的类。</span><span class="sxs-lookup"><span data-stu-id="93f63-122">The <xref:System.ComponentModel> namespace provides classes that are used to implement the run-time and design-time behavior of components and controls.</span></span> <span data-ttu-id="93f63-123">此命名空间包括用于特性和类型转换器的实现、数据源绑定和组件授权的基类和接口。</span><span class="sxs-lookup"><span data-stu-id="93f63-123">This namespace includes the base classes and interfaces for implementing attributes and type converters, binding to data sources, and licensing components.</span></span>  
  
 <span data-ttu-id="93f63-124">核心组件类包括：</span><span class="sxs-lookup"><span data-stu-id="93f63-124">The core component classes are:</span></span>  
  
- <span data-ttu-id="93f63-125"><xref:System.ComponentModel.Component>.</span><span class="sxs-lookup"><span data-stu-id="93f63-125"><xref:System.ComponentModel.Component>.</span></span> <span data-ttu-id="93f63-126"><xref:System.ComponentModel.IComponent> 接口的基实现。</span><span class="sxs-lookup"><span data-stu-id="93f63-126">A base implementation for the <xref:System.ComponentModel.IComponent> interface.</span></span> <span data-ttu-id="93f63-127">此类可以实现在应用程序之间共享对象。</span><span class="sxs-lookup"><span data-stu-id="93f63-127">This class enables object sharing between applications.</span></span>  
  
- <span data-ttu-id="93f63-128"><xref:System.ComponentModel.MarshalByValueComponent>。</span><span class="sxs-lookup"><span data-stu-id="93f63-128"><xref:System.ComponentModel.MarshalByValueComponent>.</span></span> <span data-ttu-id="93f63-129"><xref:System.ComponentModel.IComponent> 接口的基实现。</span><span class="sxs-lookup"><span data-stu-id="93f63-129">A base implementation for the <xref:System.ComponentModel.IComponent> interface.</span></span>  
  
- <span data-ttu-id="93f63-130"><xref:System.ComponentModel.Container>.</span><span class="sxs-lookup"><span data-stu-id="93f63-130"><xref:System.ComponentModel.Container>.</span></span> <span data-ttu-id="93f63-131"><xref:System.ComponentModel.IContainer> 接口的基实现。</span><span class="sxs-lookup"><span data-stu-id="93f63-131">The base implementation for the <xref:System.ComponentModel.IContainer> interface.</span></span> <span data-ttu-id="93f63-132">此类封装零个或多个组件。</span><span class="sxs-lookup"><span data-stu-id="93f63-132">This class encapsulates zero or more components.</span></span>  
  
 <span data-ttu-id="93f63-133">部分用于组件授权的类包括：</span><span class="sxs-lookup"><span data-stu-id="93f63-133">Some of the classes used for component licensing are:</span></span>  
  
- <span data-ttu-id="93f63-134"><xref:System.ComponentModel.License>.</span><span class="sxs-lookup"><span data-stu-id="93f63-134"><xref:System.ComponentModel.License>.</span></span> <span data-ttu-id="93f63-135">所有许可证的抽象基类。</span><span class="sxs-lookup"><span data-stu-id="93f63-135">The abstract base class for all licenses.</span></span> <span data-ttu-id="93f63-136">对组件的特定实例授予许可证。</span><span class="sxs-lookup"><span data-stu-id="93f63-136">A license is granted to a specific instance of a component.</span></span>  
  
- <span data-ttu-id="93f63-137"><xref:System.ComponentModel.LicenseManager>。</span><span class="sxs-lookup"><span data-stu-id="93f63-137"><xref:System.ComponentModel.LicenseManager>.</span></span> <span data-ttu-id="93f63-138">提供属性和方法，用以将许可证添加到组件和管理 <xref:System.ComponentModel.LicenseProvider>。</span><span class="sxs-lookup"><span data-stu-id="93f63-138">Provides properties and methods to add a license to a component and to manage a <xref:System.ComponentModel.LicenseProvider>.</span></span>  
  
- <span data-ttu-id="93f63-139"><xref:System.ComponentModel.LicenseProvider>。</span><span class="sxs-lookup"><span data-stu-id="93f63-139"><xref:System.ComponentModel.LicenseProvider>.</span></span> <span data-ttu-id="93f63-140">实现许可证提供程序的抽象基类。</span><span class="sxs-lookup"><span data-stu-id="93f63-140">The abstract base class for implementing a license provider.</span></span>  
  
- <span data-ttu-id="93f63-141"><xref:System.ComponentModel.LicenseProviderAttribute>.</span><span class="sxs-lookup"><span data-stu-id="93f63-141"><xref:System.ComponentModel.LicenseProviderAttribute>.</span></span> <span data-ttu-id="93f63-142">指定要与某个类一起使用的 <xref:System.ComponentModel.LicenseProvider> 类。</span><span class="sxs-lookup"><span data-stu-id="93f63-142">Specifies the <xref:System.ComponentModel.LicenseProvider> class to use with a class.</span></span>  
  
 <span data-ttu-id="93f63-143">常用于描述和保存组件的类。</span><span class="sxs-lookup"><span data-stu-id="93f63-143">Classes commonly used for describing and persisting components.</span></span>  
  
- <span data-ttu-id="93f63-144"><xref:System.ComponentModel.TypeDescriptor>。</span><span class="sxs-lookup"><span data-stu-id="93f63-144"><xref:System.ComponentModel.TypeDescriptor>.</span></span> <span data-ttu-id="93f63-145">提供有关组件特征的信息，如组件的特性、属性和事件。</span><span class="sxs-lookup"><span data-stu-id="93f63-145">Provides information about the characteristics for a component, such as its attributes, properties, and events.</span></span>  
  
- <span data-ttu-id="93f63-146"><xref:System.ComponentModel.EventDescriptor>。</span><span class="sxs-lookup"><span data-stu-id="93f63-146"><xref:System.ComponentModel.EventDescriptor>.</span></span> <span data-ttu-id="93f63-147">提供有关事件的信息。</span><span class="sxs-lookup"><span data-stu-id="93f63-147">Provides information about an event.</span></span>  
  
- <span data-ttu-id="93f63-148"><xref:System.ComponentModel.PropertyDescriptor>.</span><span class="sxs-lookup"><span data-stu-id="93f63-148"><xref:System.ComponentModel.PropertyDescriptor>.</span></span> <span data-ttu-id="93f63-149">提供有关属性的信息。</span><span class="sxs-lookup"><span data-stu-id="93f63-149">Provides information about a property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="93f63-150">相关章节</span><span class="sxs-lookup"><span data-stu-id="93f63-150">Related Sections</span></span>  

 [<span data-ttu-id="93f63-151">控件和组件创作疑难解答</span><span class="sxs-lookup"><span data-stu-id="93f63-151">Troubleshooting Control and Component Authoring</span></span>](/dotnet/desktop/winforms/controls/troubleshooting-control-and-component-authoring)  
 <span data-ttu-id="93f63-152">解释如何解决常见问题。</span><span class="sxs-lookup"><span data-stu-id="93f63-152">Explains how to fix common problems.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93f63-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="93f63-153">See also</span></span>

- [<span data-ttu-id="93f63-154">如何：在 Windows 窗体中访问设计时支持</span><span class="sxs-lookup"><span data-stu-id="93f63-154">How to: Access Design-Time Support in Windows Forms</span></span>](/dotnet/desktop/winforms/controls/developing-windows-forms-controls-at-design-time)
