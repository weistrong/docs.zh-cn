---
description: 了解详细信息：如何：创建 AJAX-Enabled WCF 服务和访问服务的 ASP.NET 客户端
title: 在 Visual Studio 中创建 AJAX-Enabled WCF 服务和 ASP.NET 客户端
ms.date: 08/17/2018
ms.assetid: 95012df8-2a66-420d-944a-8afab261013e
ms.openlocfilehash: 59b0cab9b28dd68b27529b5d880138cc283144a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780344"
---
# <a name="how-to-create-an-ajax-enabled-wcf-service-and-an-aspnet-client-that-accesses-the-service"></a><span data-ttu-id="8896e-103">如何：创建支持 AJAX 的 WCF 服务和访问该服务的 ASP.NET 客户端</span><span class="sxs-lookup"><span data-stu-id="8896e-103">How to: Create an AJAX-Enabled WCF Service and an ASP.NET Client that Accesses the Service</span></span>

<span data-ttu-id="8896e-104">本主题演示如何使用 Visual Studio 创建启用 AJAX 的 Windows Communication Foundation (WCF) 服务和访问服务的 ASP.NET 客户端。</span><span class="sxs-lookup"><span data-stu-id="8896e-104">This topic shows how to use Visual Studio to create an AJAX-enabled Windows Communication Foundation (WCF) service and an ASP.NET client that accesses the service.</span></span>

## <a name="create-an-aspnet-web-app"></a><span data-ttu-id="8896e-105">创建 ASP.NET Web 应用</span><span class="sxs-lookup"><span data-stu-id="8896e-105">Create an ASP.NET web app</span></span>

1. <span data-ttu-id="8896e-106">打开 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="8896e-106">Open Visual Studio.</span></span>

1. <span data-ttu-id="8896e-107">从 "**文件**" 菜单中选择 "**新建**  >  **项目**"</span><span class="sxs-lookup"><span data-stu-id="8896e-107">From the **File** menu, select **New** > **Project**</span></span>

1. <span data-ttu-id="8896e-108">在 "**新建项目**" 对话框中，展开 "**已安装** 的  >  **Visual c #**  >  **Web** " 类别，然后选择 " **ASP.NET Web 应用程序 ( .NET Framework)**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-108">In the **New Project** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select **ASP.NET Web Application (.NET Framework)**.</span></span>

1. <span data-ttu-id="8896e-109">将项目命名为 **SandwichServices** ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="8896e-109">Name the Project **SandwichServices** and click **OK**.</span></span>

1. <span data-ttu-id="8896e-110">在 " **新建 ASP.NET Web 应用程序** " 对话框中，选择 " **空** "，然后选择 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="8896e-110">In the **New ASP.NET Web Application** dialog, select **Empty** and then select **OK**.</span></span>

   ![Visual Studio 中的 ASP.NET web 应用类型对话框](./media/create-an-ajax-wcf-asp-net-client/new-asp-net-web-app-type.png)

## <a name="add-a-web-form"></a><span data-ttu-id="8896e-112">添加 web 窗体</span><span class="sxs-lookup"><span data-stu-id="8896e-112">Add a web form</span></span>

1. <span data-ttu-id="8896e-113">在 **解决方案资源管理器** 中右键单击 "SandwichServices" 项目，然后选择 "**添加**  >  **新项**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-113">Right-click the SandwichServices project in **Solution Explorer** and select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="8896e-114">在 "**添加新项**" 对话框中，展开 "**已安装** 的  >  **Visual c #**  >  **Web** " 类别，然后选择 " **Web 窗体**" 模板。</span><span class="sxs-lookup"><span data-stu-id="8896e-114">In the **Add New Item** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select the **Web Form** template.</span></span>

1. <span data-ttu-id="8896e-115">接受默认名称 " (**webform1.aspx** ") ，然后选择 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-115">Accept the default name (**WebForm1**), and then select **Add**.</span></span>

   <span data-ttu-id="8896e-116">*Webform1.aspx* 在 **源** 视图中打开。</span><span class="sxs-lookup"><span data-stu-id="8896e-116">*WebForm1.aspx* opens in **Source** view.</span></span>

