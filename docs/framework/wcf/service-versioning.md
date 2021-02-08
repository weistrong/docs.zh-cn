---
description: 了解详细信息：服务版本控制
title: 服务版本控制
ms.date: 03/30/2017
ms.assetid: 37575ead-d820-4a67-8059-da11a2ab48e2
ms.openlocfilehash: 3a49b29b3f99caff688a0c1540698d80608a7ce2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792981"
---
# <a name="service-versioning"></a><span data-ttu-id="1618f-103">服务版本控制</span><span class="sxs-lookup"><span data-stu-id="1618f-103">Service Versioning</span></span>

<span data-ttu-id="1618f-104">服务（及其公开的终结点）在初始部署之后，可能出于多种原因（例如，更改业务需求、信息技术需求，或者为了解决其他问题）而需要更改，并且在其生存期期间可能需要更改多次。</span><span class="sxs-lookup"><span data-stu-id="1618f-104">After initial deployment, and potentially several times during their lifetime, services (and the endpoints they expose) may need to be changed for a variety of reasons, such as changing business needs, information technology requirements, or to address other issues.</span></span> <span data-ttu-id="1618f-105">每次更改都会引入服务的一个新版本。</span><span class="sxs-lookup"><span data-stu-id="1618f-105">Each change introduces a new version of the service.</span></span> <span data-ttu-id="1618f-106">本主题说明如何在 Windows Communication Foundation (WCF) 中考虑版本控制。</span><span class="sxs-lookup"><span data-stu-id="1618f-106">This topic explains how to consider versioning in Windows Communication Foundation (WCF).</span></span>  
  
## <a name="four-categories-of-service-changes"></a><span data-ttu-id="1618f-107">服务更改的四个类别</span><span class="sxs-lookup"><span data-stu-id="1618f-107">Four Categories of Service Changes</span></span>  

 <span data-ttu-id="1618f-108">可能需要的服务更改可分成四类：</span><span class="sxs-lookup"><span data-stu-id="1618f-108">The changes to services that may be required can be classified into four categories:</span></span>  
  
- <span data-ttu-id="1618f-109">协定更改：例如，可能添加某个操作，或者可能添加或更改消息中的某个数据元素。</span><span class="sxs-lookup"><span data-stu-id="1618f-109">Contract changes: For example, an operation might be added, or a data element in a message might be added or changed.</span></span>  
  
- <span data-ttu-id="1618f-110">地址更改：例如，服务移至另一个位置，终结点在此位置获得新地址。</span><span class="sxs-lookup"><span data-stu-id="1618f-110">Address changes: For example, a service moves to a different location where endpoints have new addresses.</span></span>  
  
- <span data-ttu-id="1618f-111">绑定更改：例如，安全机制更改或其设置更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-111">Binding changes: For example, a security mechanism changes or its settings change.</span></span>  
  
- <span data-ttu-id="1618f-112">实现更改：例如，当内部方法实现更改时。</span><span class="sxs-lookup"><span data-stu-id="1618f-112">Implementation changes: For example, when an internal method implementation changes.</span></span>  
  
 <span data-ttu-id="1618f-113">这些更改中有一些称为“中断性”，而其他则为“非中断性”。</span><span class="sxs-lookup"><span data-stu-id="1618f-113">Some of these changes are called "breaking" and others are "nonbreaking."</span></span> <span data-ttu-id="1618f-114">如果在早期版本中已成功处理的所有消息都已在新版本中成功处理 *，则更改* 不会中断。</span><span class="sxs-lookup"><span data-stu-id="1618f-114">A change is *nonbreaking* if all messages that would have been processed successfully in the previous version are processed successfully in the new version.</span></span> <span data-ttu-id="1618f-115">不符合该条件的任何更改都是一项 *重大* 更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-115">Any change that does not meet that criterion is a *breaking* change.</span></span>  
  
## <a name="service-orientation-and-versioning"></a><span data-ttu-id="1618f-116">面向服务和版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-116">Service Orientation and Versioning</span></span>  

 <span data-ttu-id="1618f-117">面向服务的原则之一是服务和客户端自主（即独立）。</span><span class="sxs-lookup"><span data-stu-id="1618f-117">One of the tenets of service orientation is that services and clients are autonomous (or independent).</span></span> <span data-ttu-id="1618f-118">这其中的一层含义是，服务开发人员不能假设他们能控制，甚至是了解所有服务客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-118">Among other things, this implies that service developers cannot assume that they control or even know about all service clients.</span></span> <span data-ttu-id="1618f-119">这消除了在服务更改版本时重建和重新部署所有客户端的可能。</span><span class="sxs-lookup"><span data-stu-id="1618f-119">This eliminates the option of rebuilding and redeploying all clients when a service changes versions.</span></span> <span data-ttu-id="1618f-120">本主题假设服务遵循这一原则，并因此必须独立于其客户端进行更改或“版本变更”。</span><span class="sxs-lookup"><span data-stu-id="1618f-120">This topic assumes the service adheres to this tenet and therefore must be changed or "versioned" independent of its clients.</span></span>  
  
 <span data-ttu-id="1618f-121">如果出现意外的并且无法避免的中断性更改，应用程序可选择忽略此原则，并要求以新版本的服务重建和重新部署客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-121">In cases where a breaking change is unexpected and cannot be avoided, an application may choose to ignore this tenet and require that clients be rebuilt and redeployed with a new version of the service.</span></span>  
  
