---
description: '了解详细信息： MissingInteropDataException 类 ( .NET Native) '
title: 缺少互操作数据异常类 (.NET Native)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: eab4bcf8-9f5f-4731-87d8-842748a6062a
ms.openlocfilehash: ee1544d6a0e1e6a3f0e4386650754ed84b49015b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738697"
---
# <a name="missinginteropdataexception-class-net-native"></a><span data-ttu-id="837eb-103">缺少互操作数据异常类 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="837eb-103">MissingInteropDataException Class (.NET Native)</span></span>

<span data-ttu-id="837eb-104">**适用于 Windows 10 的 .NET for Windows apps，仅 .NET Native**</span><span class="sxs-lookup"><span data-stu-id="837eb-104">**.NET for Windows apps for Windows 10, .NET Native only**</span></span>  
  
 <span data-ttu-id="837eb-105">当手动封送方法被调用但一个类型的元数据无法通过动态分析找到或无法在运行时指令文件中找到时，会引发该异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-105">The exception that is thrown when a manual marshaling method is called, but metadata for a type isn't found by static analysis or in a runtime directives file.</span></span>  
  
 <span data-ttu-id="837eb-106">命名空间：System.Runtime.CompilerServices</span><span class="sxs-lookup"><span data-stu-id="837eb-106">**Namespace:** System.Runtime.CompilerServices</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="837eb-107">`MissingInteropDataException`类仅供 .NET Native 工具链内部使用。</span><span class="sxs-lookup"><span data-stu-id="837eb-107">The `MissingInteropDataException` class is intended solely for internal use by the .NET Native tool chain.</span></span> <span data-ttu-id="837eb-108">它不用于在第三方代码中使用，也不应用它处理应用程序代码中的异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-108">It is not intended for use in third-party code, nor should you handle the exception in your application code.</span></span> <span data-ttu-id="837eb-109">相反，你可以通过将条目添加到[运行时指令文件](runtime-directives-rd-xml-configuration-file-reference.md)来消除异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-109">Instead, you eliminate the exception by adding entries to your [runtime directives file](runtime-directives-rd-xml-configuration-file-reference.md).</span></span> <span data-ttu-id="837eb-110">有关详细信息，请参见“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="837eb-110">For more information, see the Remarks section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="837eb-111">语法</span><span class="sxs-lookup"><span data-stu-id="837eb-111">Syntax</span></span>  

 [!code-csharp[ProjectN#21](../../../samples/snippets/csharp/VS_Snippets_CLR/projectn/cs/missinginteropdataexception_syntax1.cs#21)]
 [!code-vb[ProjectN#21](../../../samples/snippets/visualbasic/VS_Snippets_CLR/projectn/vb/missinginteropdataexception_syntax1.vb#21)]  
  
 <span data-ttu-id="837eb-112">`MissingInteropDataException` 类包含以下成员：</span><span class="sxs-lookup"><span data-stu-id="837eb-112">The `MissingInteropDataException` class has the following members:</span></span>  
  
## <a name="constructors"></a><span data-ttu-id="837eb-113">构造函数</span><span class="sxs-lookup"><span data-stu-id="837eb-113">Constructors</span></span>  
  
|<span data-ttu-id="837eb-114">构造函数</span><span class="sxs-lookup"><span data-stu-id="837eb-114">Constructor</span></span>|<span data-ttu-id="837eb-115">说明</span><span class="sxs-lookup"><span data-stu-id="837eb-115">Description</span></span>|  
|-----------------|-----------------|  
|`public MissingInteropDataException(String resourceId, Type pertinentType)`|<span data-ttu-id="837eb-116">通过使用系统提供的消息（该消息描述错误以及缺少数据的类型）的 ID 初始化 `MissingInteropDataException` 类的新实例。</span><span class="sxs-lookup"><span data-stu-id="837eb-116">Initializes a new instance of the `MissingInteropDataException` class by using the ID of a system-supplied message that describes the error and the type whose data is missing.</span></span> <span data-ttu-id="837eb-117">此构造函数仅供 .NET Native 工具链内部使用。</span><span class="sxs-lookup"><span data-stu-id="837eb-117">This constructor is for internal use by the .NET Native tool chain only.</span></span>|  
  
## <a name="properties"></a><span data-ttu-id="837eb-118">属性</span><span class="sxs-lookup"><span data-stu-id="837eb-118">Properties</span></span>  
  
|<span data-ttu-id="837eb-119">属性</span><span class="sxs-lookup"><span data-stu-id="837eb-119">Property</span></span>|<span data-ttu-id="837eb-120">说明</span><span class="sxs-lookup"><span data-stu-id="837eb-120">Description</span></span>|  
|--------------|-----------------|  
|`public IDictionary Data { get; }`|<span data-ttu-id="837eb-121">获取键/值对的集合，这些键/值对提供有关该异常的其他用户定义信息。</span><span class="sxs-lookup"><span data-stu-id="837eb-121">Gets a collection of key/value pairs that provide additional user-defined information about the exception.</span></span> <span data-ttu-id="837eb-122">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-122">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public string HelpLink { get; set; }`|<span data-ttu-id="837eb-123">获取或设置指向与此异常关联的帮助文件链接。</span><span class="sxs-lookup"><span data-stu-id="837eb-123">Gets or sets a link to the help file associated with this exception.</span></span> <span data-ttu-id="837eb-124">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-124">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public int HResult { get; protected set; }`|<span data-ttu-id="837eb-125">获取或设置分配给特定异常的编码数值 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="837eb-125">Gets or sets the `HRESULT`, which is a coded numeric value that is assigned to a specific exception.</span></span> <span data-ttu-id="837eb-126">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-126">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public Exception InnerException { get; }`|<span data-ttu-id="837eb-127">获取导致当前异常的异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-127">Gets the exception that caused the current exception.</span></span> <span data-ttu-id="837eb-128">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-128">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public string Message { get; }`|<span data-ttu-id="837eb-129">获取描述当前异常的消息。</span><span class="sxs-lookup"><span data-stu-id="837eb-129">Gets a message that describes the current exception.</span></span> <span data-ttu-id="837eb-130">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-130">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public Type MissingType { get; private set; }`|<span data-ttu-id="837eb-131">获取或设置丢失数据的类型。</span><span class="sxs-lookup"><span data-stu-id="837eb-131">Gets or sets the type whose data is missing.</span></span>|  
|`public string Source { get; set; }`|<span data-ttu-id="837eb-132">获取或设置引起错误的应用或对象名。</span><span class="sxs-lookup"><span data-stu-id="837eb-132">Gets or sets the name of the app or object that caused the error.</span></span> <span data-ttu-id="837eb-133">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-133">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public string StackTrace { get; }`|<span data-ttu-id="837eb-134">获取调用堆栈上的即时框架字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="837eb-134">Gets a string representation of the immediate frames on the call stack.</span></span> <span data-ttu-id="837eb-135">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-135">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public MethodBase TargetSite { get; }`|<span data-ttu-id="837eb-136">获取引发当前异常的方法。</span><span class="sxs-lookup"><span data-stu-id="837eb-136">Gets the method that threw the current exception.</span></span> <span data-ttu-id="837eb-137">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-137">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
  
## <a name="methods"></a><span data-ttu-id="837eb-138">方法</span><span class="sxs-lookup"><span data-stu-id="837eb-138">Methods</span></span>  
  
|<span data-ttu-id="837eb-139">方法</span><span class="sxs-lookup"><span data-stu-id="837eb-139">Method</span></span>|<span data-ttu-id="837eb-140">说明</span><span class="sxs-lookup"><span data-stu-id="837eb-140">Description</span></span>|  
|------------|-----------------|  
|`public bool Equals(Object obj)`|<span data-ttu-id="837eb-141">确定指定对象是否等于当前对象。</span><span class="sxs-lookup"><span data-stu-id="837eb-141">Determines whether the specified object is equal to the current object.</span></span>  <span data-ttu-id="837eb-142">（从 <xref:System.Object> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-142">(Inherited from <xref:System.Object>.)</span></span>|  
|`protected void Finalize()`|<span data-ttu-id="837eb-143">在垃圾回收将某一对象回收前允许该对象尝试释放资源并执行其他清理操作。</span><span class="sxs-lookup"><span data-stu-id="837eb-143">Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.</span></span> <span data-ttu-id="837eb-144">（从 <xref:System.Object> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-144">(Inherited from <xref:System.Object>.)</span></span>|  
|`public Exception GetBaseException()`|<span data-ttu-id="837eb-145">返回是一个或多个后续异常的根本原因的异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-145">Returns the exception that is the root cause of one or more subsequent exceptions.</span></span> <span data-ttu-id="837eb-146">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-146">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public int GetHashCode()`|<span data-ttu-id="837eb-147">为 `MissingInteropDataException` 实例返回一个哈希代码。</span><span class="sxs-lookup"><span data-stu-id="837eb-147">Returns a hash code for a `MissingInteropDataException` instance.</span></span>   <span data-ttu-id="837eb-148">（从 <xref:System.Object> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-148">(Inherited from <xref:System.Object>.)</span></span>|  
|`public void GetObjectData(SerializationInfo info, StreamingContext context)`|<span data-ttu-id="837eb-149">设置一个包含有关异常信息的 <xref:System.Runtime.Serialization.SerializationInfo> 对象。</span><span class="sxs-lookup"><span data-stu-id="837eb-149">Sets a <xref:System.Runtime.Serialization.SerializationInfo> object with information about the exception.</span></span>  <span data-ttu-id="837eb-150">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-150">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`public Type GetType()`|<span data-ttu-id="837eb-151">获取当前实例的运行时类型。</span><span class="sxs-lookup"><span data-stu-id="837eb-151">Gets the runtime type of the current instance.</span></span> <span data-ttu-id="837eb-152">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-152">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
|`protected Object MemberwiseClone()`|<span data-ttu-id="837eb-153">创建当前对象的卷影副本。</span><span class="sxs-lookup"><span data-stu-id="837eb-153">Creates a shallow copy of the current object.</span></span> <span data-ttu-id="837eb-154">（从 <xref:System.Object> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-154">(Inherited from <xref:System.Object>.)</span></span>|  
|`public string ToString()`|<span data-ttu-id="837eb-155">返回当前异常的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="837eb-155">Returns the string representation of the current exception.</span></span> <span data-ttu-id="837eb-156">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-156">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
  
## <a name="events"></a><span data-ttu-id="837eb-157">事件</span><span class="sxs-lookup"><span data-stu-id="837eb-157">Events</span></span>  
  
|<span data-ttu-id="837eb-158">事件</span><span class="sxs-lookup"><span data-stu-id="837eb-158">Event</span></span>|<span data-ttu-id="837eb-159">说明</span><span class="sxs-lookup"><span data-stu-id="837eb-159">Description</span></span>|  
|-----------|-----------------|  
|`protected event EventHandler<SafeSerializationEventArgs> SerializeObjectState`|<span data-ttu-id="837eb-160">当异常被序列化用来创建包含有关该异常的徐列出数据的异常状态对象时会出现该问题。</span><span class="sxs-lookup"><span data-stu-id="837eb-160">Occurs when an exception is serialized to create an exception state object that contains serialized data about the exception.</span></span> <span data-ttu-id="837eb-161">（从 <xref:System.Exception?displayProperty=nameWithType> 继承。）</span><span class="sxs-lookup"><span data-stu-id="837eb-161">(Inherited from <xref:System.Exception?displayProperty=nameWithType>.)</span></span>|  
  
## <a name="usage-details"></a><span data-ttu-id="837eb-162">使用情况详细信息</span><span class="sxs-lookup"><span data-stu-id="837eb-162">Usage Details</span></span>  

 <span data-ttu-id="837eb-163">由于类型信息无效而导致无法成功调用 COM 或 Windows 运行时组件时会引发 `MissingInteropDataException` 异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-163">The `MissingInteropDataException` exception is thrown when a method call to a COM or Windows Runtime component cannot be made successfully because type information isn't available.</span></span>  
  
 <span data-ttu-id="837eb-164">在运行时可用于应用的元数据由运行时指令定义 (XML 配置) 文件， \*.rd.xml。</span><span class="sxs-lookup"><span data-stu-id="837eb-164">The metadata that is available to an app at run time is defined by the runtime directives (XML configuration) file, \*.rd.xml.</span></span> <span data-ttu-id="837eb-165">为防止应用发生此异常，你必须修改该文件，以定义运行时必须存在的元数据。</span><span class="sxs-lookup"><span data-stu-id="837eb-165">To prevent your app from throwing this exception, you must modify this file to define the metadata that must be present at run time.</span></span> <span data-ttu-id="837eb-166">通常会通过将 `MarshalObject`、`MarshalDelegate` 或 `MarshalStructure` 属性添加到运行时指令文件中的相应程序元素来解决该错误。</span><span class="sxs-lookup"><span data-stu-id="837eb-166">Most commonly, you address this error by adding a `MarshalObject`, `MarshalDelegate`, or `MarshalStructure` attribute to an appropriate program element in the runtime directives file.</span></span> <span data-ttu-id="837eb-167">有关本文件的格式信息，请参阅[运行时指令 (rd.xml) 配置文件参考](runtime-directives-rd-xml-configuration-file-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="837eb-167">For information about the format of this file, see [Runtime Directives (rd.xml) Configuration File Reference](runtime-directives-rd-xml-configuration-file-reference.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="837eb-168">由于此异常表示应用程序需要的元数据在运行时间不可用，因此不应在 `try`/`catch` 块中处理此异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-168">Because this exception indicates that metadata needed by your application isn’t available at run time, you shouldn’t handle this exception in a `try`/`catch` block.</span></span> <span data-ttu-id="837eb-169">相反，你应该诊断引起此异常的原因并通过将适当的条目添加到运行时指令文件消除异常。</span><span class="sxs-lookup"><span data-stu-id="837eb-169">Instead, you should diagnose the cause of the exception and eliminate it by adding the appropriate entry to a runtime directives file.</span></span>  
  
 <span data-ttu-id="837eb-170">`MissingInteropDataException` 类包含单个唯一成员，即 `MissingType` 属性，它表示一种类型，而如果想成功完成方法调用需使用到该类型的元数据。</span><span class="sxs-lookup"><span data-stu-id="837eb-170">The `MissingInteropDataException` class contains a single unique member, the `MissingType` property, that indicates the type whose metadata is needed for a successful method call.</span></span> <span data-ttu-id="837eb-171">所有剩余成员均继承自基类 <xref:System.Exception?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="837eb-171">All remaining members are inherited from the base class, <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="837eb-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="837eb-172">See also</span></span>

- <xref:System.Exception?displayProperty=nameWithType>
- [<span data-ttu-id="837eb-173">MissingMetadataException 类</span><span class="sxs-lookup"><span data-stu-id="837eb-173">MissingMetadataException Class</span></span>](missingmetadataexception-class-net-native.md)
- [<span data-ttu-id="837eb-174">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="837eb-174">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
