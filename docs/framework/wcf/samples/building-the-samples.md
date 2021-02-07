---
description: 了解详细信息：构建 Windows Communication Foundation 示例
title: 生成 Windows Communication Foundation 示例
ms.date: 03/30/2017
ms.assetid: 2899e7a5-9cb2-4e8d-b8d2-f31391549198
ms.openlocfilehash: a53073ac92369574b204dbce998bebb8844fce8d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704181"
---
# <a name="building-the-windows-communication-foundation-samples"></a><span data-ttu-id="cf666-103">生成 Windows Communication Foundation 示例</span><span class="sxs-lookup"><span data-stu-id="cf666-103">Building the Windows Communication Foundation Samples</span></span>

<span data-ttu-id="cf666-104">可使用 Visual Studio IDE 或从命令行使用 **msbuild** 命令生成 WCF) 示例 (Windows Communication Foundation。</span><span class="sxs-lookup"><span data-stu-id="cf666-104">The Windows Communication Foundation (WCF) samples can be built using the Visual Studio IDE or using the **msbuild** command from the command line.</span></span> <span data-ttu-id="cf666-105">本主题介绍这两个过程。</span><span class="sxs-lookup"><span data-stu-id="cf666-105">Both procedures are described in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="cf666-106">在生成或运行任何 WCF 示例之前，请确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="cf666-106">Before building or running any of the WCF samples, ensure you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

## <a name="to-build-the-sample-using-a-command-prompt"></a><span data-ttu-id="cf666-107">使用命令提示生成示例</span><span class="sxs-lookup"><span data-stu-id="cf666-107">To build the sample using a command prompt</span></span>

1. <span data-ttu-id="cf666-108">打开 Visual Studio 开发人员命令提示，并导航到安装示例的目录位置下语言特定的子目录。</span><span class="sxs-lookup"><span data-stu-id="cf666-108">Open Developer Command Prompt for Visual Studio and navigate to the language-specific subdirectory under the directory location where you installed the sample.</span></span>

2. <span data-ttu-id="cf666-109">`msbuild`在命令行中键入。</span><span class="sxs-lookup"><span data-stu-id="cf666-109">Type `msbuild` at the command line.</span></span> <span data-ttu-id="cf666-110">将为 *client\bin* 生成客户端程序文件，并将服务程序文件构建到 *service\bin* 中。</span><span class="sxs-lookup"><span data-stu-id="cf666-110">The client program files are built to *client\bin* and the service program files are built to *service\bin*.</span></span> <span data-ttu-id="cf666-111">如果服务由 Internet Information Services (IIS) 承载，则服务程序文件也会复制到 *servicemodelsamples* 目录及其 *\bin* 子目录中。</span><span class="sxs-lookup"><span data-stu-id="cf666-111">If the service is hosted by Internet Information Services (IIS), the service program files are also copied to the *servicemodelsamples* directory and its *\bin* subdirectory.</span></span>

> [!NOTE]
> <span data-ttu-id="cf666-112">必须在 *%systemdrive%\inetpub\wwwroot* 上设置 acl，才能向运行的帐户授予 "修改" 权限。</span><span class="sxs-lookup"><span data-stu-id="cf666-112">You must set the ACLs on *%systemdrive%\inetpub\wwwroot* to grant modify permissions to the account under which you are running.</span></span> <span data-ttu-id="cf666-113">否则，某些后期生成事件将失败。</span><span class="sxs-lookup"><span data-stu-id="cf666-113">Otherwise some post build events fail.</span></span> <span data-ttu-id="cf666-114">或者，您可以将 ACL 保留原样，而以管理员身份运行 SDK 命令提示。</span><span class="sxs-lookup"><span data-stu-id="cf666-114">Alternatively, you can leave the ACLs as they are and run the SDK command prompt as administrator.</span></span>

## <a name="to-build-the-sample-using-visual-studio"></a><span data-ttu-id="cf666-115">使用 Visual Studio 生成示例</span><span class="sxs-lookup"><span data-stu-id="cf666-115">To build the sample using Visual Studio</span></span>

1. <span data-ttu-id="cf666-116">在 Visual Studio 的 "**文件**" 菜单中，选择 "**打开**  >  **项目/解决方案**"。</span><span class="sxs-lookup"><span data-stu-id="cf666-116">From the **File** menu in Visual Studio, select **Open** > **Project/Solution**.</span></span> <span data-ttu-id="cf666-117">导航到安装示例的目录下特定于语言的子目录，然后双击 .sln 文件图标，在 Visual Studio 中打开该解决方案。</span><span class="sxs-lookup"><span data-stu-id="cf666-117">Navigate to the language-specific subdirectory under the directory in which you installed the sample, and double-click the .sln file icon to open the solution in Visual Studio.</span></span>

1. <span data-ttu-id="cf666-118">在 " **生成** " 菜单中，选择 " **重新生成解决方案**"。</span><span class="sxs-lookup"><span data-stu-id="cf666-118">From the **Build** menu, select **Rebuild Solution**.</span></span>

   <span data-ttu-id="cf666-119">客户端程序文件在 client\bin 中生成，服务程序文件在 service\bin 中生成。</span><span class="sxs-lookup"><span data-stu-id="cf666-119">The client program files are built to client\bin and the service program files are built to service\bin.</span></span> <span data-ttu-id="cf666-120">如果服务在 IIS 中承载，则服务程序文件也会复制到 *servicemodelsamples* 目录及其 *\bin* 子目录中。</span><span class="sxs-lookup"><span data-stu-id="cf666-120">If the service is hosted in IIS, the service program files are also copied to the *servicemodelsamples* directory and its *\bin* subdirectory.</span></span>

> [!NOTE]
> <span data-ttu-id="cf666-121">您必须在 %systemdrive%\inetpub\wwwroot 上设置 ACL，以便为您运行的帐户授予修改权限。</span><span class="sxs-lookup"><span data-stu-id="cf666-121">You must set the ACLs on %systemdrive%\inetpub\wwwroot to grant modify permissions to the account under which you are running.</span></span> <span data-ttu-id="cf666-122">否则，某些后期生成事件将失败。</span><span class="sxs-lookup"><span data-stu-id="cf666-122">Otherwise some post build events fail.</span></span> <span data-ttu-id="cf666-123">或者，您可以将 ACL 保留原样，而以管理员身份运行 SDK 命令提示或 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="cf666-123">Alternatively, you can leave the ACLs as they are and run the SDK command prompt or Visual Studio as administrator.</span></span> <span data-ttu-id="cf666-124">某些 Visual Studio 操作 (例如将调试程序附加到 ASP.NET 工作进程) 也需要管理权限。</span><span class="sxs-lookup"><span data-stu-id="cf666-124">Some Visual Studio actions (such as attaching a debugger to the ASP.NET worker process) also require administrative privileges.</span></span>

## <a name="setup-batch-files-and-scripts"></a><span data-ttu-id="cf666-125">设置批处理文件和脚本</span><span class="sxs-lookup"><span data-stu-id="cf666-125">Setup Batch Files and Scripts</span></span>

 <span data-ttu-id="cf666-126">Setup.exe 和 Cleanup.exe 批处理文件和脚本应从 Visual Studio 开发人员命令提示运行。</span><span class="sxs-lookup"><span data-stu-id="cf666-126">Setup.exe and Cleanup.exe batch files and scripts should be run from Developer Command Prompt for Visual Studio.</span></span> <span data-ttu-id="cf666-127">有几个设置和清理文件将执行需要具有管理特权的任务，应使用管理特权来启动它们。</span><span class="sxs-lookup"><span data-stu-id="cf666-127">Several set up and clean up files perform tasks that require administrative privileges and should be launched with administrator privileges.</span></span>

## <a name="important-security-information-about-metadata-endpoints"></a><span data-ttu-id="cf666-128">有关元数据终结点的重要安全信息</span><span class="sxs-lookup"><span data-stu-id="cf666-128">Important Security Information about Metadata Endpoints</span></span>

 <span data-ttu-id="cf666-129">为了避免无意中泄漏可能敏感的服务元数据，Windows Communication Foundation 的默认配置 (WCF) 服务将禁用元数据发布。</span><span class="sxs-lookup"><span data-stu-id="cf666-129">To prevent unintentional disclosure of potentially sensitive service metadata, the default configuration for Windows Communication Foundation (WCF) services disables metadata publishing.</span></span> <span data-ttu-id="cf666-130">默认情况下此行为是安全的，但也意味着你无法使用元数据导入工具（例如 Svcutil.exe）生成调用服务所需的客户端代码，除非在配置中显式启用服务的元数据发布行为。</span><span class="sxs-lookup"><span data-stu-id="cf666-130">This behavior is secure by default, but also means that you cannot use a metadata import tool (such as Svcutil.exe) to generate the client code required to call the service unless the service’s metadata publishing behavior is explicitly enabled in configuration.</span></span> <span data-ttu-id="cf666-131">为了使示例体验更简单，几乎所有示例都公开一个不安全的元数据发布终结点。</span><span class="sxs-lookup"><span data-stu-id="cf666-131">To make experimenting with the samples easier, almost all samples expose an unsecured metadata publishing endpoint.</span></span> <span data-ttu-id="cf666-132">此类终结点或许可以供未通过身份验证的匿名使用者使用，因此在部署此类终结点之前，必须谨慎以确保适合公开透露服务元数据。</span><span class="sxs-lookup"><span data-stu-id="cf666-132">Such endpoints are potentially available to anonymous unauthenticated consumers and care must be taken before deploying such endpoints to ensure that publicly disclosing a service’s metadata is appropriate.</span></span> <span data-ttu-id="cf666-133">有关发布服务元数据的详细信息，请参阅 [元数据发布行为](metadata-publishing-behavior.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="cf666-133">For more information about publishing service metadata, see the [Metadata Publishing Behavior](metadata-publishing-behavior.md) sample.</span></span> <span data-ttu-id="cf666-134">有关保护元数据终结点的示例，请参阅 [自定义安全元数据终结点](custom-secure-metadata-endpoint.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="cf666-134">See the [Custom Secure Metadata Endpoint](custom-secure-metadata-endpoint.md) sample for a sample securing a metadata endpoint.</span></span>

## <a name="exception-handling"></a><span data-ttu-id="cf666-135">异常处理</span><span class="sxs-lookup"><span data-stu-id="cf666-135">Exception Handling</span></span>

 <span data-ttu-id="cf666-136">一般来说，这些示例不包括异常处理，以使代码集中处理示例的主题。</span><span class="sxs-lookup"><span data-stu-id="cf666-136">Generally speaking these samples do not include exception handling to keep the code focused on the subject of the sample.</span></span> <span data-ttu-id="cf666-137">有关异常处理的详细信息，请参阅 [预期异常](expected-exceptions.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="cf666-137">For more information about exception handling, see the [Expected Exceptions](expected-exceptions.md) sample.</span></span>

## <a name="regenerating-clients-and-configuration-with-svcutil"></a><span data-ttu-id="cf666-138">使用 Svcutil 重新生成客户端和配置</span><span class="sxs-lookup"><span data-stu-id="cf666-138">Regenerating Clients and Configuration with Svcutil</span></span>

 <span data-ttu-id="cf666-139">您可以使用 "配置 [元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 为大多数示例重新生成客户端代码和配置。</span><span class="sxs-lookup"><span data-stu-id="cf666-139">You can use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to regenerate client code and configuration for most of the samples.</span></span> <span data-ttu-id="cf666-140">某些示例需要手动编辑的配置。</span><span class="sxs-lookup"><span data-stu-id="cf666-140">Some samples require manually edited configuration.</span></span> <span data-ttu-id="cf666-141">例如，如果您使用 Svcutil.exe 为某个使用客户端证书凭据的示例重新生成配置，必须手动指定之前配置的凭据。</span><span class="sxs-lookup"><span data-stu-id="cf666-141">For example, if you use Svcutil.exe to regenerate the configuration for a sample that uses client certificate credentials, you must manually specify the credentials previously configured.</span></span> <span data-ttu-id="cf666-142">某些示例使用特定的 Svcutil.exe 选项来影响生成的代码，这些选项在具体的示例主题中进行指定。</span><span class="sxs-lookup"><span data-stu-id="cf666-142">Some samples use specific Svcutil.exe options to affect the generated code, these options are specified in the specific sample topics.</span></span>

### <a name="to-regenerate-the-client-and-configuration-files"></a><span data-ttu-id="cf666-143">重新生成客户端和配置文件</span><span class="sxs-lookup"><span data-stu-id="cf666-143">To regenerate the client and configuration files</span></span>

1. <span data-ttu-id="cf666-144">打开 SDK 命令提示，然后定位到安装示例的目录位置下的语言特定的子目录。</span><span class="sxs-lookup"><span data-stu-id="cf666-144">Open an SDK command prompt and navigate to the language-specific subdirectory under the directory location where you installed the sample.</span></span>

2. <span data-ttu-id="cf666-145">如果服务是 Web 承载的类型，请使用以下命令。</span><span class="sxs-lookup"><span data-stu-id="cf666-145">If the service is a Web-hosted type, use the following command.</span></span>

    ```console
    svcutil.exe /n:"http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples" http://localhost/servicemodelsamples/service.svc/mex /out:generatedClient.cs
    ```

     <span data-ttu-id="cf666-146">如果服务是自承载类型，请键入以下命令。</span><span class="sxs-lookup"><span data-stu-id="cf666-146">If the service is a self-hosted type the following command.</span></span>

    ```console
    svcutil.exe /n:"http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples" http://localhost:8000/servicemodelsamples/service.svc/mex /out:generatedClient.cs
    ```

     <span data-ttu-id="cf666-147">替换 `http://localhost:8000/ServiceModelSamples/service.svc/mex` 为自承载服务的 mex 终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="cf666-147">Replace `http://localhost:8000/ServiceModelSamples/service.svc/mex` with the address of the self-hosted service's mex endpoint.</span></span>

     <span data-ttu-id="cf666-148">若要在 Visual Basic 类型中生成客户端，请使用以下命令。</span><span class="sxs-lookup"><span data-stu-id="cf666-148">To generate the client in a Visual Basic type, use the following command.</span></span>

    ```console
    svcutil.exe /n:"http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples" http://localhost/servicemodelsamples/service.svc/mex /l:vb /out:generatedClient.vb
    ```

     <span data-ttu-id="cf666-149">如果服务是自承载类型，请使用以下命令。</span><span class="sxs-lookup"><span data-stu-id="cf666-149">If the service is a self-hosted type, use the following command.</span></span>

    ```console
    svcutil.exe /n:"http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples" http://localhost:8000/servicemodelsamples/service.svc/mex /l:vb /out:generatedClient.vb
    ```

    > [!NOTE]
    > <span data-ttu-id="cf666-150">若要跳过客户端配置的生成，请添加 **/noConfig** 选项。</span><span class="sxs-lookup"><span data-stu-id="cf666-150">To skip the generation of client configuration add the **/noConfig** option.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf666-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="cf666-151">See also</span></span>

- [<span data-ttu-id="cf666-152">运行 Windows Communication Foundation 示例</span><span class="sxs-lookup"><span data-stu-id="cf666-152">Running the Windows Communication Foundation Samples</span></span>](running-the-samples.md)
- [<span data-ttu-id="cf666-153">ServiceModel 元数据实用工具 (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="cf666-153">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../servicemodel-metadata-utility-tool-svcutil-exe.md)