## <a name="contract-versioning"></a><span data-ttu-id="1618f-122">协定版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-122">Contract Versioning</span></span>  

 <span data-ttu-id="1618f-123">客户端使用的协定不需要与服务所使用的协定相同；它们只需要兼容即可。</span><span class="sxs-lookup"><span data-stu-id="1618f-123">Contracts used by a client do not need to be the same as the contract used by the service; they need only to be compatible.</span></span>  
  
 <span data-ttu-id="1618f-124">对于服务协定，兼容性意味着可以添加服务所公开的新操作，但是不能移除或从语义上更改现有操作。</span><span class="sxs-lookup"><span data-stu-id="1618f-124">For service contracts, compatibility means new operations exposed by the service can be added but existing operations cannot be removed or changed semantically.</span></span>  
  
 <span data-ttu-id="1618f-125">对于数据协定，兼容性意味着可以添加新的架构类型定义，但是不能以中断性方式更改架构类型定义。</span><span class="sxs-lookup"><span data-stu-id="1618f-125">For data contracts, compatibility means new schema type definitions can be added but existing schema type definitions cannot be changed in breaking ways.</span></span> <span data-ttu-id="1618f-126">中断性更改可包括移除数据成员或不兼容地更改其数据类型。</span><span class="sxs-lookup"><span data-stu-id="1618f-126">Breaking changes might include removing data members or changing their data type incompatibly.</span></span> <span data-ttu-id="1618f-127">这一特点允许服务在某种程度上更改其协定的版本而又不中断客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-127">This feature allows the service some latitude in changing the version of its contracts without breaking clients.</span></span> <span data-ttu-id="1618f-128">接下来的两部分介绍了可对 WCF 数据和服务协定进行的不间断和重大更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-128">The next two sections explain nonbreaking and breaking changes that can be made to WCF data and service contracts.</span></span>  
  
## <a name="data-contract-versioning"></a><span data-ttu-id="1618f-129">数据协定版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-129">Data Contract Versioning</span></span>  

 <span data-ttu-id="1618f-130">本节讨论使用 <xref:System.Runtime.Serialization.DataContractSerializer> 和 <xref:System.Runtime.Serialization.DataContractAttribute> 类时的数据版本管理。</span><span class="sxs-lookup"><span data-stu-id="1618f-130">This section deals with data versioning when using the <xref:System.Runtime.Serialization.DataContractSerializer> and <xref:System.Runtime.Serialization.DataContractAttribute> classes.</span></span>  
  
### <a name="strict-versioning"></a><span data-ttu-id="1618f-131">严格版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-131">Strict Versioning</span></span>  

 <span data-ttu-id="1618f-132">很多情况下，当更改版本是一个问题时，服务开发人员无法控制客户端，因此无法假设它们将对消息 XML 或架构中的更改作何反应。</span><span class="sxs-lookup"><span data-stu-id="1618f-132">In many scenarios when changing versions is an issue, the service developer does not have control over the clients and therefore cannot make assumptions about how they would react to changes in the message XML or schema.</span></span> <span data-ttu-id="1618f-133">在这些情况下，出于两个原因，必须保证将针对旧架构验证新消息：</span><span class="sxs-lookup"><span data-stu-id="1618f-133">In these cases, you must guarantee that the new messages will validate against the old schema, for two reasons:</span></span>  
  
- <span data-ttu-id="1618f-134">开发旧客户端时的假设是架构将不会更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-134">The old clients were developed with the assumption that the schema will not change.</span></span> <span data-ttu-id="1618f-135">这些旧客户端可能无法处理设计时并未考虑要处理的消息。</span><span class="sxs-lookup"><span data-stu-id="1618f-135">They may fail to process messages that they were never designed for.</span></span>  
  
- <span data-ttu-id="1618f-136">旧客户端可能就在尝试处理消息之前针对旧架构执行实际架构验证。</span><span class="sxs-lookup"><span data-stu-id="1618f-136">The old clients may perform actual schema validation against the old schema before even attempting to process the messages.</span></span>  
  
 <span data-ttu-id="1618f-137">此类情况下的建议方法是将现有数据协定视为不可变，并用唯一的 XML 限定名创建新协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-137">The recommended approach in such scenarios is to treat existing data contracts as immutable and create new ones with unique XML qualified names.</span></span> <span data-ttu-id="1618f-138">服务开发人员然后可向现有服务协定添加新方法或者以使用新数据协定的方法创建新服务协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-138">The service developer would then either add new methods to an existing service contract or create a new service contract with methods that use the new data contract.</span></span>  
  
 <span data-ttu-id="1618f-139">通常的情况是，服务开发人员需要编写一些业务逻辑，这些逻辑应在数据协定的所有版本内运行，此外还需要针对该数据协定的每个版本编写特定于版本的业务代码。</span><span class="sxs-lookup"><span data-stu-id="1618f-139">It will often be the case that a service developer needs to write some business logic that should run within all versions of a data contract plus version-specific business code for each version of the data contract.</span></span> <span data-ttu-id="1618f-140">本主题最后的附录说明了如何使用接口来满足这种需要。</span><span class="sxs-lookup"><span data-stu-id="1618f-140">The appendix at the end of this topic explains how interfaces can be used to satisfy this need.</span></span>  
  
