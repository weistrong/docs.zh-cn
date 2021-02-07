---
description: 详细了解：部分信任的最佳实践
title: 部分信任最佳实践
ms.date: 03/30/2017
ms.assetid: 0d052bc0-5b98-4c50-8bb5-270cc8a8b145
ms.openlocfilehash: abdc0fbbb84581b302bca8d514a5f8f5cc2703e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733549"
---
# <a name="partial-trust-best-practices"></a><span data-ttu-id="7eb64-103">部分信任最佳实践</span><span class="sxs-lookup"><span data-stu-id="7eb64-103">Partial Trust Best Practices</span></span>

<span data-ttu-id="7eb64-104">本主题介绍在部分信任环境中运行 Windows Communication Foundation (WCF) 时的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="7eb64-104">This topic describes best practices when running Windows Communication Foundation (WCF) in a partial trust environment.</span></span>

## <a name="serialization"></a><span data-ttu-id="7eb64-105">序列化</span><span class="sxs-lookup"><span data-stu-id="7eb64-105">Serialization</span></span>

<span data-ttu-id="7eb64-106">当在部分受信任的应用程序中使用 <xref:System.Runtime.Serialization.DataContractSerializer> 时，请应用以下做法。</span><span class="sxs-lookup"><span data-stu-id="7eb64-106">Apply the following practices when using the <xref:System.Runtime.Serialization.DataContractSerializer> in a partially-trusted application.</span></span>

- <span data-ttu-id="7eb64-107">必须使用 `[DataContract]` 属性显式标记所有可序列化类型。</span><span class="sxs-lookup"><span data-stu-id="7eb64-107">All serializable types must be explicitly marked with the `[DataContract]` attribute.</span></span> <span data-ttu-id="7eb64-108">在部分信任环境中不支持以下技术：</span><span class="sxs-lookup"><span data-stu-id="7eb64-108">The following techniques are not supported in a partial trust environment:</span></span>

- <span data-ttu-id="7eb64-109">使用 <xref:System.SerializableAttribute> 标记要序列化的类。</span><span class="sxs-lookup"><span data-stu-id="7eb64-109">Marking classes to be serialized with the <xref:System.SerializableAttribute>.</span></span>

- <span data-ttu-id="7eb64-110">实现 <xref:System.Runtime.Serialization.ISerializable> 接口以允许类控制其序列化过程。</span><span class="sxs-lookup"><span data-stu-id="7eb64-110">Implementing the <xref:System.Runtime.Serialization.ISerializable> interface to allow a class to control its serialization process.</span></span>

### <a name="using-datacontractserializer"></a><span data-ttu-id="7eb64-111">使用 DataContractSerializer</span><span class="sxs-lookup"><span data-stu-id="7eb64-111">Using DataContractSerializer</span></span>

- <span data-ttu-id="7eb64-112">使用 `[DataContract]` 属性标记的所有类型都必须是公共的。</span><span class="sxs-lookup"><span data-stu-id="7eb64-112">All types marked with the `[DataContract]` attribute must be public.</span></span> <span data-ttu-id="7eb64-113">在部分信任环境中无法序列化非公共类型。</span><span class="sxs-lookup"><span data-stu-id="7eb64-113">Non-public types cannot be serialized in a partial trust environment.</span></span>

- <span data-ttu-id="7eb64-114">可序列化 `[DataContract]` 类型中的所有 `[DataContract]` 成员都必须是公共的。</span><span class="sxs-lookup"><span data-stu-id="7eb64-114">All `[DataContract]` members in a serializable `[DataContract]` type must be public.</span></span> <span data-ttu-id="7eb64-115">在部分信任环境中无法序列化具有非公共 `[DataMember]` 的类型。</span><span class="sxs-lookup"><span data-stu-id="7eb64-115">A type with a non-public `[DataMember]` cannot be serialized in a partial trust environment.</span></span>