1. <span data-ttu-id="8896e-117">在标记中添加以下标记 **\<body>** ：</span><span class="sxs-lookup"><span data-stu-id="8896e-117">Add the following markup inside the **\<body>** tags:</span></span>

   ```html
   <input type="button" value="Price of 3 sandwiches" onclick="Calculate()"/>
   <br />
   <span id="additionResult"></span>
   ```

## <a name="create-an-ajax-enabled-wcf-service"></a><span data-ttu-id="8896e-118">创建启用 AJAX 的 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="8896e-118">Create an AJAX-enabled WCF service</span></span>

1. <span data-ttu-id="8896e-119">在 **解决方案资源管理器** 中右键单击 "SandwichServices" 项目，然后选择 "**添加**  >  **新项**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-119">Right-click the SandwichServices project in **Solution Explorer** and select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="8896e-120">在 "**添加新项**" 对话框中，展开 "**已安装** 的  >  **Visual c #**  >  **Web** " 类别，然后选择 **WCF 服务 (启用 AJAX 的)** 模板。</span><span class="sxs-lookup"><span data-stu-id="8896e-120">In the **Add New Item** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select the **WCF Service (AJAX-enabled)** template.</span></span>

   ![WCF 服务 (Visual Studio 中启用 AJAX 的) 项模板](./media/create-an-ajax-wcf-asp-net-client/add-wcf-service.png)

1. <span data-ttu-id="8896e-122">将服务命名为 " **CostService** "，然后选择 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-122">Name the service **CostService** and then select **Add**.</span></span>

   <span data-ttu-id="8896e-123">*CostService.svc.cs* 在编辑器中打开。</span><span class="sxs-lookup"><span data-stu-id="8896e-123">*CostService.svc.cs* opens in the editor.</span></span>

1. <span data-ttu-id="8896e-124">在服务中实现该操作。</span><span class="sxs-lookup"><span data-stu-id="8896e-124">Implement the operation in the service.</span></span> <span data-ttu-id="8896e-125">将以下方法添加到 CostService 类，以计算数量三明治的成本：</span><span class="sxs-lookup"><span data-stu-id="8896e-125">Add the following method to the CostService class to calculate the cost of a quantity of sandwiches:</span></span>

    ```csharp
    [OperationContract]
    public double CostOfSandwiches(int quantity)
    {
        return 1.25 * quantity;
    }
    ```

## <a name="configure-the-client-to-access-the-service"></a><span data-ttu-id="8896e-126">配置客户端以访问服务</span><span class="sxs-lookup"><span data-stu-id="8896e-126">Configure the client to access the service</span></span>

1. <span data-ttu-id="8896e-127">打开 *webform1.aspx* 文件，然后选择 " **设计** " 视图。</span><span class="sxs-lookup"><span data-stu-id="8896e-127">Open the *WebForm1.aspx* file and select the **Design** view.</span></span>

2. <span data-ttu-id="8896e-128">从 " **视图** " 菜单中选择 **"工具箱**"。</span><span class="sxs-lookup"><span data-stu-id="8896e-128">From the **View** menu, select **Toolbox**.</span></span>

3. <span data-ttu-id="8896e-129">展开 " **AJAX 扩展** " 节点，将 **ScriptManager** 拖放到窗体上。</span><span class="sxs-lookup"><span data-stu-id="8896e-129">Expand the **AJAX Extensions** node and drag and drop a **ScriptManager** onto the form.</span></span>

4. <span data-ttu-id="8896e-130">返回到 **源** 视图，在标记之间添加以下代码， **\<ScriptManager>** 以指定 WCF 服务的路径：</span><span class="sxs-lookup"><span data-stu-id="8896e-130">Back in the **Source** view, add the following code between the **\<ScriptManager>** tags to specify the path to the WCF service:</span></span>

    ```xml
    <Services>
       <asp:ServiceReference Path="~/CostService.svc" />
    </Services>
    ```