### <a name="lax-versioning"></a><span data-ttu-id="1618f-141">宽松版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-141">Lax Versioning</span></span>  

 <span data-ttu-id="1618f-142">在很多其他情况下，服务开发人员可假设向数据协定添加新的可选成员不会中断现有客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-142">In many other scenarios, the service developer can make the assumption that adding a new, optional member to the data contract will not break existing clients.</span></span> <span data-ttu-id="1618f-143">这要求服务开发人员调查现有客户端是否并不执行架构验证，以及它们是否忽略未知数据成员。</span><span class="sxs-lookup"><span data-stu-id="1618f-143">This requires the service developer to investigate whether existing clients are not performing schema validation and that they ignore unknown data members.</span></span> <span data-ttu-id="1618f-144">在这些情况下，就可以利用以非中断的方式添加新成员的数据协定功能。</span><span class="sxs-lookup"><span data-stu-id="1618f-144">In these scenarios, it is possible to take advantage of data contract features for adding new members in a nonbreaking way.</span></span> <span data-ttu-id="1618f-145">如果数据协定的版本管理功能已经用于服务的第一个版本，服务开发人员就可以肯定地作此假设。</span><span class="sxs-lookup"><span data-stu-id="1618f-145">The service developer can make this assumption with confidence if the data contract features for versioning were already used for the first version of the service.</span></span>  
  
 <span data-ttu-id="1618f-146">WCF、ASP.NET Web 服务和许多其他 Web 服务堆栈支持 *宽松版本控制*：也就是说，它们不会为收到的数据中的新未知数据成员引发异常。</span><span class="sxs-lookup"><span data-stu-id="1618f-146">WCF, ASP.NET Web Services, and many other Web service stacks support *lax versioning*: that is, they do not throw exceptions for new unknown data members in received data.</span></span>  
  
 <span data-ttu-id="1618f-147">很容易误以为添加新成员将不会中断现有客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-147">It is easy to mistakenly believe that adding a new member will not break existing clients.</span></span> <span data-ttu-id="1618f-148">如果不确定所有客户端是否都能处理宽松版本管理，则建议使用严格版本管理准则，并将数据协定视为不可变。</span><span class="sxs-lookup"><span data-stu-id="1618f-148">If you are unsure that all clients can handle lax versioning, the recommendation is to use the strict versioning guidelines and treat data contracts as immutable.</span></span>  
  
 <span data-ttu-id="1618f-149">有关数据协定的宽松和严格版本控制的详细指南，请参阅 [最佳做法：数据协定版本控制](best-practices-data-contract-versioning.md)。</span><span class="sxs-lookup"><span data-stu-id="1618f-149">For detailed guidelines for both lax and strict versioning of data contracts, see [Best Practices: Data Contract Versioning](best-practices-data-contract-versioning.md).</span></span>  
  
### <a name="distinguishing-between-data-contract-and-net-types"></a><span data-ttu-id="1618f-150">区分数据协定和 .NET 类型</span><span class="sxs-lookup"><span data-stu-id="1618f-150">Distinguishing Between Data Contract and .NET Types</span></span>  

 <span data-ttu-id="1618f-151">通过将 <xref:System.Runtime.Serialization.DataContractAttribute> 属性应用于类，.NET 类或结构可映射为数据协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-151">A .NET class or structure can be projected as a data contract by applying the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to the class.</span></span> <span data-ttu-id="1618f-152">.NET 类型与其数据协定映射二者完全不同。</span><span class="sxs-lookup"><span data-stu-id="1618f-152">The .NET type and its data contract projections are two distinct matters.</span></span> <span data-ttu-id="1618f-153">同一个数据协定映射可能有多个 .NET 类型。</span><span class="sxs-lookup"><span data-stu-id="1618f-153">It is possible to have multiple .NET types with the same data contract projection.</span></span> <span data-ttu-id="1618f-154">此区别尤其有益于允许在保留映射的数据协定的同时更改 .NET 类型，从而甚至在是严格意义上保持与现有客户端的兼容性。</span><span class="sxs-lookup"><span data-stu-id="1618f-154">This distinction is especially useful in allowing you to change the .NET type while maintaining the projected data contract, thereby maintaining compatibility with existing clients even in the strict sense of the word.</span></span> <span data-ttu-id="1618f-155">为了保持 .NET 类型与数据协定之间的这一区别，始终应该执行两项操作：</span><span class="sxs-lookup"><span data-stu-id="1618f-155">There are two things you should always do to maintain this distinction between .NET type and data contract:</span></span>  
  
- <span data-ttu-id="1618f-156">指定一个 <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> 和 <xref:System.Runtime.Serialization.DataContractAttribute.Namespace%2A>。</span><span class="sxs-lookup"><span data-stu-id="1618f-156">Specify a <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> and <xref:System.Runtime.Serialization.DataContractAttribute.Namespace%2A>.</span></span> <span data-ttu-id="1618f-157">应总是指定数据协定的名称和命名空间，以防止在协定中暴露 .NET 类型的名称和命名空间。</span><span class="sxs-lookup"><span data-stu-id="1618f-157">You should always specify the name and namespace of your data contract to prevent your .NET type’s name and namespace from being exposed in the contract.</span></span> <span data-ttu-id="1618f-158">这样，如果以后决定更改 .NET 命名空间或类型名称，数据协定将保持不变。</span><span class="sxs-lookup"><span data-stu-id="1618f-158">This way, if you decide later to change the .NET namespace or type name, your data contract remains the same.</span></span>  
  
