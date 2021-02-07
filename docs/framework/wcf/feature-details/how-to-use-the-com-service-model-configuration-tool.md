---
description: 了解详细信息：如何：使用 COM + 服务模型配置工具
title: 如何：使用 COM+ 服务模型配置工具
ms.date: 03/30/2017
helpviewer_keywords:
- COM+ [WCF], using service model configuration tool
ms.assetid: 7e68cd8d-5fda-4641-b92f-290db874376e
ms.openlocfilehash: 2047604f327cd871629bbdac403e9acd816bbdb1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734082"
---
# <a name="how-to-use-the-com-service-model-configuration-tool"></a><span data-ttu-id="ed4c8-103">如何：使用 COM+ 服务模型配置工具</span><span class="sxs-lookup"><span data-stu-id="ed4c8-103">How to: Use the COM+ Service Model Configuration Tool</span></span>

<span data-ttu-id="ed4c8-104">在选择了适当的宿主模式之后，就可使用 COM+ 服务模型配置命令行工具 (ComSvcConfig.exe) 来配置将作为 Web 服务公开的应用程序接口。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-104">Once you have selected an appropriate hosting mode, use the COM+ Service Model Configuration command-line tool (ComSvcConfig.exe) to configure the application interfaces that will be exposed as Web services.</span></span>

> [!NOTE]
> <span data-ttu-id="ed4c8-105">你必须具有计算机上的管理员身份，才能执行下列各项任务。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-105">You must be an administrator on the machine to perform any of the following tasks.</span></span>

 <span data-ttu-id="ed4c8-106">在 Windows 7 计算机上使用 ComSvcConfig.exe 配置 Web 服务以使用最新服务模型版本（当前版本为 v4.5）时，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="ed4c8-106">When using ComSvcConfig.exe on a Windows 7 machine to configure a web service to use the latest service model version (currently v4.5), perform the following steps:</span></span>

1. <span data-ttu-id="ed4c8-107">将注册表项设置  `[HKEY_LOCAL_COMPUTER\SOFTWARE\Microsoft\.NETFramework]\OnlyUseLatestCLR` 为 DWORD 值0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed4c8-107">Set the registry key  `[HKEY_LOCAL_COMPUTER\SOFTWARE\Microsoft\.NETFramework]\OnlyUseLatestCLR` to a DWORD value of 0x00000001</span></span>

2. <span data-ttu-id="ed4c8-108">运行 comsvcconfig.exe</span><span class="sxs-lookup"><span data-stu-id="ed4c8-108">Run comsvcconfig.exe</span></span>

3. <span data-ttu-id="ed4c8-109">将步骤 1 中的注册表项还原到其原始值，或者在不存在原始值时将该注册表项删除。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-109">Revert the registry key added in step 1 back to its original value, or delete it if did not exist.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed4c8-110">还原此注册表项十分重要。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-110">Reverting this registry key is important.</span></span> <span data-ttu-id="ed4c8-111">这是一个兼容性注册表项。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-111">This is a compatibility key.</span></span> <span data-ttu-id="ed4c8-112">不还原此更改可能会造成在计算机上运行的其他 .NET 应用程序产生问题）</span><span class="sxs-lookup"><span data-stu-id="ed4c8-112">Not reverting this change may cause issues with other .NET applications running on the machine).</span></span>

