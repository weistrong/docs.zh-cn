---
description: 了解详细信息： Internet Information Services (IIS) 服务器证书安装说明
title: Internet Information Services (IIS) 服务器证书安装说明
ms.date: 03/30/2017
ms.assetid: 11281490-d2ac-4324-8f33-e7714611a34b
ms.openlocfilehash: 1ac5209e9ff82911b0631c190e16ff457fea0db6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631848"
---
# <a name="internet-information-services-iis-server-certificate-installation-instructions"></a><span data-ttu-id="19ef9-103">Internet Information Services (IIS) 服务器证书安装说明</span><span class="sxs-lookup"><span data-stu-id="19ef9-103">Internet Information Services (IIS) Server Certificate Installation Instructions</span></span>

<span data-ttu-id="19ef9-104">若要运行可与 Internet 信息服务 (IIS) 安全通信的示例，您必须创建和安装服务器证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-104">To run the samples that securely communicate with Internet Information Services (IIS), you must create and install a server certificate.</span></span>  
  
## <a name="step-1-creating-certificates"></a><span data-ttu-id="19ef9-105">步骤 1。</span><span class="sxs-lookup"><span data-stu-id="19ef9-105">Step 1.</span></span> <span data-ttu-id="19ef9-106">创建证书</span><span class="sxs-lookup"><span data-stu-id="19ef9-106">Creating Certificates</span></span>  

 <span data-ttu-id="19ef9-107">若要为你的计算机创建证书，请使用管理员权限打开 Visual Studio 开发人员命令提示，并运行每个使用与 IIS 安全通信的示例中包含的 Setup.bat。</span><span class="sxs-lookup"><span data-stu-id="19ef9-107">To create a certificate for your computer, open a Developer Command Prompt for Visual Studio with administrator privileges and run the Setup.bat that is included in each of the samples that use secure communication with IIS.</span></span> <span data-ttu-id="19ef9-108">在运行此批处理文件之前，确保路径包括其中包含 Makecert.exe 的文件夹。</span><span class="sxs-lookup"><span data-stu-id="19ef9-108">Ensure that the path includes the folder that contains Makecert.exe before you run this batch file.</span></span> <span data-ttu-id="19ef9-109">以下命令用于在 Setup.bat 中创建证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-109">The following command is used to create the certificate in Setup.bat.</span></span>  
  
```console  
makecert -sr LocalMachine -ss My -n CN=ServiceModelSamples-HTTPS-Server -sky exchange -sk ServiceModelSamples-HTTPS-Key  
```  
  
## <a name="step-2-installing-certificates"></a><span data-ttu-id="19ef9-110">步骤 2.</span><span class="sxs-lookup"><span data-stu-id="19ef9-110">Step 2.</span></span> <span data-ttu-id="19ef9-111">安装证书</span><span class="sxs-lookup"><span data-stu-id="19ef9-111">Installing Certificates</span></span>  

 <span data-ttu-id="19ef9-112">安装刚刚创建的证书所需执行的步骤取决于您所使用的 IIS 版本。</span><span class="sxs-lookup"><span data-stu-id="19ef9-112">The steps required to install the certificates you just created depend on which version of IIS you are using.</span></span>  
  
#### <a name="to-install-iis-on-iis-51-windows-xp-and-iis-60-windows-server-2003"></a><span data-ttu-id="19ef9-113">在 IIS 5.1 (Windows XP) 和 IIS 6.0 (Windows Server 2003) 上安装 IIS</span><span class="sxs-lookup"><span data-stu-id="19ef9-113">To install IIS on IIS 5.1 (Windows XP) and IIS 6.0 (Windows Server 2003)</span></span>  
  
1. <span data-ttu-id="19ef9-114">打开 Internet 信息服务管理器 MMC 管理单元。</span><span class="sxs-lookup"><span data-stu-id="19ef9-114">Open the Internet Information Services Manager MMC Snap-In.</span></span>  
  
2. <span data-ttu-id="19ef9-115">右键单击 "默认网站"，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="19ef9-115">Right-click the default Web site and select **Properties**.</span></span>  
  
3. <span data-ttu-id="19ef9-116">选择 " **目录安全** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="19ef9-116">Select the **Directory Security** tab.</span></span>  
  
4. <span data-ttu-id="19ef9-117">单击 " **服务器证书** " 按钮。</span><span class="sxs-lookup"><span data-stu-id="19ef9-117">Click the **Server Certificate** button.</span></span> <span data-ttu-id="19ef9-118">Web 服务器证书向导将启动。</span><span class="sxs-lookup"><span data-stu-id="19ef9-118">The Web Server Certificate Wizard starts.</span></span>  
  
5. <span data-ttu-id="19ef9-119">完成向导。</span><span class="sxs-lookup"><span data-stu-id="19ef9-119">Complete the wizard.</span></span> <span data-ttu-id="19ef9-120">选择用于分配证书的选项。</span><span class="sxs-lookup"><span data-stu-id="19ef9-120">Select the option to assign a certificate.</span></span> <span data-ttu-id="19ef9-121">从显示的证书列表中选择 ServiceModelSamples-HTTPS-Server 证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-121">Select the ServiceModelSamples-HTTPS-Server certificate from the list of certificates that are displayed.</span></span>  
  
     <span data-ttu-id="19ef9-122">![IIS 证书向导](media/iiscertificate-wizard.GIF "IISCertificate_Wizard")</span><span class="sxs-lookup"><span data-stu-id="19ef9-122">![IIS Certificate Wizard](media/iiscertificate-wizard.GIF "IISCertificate_Wizard")</span></span>  
  