- <span data-ttu-id="1618f-159">指定 <xref:System.Runtime.Serialization.DataMemberAttribute.Name%2A>。</span><span class="sxs-lookup"><span data-stu-id="1618f-159">Specify <xref:System.Runtime.Serialization.DataMemberAttribute.Name%2A>.</span></span> <span data-ttu-id="1618f-160">应总是指定数据成员的名称，以防止在协定中暴露 .NET 成员名称。</span><span class="sxs-lookup"><span data-stu-id="1618f-160">You should always specify the name of your data members to prevent your .NET member name from being exposed in the contract.</span></span> <span data-ttu-id="1618f-161">这样，如果以后决定更改成员的 .NET 名称，数据协定将保持不变。</span><span class="sxs-lookup"><span data-stu-id="1618f-161">This way, if you decide later to change the .NET name of the member, your data contract remains the same.</span></span>  
  
### <a name="changing-or-removing-members"></a><span data-ttu-id="1618f-162">更改或移除成员</span><span class="sxs-lookup"><span data-stu-id="1618f-162">Changing or Removing Members</span></span>  

 <span data-ttu-id="1618f-163">即使是在允许宽松版本管理的情况下，更改成员的名称或数据类型或者移除数据成员仍然是中断性更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-163">Changing the name or data type of a member, or removing data members is a breaking change even if lax versioning is allowed.</span></span> <span data-ttu-id="1618f-164">如果必须更改或移除，请创建新的数据协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-164">If this is necessary, create a new data contract.</span></span>  
  
 <span data-ttu-id="1618f-165">如果服务兼容性高度重要，可以考虑忽略代码中未使用的数据成员并将其保留原位。</span><span class="sxs-lookup"><span data-stu-id="1618f-165">If service compatibility is of high importance, you might consider ignoring unused data members in your code and leave them in place.</span></span> <span data-ttu-id="1618f-166">如果要将一个数据成员拆分成多个成员，则可以考虑将现有成员保留在原位，作为可为下级客户端（未升级到最新版本的客户端）执行所需的拆分和重新聚合的属性。</span><span class="sxs-lookup"><span data-stu-id="1618f-166">If you are splitting up a data member into multiple members, you might consider leaving the existing member in place as a property that can perform the required splitting and re-aggregation for down-level clients (clients that are not upgraded to the latest version).</span></span>  
  
 <span data-ttu-id="1618f-167">同样，对数据协定的名称或命名空间进行更改也是中断性更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-167">Similarly, changes to the data contract’s name or namespace are breaking changes.</span></span>  
  
### <a name="round-trips-of-unknown-data"></a><span data-ttu-id="1618f-168">未知数据的往返</span><span class="sxs-lookup"><span data-stu-id="1618f-168">Round-Trips of Unknown Data</span></span>  

 <span data-ttu-id="1618f-169">某些情况下，需要“往返”传递来自于新版本中添加的成员的未知数据。</span><span class="sxs-lookup"><span data-stu-id="1618f-169">In some scenarios, there is a need to "round-trip" unknown data that comes from members added in a new version.</span></span> <span data-ttu-id="1618f-170">例如，“versionNew”服务将数据与某些新添加的成员一起发送到“versionOld”客户端。</span><span class="sxs-lookup"><span data-stu-id="1618f-170">For example, a "versionNew" service sends data with some newly added members to a "versionOld" client.</span></span> <span data-ttu-id="1618f-171">客户端在处理该消息时将忽略新添加的成员，但会将相同的数据（包括新添加的成员）重新发送回 versionNew 服务。</span><span class="sxs-lookup"><span data-stu-id="1618f-171">The client ignores the newly added members when processing the message, but it resends that same data, including the newly added members, back to the versionNew service.</span></span> <span data-ttu-id="1618f-172">此现象的典型情况是数据更新，更新过程从服务检索数据，更改数据，然后将其返回。</span><span class="sxs-lookup"><span data-stu-id="1618f-172">The typical scenario for this is data updates where data is retrieved from the service, changed, and returned.</span></span>  
  
 <span data-ttu-id="1618f-173">若要对某一特定类型启用往返功能，该类型必须实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 接口。</span><span class="sxs-lookup"><span data-stu-id="1618f-173">To enable round-tripping for a particular type, the type must implement the <xref:System.Runtime.Serialization.IExtensibleDataObject> interface.</span></span> <span data-ttu-id="1618f-174">此接口包含一个属性 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A>，它将返回 <xref:System.Runtime.Serialization.ExtensionDataObject> 类型。</span><span class="sxs-lookup"><span data-stu-id="1618f-174">The interface contains one property, <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> that returns the <xref:System.Runtime.Serialization.ExtensionDataObject> type.</span></span> <span data-ttu-id="1618f-175">该属性用于存储未来版本的数据协定中对于当前版本未知的任何数据。</span><span class="sxs-lookup"><span data-stu-id="1618f-175">The property is used to store any data from future versions of the data contract that is unknown to the current version.</span></span> <span data-ttu-id="1618f-176">客户端无法处理这些数据，但在实例序列化的时候，<xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> 属性的内容将与数据协定成员的其余数据一起写入。</span><span class="sxs-lookup"><span data-stu-id="1618f-176">This data is opaque to the client, but when the instance is serialized, the content of the <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> property is written with the rest of the data contract members' data.</span></span>  
  
 <span data-ttu-id="1618f-177">建议所有类型都实现此接口以接纳新的未知未来成员。</span><span class="sxs-lookup"><span data-stu-id="1618f-177">It is recommended that all your types implement this interface to accommodate new and unknown future members.</span></span>  
  
