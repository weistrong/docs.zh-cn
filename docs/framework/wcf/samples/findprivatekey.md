---
description: 了解详细信息： FindPrivateKey 示例
title: FindPrivateKey 示例
ms.date: 12/04/2017
helpviewer_keywords:
- FindPrivateKey
ms.assetid: 16b54116-0ceb-4413-af0c-753bb2a785a6
ms.openlocfilehash: 0e876aa3e1f6dde16acbb3ddd2a130ad49d369fc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732418"
---
# <a name="findprivatekey-sample"></a><span data-ttu-id="88dd7-103">FindPrivateKey 示例</span><span class="sxs-lookup"><span data-stu-id="88dd7-103">FindPrivateKey sample</span></span>

<span data-ttu-id="88dd7-104">查找与证书存储区中的特定 X.509 证书关联的私钥文件的位置和名称可能很困难。</span><span class="sxs-lookup"><span data-stu-id="88dd7-104">It can be difficult to find the location and name of the private key file associated with a specific X.509 certificate in the certificate store.</span></span> <span data-ttu-id="88dd7-105">使用 FindPrivateKey.exe 工具可以更快地完成此过程。</span><span class="sxs-lookup"><span data-stu-id="88dd7-105">The FindPrivateKey.exe tool facilitates this process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88dd7-106">FindPrivateKey 是一个需要在使用之前进行编译的样本。</span><span class="sxs-lookup"><span data-stu-id="88dd7-106">FindPrivateKey is a sample that needs to be compiled prior to use.</span></span> <span data-ttu-id="88dd7-107">有关如何生成 FindPrivateKey 工具的说明，请参阅 [生成 FindPrivateKey 项目](#to-build-the-findprivatekey-project) 部分。</span><span class="sxs-lookup"><span data-stu-id="88dd7-107">See the [To build the FindPrivateKey project](#to-build-the-findprivatekey-project) section for instructions on how to build the FindPrivateKey tool.</span></span>

<span data-ttu-id="88dd7-108">X.509 证书是由计算机管理员或计算机上的任何用户安装的。</span><span class="sxs-lookup"><span data-stu-id="88dd7-108">X.509 certificates are installed by an Administrator or any user in the machine.</span></span> <span data-ttu-id="88dd7-109">但是，证书可以通过在不同帐户下运行的服务进行访问。</span><span class="sxs-lookup"><span data-stu-id="88dd7-109">However, the certificate may be accessed by a service running under a different account.</span></span> <span data-ttu-id="88dd7-110">例如，NETWORK SERVICE 帐户。</span><span class="sxs-lookup"><span data-stu-id="88dd7-110">For example, the NETWORK SERVICE account.</span></span>

<span data-ttu-id="88dd7-111">此帐户可能没有访问私钥文件的权限，因为证书原来并不是由它安装的。</span><span class="sxs-lookup"><span data-stu-id="88dd7-111">This account may not have access to the private key file because the certificate was not installed by it originally.</span></span> <span data-ttu-id="88dd7-112">FindPrivateKey 工具可以为您提供给定 X.509 证书的私钥文件的位置。</span><span class="sxs-lookup"><span data-stu-id="88dd7-112">The FindPrivateKey tool gives you the location of a given X.509 Certificate's private key file.</span></span> <span data-ttu-id="88dd7-113">您可以在知道特定 X.509 证书的私钥文件的位置后立即添加或移除对此文件的权限。</span><span class="sxs-lookup"><span data-stu-id="88dd7-113">You can add permissions or remove permissions to this file once you know the location of the particular X.509 certificates' private key file.</span></span>

<span data-ttu-id="88dd7-114">使用证书进行安全的示例使用 *Setup.bat* 文件中的 FindPrivateKey 工具。</span><span class="sxs-lookup"><span data-stu-id="88dd7-114">The samples that use certificates for security use the FindPrivateKey tool in the *Setup.bat* file.</span></span> <span data-ttu-id="88dd7-115">找到私钥文件后，可以使用其他工具（如 *Cacls.exe* ）将适当的访问权限设置到该文件。</span><span class="sxs-lookup"><span data-stu-id="88dd7-115">Once the private key file has been found, you can use other tools such as *Cacls.exe* to set the appropriate access rights onto the file.</span></span>