- <span data-ttu-id="7eb64-116">必须将处理序列化事件的方法（如 `OnSerializing`、`OnSerialized`、`OnDeserializing` 和 `OnDeserialized`）声明为公共的。</span><span class="sxs-lookup"><span data-stu-id="7eb64-116">Methods that handle serialization events (such as `OnSerializing`, `OnSerialized`, `OnDeserializing`, and `OnDeserialized`) must be declared as public.</span></span> <span data-ttu-id="7eb64-117">但是，同时支持 <xref:System.Runtime.Serialization.IDeserializationCallback.OnDeserialization%28System.Object%29> 的显式实现和隐式实现。</span><span class="sxs-lookup"><span data-stu-id="7eb64-117">However, both explicit and implicit implementations of <xref:System.Runtime.Serialization.IDeserializationCallback.OnDeserialization%28System.Object%29> are supported.</span></span>

- <span data-ttu-id="7eb64-118">在程序集中实现的、使用 `[DataContract]` 标记的 <xref:System.Security.AllowPartiallyTrustedCallersAttribute> 类型不得在类型构造函数中执行与安全相关的操作，因为在反序列化期间 <xref:System.Runtime.Serialization.DataContractSerializer> 不调用新实例化的对象的构造函数。</span><span class="sxs-lookup"><span data-stu-id="7eb64-118">`[DataContract]` types implemented in assemblies marked with the <xref:System.Security.AllowPartiallyTrustedCallersAttribute> must not perform security-related actions in the type constructor, as the <xref:System.Runtime.Serialization.DataContractSerializer> does not call the constructor of the newly-instantiated object during deserialization.</span></span> <span data-ttu-id="7eb64-119">具体说来，对于 `[DataContract]` 类型，必须避免使用以下常见安全技术：</span><span class="sxs-lookup"><span data-stu-id="7eb64-119">Specifically, the following common security techniques must be avoided for `[DataContract]` types:</span></span>

- <span data-ttu-id="7eb64-120">尝试通过使类型的构造函数变为内部或私有来限制部分信任访问。</span><span class="sxs-lookup"><span data-stu-id="7eb64-120">Attempting to restrict partial trust access by making the type's constructor internal or private.</span></span>

- <span data-ttu-id="7eb64-121">通过将 `[LinkDemand]` 添加到类型的构造函数来限制对该类型的访问。</span><span class="sxs-lookup"><span data-stu-id="7eb64-121">Restricting access to the type by adding a `[LinkDemand]` to the type's constructor.</span></span>

- <span data-ttu-id="7eb64-122">假定由于已成功实例化对象，构造函数强制执行的任何验证检查已成功通过。</span><span class="sxs-lookup"><span data-stu-id="7eb64-122">Assuming that because the object has been successfully instantiated, any validation checks enforced by the constructor have passed successfully.</span></span>

### <a name="using-ixmlserializable"></a><span data-ttu-id="7eb64-123">使用 IXmlSerializable</span><span class="sxs-lookup"><span data-stu-id="7eb64-123">Using IXmlSerializable</span></span>

<span data-ttu-id="7eb64-124">以下最佳实践适用于实现 <xref:System.Xml.Serialization.IXmlSerializable> 且使用 <xref:System.Runtime.Serialization.DataContractSerializer> 进行序列化的类型：</span><span class="sxs-lookup"><span data-stu-id="7eb64-124">The following best practices apply for types that implement <xref:System.Xml.Serialization.IXmlSerializable> and are serialized using the <xref:System.Runtime.Serialization.DataContractSerializer>:</span></span>

- <span data-ttu-id="7eb64-125"><xref:System.Xml.Serialization.IXmlSerializable.GetSchema%2A> 静态方法实现必须为 `public`。</span><span class="sxs-lookup"><span data-stu-id="7eb64-125">The <xref:System.Xml.Serialization.IXmlSerializable.GetSchema%2A> static method implementations must be `public`.</span></span>