### <a name="data-contract-libraries"></a><span data-ttu-id="1618f-178">数据协定库</span><span class="sxs-lookup"><span data-stu-id="1618f-178">Data Contract Libraries</span></span>  

 <span data-ttu-id="1618f-179">可以存在数据协定库，协定在这里发布到中心储存库，然后服务和类型实现者实现和公开来自于该储存库中的数据协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-179">There may be libraries of data contracts where a contract is published to a central repository, and service and type implementers implement and expose data contracts from that repository.</span></span> <span data-ttu-id="1618f-180">在此情况下，在将数据协定发布到储存库时，您无法控制谁将创建实现此协定的类型。</span><span class="sxs-lookup"><span data-stu-id="1618f-180">In that case, when you publish a data contract to the repository, you have no control over who creates types that implement it.</span></span> <span data-ttu-id="1618f-181">因此，在协定发布之后，就不能进行修改，这实际上是使协定不可变。</span><span class="sxs-lookup"><span data-stu-id="1618f-181">Thus, you cannot modify the contract once it is published, rendering it effectively immutable.</span></span>  
  
### <a name="when-using-the-xmlserializer"></a><span data-ttu-id="1618f-182">使用 XmlSerializer 的场合</span><span class="sxs-lookup"><span data-stu-id="1618f-182">When Using the XmlSerializer</span></span>  

 <span data-ttu-id="1618f-183">在使用 <xref:System.Xml.Serialization.XmlSerializer> 类时，同样的版本管理原则依然适用。</span><span class="sxs-lookup"><span data-stu-id="1618f-183">The same versioning principles apply when using the <xref:System.Xml.Serialization.XmlSerializer> class.</span></span> <span data-ttu-id="1618f-184">在需要严格版本管理时，请将数据协定视为不可变，并为新版本创建具有唯一限定名的新数据协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-184">When strict versioning is required, treat data contracts as immutable and create new data contracts with unique, qualified names for the new versions.</span></span> <span data-ttu-id="1618f-185">如果确定可以使用宽松版本管理，则可在新版本中添加新的可序列化成员，但不能更改或移除现有成员。</span><span class="sxs-lookup"><span data-stu-id="1618f-185">When you are sure that lax versioning can be used, you can add new serializable members in new versions but not change or remove existing members.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1618f-186"><xref:System.Xml.Serialization.XmlSerializer> 使用 <xref:System.Xml.Serialization.XmlAnyElementAttribute> 和 <xref:System.Xml.Serialization.XmlAnyAttributeAttribute> 属性来支持未知数据的往返。</span><span class="sxs-lookup"><span data-stu-id="1618f-186">The <xref:System.Xml.Serialization.XmlSerializer> uses the <xref:System.Xml.Serialization.XmlAnyElementAttribute> and <xref:System.Xml.Serialization.XmlAnyAttributeAttribute> attributes to support round-tripping of unknown data.</span></span>  
  
## <a name="message-contract-versioning"></a><span data-ttu-id="1618f-187">消息协定版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-187">Message Contract Versioning</span></span>  

 <span data-ttu-id="1618f-188">消息协定版本管理的准则非常类似于数据协定的版本管理。</span><span class="sxs-lookup"><span data-stu-id="1618f-188">The guidelines for message contract versioning are very similar to versioning data contracts.</span></span> <span data-ttu-id="1618f-189">如果需要严格版本管理，则不应更改消息主体，而是应该创建具有唯一限定名的新消息协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-189">If strict versioning is required, you should not change your message body but instead create a new message contract with a unique qualified name.</span></span> <span data-ttu-id="1618f-190">如果确定可以使用宽松版本管理，则可添加新的消息主体部件，但不能更改或移除现有部件。</span><span class="sxs-lookup"><span data-stu-id="1618f-190">If you know that you can use lax versioning, you can add new message body parts but not change or remove existing ones.</span></span> <span data-ttu-id="1618f-191">此准则同时适用于裸消息协定和包装消息协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-191">This guidance applies both to bare and wrapped message contracts.</span></span>  
  
 <span data-ttu-id="1618f-192">总是可以添加消息头，即使是使用了严格版本管理。</span><span class="sxs-lookup"><span data-stu-id="1618f-192">Message headers can always be added, even if strict versioning is in use.</span></span> <span data-ttu-id="1618f-193">MustUnderstand 标志可能影响版本管理。</span><span class="sxs-lookup"><span data-stu-id="1618f-193">The MustUnderstand flag may affect versioning.</span></span> <span data-ttu-id="1618f-194">一般而言，WCF 中标头的版本控制模型如 SOAP 规范中所述。</span><span class="sxs-lookup"><span data-stu-id="1618f-194">In general, the versioning model for headers in WCF is as described in the SOAP specification.</span></span>  
  
## <a name="service-contract-versioning"></a><span data-ttu-id="1618f-195">服务协定版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-195">Service Contract Versioning</span></span>  

 <span data-ttu-id="1618f-196">与数据协定版本管理相似，服务协定版本管理也涉及添加、更改和移除操作。</span><span class="sxs-lookup"><span data-stu-id="1618f-196">Similar to data contract versioning, service contract versioning also involves adding, changing, and removing operations.</span></span>  
  
