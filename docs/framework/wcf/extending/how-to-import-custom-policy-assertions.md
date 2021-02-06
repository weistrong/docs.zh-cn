---
description: 了解详细信息：如何：导入自定义策略断言
title: 如何：导人自定义策略断言
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1f41d787-accb-4a10-bfc6-a807671d1581
ms.openlocfilehash: e9190a97ed7d2d369b8f9ddc3d7fec71daf1e54f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644328"
---
# <a name="how-to-import-custom-policy-assertions"></a><span data-ttu-id="01bf2-103">如何：导人自定义策略断言</span><span class="sxs-lookup"><span data-stu-id="01bf2-103">How to: Import Custom Policy Assertions</span></span>

<span data-ttu-id="01bf2-104">策略断言说明服务终结点的功能和要求。</span><span class="sxs-lookup"><span data-stu-id="01bf2-104">Policy assertions describe the capabilities and requirements of a service endpoint.</span></span>  <span data-ttu-id="01bf2-105">客户端应用程序可以在服务元数据中使用策略断言来配置客户端绑定或自定义服务终结点的服务协定。</span><span class="sxs-lookup"><span data-stu-id="01bf2-105">Client applications can use policy assertions in service metadata to configure the client binding or to customize the service contract for a service endpoint.</span></span>  
  
 <span data-ttu-id="01bf2-106">自定义策略断言可通过实现 <xref:System.ServiceModel.Description.IPolicyImportExtension?displayProperty=nameWithType> 接口并将该对象传递给元数据系统或通过在应用程序配置文件中注册实现类型来导入。</span><span class="sxs-lookup"><span data-stu-id="01bf2-106">Custom policy assertions are imported by implementing the <xref:System.ServiceModel.Description.IPolicyImportExtension?displayProperty=nameWithType> interface and passing that object to the metadata system or by registering the implementation type in your application configuration file.</span></span>  <span data-ttu-id="01bf2-107">接口的实现 <xref:System.ServiceModel.Description.IPolicyImportExtension> 必须提供无参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="01bf2-107">Implementations of the <xref:System.ServiceModel.Description.IPolicyImportExtension> interface must provide a parameterless constructor.</span></span>  
  
### <a name="to-import-custom-policy-assertions"></a><span data-ttu-id="01bf2-108">导入自定义策略断言</span><span class="sxs-lookup"><span data-stu-id="01bf2-108">To import custom policy assertions</span></span>  
  
1. <span data-ttu-id="01bf2-109">在类上实现 <xref:System.ServiceModel.Description.IPolicyImportExtension?displayProperty=nameWithType> 接口。</span><span class="sxs-lookup"><span data-stu-id="01bf2-109">Implement the <xref:System.ServiceModel.Description.IPolicyImportExtension?displayProperty=nameWithType> interface on a class.</span></span> <span data-ttu-id="01bf2-110">请参见下面的过程。</span><span class="sxs-lookup"><span data-stu-id="01bf2-110">See the following procedures.</span></span>  
  
2. <span data-ttu-id="01bf2-111">通过以下方式之一插入自定义策略导入程序：</span><span class="sxs-lookup"><span data-stu-id="01bf2-111">Insert the custom policy importer either by:</span></span>  
  
3. <span data-ttu-id="01bf2-112">使用配置文件。</span><span class="sxs-lookup"><span data-stu-id="01bf2-112">Using a configuration file.</span></span> <span data-ttu-id="01bf2-113">请参见下面的过程。</span><span class="sxs-lookup"><span data-stu-id="01bf2-113">See the following procedures.</span></span>  
  