- <span data-ttu-id="7eb64-126">实现 <xref:System.Xml.Serialization.IXmlSerializable> 接口的实例方法必须为 `public`。</span><span class="sxs-lookup"><span data-stu-id="7eb64-126">The instance methods that implement the <xref:System.Xml.Serialization.IXmlSerializable> interface must be `public`.</span></span>

## <a name="using-wcf-from-fully-trusted-platform-code-that-allows-calls-from-partially-trusted-callers"></a><span data-ttu-id="7eb64-127">从允许来自部分受信任的调用方的调用的完全受信任平台代码使用 WCF</span><span class="sxs-lookup"><span data-stu-id="7eb64-127">Using WCF from Fully-Trusted Platform Code that Allows Calls from Partially Trusted Callers</span></span>

<span data-ttu-id="7eb64-128">WCF 部分信任安全模型假定 WCF 公共方法或属性的任何调用方在代码访问安全性 (CAS) 宿主应用程序的上下文中运行。</span><span class="sxs-lookup"><span data-stu-id="7eb64-128">The WCF partial trust security model assumes that any caller of a WCF public method or property is running in the code access security (CAS) context of the hosting application.</span></span> <span data-ttu-id="7eb64-129">WCF 还假设每个只有一个应用程序安全上下文 <xref:System.AppDomain> ，并且在 <xref:System.AppDomain> 创建时由受信任的主机建立此上下文 (例如，通过调用 <xref:System.AppDomain.CreateDomain%2A> 或通过 ASP.NET 应用程序管理器) 。</span><span class="sxs-lookup"><span data-stu-id="7eb64-129">WCF also assumes that only one application security context exists for each <xref:System.AppDomain>, and that this context is established at <xref:System.AppDomain> creation time by a trusted host (for example, by a call to <xref:System.AppDomain.CreateDomain%2A> or by the ASP.NET Application Manager).</span></span>

<span data-ttu-id="7eb64-130">此安全模型适用于无法断言其他 CAS 权限的用户编写应用程序，如在 Medium Trust ASP.NET 应用程序中运行的用户代码。</span><span class="sxs-lookup"><span data-stu-id="7eb64-130">This security model applies to user-written applications that cannot assert additional CAS permissions, such as user code running in a Medium Trust ASP.NET application.</span></span> <span data-ttu-id="7eb64-131">但是，完全受信任的平台代码 (例如，安装在全局程序集缓存中并接受部分受信任代码调用的第三方程序集) 必须在代表部分受信任的应用程序调用 WCF 时小心，以免引入应用程序级别的安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="7eb64-131">However, fully-trusted platform code (for example, a third-party assembly that is installed in the global assembly cache and accepts calls from partially-trusted code) must take explicit care when calling into WCF on behalf of a partially-trusted application to avoid introducing application-level security vulnerabilities.</span></span>

