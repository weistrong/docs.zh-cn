---
description: '了解有关以下内容的详细信息：如何：添加数据服务引用 (WCF Data Services) '
title: 如何：添加数据服务引用（WCF 数据服务）
ms.date: 08/24/2018
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 62c6f318-3ee1-433a-b7a3-efa234c3034c
ms.openlocfilehash: 907ad9a7dc3710a6e565de55c74a0d279d20e159
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99765745"
---
# <a name="how-to-add-a-data-service-reference-wcf-data-services"></a><span data-ttu-id="48eee-103">如何： (WCF Data Services 中添加数据服务引用) </span><span class="sxs-lookup"><span data-stu-id="48eee-103">How to: Add a data service reference (WCF Data Services)</span></span>

[!INCLUDE [wcf-deprecated](~/includes/wcf-deprecated.md)]

<span data-ttu-id="48eee-104">您可以使用 Visual Studio 中的 **添加服务引用** 对话框添加对 WCF Data Services 的引用。</span><span class="sxs-lookup"><span data-stu-id="48eee-104">You can use the **Add Service Reference** dialog in Visual Studio to add a reference to WCF Data Services.</span></span> <span data-ttu-id="48eee-105">这使您可以更轻松地在使用 Visual Studio 开发的客户端应用程序中访问数据服务。</span><span class="sxs-lookup"><span data-stu-id="48eee-105">This enables you to more easily access a data service in a client application that you develop in Visual Studio.</span></span> <span data-ttu-id="48eee-106">完成此过程后，会基于从数据服务获取的元数据生成数据类。</span><span class="sxs-lookup"><span data-stu-id="48eee-106">When you complete this procedure, data classes are generated based on metadata that is obtained from the data service.</span></span> <span data-ttu-id="48eee-107">有关详细信息，请参阅 [生成数据服务客户端库](generating-the-data-service-client-library-wcf-data-services.md)。</span><span class="sxs-lookup"><span data-stu-id="48eee-107">For more information, see [Generating the Data Service Client Library](generating-the-data-service-client-library-wcf-data-services.md).</span></span>

## <a name="add-a-data-service-reference"></a><span data-ttu-id="48eee-108">添加数据服务引用</span><span class="sxs-lookup"><span data-stu-id="48eee-108">Add a data service reference</span></span>

1. <span data-ttu-id="48eee-109">（可选）如果数据服务不是解决方案的一部分，且未运行，请启动数据服务，并记下数据服务的 URI。</span><span class="sxs-lookup"><span data-stu-id="48eee-109">(Optional) If the data service is not part of the solution and is not already running, start the data service and note the URI of the data service.</span></span>

2. <span data-ttu-id="48eee-110">在 Visual Studio 的 **解决方案资源管理器** 中，右键单击客户端项目，然后选择 "**添加**  >  **服务引用**"。</span><span class="sxs-lookup"><span data-stu-id="48eee-110">In Visual Studio, in **Solution Explorer**, right-click the client project and then select **Add** > **Service Reference**.</span></span>

3. <span data-ttu-id="48eee-111">如果数据服务是当前解决方案的一部分，请单击 " **发现**"。</span><span class="sxs-lookup"><span data-stu-id="48eee-111">If the data service is part of the current solution, click **Discover**.</span></span>

     <span data-ttu-id="48eee-112">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="48eee-112">-or-</span></span>

     <span data-ttu-id="48eee-113">在 " **地址** " 文本框中，键入数据服务的基 URL （例如）， `http://localhost:1234/Northwind.svc` 然后单击 " **开始**"。</span><span class="sxs-lookup"><span data-stu-id="48eee-113">In the **Address** text box, type the base URL of the data service, such as `http://localhost:1234/Northwind.svc`, and then click **Go**.</span></span>

4. <span data-ttu-id="48eee-114">选择“确定”。</span><span class="sxs-lookup"><span data-stu-id="48eee-114">Select **OK**.</span></span>

     <span data-ttu-id="48eee-115">一个新的代码文件，其中包含可以访问数据服务资源并与其交互的数据类将添加到该项目中。</span><span class="sxs-lookup"><span data-stu-id="48eee-115">A new code file that contains the data classes that can access and interact with data service resources is added to the project.</span></span>

## <a name="see-also"></a><span data-ttu-id="48eee-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="48eee-116">See also</span></span>

- [<span data-ttu-id="48eee-117">快速入门</span><span class="sxs-lookup"><span data-stu-id="48eee-117">Quickstart</span></span>](quickstart-wcf-data-services.md)