4. <span data-ttu-id="01bf2-114">将配置文件与配置的 [元数据实用工具工具一起使用 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md)。</span><span class="sxs-lookup"><span data-stu-id="01bf2-114">Using a configuration file with [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="01bf2-115">请参见下面的过程。</span><span class="sxs-lookup"><span data-stu-id="01bf2-115">See the following procedures.</span></span>  
  
5. <span data-ttu-id="01bf2-116">以编程方式插入策略导入程序。</span><span class="sxs-lookup"><span data-stu-id="01bf2-116">Programmatically inserting the policy importer.</span></span> <span data-ttu-id="01bf2-117">请参见下面的过程。</span><span class="sxs-lookup"><span data-stu-id="01bf2-117">See the following procedures.</span></span>  
  
### <a name="to-implement-the-systemservicemodeldescriptionipolicyimportextension-interface-on-any-class"></a><span data-ttu-id="01bf2-118">在任何类上实现 System.ServiceModel.Description.IPolicyImportExtension 接口</span><span class="sxs-lookup"><span data-stu-id="01bf2-118">To implement the System.ServiceModel.Description.IPolicyImportExtension interface on any class</span></span>  
  
1. <span data-ttu-id="01bf2-119">在 <xref:System.ServiceModel.Description.IPolicyImportExtension.ImportPolicy%2A?displayProperty=nameWithType> 方法中，对于感兴趣的每个策略主题，通过在传递给该方法的 <xref:System.ServiceModel.Description.PolicyConversionContext?displayProperty=nameWithType> 对象上调用相应方法（具体取决于所需的断言范围），查找要导入的策略断言。</span><span class="sxs-lookup"><span data-stu-id="01bf2-119">In the <xref:System.ServiceModel.Description.IPolicyImportExtension.ImportPolicy%2A?displayProperty=nameWithType> method, for each policy subject that you are interested in, find the policy assertions that you want to import by calling the appropriate method (depending upon the scope of the assertion that you want) on the <xref:System.ServiceModel.Description.PolicyConversionContext?displayProperty=nameWithType> object passed to the method.</span></span> <span data-ttu-id="01bf2-120">下面的代码示例演示如何使用 <xref:System.ServiceModel.Description.PolicyAssertionCollection.Remove%2A?displayProperty=nameWithType> 方法定位自定义策略断言并在一个步骤中将该断言从集合中删除。</span><span class="sxs-lookup"><span data-stu-id="01bf2-120">The following code example shows how to use the <xref:System.ServiceModel.Description.PolicyAssertionCollection.Remove%2A?displayProperty=nameWithType> method to locate the custom policy assertion and remove it from the collection in one step.</span></span> <span data-ttu-id="01bf2-121">如果使用删除方法定位并删除断言，则不必执行步骤 4。</span><span class="sxs-lookup"><span data-stu-id="01bf2-121">If you use the remove method to locate and remove the assertion, you do not have to perform step 4.</span></span>  
  
     [!code-csharp[CustomPolicySample#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/custompolicysample/cs/policyimporter.cs#9)]
     [!code-vb[CustomPolicySample#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/custompolicysample/vb/policyimporter.vb#9)]  
  
2. <span data-ttu-id="01bf2-122">处理策略断言。</span><span class="sxs-lookup"><span data-stu-id="01bf2-122">Process the policy assertions.</span></span> <span data-ttu-id="01bf2-123">请注意，策略系统不会标准化嵌入的策略和 `wsp:optional`。</span><span class="sxs-lookup"><span data-stu-id="01bf2-123">Note that the policy system does not normalize nested policies and `wsp:optional`.</span></span> <span data-ttu-id="01bf2-124">您必须在策略导入扩展实现中处理这些结构。</span><span class="sxs-lookup"><span data-stu-id="01bf2-124">You must process these constructs in your policy import extension implementation.</span></span>  
  
3. <span data-ttu-id="01bf2-125">对支持策略断言指定的功能或需求的绑定或协定执行自定义。</span><span class="sxs-lookup"><span data-stu-id="01bf2-125">Perform the customization to the binding or contract that supports the capability or requirement specified by the policy assertion.</span></span> <span data-ttu-id="01bf2-126">断言通常指示绑定需要特定配置或特定绑定元素。</span><span class="sxs-lookup"><span data-stu-id="01bf2-126">Typically assertions indicate that a binding requires a particular configuration or a specific binding element.</span></span> <span data-ttu-id="01bf2-127">可以通过访问 <xref:System.ServiceModel.Description.PolicyConversionContext.BindingElements%2A?displayProperty=nameWithType> 属性来进行这些修改。</span><span class="sxs-lookup"><span data-stu-id="01bf2-127">Make these modifications by accessing the <xref:System.ServiceModel.Description.PolicyConversionContext.BindingElements%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="01bf2-128">其他断言需要您修改协定。</span><span class="sxs-lookup"><span data-stu-id="01bf2-128">Other assertions require that you modify the contract.</span></span>  <span data-ttu-id="01bf2-129">可以使用 <xref:System.ServiceModel.Description.PolicyConversionContext.Contract%2A?displayProperty=nameWithType> 属性来访问并修改该协定。</span><span class="sxs-lookup"><span data-stu-id="01bf2-129">You can access and modify the contract using the <xref:System.ServiceModel.Description.PolicyConversionContext.Contract%2A?displayProperty=nameWithType> property.</span></span>  <span data-ttu-id="01bf2-130">请注意，对于同一个绑定和协定，可能会多次调用策略导入程序，但导入的是不同的替代策略（如果一个替代策略导入失败）。</span><span class="sxs-lookup"><span data-stu-id="01bf2-130">Note that your policy importer may get called multiple times for the same binding and contract, but different policy alternatives if importing a policy alternative fails.</span></span> <span data-ttu-id="01bf2-131">你的代码应该能够处理这一行为。</span><span class="sxs-lookup"><span data-stu-id="01bf2-131">Your code should be resilient to this behavior.</span></span>  
  
4. <span data-ttu-id="01bf2-132">从断言集合中删除自定义策略断言。</span><span class="sxs-lookup"><span data-stu-id="01bf2-132">Remove the custom policy assertion from the assertion collection.</span></span> <span data-ttu-id="01bf2-133">如果不删除断言 Windows Communication Foundation (WCF) 会假定策略导入不成功且不导入关联的绑定。</span><span class="sxs-lookup"><span data-stu-id="01bf2-133">If you do not remove the assertion Windows Communication Foundation (WCF) assumes that the policy import was unsuccessful and does not import the associated binding.</span></span> <span data-ttu-id="01bf2-134">如果您使用 <xref:System.ServiceModel.Description.PolicyAssertionCollection.Remove%2A?displayProperty=nameWithType> 方法定位自定义策略断言并在一个步骤中将该断言从集合中删除，则不必执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="01bf2-134">If you used the <xref:System.ServiceModel.Description.PolicyAssertionCollection.Remove%2A?displayProperty=nameWithType> method to locate the custom policy assertion and remove it from the collection in one step you do not have to perform this step.</span></span>  
  
### <a name="to-insert-the-custom-policy-importer-into-the-metadata-system-using-a-configuration-file"></a><span data-ttu-id="01bf2-135">使用配置文件将自定义策略导入程序插入到元数据系统</span><span class="sxs-lookup"><span data-stu-id="01bf2-135">To insert the custom policy importer into the metadata System using a configuration file</span></span>  
  
1. <span data-ttu-id="01bf2-136">将导入程序类型添加到 `<extensions>` [\<policyImporters>](../../configure-apps/file-schema/wcf/policyimporters.md) 客户端配置文件中元素内的元素中。</span><span class="sxs-lookup"><span data-stu-id="01bf2-136">Add the importer type to the `<extensions>` element inside the [\<policyImporters>](../../configure-apps/file-schema/wcf/policyimporters.md) element in the client configuration file.</span></span>  
  
     [!code-xml[CustomPolicySample#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/custompolicysample/cs/client.exe.config#7)]
  
2. <span data-ttu-id="01bf2-137">在客户端应用程序中，使用 <xref:System.ServiceModel.Description.MetadataResolver?displayProperty=nameWithType> 或 <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType> 解析元数据，这会自动调用导入程序。</span><span class="sxs-lookup"><span data-stu-id="01bf2-137">In the client application, use the <xref:System.ServiceModel.Description.MetadataResolver?displayProperty=nameWithType> or <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType> to resolve the metadata and the importer is invoked automatically.</span></span>  
  
     [!code-csharp[CustomPolicySample#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/custompolicysample/cs/client.cs#10)]
     [!code-vb[CustomPolicySample#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/custompolicysample/vb/client.vb#10)]  
  
### <a name="to-insert-the-custom-policy-importer-into-the-metadata-system-using-svcutilexe"></a><span data-ttu-id="01bf2-138">使用 Svcutil.exe 将自定义策略导入程序插入到元数据系统</span><span class="sxs-lookup"><span data-stu-id="01bf2-138">To insert the custom policy importer into the metadata system using Svcutil.exe</span></span>  
  
1. <span data-ttu-id="01bf2-139">将导入程序类型添加到 `<extensions>` [\<policyImporters>](../../configure-apps/file-schema/wcf/policyimporters.md) Svcutil.exe.config 配置文件中元素内的元素中。</span><span class="sxs-lookup"><span data-stu-id="01bf2-139">Add the importer type to the `<extensions>` element inside the [\<policyImporters>](../../configure-apps/file-schema/wcf/policyimporters.md) element in the Svcutil.exe.config configuration file.</span></span> <span data-ttu-id="01bf2-140">也可以通过使用 `/svcutilConfig` 选项指示 Svcutil.exe 加载在其他配置文件中注册的策略导入程序类型。</span><span class="sxs-lookup"><span data-stu-id="01bf2-140">You can also point Svcutil.exe to load policy importer types registered in a different configuration file by using the `/svcutilConfig` option.</span></span>  
  
2. <span data-ttu-id="01bf2-141">使用工作 [元数据实用工具工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 导入元数据，并自动调用导入程序。</span><span class="sxs-lookup"><span data-stu-id="01bf2-141">Use [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to import the metadata and the importer is invoked automatically.</span></span>  
  
### <a name="to-insert-the-custom-policy-importer-into-the-metadata-system-programmatically"></a><span data-ttu-id="01bf2-142">以编程方式将自定义策略导入程序插入到元数据系统</span><span class="sxs-lookup"><span data-stu-id="01bf2-142">To insert the custom policy importer into the metadata system programmatically</span></span>  
  
1. <span data-ttu-id="01bf2-143">导入元数据之前，将导入程序添加到 <xref:System.ServiceModel.Description.MetadataImporter.PolicyImportExtensions%2A?displayProperty=nameWithType> 属性（例如，如果您使用的是 <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType>）。</span><span class="sxs-lookup"><span data-stu-id="01bf2-143">Add the importer to the <xref:System.ServiceModel.Description.MetadataImporter.PolicyImportExtensions%2A?displayProperty=nameWithType> property (for example, if you are using the <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType>) prior to importing the metadata.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01bf2-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="01bf2-144">See also</span></span>

- <xref:System.ServiceModel.Description.MetadataResolver?displayProperty=nameWithType>
- <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType>
- <xref:System.ServiceModel.Description.MetadataResolver?displayProperty=nameWithType>
- [<span data-ttu-id="01bf2-145">扩展元数据系统</span><span class="sxs-lookup"><span data-stu-id="01bf2-145">Extending the Metadata System</span></span>](extending-the-metadata-system.md)