<span data-ttu-id="88dd7-116">当在用户帐户下运行 Windows Communication Foundation (WCF) 服务（如自承载可执行文件）时，请确保用户帐户对文件具有只读访问权限。</span><span class="sxs-lookup"><span data-stu-id="88dd7-116">When running a Windows Communication Foundation (WCF) service under a user account, such as a self-hosted executable, ensure that the user account has read-only access to the file.</span></span> <span data-ttu-id="88dd7-117">Internet Information Services () IIS 下运行 WCF 服务时，服务运行的默认帐户是 IIS 7 和更早版本上的网络服务，或者 IIS 7.5 及更高版本上的应用程序池标识。</span><span class="sxs-lookup"><span data-stu-id="88dd7-117">When running a WCF service under Internet Information Services (IIS) the default accounts that the service runs under are the NETWORK SERVICE on IIS 7 and earlier versions, or Application Pool Identity on IIS 7.5 and later versions.</span></span> <span data-ttu-id="88dd7-118">有关详细信息，请参阅 [应用程序池标识](/iis/manage/configuring-security/application-pool-identities)。</span><span class="sxs-lookup"><span data-stu-id="88dd7-118">For more information, see [Application Pool Identities](/iis/manage/configuring-security/application-pool-identities).</span></span>

## <a name="examples"></a><span data-ttu-id="88dd7-119">示例</span><span class="sxs-lookup"><span data-stu-id="88dd7-119">Examples</span></span>

<span data-ttu-id="88dd7-120">在访问该进程没有读取权限的证书时，将看到类似于以下示例的异常消息：</span><span class="sxs-lookup"><span data-stu-id="88dd7-120">When accessing a certificate for which the process doesn't have read privilege, you see an exception message similar to the following example:</span></span>

```output
System.ArgumentException was unhandled
Message="The certificate 'CN=localhost' must have a private key that is capable of key exchange.  The process must have access rights for the private key."
Source="System.ServiceModel"
```

<span data-ttu-id="88dd7-121">出现这种情况时，请使用 FindPrivateKey 工具查找私钥文件，然后为运行服务的进程设置访问权限。</span><span class="sxs-lookup"><span data-stu-id="88dd7-121">When this occurs, use the FindPrivateKey tool to find the private key file, and then set the access right for the process that the service is running under.</span></span> <span data-ttu-id="88dd7-122">例如，可以通过 Cacls.exe 工具来完成此操作，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="88dd7-122">For example, this can be done with the Cacls.exe tool as shown in the following example:</span></span>

```console
cacls.exe "C:\Documents and Settings\All Users\Application Data\Microsoft\Crypto\RSA\MachineKeys\8aeda5eb81555f14f8f9960745b5a40d_38f7de48-5ee9-452d-8a5a-92789d7110b1" /E /G "NETWORK SERVICE":R
```

#### <a name="to-build-the-findprivatekey-project"></a><span data-ttu-id="88dd7-123">生成 FindPrivateKey 项目</span><span class="sxs-lookup"><span data-stu-id="88dd7-123">To build the FindPrivateKey project</span></span>