### <a name="specifying-name-namespace-and-action"></a><span data-ttu-id="1618f-197">指定名称、命名空间和动作</span><span class="sxs-lookup"><span data-stu-id="1618f-197">Specifying Name, Namespace, and Action</span></span>  

 <span data-ttu-id="1618f-198">默认情况下，服务协定的名称就是接口的名称。</span><span class="sxs-lookup"><span data-stu-id="1618f-198">By default, the name of a service contract is the name of the interface.</span></span> <span data-ttu-id="1618f-199">其默认命名空间为 " http://tempuri.org "，每个操作的操作为 " http://tempuri.org/contractname/methodname "。</span><span class="sxs-lookup"><span data-stu-id="1618f-199">Its default namespace is "http://tempuri.org", and each operation’s action is "http://tempuri.org/contractname/methodname".</span></span> <span data-ttu-id="1618f-200">建议为服务协定显式指定一个名称和命名空间，并为每个操作显式指定一个操作，以避免使用 " http://tempuri.org " 并防止接口和方法名称在服务的协定中公开。</span><span class="sxs-lookup"><span data-stu-id="1618f-200">It is recommended that you explicitly specify a name and namespace for the service contract, and an action for each operation to avoid using "http://tempuri.org" and to prevent interface and method names from being exposed in the service’s contract.</span></span>  
  
### <a name="adding-parameters-and-operations"></a><span data-ttu-id="1618f-201">添加参数和操作</span><span class="sxs-lookup"><span data-stu-id="1618f-201">Adding Parameters and Operations</span></span>  

 <span data-ttu-id="1618f-202">添加服务公开的服务操作是非中断性更改，因为现有客户端不需要考虑这些新操作。</span><span class="sxs-lookup"><span data-stu-id="1618f-202">Adding service operations exposed by the service is a nonbreaking change because existing clients need not be concerned about those new operations.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1618f-203">向双工回调协定添加操作是中断性更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-203">Adding operations to a duplex callback contract is a breaking change.</span></span>  
  
### <a name="changing-operation-parameter-or-return-types"></a><span data-ttu-id="1618f-204">更改操作参数或返回类型</span><span class="sxs-lookup"><span data-stu-id="1618f-204">Changing Operation Parameter or Return Types</span></span>  

 <span data-ttu-id="1618f-205">更改参数或返回类型通常是中断性更改，除非新旧类型实现了相同的数据协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-205">Changing parameter or return types generally is a breaking change unless the new type implements the same data contract implemented by the old type.</span></span> <span data-ttu-id="1618f-206">若要进行这样的更改，请向服务协定添加新操作，或者定义新的服务协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-206">To make such a change, add a new operation to the service contract or define a new service contract.</span></span>  
  
### <a name="removing-operations"></a><span data-ttu-id="1618f-207">移除操作</span><span class="sxs-lookup"><span data-stu-id="1618f-207">Removing Operations</span></span>  

 <span data-ttu-id="1618f-208">移除操作也是中断性更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-208">Removing operations is also a breaking change.</span></span> <span data-ttu-id="1618f-209">若要进行这样的更改，请定义一个新的服务协定，并在新的终结点上公开该协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-209">To make such a change, define a new service contract and expose it on a new endpoint.</span></span>  
  
### <a name="fault-contracts"></a><span data-ttu-id="1618f-210">错误协定</span><span class="sxs-lookup"><span data-stu-id="1618f-210">Fault Contracts</span></span>  

 <span data-ttu-id="1618f-211"><xref:System.ServiceModel.FaultContractAttribute> 属性使得服务协定开发人员能够指定有关可从协定的操作返回的错误的消息。</span><span class="sxs-lookup"><span data-stu-id="1618f-211">The <xref:System.ServiceModel.FaultContractAttribute> attribute enables a service contract developer to specify information about faults that can be returned from the contract's operations.</span></span>  
  
 <span data-ttu-id="1618f-212">服务的协定中所描述的错误列表并非详尽无遗。</span><span class="sxs-lookup"><span data-stu-id="1618f-212">The list of faults described in a service's contract is not considered exhaustive.</span></span> <span data-ttu-id="1618f-213">操作可能随时返回其协定中未描述的错误。</span><span class="sxs-lookup"><span data-stu-id="1618f-213">At any time, an operation may return faults that are not described in its contract.</span></span> <span data-ttu-id="1618f-214">因此，更改协定中描述的错误集合不会被视为中断性更改。</span><span class="sxs-lookup"><span data-stu-id="1618f-214">Therefore changing the set of faults described in the contract is not considered breaking.</span></span> <span data-ttu-id="1618f-215">例如，使用 <xref:System.ServiceModel.FaultContractAttribute> 向协定添加新的错误，或者从协定中移除现有错误。</span><span class="sxs-lookup"><span data-stu-id="1618f-215">For example, adding a new fault to the contract using the <xref:System.ServiceModel.FaultContractAttribute> or removing an existing fault from the contract.</span></span>  
  