5. <span data-ttu-id="8896e-131">添加 JavaScript 函数的代码 `Calculate()` 。</span><span class="sxs-lookup"><span data-stu-id="8896e-131">Add the code for the JavaScript function `Calculate()`.</span></span> <span data-ttu-id="8896e-132">将以下代码放置在 web 窗体的 **head** 部分：</span><span class="sxs-lookup"><span data-stu-id="8896e-132">Place the following code in the **head** section of the web form:</span></span>

    ```html
    <script type="text/javascript">

        function Calculate() {
            CostService.CostOfSandwiches(3, onSuccess);
        }

        function onSuccess(result) {
            var myres = $get("additionResult");
            myres.innerHTML = result;
        }

    </script>
    ```

   <span data-ttu-id="8896e-133">此代码将调用 CostService 的方法来计算三个三明治的价格，然后将结果显示在名为 **additionResult** 的范围内。</span><span class="sxs-lookup"><span data-stu-id="8896e-133">This code calls the method of CostService to calculate the price for three sandwiches, and then displays the result in the span called **additionResult**.</span></span>

## <a name="run-the-program"></a><span data-ttu-id="8896e-134">运行程序</span><span class="sxs-lookup"><span data-stu-id="8896e-134">Run the program</span></span>

<span data-ttu-id="8896e-135">请确保 *webform1.aspx* 具有焦点，然后按 " **启动** " 按钮以启动 web 客户端。</span><span class="sxs-lookup"><span data-stu-id="8896e-135">Make sure that *WebForm1.aspx* has focus, and then press **Start** button to launch the web client.</span></span> <span data-ttu-id="8896e-136">该按钮具有一个绿色三角形，并显示类似于 **IIS Express (Microsoft Edge)** 的内容。</span><span class="sxs-lookup"><span data-stu-id="8896e-136">The button has a green triangle and says something like **IIS Express (Microsoft Edge)**.</span></span> <span data-ttu-id="8896e-137">也可以按 <kbd>F5</kbd>。</span><span class="sxs-lookup"><span data-stu-id="8896e-137">Or, you can press <kbd>F5</kbd>.</span></span> <span data-ttu-id="8896e-138">单击 " **3 三明治** " 按钮的 "价格" 以生成 "3.75" 的预期输出。</span><span class="sxs-lookup"><span data-stu-id="8896e-138">Click the **Price of 3 sandwiches** button to generate the expected output of "3.75".</span></span>

## <a name="example"></a><span data-ttu-id="8896e-139">示例</span><span class="sxs-lookup"><span data-stu-id="8896e-139">Example</span></span>

<span data-ttu-id="8896e-140">下面是 *CostService.svc.cs* 文件中的完整代码：</span><span class="sxs-lookup"><span data-stu-id="8896e-140">The following is the full code in the *CostService.svc.cs* file:</span></span>

```csharp
using System.ServiceModel;
using System.ServiceModel.Activation;

namespace SandwichServices
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class CostService
    {
        [OperationContract]
        public double CostOfSandwiches(int quantity)
        {
            return 1.25 * quantity;
        }
    }
}
```

<span data-ttu-id="8896e-141">下面是 *webform1.aspx* 页的完整内容：</span><span class="sxs-lookup"><span data-stu-id="8896e-141">The following is the full contents of the *WebForm1.aspx* page:</span></span>

```aspx-csharp
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs" Inherits="SandwichServices.WebForm1" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <script type="text/javascript">

        function Calculate() {
            CostService.CostOfSandwiches(3, onSuccess);
        }

        function onSuccess(result) {
            var myres = $get("additionResult");
            myres.innerHTML = result;
        }

    </script>
</head>
<body>
    <form id="form1" runat="server">
        <div>
        </div>
        <asp:ScriptManager ID="ScriptManager1" runat="server">
            <Services>
                <asp:ServiceReference Path="~/CostService.svc" />
            </Services>
        </asp:ScriptManager>

        <input type="button" value="Price of 3 sandwiches" onclick="Calculate()" />
        <br />
        <span id="additionResult"></span>
    </form>
</body>
</html>
```