<span data-ttu-id="7eb64-132">完全信任代码应避免通过 <xref:System.Security.PermissionSet.Assert%2A> <xref:System.Security.PermissionSet.PermitOnly%2A> <xref:System.Security.PermissionSet.Deny%2A> 在代表部分受信任的代码调用 WCF api 之前调用、或) 来更改当前线程的 CAS 权限集 (。</span><span class="sxs-lookup"><span data-stu-id="7eb64-132">Full-trust code should avoid altering the CAS permission set of the current thread (by calling <xref:System.Security.PermissionSet.Assert%2A>, <xref:System.Security.PermissionSet.PermitOnly%2A>, or <xref:System.Security.PermissionSet.Deny%2A>) prior to calling WCF APIs on behalf of partially-trusted code.</span></span> <span data-ttu-id="7eb64-133">断言、拒绝或通过其他方式创建特定于线程且独立于应用程序级安全上下文的权限上下文可能会导致意外行为。</span><span class="sxs-lookup"><span data-stu-id="7eb64-133">Asserting, denying, or otherwise creating a thread-specific permission context that is independent of the application-level security context can result in unexpected behavior.</span></span> <span data-ttu-id="7eb64-134">根据应用程序，此行为可能会导致应用程序级安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="7eb64-134">Depending on the application, this behavior may result in application-level security vulnerabilities.</span></span>

<span data-ttu-id="7eb64-135">使用线程特定的权限上下文调用 WCF 的代码必须准备好处理可能出现的以下情况：</span><span class="sxs-lookup"><span data-stu-id="7eb64-135">Code that calls into WCF using a thread-specific permission context must be prepared to handle the following situations that may arise:</span></span>

- <span data-ttu-id="7eb64-136">在操作期间可能未维护线程特定的安全上下文，这导致潜在的安全异常。</span><span class="sxs-lookup"><span data-stu-id="7eb64-136">The thread-specific security context may not be maintained for the duration of the operation, which results in potential security exceptions.</span></span>

- <span data-ttu-id="7eb64-137">内部 WCF 代码以及任何用户提供的回调都可能在不同的安全上下文中运行，该上下文与最初启动调用的安全上下文不同。</span><span class="sxs-lookup"><span data-stu-id="7eb64-137">Internal WCF code as well as any user-provided callbacks may run in a different security context than the one under which the call was originally initiated.</span></span> <span data-ttu-id="7eb64-138">这些上下文包括：</span><span class="sxs-lookup"><span data-stu-id="7eb64-138">These contexts include:</span></span>

  - <span data-ttu-id="7eb64-139">应用程序权限上下文。</span><span class="sxs-lookup"><span data-stu-id="7eb64-139">The application permission context.</span></span>

  - <span data-ttu-id="7eb64-140">之前由其他用户线程创建的、用于在当前运行的生存期内调用 WCF 的任何线程特定权限上下文 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="7eb64-140">Any thread-specific permission context previously created by other user threads used to call into WCF during the lifetime of the currently running <xref:System.AppDomain>.</span></span>

<span data-ttu-id="7eb64-141">WCF 保证部分受信任的代码无法获取完全信任的权限，除非在调用 WCF 公共 Api 之前，完全受信任的组件断言了此类权限。</span><span class="sxs-lookup"><span data-stu-id="7eb64-141">WCF guarantees that partially-trusted code cannot obtain full-trust permissions unless such permissions are asserted by a fully-trusted component prior to calling into WCF public APIs.</span></span> <span data-ttu-id="7eb64-142">但是，它不保证断言完全信任的效果隔离到特定的线程、操作或用户操作。</span><span class="sxs-lookup"><span data-stu-id="7eb64-142">However, it does not guarantee that the effects of asserting full trust is isolated to a particular thread, operation, or user action.</span></span>

<span data-ttu-id="7eb64-143">作为最佳实践，避免通过调用 <xref:System.Security.PermissionSet.Assert%2A>、<xref:System.Security.PermissionSet.PermitOnly%2A> 或 <xref:System.Security.PermissionSet.Deny%2A> 创建线程特定的权限上下文。</span><span class="sxs-lookup"><span data-stu-id="7eb64-143">As a best practice, avoid creating thread-specific permission context by calling <xref:System.Security.PermissionSet.Assert%2A>, <xref:System.Security.PermissionSet.PermitOnly%2A>, or <xref:System.Security.PermissionSet.Deny%2A>.</span></span> <span data-ttu-id="7eb64-144">而是对应用程序本身授予或拒绝特权，以便不需要 <xref:System.Security.PermissionSet.Assert%2A>、<xref:System.Security.PermissionSet.Deny%2A> 或 <xref:System.Security.PermissionSet.PermitOnly%2A>。</span><span class="sxs-lookup"><span data-stu-id="7eb64-144">Instead, grant or deny the privilege to the application itself, so that no <xref:System.Security.PermissionSet.Assert%2A>, <xref:System.Security.PermissionSet.Deny%2A>, or <xref:System.Security.PermissionSet.PermitOnly%2A> is required.</span></span>

## <a name="see-also"></a><span data-ttu-id="7eb64-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="7eb64-145">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.Xml.Serialization.IXmlSerializable>