### <a name="service-contract-libraries"></a><span data-ttu-id="1618f-216">服务协定库</span><span class="sxs-lookup"><span data-stu-id="1618f-216">Service Contract Libraries</span></span>  

 <span data-ttu-id="1618f-217">组织可以有协定库，协定在这里发布到中心储存库，然后服务实现者从该储存库实现协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-217">Organizations may have libraries of contracts where a contract is published to a central repository and service implementers implement contracts from that repository.</span></span> <span data-ttu-id="1618f-218">在此情况下，在将服务协定发布到储存库时，您无法控制谁将创建实现此协定的服务。</span><span class="sxs-lookup"><span data-stu-id="1618f-218">In this case, when you publish a service contract to the repository you have no control over who creates services that implement it.</span></span> <span data-ttu-id="1618f-219">因此，在服务协定发布之后，就不能进行修改，这实际上是使协定不可变。</span><span class="sxs-lookup"><span data-stu-id="1618f-219">Therefore, you cannot modify the service contract once published, rendering it effectively immutable.</span></span> <span data-ttu-id="1618f-220">WCF 支持协定继承，该继承可用于创建新的协定来扩展现有的协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-220">WCF supports contract inheritance, which can be used to create a new contract that extends existing contracts.</span></span> <span data-ttu-id="1618f-221">若要使用此功能，请定义一个继承自旧服务协定接口的新服务协定接口，然后向新接口添加方法。</span><span class="sxs-lookup"><span data-stu-id="1618f-221">To use this feature, define a new service contract interface that inherits from the old service contract interface, then add methods to the new interface.</span></span> <span data-ttu-id="1618f-222">然后将实现旧协定的服务更改为实现新协定，并将“versionOld”终结点定义更改为使用新协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-222">You then change the service that implements the old contract to implement the new contract and change the "versionOld" endpoint definition to use the new contract.</span></span> <span data-ttu-id="1618f-223">对于“versionOld”客户端，终结点将仍然表现为公开“versionOld”协定；而对于“versionNew”客户端，终结点将表现为公开“versionNew”协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-223">To "versionOld" clients, the endpoint will continue to appear as exposing the "versionOld" contract; to "versionNew" clients, the endpoint will appear to expose the "versionNew" contract.</span></span>  
  
## <a name="address-and-binding-versioning"></a><span data-ttu-id="1618f-224">地址和绑定版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-224">Address and Binding Versioning</span></span>  

 <span data-ttu-id="1618f-225">对终结点地址和绑定的更改是中断性更改，除非客户端能够动态发现新的终结点地址或绑定。</span><span class="sxs-lookup"><span data-stu-id="1618f-225">Changes to endpoint address and binding are breaking changes unless clients are capable of dynamically discovering the new endpoint address or binding.</span></span> <span data-ttu-id="1618f-226">实现此功能的一种机制是使用通用发现、描述和集成 (UDDI) 注册表以及 UDDI 调用模式，在此机制下，客户端尝试与终结点进行通信，并在失败时查询已知的 UDDI 注册表，以获得当前终结点元数据。</span><span class="sxs-lookup"><span data-stu-id="1618f-226">One mechanism for implementing this capability is by using a Universal Discovery Description and Integration (UDDI) registry and the UDDI Invocation Pattern where a client attempts to communicate with an endpoint and, upon failure, queries a well-known UDDI registry for the current endpoint metadata.</span></span> <span data-ttu-id="1618f-227">然后，客户端使用这些元数据中的地址和绑定来与终结点进行通信。</span><span class="sxs-lookup"><span data-stu-id="1618f-227">The client then uses the address and binding from this metadata to communicate with the endpoint.</span></span> <span data-ttu-id="1618f-228">如果此通信成功，客户端将缓存这些地址和绑定信息以备将来使用。</span><span class="sxs-lookup"><span data-stu-id="1618f-228">If this communication succeeds, the client caches the address and binding information for future use.</span></span>  
  
## <a name="routing-service-and-versioning"></a><span data-ttu-id="1618f-229">路由服务和版本管理</span><span class="sxs-lookup"><span data-stu-id="1618f-229">Routing Service and Versioning</span></span>  

 <span data-ttu-id="1618f-230">如果对服务所做的更改是中断性更改，并且您需要同时运行该服务的两个或多个不同版本，则可使用 WCF 路由服务将消息路由到适当的服务实例。</span><span class="sxs-lookup"><span data-stu-id="1618f-230">If the changes made to a service are breaking changes and you need to have two or more different versions of a service running simultaneously you can use the WCF Routing Service to route messages to the appropriate service instance.</span></span> <span data-ttu-id="1618f-231">WCF 路由服务使用基于内容的路由，换句话说，该服务使用消息中的信息来确定将消息路由到何处。</span><span class="sxs-lookup"><span data-stu-id="1618f-231">The WCF Routing Service uses content-based routing, in other words, it uses information within the message to determine where to route the message.</span></span> <span data-ttu-id="1618f-232">有关 WCF 路由服务的详细信息，请参阅 [路由服务](./feature-details/routing-service.md)。</span><span class="sxs-lookup"><span data-stu-id="1618f-232">For more information about the WCF Routing Service see [Routing Service](./feature-details/routing-service.md).</span></span> <span data-ttu-id="1618f-233">有关如何使用 WCF 路由服务进行服务版本控制的示例，请参阅 [如何：服务版本控制](./feature-details/how-to-service-versioning.md)。</span><span class="sxs-lookup"><span data-stu-id="1618f-233">For an example of how to use the WCF Routing Service for service versioning see [How To: Service Versioning](./feature-details/how-to-service-versioning.md).</span></span>  
  