<span data-ttu-id="88dd7-124">若要下载此项目，请访问 [Windows Communication Foundation (WCF) ，并 Windows Workflow Foundation () 的 WF .NET Framework 示例](https://www.microsoft.com/download/details.aspx?id=21459)。</span><span class="sxs-lookup"><span data-stu-id="88dd7-124">To download the project, visit [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459).</span></span>

1. <span data-ttu-id="88dd7-125">打开文件资源管理器并导航到安装示例的目录位置下的 *WF_WCF_Samples \wcf\setup\findprivatekey\cs* "文件夹。</span><span class="sxs-lookup"><span data-stu-id="88dd7-125">Open File Explorer and navigate to the *WF_WCF_Samples\WCF\Setup\FindPrivateKey\CS* folder under the directory location where you installed the sample.</span></span>

2. <span data-ttu-id="88dd7-126">双击 .sln 文件图标，在 Visual Studio 中打开该文件。</span><span class="sxs-lookup"><span data-stu-id="88dd7-126">Double-click the .sln file icon to open the file in Visual Studio.</span></span>

3. <span data-ttu-id="88dd7-127">在 " **生成** " 菜单中，选择 " **重新生成解决方案**"。</span><span class="sxs-lookup"><span data-stu-id="88dd7-127">In the **Build** menu, select **Rebuild Solution**.</span></span>

4. <span data-ttu-id="88dd7-128">生成解决方案将生成如下文件：FindPrivateKey.exe。</span><span class="sxs-lookup"><span data-stu-id="88dd7-128">Building the solution generates the file: FindPrivateKey.exe.</span></span>

## <a name="conventionscommand-line-entries"></a><span data-ttu-id="88dd7-129">约定-命令行条目</span><span class="sxs-lookup"><span data-stu-id="88dd7-129">Conventions—Command-Line entries</span></span>

 <span data-ttu-id="88dd7-130">"[*选项*]" 代表一组可选参数。</span><span class="sxs-lookup"><span data-stu-id="88dd7-130">"[*option*]" represents an optional set of parameters.</span></span>

 <span data-ttu-id="88dd7-131">"{*option*}" 代表一组必需的参数。</span><span class="sxs-lookup"><span data-stu-id="88dd7-131">"{*option*}" represents a mandatory set of parameters.</span></span>

 <span data-ttu-id="88dd7-132">"*选项 1* &#124; *选项 2*" 表示在选项集之间选择。</span><span class="sxs-lookup"><span data-stu-id="88dd7-132">"*option1* &#124; *option2*" represents a choice between sets of options.</span></span>

 <span data-ttu-id="88dd7-133">" \<*value*> " 表示要输入的参数值。</span><span class="sxs-lookup"><span data-stu-id="88dd7-133">"\<*value*>" represents a parameter value to be entered.</span></span>

## <a name="usage"></a><span data-ttu-id="88dd7-134">使用情况</span><span class="sxs-lookup"><span data-stu-id="88dd7-134">Usage</span></span>

```console
FindPrivateKey <storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]
```

<span data-ttu-id="88dd7-135">其中：</span><span class="sxs-lookup"><span data-stu-id="88dd7-135">Where:</span></span>

| <span data-ttu-id="88dd7-136">参数</span><span class="sxs-lookup"><span data-stu-id="88dd7-136">Parameter</span></span>         | <span data-ttu-id="88dd7-137">说明</span><span class="sxs-lookup"><span data-stu-id="88dd7-137">Description</span></span>                                                                       |
|-----------------|-----------------------------------------------------------------------------------|
| `<subjectName>` | <span data-ttu-id="88dd7-138">证书的使用者名称</span><span class="sxs-lookup"><span data-stu-id="88dd7-138">The subject name of the certificate</span></span>                                               |
| `<thumbprint>`  | <span data-ttu-id="88dd7-139">证书的指纹 (你可以使用 Certmgr.exe 工具来查找此) </span><span class="sxs-lookup"><span data-stu-id="88dd7-139">The thumbprint of the certificate (You can use the Certmgr.exe tool to find this)</span></span> |
| `-f`            | <span data-ttu-id="88dd7-140">仅输出文件名</span><span class="sxs-lookup"><span data-stu-id="88dd7-140">output file name only</span></span>                                                             |
| `-d`            | <span data-ttu-id="88dd7-141">仅输出目录</span><span class="sxs-lookup"><span data-stu-id="88dd7-141">output directory only</span></span>                                                             |
| `-a`            | <span data-ttu-id="88dd7-142">输出绝对文件名</span><span class="sxs-lookup"><span data-stu-id="88dd7-142">output absolute file name</span></span>                                                         |

<span data-ttu-id="88dd7-143">如果未在命令提示符处指定任何参数，则会显示具有此信息的帮助文本。</span><span class="sxs-lookup"><span data-stu-id="88dd7-143">If no parameters are specified at the command prompt, then help text with this information is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="88dd7-144">示例</span><span class="sxs-lookup"><span data-stu-id="88dd7-144">Examples</span></span>

<span data-ttu-id="88dd7-145">此示例在当前用户的个人存储中查找使用者名称为 "CN = localhost" 的证书的文件名。</span><span class="sxs-lookup"><span data-stu-id="88dd7-145">This example finds the filename of the certificate with a subject name of "CN=localhost", in the Personal store of the Current User.</span></span>

```console
FindPrivateKey My CurrentUser -n "CN=localhost"
```

<span data-ttu-id="88dd7-146">此示例在当前用户的个人存储中查找使用者名称为 "CN = localhost" 的证书的文件名，并输出完整目录路径。</span><span class="sxs-lookup"><span data-stu-id="88dd7-146">This example finds the filename of the certificate with a subject name of "CN=localhost", in the Personal store of the Current User and output the full directory path.</span></span>

```console
FindPrivateKey My CurrentUser -n "CN=localhost" -a
```

<span data-ttu-id="88dd7-147">此示例在“本地计算机”的“个人”存储区中查找指纹为 "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" 的证书的文件名。</span><span class="sxs-lookup"><span data-stu-id="88dd7-147">This example finds the filename of the certificate with a thumbprint of "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52", in the Personal store of the Local Computer.</span></span>

```console
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52"
```