> [!WARNING]
> <span data-ttu-id="ed4c8-113">在 Windows 8 计算机上使用 ComSvcConfig.exe/install 时，会显示一个对话框，其中显示 "你的电脑上的应用需要以下 Windows 功能： .NET Framework 3.5 (包括 .NET 2.0 和 .NET 3.0" （如果未安装 .NET Framework 3.5）。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-113">When using ComSvcConfig.exe  /install on a Windows 8 machine, a dialog is displayed stating "An app on your PC needs the following Windows feature: .NET Framework 3.5 (includes .NET 2.0 and .NET 3.0" if .NET Framework 3.5 is not installed.</span></span> <span data-ttu-id="ed4c8-114">可忽略此对话框。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-114">This dialog may be ignored.</span></span> <span data-ttu-id="ed4c8-115">或者，可以将 OnlyUseLatestCLR 注册表项设置为 DWORD 值 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ed4c8-115">Alternatively you can sed the OnlyUseLatestCLR registry key to a DWORD value of 0x00000001</span></span>

## <a name="add-an-interface-using-the-com-hosting-mode"></a><span data-ttu-id="ed4c8-116">使用 COM + 宿主模式添加接口</span><span class="sxs-lookup"><span data-stu-id="ed4c8-116">Add an interface using the COM+ hosting mode</span></span>

- <span data-ttu-id="ed4c8-117">使用 `/install` 和 `/hosting:complus` 选项运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-117">Run ComSvcConfig using the `/install` and `/hosting:complus` options, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /install /application:OnlineStore /contract:ItemOrders.Financial,IFinances /hosting:complus /verbose
    ```

     <span data-ttu-id="ed4c8-118">此命令将 `IFinances` 组件（它属于 OnlineStore COM+ 应用程序）的 `ItemOrders.IFinancial` 接口添加到将作为 Web 服务公开的接口集。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-118">The command adds the `IFinances` interface of the `ItemOrders.IFinancial` component (from the OnlineStore COM+ application) to the set of interfaces that will be exposed as Web services.</span></span> <span data-ttu-id="ed4c8-119">此服务使用 COM+ 宿主模式，因此要求显式激活应用程序。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-119">The service uses the COM+ hosting mode and therefore requires explicit application activation.</span></span>

     <span data-ttu-id="ed4c8-120">尽管通配符星号)  (\* 可用于组件和接口，但请避免使用它，因为你可能希望仅将选定的功能作为 Web 服务公开。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-120">While the wildcard asterisk (\*) character can be used for the component and the interface, avoid using it because you might want to expose only selected functionality as a Web service.</span></span> <span data-ttu-id="ed4c8-121">如果对此组件的将来版本运行命令，则使用通配符可能意外地公开在确定配置语法时尚不存在的接口。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-121">If run with a future version of this component, using the wildcard may unintentionally expose interfaces that may not have been present when the configuration syntax was determined.</span></span>

     <span data-ttu-id="ed4c8-122">/verbose 选项指示该工具除显示所有错误以外，还要显示警告。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-122">The /verbose option instructs the tool to display warnings in addition to any errors.</span></span>

     <span data-ttu-id="ed4c8-123">所公开的服务的协定将包含 `IFinances` 接口中的所有方法。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-123">The contract for the exposed service will contain all of the methods from the `IFinances` interface.</span></span>

## <a name="add-specific-methods-from-an-interface-using-the-com-hosting-mode"></a><span data-ttu-id="ed4c8-124">使用 COM + 宿主模式从接口添加特定方法</span><span class="sxs-lookup"><span data-stu-id="ed4c8-124">Add specific methods from an interface using the COM+ hosting mode</span></span>

- <span data-ttu-id="ed4c8-125">使用 `/install` 和 `/hosting:complus` 选项以及所需方法的显式命名运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-125">Run ComSvcConfig using the `/install` and `/hosting:complus` options with explicit naming of the required methods, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /install /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{Credit,Debit} /hosting:complus /verbose
    ```

     <span data-ttu-id="ed4c8-126">此命令仅将 `Credit` 接口中的 `Debit` 和 `IFinances` 方法作为操作添加到所公开的服务协定中。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-126">The command adds only the `Credit` and `Debit` methods from the `IFinances` interface as operations to the exposed service contract.</span></span> <span data-ttu-id="ed4c8-127">此接口中的其他所有方法将在协定中省略，并且无法从 Web 服务客户端调用。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-127">All other methods on the interface will be omitted from the contract and will not be callable from Web service clients.</span></span>

## <a name="add-an-interface-using-the-web-hosting-mode"></a><span data-ttu-id="ed4c8-128">使用 Web 宿主模式添加接口</span><span class="sxs-lookup"><span data-stu-id="ed4c8-128">Add an interface using the Web hosting mode</span></span>

- <span data-ttu-id="ed4c8-129">使用 `/install` 选项和 `/hosting:was` 选项运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-129">Run ComSvcConfig using the `/install` option and the `/hosting:was` option, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /install /application:OnlineWarehouse /contract:ItemInventory.Warehouse,IStockLevels /hosting:was /webDirectory:root/OnlineWarehouse /mex /verbose
    ```

     <span data-ttu-id="ed4c8-130">此命令将 `IStockLevels` 组件（它属于 OnlineWarehouse COM+ 应用程序）的 `ItemInventory.Warehouse` 接口添加到将作为 Web 服务公开的接口集。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-130">The command adds the `IStockLevels` interface on the `ItemInventory.Warehouse` component (from the OnlineWarehouse COM+ application) to the set of interfaces that will be exposed as Web services.</span></span> <span data-ttu-id="ed4c8-131">此服务以 Web 方式承载在 IIS 的 OnlineWarehouse 虚拟目录中，而不是承载在 COM+ 中，因此应用程序将根据需要自动激活。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-131">The service is Web hosted in the OnlineWarehouse virtual directory of IIS rather than in COM+, and thus the application is automatically activated as required.</span></span>

     <span data-ttu-id="ed4c8-132">若要使用 Web 承载的进程内配置，必须使用组件服务管理控制台将 COM+ 应用程序配置为作为库应用程序而不是服务器应用程序运行。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-132">To use the Web-hosted in-process configuration, the COM+ application must be configured to run as a Library application rather than a Server application using the Component Services administration console.</span></span> <span data-ttu-id="ed4c8-133">被配置为服务器应用程序的应用程序使用标准 Web 承载模式，并促使进程跃点处理每个请求。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-133">Applications configured as Server applications use the standard Web-hosted mode and incur a process hop to process each request.</span></span>

     <span data-ttu-id="ed4c8-134">`/mex` 选项用于添加其他元数据交换 (MEX) 服务终结点，它们与应用程序的服务终结点使用相同的传输协议，以支持要从服务中检索协定定义的客户端。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-134">The `/mex` option adds an additional Metadata Exchange (MEX) service endpoint that uses the same transport as the application's service endpoint to support clients that want to retrieve a contract definition from the service.</span></span>

## <a name="remove-a-web-service-for-a-specified-interface"></a><span data-ttu-id="ed4c8-135">删除指定接口的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="ed4c8-135">Remove a Web service for a specified interface</span></span>

- <span data-ttu-id="ed4c8-136">使用 `/uninstall` 选项运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-136">Run ComSvcConfig using the `/uninstall` option, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /uninstall /application:OnlineStore /contract:ItemOrders.Financial,IFinances /hosting:complus
    ```

     <span data-ttu-id="ed4c8-137">此命令将移除 `IFinances` 组件（它属于 OnlineStore COM+ 应用程序）上的 `ItemOrders.Financial` 接口。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-137">The command removes the `IFinances` interface on the `ItemOrders.Financial` component (from the OnlineStore COM+ application).</span></span>

## <a name="list-currently-exposed-interfaces"></a><span data-ttu-id="ed4c8-138">列出当前公开的接口</span><span class="sxs-lookup"><span data-stu-id="ed4c8-138">List currently exposed interfaces</span></span>

- <span data-ttu-id="ed4c8-139">使用 `/list` 选项运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-139">Run ComSvcConfig using the `/list` option, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /list
    ```

     <span data-ttu-id="ed4c8-140">此命令列出当前公开的接口以及相应的地址和绑定详细信息，范围局限于本地计算机。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-140">The command lists the currently exposed interfaces, along with the corresponding address and binding details, scoped to the local machine.</span></span>

## <a name="list-specific-currently-exposed-interfaces"></a><span data-ttu-id="ed4c8-141">列出特定的当前公开的接口</span><span class="sxs-lookup"><span data-stu-id="ed4c8-141">List specific currently exposed interfaces</span></span>

- <span data-ttu-id="ed4c8-142">使用 `/list` 选项运行 ComSvcConfig，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-142">Run ComSvcConfig using the `/list` option, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /list /application:OnlineStore /hosting:complus
    ```

     <span data-ttu-id="ed4c8-143">此命令列出当前公开的 COM+ 承载接口以及相应的地址和绑定详细信息，范围局限于本地计算机上的 OnlineStore COM+ 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-143">The command lists currently exposed COM+-hosted interfaces, along with the corresponding address and binding details, for the OnlineStore COM+ application on the local machine.</span></span>

## <a name="display-help-for-options"></a><span data-ttu-id="ed4c8-144">显示选项的帮助</span><span class="sxs-lookup"><span data-stu-id="ed4c8-144">Display help for options</span></span>

- <span data-ttu-id="ed4c8-145">使用 /? 选项运行 ComSvcConfig，</span><span class="sxs-lookup"><span data-stu-id="ed4c8-145">Run ComSvcConfig using the /?</span></span> <span data-ttu-id="ed4c8-146">如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="ed4c8-146">option, as shown in the following example.</span></span>

    ```console
    ComSvcConfig.exe /?
    ```

## <a name="see-also"></a><span data-ttu-id="ed4c8-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed4c8-147">See also</span></span>

- [<span data-ttu-id="ed4c8-148">与 COM + 应用程序集成概述</span><span class="sxs-lookup"><span data-stu-id="ed4c8-148">Integrating with COM+ Applications Overview</span></span>](integrating-with-com-plus-applications-overview.md)