## <a name="appendix"></a><span data-ttu-id="1618f-234">附录</span><span class="sxs-lookup"><span data-stu-id="1618f-234">Appendix</span></span>  

 <span data-ttu-id="1618f-235">在需要严格版本管理时，通常的数据协定版本管理准则是将数据协定视为不可变，并在需要更改时创建新的协定。</span><span class="sxs-lookup"><span data-stu-id="1618f-235">The general data contract versioning guidance when strict versioning is needed is to treat data contracts as immutable and create new ones when changes are required.</span></span> <span data-ttu-id="1618f-236">对于每个新的数据协定，需要分别创建一个新类，因此需要一种机制来避免不得不获得按照旧数据协定类编写的现有代码，并按照新数据协定类重新编写代码。</span><span class="sxs-lookup"><span data-stu-id="1618f-236">A new class needs to be created for each new data contract, so a mechanism is needed to avoid having to take existing code that was written in terms of the old data contract class and rewrite it in terms of the new data contract class.</span></span>  
  
 <span data-ttu-id="1618f-237">这样的一种机制是使用接口来定义每个数据协定的成员，并按照这些接口，而不是实现这些接口的数据协定类来编写内部实现代码。</span><span class="sxs-lookup"><span data-stu-id="1618f-237">One such mechanism is to use interfaces to define the members of each data contract and write internal implementation code in terms of the interfaces rather than the data contract classes that implement the interfaces.</span></span> <span data-ttu-id="1618f-238">某个服务的版本 1 的以下代码显示了一个 `IPurchaseOrderV1` 接口和一个 `PurchaseOrderV1`：</span><span class="sxs-lookup"><span data-stu-id="1618f-238">The following code for version 1 of a service shows an `IPurchaseOrderV1` interface and a `PurchaseOrderV1`:</span></span>  
  
```csharp  
public interface IPurchaseOrderV1  
{  
    string OrderId { get; set; }  
    string CustomerId { get; set; }  
}  
  
[DataContract(  
Name = "PurchaseOrder",  
Namespace = "http://examples.microsoft.com/WCF/2005/10/PurchaseOrder")]  
public class PurchaseOrderV1 : IPurchaseOrderV1  
{  
    [DataMember(...)]  
    public string OrderId {...}  
    [DataMember(...)]  
    public string CustomerId {...}  
}  
```  
  
 <span data-ttu-id="1618f-239">该服务协定的操作将按照 `PurchaseOrderV1` 编写，而实际的业务逻辑将按照 `IPurchaseOrderV1` 编写。</span><span class="sxs-lookup"><span data-stu-id="1618f-239">While the service contract’s operations would be written in terms of `PurchaseOrderV1`, the actual business logic would be in terms of `IPurchaseOrderV1`.</span></span> <span data-ttu-id="1618f-240">然后，在版本 2 中，将有一个新的 `IPurchaseOrderV2` 接口和一个新的 `PurchaseOrderV2` 类，如下面代码中所示：</span><span class="sxs-lookup"><span data-stu-id="1618f-240">Then, in version 2, there would be a new `IPurchaseOrderV2` interface and a new `PurchaseOrderV2` class as shown in the following code:</span></span>  
  
```csharp
public interface IPurchaseOrderV2  
{  
    DateTime OrderDate { get; set; }  
}

[DataContract(
Name = "PurchaseOrder",  
Namespace = "http://examples.microsoft.com/WCF/2006/02/PurchaseOrder")]  
public class PurchaseOrderV2 : IPurchaseOrderV1, IPurchaseOrderV2  
{  
    [DataMember(...)]  
    public string OrderId {...}  
    [DataMember(...)]  
    public string CustomerId {...}  
    [DataMember(...)]  
    public DateTime OrderDate { ... }  
}  
```  
  
 <span data-ttu-id="1618f-241">该服务协定将更新为包含按照 `PurchaseOrderV2` 编写的新操作。</span><span class="sxs-lookup"><span data-stu-id="1618f-241">The service contract would be updated to include new operations that are written in terms of `PurchaseOrderV2`.</span></span> <span data-ttu-id="1618f-242">按照 `IPurchaseOrderV1` 编写的现有业务逻辑对于 `PurchaseOrderV2` 仍然可用，并且需要 `OrderDate` 属性的新业务逻辑将按照 `IPurchaseOrderV2` 编写。</span><span class="sxs-lookup"><span data-stu-id="1618f-242">Existing business logic written in terms of `IPurchaseOrderV1` would continue to work for `PurchaseOrderV2` and new business logic that needs the `OrderDate` property would be written in terms of `IPurchaseOrderV2`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1618f-243">请参阅</span><span class="sxs-lookup"><span data-stu-id="1618f-243">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractSerializer>
- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A>
- <xref:System.Runtime.Serialization.DataContractAttribute.Namespace%2A>
- <xref:System.Runtime.Serialization.DataMemberAttribute.Order%2A>
- <xref:System.Runtime.Serialization.DataMemberAttribute.IsRequired%2A>
- <xref:System.Runtime.Serialization.IExtensibleDataObject>
- <xref:System.Runtime.Serialization.ExtensionDataObject>
- <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A>
- <xref:System.Xml.Serialization.XmlSerializer>
- [<span data-ttu-id="1618f-244">数据协定等效性</span><span class="sxs-lookup"><span data-stu-id="1618f-244">Data Contract Equivalence</span></span>](./feature-details/data-contract-equivalence.md)
- [<span data-ttu-id="1618f-245">版本容错序列化回调</span><span class="sxs-lookup"><span data-stu-id="1618f-245">Version-Tolerant Serialization Callbacks</span></span>](./feature-details/version-tolerant-serialization-callbacks.md)