6. <span data-ttu-id="19ef9-123">使用 HTTPS 地址在浏览器中测试对服务的访问 `https://localhost/servicemodelsamples/service.svc` 。</span><span class="sxs-lookup"><span data-stu-id="19ef9-123">Test access to the service in a browser by using the HTTPS address `https://localhost/servicemodelsamples/service.svc`.</span></span>  
  
#### <a name="if-ssl-was-previously-configured-by-using-httpcfgexe"></a><span data-ttu-id="19ef9-124">如果以前使用 Httpcfg.exe 配置了 SSL</span><span class="sxs-lookup"><span data-stu-id="19ef9-124">If SSL was previously configured by using Httpcfg.exe</span></span>  
  
1. <span data-ttu-id="19ef9-125">使用 Makecert.exe（或运行 Setup.bat）创建服务器证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-125">Use Makecert.exe (or run Setup.bat) to create the server certificate.</span></span>  
  
2. <span data-ttu-id="19ef9-126">按照前面的步骤运行 IIS 管理器并安装证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-126">Run the IIS manager and install the certificate according to the previous steps.</span></span>  
  
3. <span data-ttu-id="19ef9-127">将以下代码行添加到客户端程序。</span><span class="sxs-lookup"><span data-stu-id="19ef9-127">Add the following line of code to the client program.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="19ef9-128">只有测试证书（比如通过 Makecert.exe 创建的那些证书）才需要此代码。</span><span class="sxs-lookup"><span data-stu-id="19ef9-128">This code is only required for test certificates such as those created by Makecert.exe.</span></span> <span data-ttu-id="19ef9-129">建议不要为成品代码执行此操作。</span><span class="sxs-lookup"><span data-stu-id="19ef9-129">It is not recommended for production code.</span></span>  
  
```csharp  
PermissiveCertificatePolicy.Enact("CN=ServiceModelSamples-HTTPS-Server");  
```  
  
#### <a name="to-install-iis-on-iis-70-windows-vista-and-windows-server-2008"></a><span data-ttu-id="19ef9-130">在 IIS 7.0（Windows Vista 和 Windows Server 2008）上安装 IIS</span><span class="sxs-lookup"><span data-stu-id="19ef9-130">To install IIS on IIS 7.0 (Windows Vista and Windows Server 2008)</span></span>  
  
1. <span data-ttu-id="19ef9-131">从 " **开始** " 菜单中，单击 " **运行**"，然后键入 **INETMGR** 以打开 IIS) MMC 管理单元 (的 Internet Information Services。</span><span class="sxs-lookup"><span data-stu-id="19ef9-131">From the **Start** menu, click **Run**, then type **inetmgr** to open the Internet Information Services (IIS) MMC snap-in.</span></span>  
  
2. <span data-ttu-id="19ef9-132">右键单击 "**默认** 网站"，然后选择 "**编辑绑定 ...** "</span><span class="sxs-lookup"><span data-stu-id="19ef9-132">Right-click the **Default Web Site** and select **Edit Bindings…**</span></span>  
  
3. <span data-ttu-id="19ef9-133">单击 "**网站绑定**" 对话框的 "**添加**" 按钮。</span><span class="sxs-lookup"><span data-stu-id="19ef9-133">Click the **Add** button of the **Site Bindings** dialog box.</span></span>  
  
4. <span data-ttu-id="19ef9-134">从 "**类型**" 下拉列表中选择 " **HTTPS** "。</span><span class="sxs-lookup"><span data-stu-id="19ef9-134">Select **HTTPS** from the **Type** drop-down list.</span></span>  
  
5. <span data-ttu-id="19ef9-135">从 " **SSL 证书**" 下拉列表中选择 " **ServiceModelSamples-HTTPS-服务器**"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="19ef9-135">Select the **ServiceModelSamples-HTTPS-Server** from the **SSL certificate** drop-down list and click **OK**.</span></span>  
  
6. <span data-ttu-id="19ef9-136">使用 HTTPS 地址在浏览器中测试对服务的访问 `https://localhost/servicemodelsamples/service.svc` 。</span><span class="sxs-lookup"><span data-stu-id="19ef9-136">Test access to the service in a browser by using the HTTPS address `https://localhost/servicemodelsamples/service.svc`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="19ef9-137">由于刚刚安装的测试证书不是受信任的证书，因此，在浏览用此证书保护的本地 Web 地址时，你可能会遇到其他 Internet Explorer 安全警告。</span><span class="sxs-lookup"><span data-stu-id="19ef9-137">Because the test certificate you have just installed is not a trusted certificate, you may encounter additional Internet Explorer security warnings when browsing to local Web addresses secured with this certificate.</span></span>  
  
## <a name="removing-certificates"></a><span data-ttu-id="19ef9-138">移除证书</span><span class="sxs-lookup"><span data-stu-id="19ef9-138">Removing Certificates</span></span>  
  
- <span data-ttu-id="19ef9-139">按照前面的指引使用 Internet Information Services 管理器，但要移除（而不是添加）证书或绑定。</span><span class="sxs-lookup"><span data-stu-id="19ef9-139">Use the Internet Information Services Manager as previously directed, but remove the certificate or binding instead of adding it.</span></span>  
  
- <span data-ttu-id="19ef9-140">使用以下命令移除计算机证书。</span><span class="sxs-lookup"><span data-stu-id="19ef9-140">Remove the computer certificate by using the following command.</span></span>  
  
    ```console  
    httpcfg delete ssl -i 0.0.0.0:443  
    ```
