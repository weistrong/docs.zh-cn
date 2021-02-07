---
description: 了解详细信息：如何：将模型和映射文件嵌入资源
title: 如何：创建模型及映射文件嵌入资源
ms.date: 03/30/2017
ms.assetid: 20dfae4d-e95a-4264-9540-f5ad23b462d3
ms.openlocfilehash: 373dfc2c93adfc510341ec0ea0487ad8962aa3e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697512"
---
# <a name="how-to-make-model-and-mapping-files-embedded-resources"></a><span data-ttu-id="89232-103">如何：创建模型及映射文件嵌入资源</span><span class="sxs-lookup"><span data-stu-id="89232-103">How to: Make Model and Mapping Files Embedded Resources</span></span>

<span data-ttu-id="89232-104">使用实体框架可以将模型和映射文件部署为应用程序的嵌入资源。</span><span class="sxs-lookup"><span data-stu-id="89232-104">The Entity Framework enables you to deploy model and mapping files as embedded resources of an application.</span></span> <span data-ttu-id="89232-105">包含嵌入模型和映射文件的程序集必须加载到实体连接所在的应用程序域中。</span><span class="sxs-lookup"><span data-stu-id="89232-105">The assembly with the embedded model and mapping files must be loaded in the same application domain as the entity connection.</span></span> <span data-ttu-id="89232-106">有关详细信息，请参阅 [连接字符串](connection-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="89232-106">For more information, see [Connection Strings](connection-strings.md).</span></span> <span data-ttu-id="89232-107">默认情况下，实体数据模型工具嵌入模型和映射文件。</span><span class="sxs-lookup"><span data-stu-id="89232-107">By default, the Entity Data Model tools embed the model and mapping files.</span></span> <span data-ttu-id="89232-108">手动定义模型和映射文件时，请使用此过程来确保将文件与实体框架的应用程序一起部署到嵌入的资源。</span><span class="sxs-lookup"><span data-stu-id="89232-108">When you manually define the model and mapping files, use this procedure to ensure that the files are deployed as embedded resources together with an Entity Framework application.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="89232-109">若要维护嵌入资源，每次修改模型和映射文件时都必须重复此过程。</span><span class="sxs-lookup"><span data-stu-id="89232-109">To maintain embedded resources, you must repeat this procedure whenever the model and mapping files are modified.</span></span>  
  
### <a name="to-embed-model-and-mapping-files"></a><span data-ttu-id="89232-110">嵌入模型和映射文件</span><span class="sxs-lookup"><span data-stu-id="89232-110">To embed model and mapping files</span></span>  
  
1. <span data-ttu-id="89232-111">在 **解决方案资源管理器** 中，选择概念 ( ") 文件。</span><span class="sxs-lookup"><span data-stu-id="89232-111">In **Solution Explorer**, select the conceptual (.csdl) file.</span></span>  
  
2. <span data-ttu-id="89232-112">在 " **属性** " 窗格中，将 " **生成操作** " 设置为 " **嵌入资源**"。</span><span class="sxs-lookup"><span data-stu-id="89232-112">In the **Properties** pane, set **Build Action** to **Embedded Resource**.</span></span>  
  
3. <span data-ttu-id="89232-113">对存储文件 (.ssdl) 和映射文件 (.msl) 重复步骤 1 和步骤 2。</span><span class="sxs-lookup"><span data-stu-id="89232-113">Repeat steps 1 and 2 for the storage (.ssdl) file and the mapping (.msl) file.</span></span>  
  
4. <span data-ttu-id="89232-114">在 **解决方案资源管理器** 中，双击 App.config 文件，然后根据 `Metadata` `connectionString` 以下格式之一修改属性中的参数：</span><span class="sxs-lookup"><span data-stu-id="89232-114">In **Solution Explorer**, double-click the App.config file and then modify the `Metadata` parameter in the `connectionString` attribute based on one of the following formats:</span></span>  
  
    - <span data-ttu-id="89232-115">`Metadata=` `res://<assemblyFullName>/<resourceName>;`</span><span class="sxs-lookup"><span data-stu-id="89232-115">`Metadata=` `res://<assemblyFullName>/<resourceName>;`</span></span>  
  
    - <span data-ttu-id="89232-116">`Metadata=` `res://*/<resourceName>;`</span><span class="sxs-lookup"><span data-stu-id="89232-116">`Metadata=` `res://*/<resourceName>;`</span></span>  
  
    - `Metadata=res://*;`  
  
     <span data-ttu-id="89232-117">有关详细信息，请参阅 [连接字符串](connection-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="89232-117">For more information, see [Connection Strings](connection-strings.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="89232-118">示例</span><span class="sxs-lookup"><span data-stu-id="89232-118">Example</span></span>  

 <span data-ttu-id="89232-119">下面的连接字符串引用 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)的嵌入模型和映射文件。</span><span class="sxs-lookup"><span data-stu-id="89232-119">The following connection string references embedded model and mapping files for the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks).</span></span> <span data-ttu-id="89232-120">该连接字符串存储在项目的 App.config 文件中。</span><span class="sxs-lookup"><span data-stu-id="89232-120">This connection string is stored in the project's App.config file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89232-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="89232-121">See also</span></span>

- [<span data-ttu-id="89232-122">建模和映射</span><span class="sxs-lookup"><span data-stu-id="89232-122">Modeling and Mapping</span></span>](modeling-and-mapping.md)
- [<span data-ttu-id="89232-123">如何：定义连接字符串</span><span class="sxs-lookup"><span data-stu-id="89232-123">How to: Define the Connection String</span></span>](how-to-define-the-connection-string.md)
- [<span data-ttu-id="89232-124">如何：生成 EntityConnection 连接字符串</span><span class="sxs-lookup"><span data-stu-id="89232-124">How to: Build an EntityConnection Connection String</span></span>](how-to-build-an-entityconnection-connection-string.md)
- <span data-ttu-id="89232-125">[ADO.NET 实体数据模型工具](/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="89232-125">[ADO.NET Entity Data Model Tools](/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span></span>
