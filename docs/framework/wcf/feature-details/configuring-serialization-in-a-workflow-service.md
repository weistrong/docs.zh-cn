---
description: 了解详细信息：配置工作流服务中的序列化
title: 配置工作流服务中的序列化
ms.date: 03/30/2017
ms.assetid: aa70b290-a2ee-4c3c-90ea-d0a7665096ae
ms.openlocfilehash: e268f82fc3c1f65086e3c6b112e481ad8abed070
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743234"
---
# <a name="configuring-serialization-in-a-workflow-service"></a><span data-ttu-id="d60eb-103">配置工作流服务中的序列化</span><span class="sxs-lookup"><span data-stu-id="d60eb-103">Configuring Serialization in a Workflow Service</span></span>

<span data-ttu-id="d60eb-104">工作流服务 Windows Communication Foundation (WCF) 服务，因此可以选择使用 <xref:System.Runtime.Serialization.DataContractSerializer> (默认) 或 <xref:System.Xml.Serialization.XmlSerializer> 。</span><span class="sxs-lookup"><span data-stu-id="d60eb-104">Workflow services are Windows Communication Foundation (WCF) services and so have the option of using either the <xref:System.Runtime.Serialization.DataContractSerializer> (the default) or the <xref:System.Xml.Serialization.XmlSerializer>.</span></span> <span data-ttu-id="d60eb-105">编写非工作流服务时，将在服务或操作协定上指定要使用的序列化程序的类型。</span><span class="sxs-lookup"><span data-stu-id="d60eb-105">When writing non-workflow services the type of serializer to use is specified on the service or operation contract.</span></span> <span data-ttu-id="d60eb-106">创建 WCF 工作流服务时，不在代码中指定这些协定，而是在运行时通过协定推理生成这些协定。</span><span class="sxs-lookup"><span data-stu-id="d60eb-106">When creating WCF workflow services you don’t specify these contracts in code, but rather they are generated at runtime by contract inference.</span></span> <span data-ttu-id="d60eb-107">有关协定推理的详细信息，请参阅  [在工作流中使用约定](using-contracts-in-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="d60eb-107">For more information about contract inference, see  [Using Contracts in Workflow](using-contracts-in-workflow.md).</span></span>  <span data-ttu-id="d60eb-108">序列化程序是使用 <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A> 属性指定的。</span><span class="sxs-lookup"><span data-stu-id="d60eb-108">The serializer is specified using the <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A> property.</span></span> <span data-ttu-id="d60eb-109">这可在设计器中进行设置，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="d60eb-109">This can be set in the designer as shown in the following illustration.</span></span>  
  
 ![在 "属性" 窗口中设置 SerializerOption 属性。](./media/configuring-serialization-in-a-workflow-service/setting-serializer-property.png)  
  
 <span data-ttu-id="d60eb-111">序列化程序也可在代码中进行设置，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="d60eb-111">The serializer can also be set in code as shown in the following example,</span></span>  
  
```csharp  
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
```  
  
  <span data-ttu-id="d60eb-112">也可在工作流服务上指定已知类型。</span><span class="sxs-lookup"><span data-stu-id="d60eb-112">Known types can be specified on Workflow services as well.</span></span> <span data-ttu-id="d60eb-113">有关已知类型的详细信息，请参阅 [数据协定已知类型](data-contract-known-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d60eb-113">For more information about Known Types, see [Data Contract Known Types](data-contract-known-types.md).</span></span> <span data-ttu-id="d60eb-114">可在设计器或代码中指定已知类型。</span><span class="sxs-lookup"><span data-stu-id="d60eb-114">Known types can be specified in the designer or in code.</span></span> <span data-ttu-id="d60eb-115">若要在设计器中指定已知类型，请在活动的 " **属性" 窗口** 中单击 "KnownTypes" 属性旁边的省略号按钮，如下 <xref:System.ServiceModel.Activities.Receive> 图所示。</span><span class="sxs-lookup"><span data-stu-id="d60eb-115">To specify known types in the designer, click the ellipsis button next to the KnownTypes property in the **Properties Window** for a <xref:System.ServiceModel.Activities.Receive> activity as shown in the following illustration.</span></span>
  
 !["KnownTypes 属性" 对话框的屏幕截图。](./media/configuring-serialization-in-a-workflow-service/known-types-properties.png)  
  
 <span data-ttu-id="d60eb-117">此时将显示 "类型集合编辑器"，可以在其中搜索和指定已知类型。</span><span class="sxs-lookup"><span data-stu-id="d60eb-117">This displays the Type Collections Editor that allows you to search for and specify known types.</span></span>  
  
 ![类型集合编辑器的屏幕截图。](./media/configuring-serialization-in-a-workflow-service/type-collection-editor.gif)  
  
 <span data-ttu-id="d60eb-119">单击 " **添加新类型** " 链接，然后使用下拉选择或搜索要添加到已知类型集合的类型。</span><span class="sxs-lookup"><span data-stu-id="d60eb-119">Click the **Add new type** link and use the drop down to select or search for a type to add to the known types collection.</span></span> <span data-ttu-id="d60eb-120">若要在代码中指定已知类型，请使用 <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A> 属性，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="d60eb-120">To specify known types in code use the <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A> property as shown in the following example.</span></span>  
  
```csharp
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
            approveExpense.KnownTypes.Add(typeof(Travel));  
            approveExpense.KnownTypes.Add(typeof(Meal));  
```
