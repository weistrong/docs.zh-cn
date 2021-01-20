---
title: 部署新式桌面应用程序
description: 部署新式桌面应用程序时需要了解的所有内容。
ms.date: 05/12/2020
ms.openlocfilehash: ba47f09b27adf270734bbfff285fe44dd4175d29
ms.sourcegitcommit: 632818f4b527e5bf3c48fc04e0c7f3b4bdb8a248
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "98615849"
---
# <a name="deploying-modern-desktop-applications"></a><span data-ttu-id="b79be-103">部署新式桌面应用程序</span><span class="sxs-lookup"><span data-stu-id="b79be-103">Deploying Modern Desktop Applications</span></span>

<span data-ttu-id="b79be-104">开发桌面应用程序时，要考虑的一个问题是如何将应用程序打包并部署到用户的计算机。</span><span class="sxs-lookup"><span data-stu-id="b79be-104">When you develop desktop applications, one thing to consider is how your application is going to be packaged and deployed to the users' machines.</span></span> <span data-ttu-id="b79be-105">打包、部署和安装的问题在于，它通常由 IT 专业人员负责，他们关心的不同方面与开发人员有关。</span><span class="sxs-lookup"><span data-stu-id="b79be-105">The problem with packaging, deployment, and installation is that it usually falls under the umbrella of the IT professionals, who care about different things than developers.</span></span>

<span data-ttu-id="b79be-106">如今，我们都熟悉了 DevOps 概念，开发人员和 IT 专业人员在其中密切合作，将应用程序移动到其生产环境中。</span><span class="sxs-lookup"><span data-stu-id="b79be-106">These days, we're all familiar with the DevOps concept, where developers and IT Pros work closely to move applications to their production environments.</span></span> <span data-ttu-id="b79be-107">但是，如果你已在桌面工作中经历了10年以上，你可能会看到以下情景。</span><span class="sxs-lookup"><span data-stu-id="b79be-107">But if you've been in the desktop battle for more than 10 years, you might have seen the following story.</span></span> <span data-ttu-id="b79be-108">开发人员团队共同工作，以满足项目截止时间。</span><span class="sxs-lookup"><span data-stu-id="b79be-108">A team of developers works together hard to meet the project deadlines.</span></span> <span data-ttu-id="b79be-109">业务人员紧张，因为他们需要系统在多个用户的计算机上工作才能运行公司。</span><span class="sxs-lookup"><span data-stu-id="b79be-109">Business people are nervous since they need the system working on many user's machines to run the company.</span></span> <span data-ttu-id="b79be-110">在 "D 天" 上，项目经理会对照每个开发人员进行检查，使其代码正常工作，并确保一切正常，使他们能够发货。</span><span class="sxs-lookup"><span data-stu-id="b79be-110">On "D-Day", the project manager checks with every developer that their code is working well and that everything is fine, so they can ship.</span></span> <span data-ttu-id="b79be-111">然后，包团队将生成应用程序的安装程序，将其分发给每个用户计算机和一组测试用户运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-111">Then, the package team comes in generating the setup for the app, distribute it to every user machine and a set of test users run the application.</span></span> <span data-ttu-id="b79be-112">嗯，它们会尝试，因为在显示任何 UI 之前，应用程序会引发一个异常，其中显示 "方法 ~ 对象 ~ 失败"。</span><span class="sxs-lookup"><span data-stu-id="b79be-112">Well, they try, because before showing any UI, the application throws an exception that says "Method ~ of object ~ failed".</span></span> <span data-ttu-id="b79be-113">紧急情况从空中开始流动，并进行短暂的调查，重点介绍引入了第三方控件的一个年轻人开发人员，这无疑是 "在开发计算机上工作"。</span><span class="sxs-lookup"><span data-stu-id="b79be-113">Panic starts flowing through the air and a brief investigation points to a young and tired developer that has introduced a third-party control, that certainly "worked on the dev machine".</span></span>

<span data-ttu-id="b79be-114">出于两个主要原因，安装桌面应用程序通常是一种痛苦：</span><span class="sxs-lookup"><span data-stu-id="b79be-114">Installing desktop applications have traditionally been a nightmare for two main reasons:</span></span>

- <span data-ttu-id="b79be-115">开发团队和 IT 团队之间缺少密切的协作文化。</span><span class="sxs-lookup"><span data-stu-id="b79be-115">Lack of close collaboration culture between dev and IT teams.</span></span>
- <span data-ttu-id="b79be-116">缺乏可靠的打包和部署技术，我们可以进行构建。</span><span class="sxs-lookup"><span data-stu-id="b79be-116">Lack of a solid packaging and deploying technology we can build upon.</span></span>

<span data-ttu-id="b79be-117">事实上，我们一直在生活，这是因为有时你后悔安装了应用，因为：</span><span class="sxs-lookup"><span data-stu-id="b79be-117">In fact, we've been living with the fact that sometimes you regret that you installed an app because:</span></span>

- <span data-ttu-id="b79be-118">它最终会在您的计算机上产生一些意外的副作用。</span><span class="sxs-lookup"><span data-stu-id="b79be-118">It ends up having some undesired side effects on your machine.</span></span>
- <span data-ttu-id="b79be-119">以前安装的某些应用程序将停止工作。</span><span class="sxs-lookup"><span data-stu-id="b79be-119">Some applications that were previously installed stop working.</span></span>

<span data-ttu-id="b79be-120">此外，不能通过卸载应用程序将系统还原到其原始状态。</span><span class="sxs-lookup"><span data-stu-id="b79be-120">Additionally, you can't just restore the system to its original state by uninstalling the app.</span></span> <span data-ttu-id="b79be-121">我们在这种情况下，我们已经梦寐以求了 "DLL Hell" 或 "Winrot" 等术语。</span><span class="sxs-lookup"><span data-stu-id="b79be-121">We're so used to live this situation that we've coined terms like "DLL Hell" or "Winrot".</span></span>

<span data-ttu-id="b79be-122">在本章中，我们将讨论 .MSIX。</span><span class="sxs-lookup"><span data-stu-id="b79be-122">In this chapter, we'll talk about MSIX.</span></span> <span data-ttu-id="b79be-123">.MSIX 是 Microsoft 的全新技术，它尝试充分利用以前的技术，为未来的打包技术提供坚实的基础。</span><span class="sxs-lookup"><span data-stu-id="b79be-123">MSIX is the brand-new technology from Microsoft that tries to capture the best of previous technologies to provide a solid foundation for the packaging technology of the future.</span></span>

<span data-ttu-id="b79be-124">打包技术与现代化有什么关系？</span><span class="sxs-lookup"><span data-stu-id="b79be-124">What does a packaging technology have to do with modernization?</span></span> <span data-ttu-id="b79be-125">事实证明，打包是企业 IT 的基本知识，其中投入了大量资金。</span><span class="sxs-lookup"><span data-stu-id="b79be-125">Well, it turns out that packaging is fundamental for the enterprise IT with lots of money invested there.</span></span> <span data-ttu-id="b79be-126">现代化并非仅与使用最新技术相关。</span><span class="sxs-lookup"><span data-stu-id="b79be-126">Modernization isn't only related to using the latest technologies.</span></span> <span data-ttu-id="b79be-127">在公司将功能交付给客户端之前，它还与缩短业务需求的上市时间有关。</span><span class="sxs-lookup"><span data-stu-id="b79be-127">It's also related to reducing time to market from the moment a business requirement is defined until your company delivers the feature to your client.</span></span>

## <a name="the-modern-application-lifecycle"></a><span data-ttu-id="b79be-128">新式应用程序生命周期</span><span class="sxs-lookup"><span data-stu-id="b79be-128">The modern application lifecycle</span></span>

<span data-ttu-id="b79be-129">如今，开发人员编写并生成应用程序的代码，然后将生成的资产传递给 IT 专业人员。</span><span class="sxs-lookup"><span data-stu-id="b79be-129">Today, developers write and build the code for an app and then pass the generated assets to the IT Pros.</span></span> <span data-ttu-id="b79be-130">然后，IT 专业人员重新配置应用程序并将其重新打包，通常是在 MSI 中，或在最近的版本中，采用 app-v 打包格式。</span><span class="sxs-lookup"><span data-stu-id="b79be-130">Then, the IT Pros reconfigure the app and repackage it, typically in an MSI or more recently in an App-V packaging format.</span></span> <span data-ttu-id="b79be-131">然后，应用程序通过不同的通道和工具进行部署。</span><span class="sxs-lookup"><span data-stu-id="b79be-131">The app is then deployed through different channels and tools.</span></span> <span data-ttu-id="b79be-132">此方法的主要问题之一通常称为 "打包 paralysis"。</span><span class="sxs-lookup"><span data-stu-id="b79be-132">One of the main problems with this approach is commonly known as "packaging paralysis".</span></span> <span data-ttu-id="b79be-133">问题在于，每次更新应用更新或操作系统时，此周期都将重复。</span><span class="sxs-lookup"><span data-stu-id="b79be-133">The problem is that this cycle repeats every time there's an app update or an OS update.</span></span>

<span data-ttu-id="b79be-134">您可以看到如下图所示的过程：</span><span class="sxs-lookup"><span data-stu-id="b79be-134">You can see the process reflected on the following picture:</span></span>

![显示新式 IT 生命周期的示意图](./media/deploy-modern-applications/modern-it-application-lifecycle.png)

<span data-ttu-id="b79be-136">公司需要通过一种方式将此打包周期分解为三个独立的周期：</span><span class="sxs-lookup"><span data-stu-id="b79be-136">Companies need a way to break this packaging cycle into three independent cycles:</span></span>

- <span data-ttu-id="b79be-137">OS 更新</span><span class="sxs-lookup"><span data-stu-id="b79be-137">OS updates</span></span>
- <span data-ttu-id="b79be-138">应用程序更新</span><span class="sxs-lookup"><span data-stu-id="b79be-138">Application updates</span></span>
- <span data-ttu-id="b79be-139">自定义</span><span class="sxs-lookup"><span data-stu-id="b79be-139">Customization</span></span>

![显示新式 IT 良性周期的图示](./media/deploy-modern-applications/modern-it-virtuous-cycle.png)

<span data-ttu-id="b79be-141">前面的关系图显示你可以：</span><span class="sxs-lookup"><span data-stu-id="b79be-141">The previous diagram shows that you can:</span></span>

- <span data-ttu-id="b79be-142">更新基础 OS，无需重新打包应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-142">Update the underlying OS without having to repackage your apps.</span></span>
- <span data-ttu-id="b79be-143">启用自定义，无需重新打包原始开发人员包。</span><span class="sxs-lookup"><span data-stu-id="b79be-143">Enable customizations from IT without the need to repackage the original developer package.</span></span>

<span data-ttu-id="b79be-144">这项根式变化会使我们成为新的和新式 IT 生命周期，如下图所示：</span><span class="sxs-lookup"><span data-stu-id="b79be-144">This radical change leads us to the new and modern IT lifecycle as shown in the following picture:</span></span>

![使用 Microsoft 工具显示应用程序生命周期的图示](./media/deploy-modern-applications/microsoft-it-tools.png)

<span data-ttu-id="b79be-146">开发人员创建应用程序并生成 .MSIX 包，IT 专业人员可以使用和配置该包，而无需重新打包。</span><span class="sxs-lookup"><span data-stu-id="b79be-146">Developers create the app and generate an MSIX package that IT Pros can consume and configure without the need of repackaging.</span></span> <span data-ttu-id="b79be-147">除了 .MSIX 技术，Microsoft 还创建了一些工具，可用于自定义和配置包，而无需重新打包。</span><span class="sxs-lookup"><span data-stu-id="b79be-147">Along with the MSIX technology, Microsoft has created tools to allow IT to customize and configure packages without repackaging.</span></span>

## <a name="msix-the-next-generation-of-deployment"></a><span data-ttu-id="b79be-148">.MSIX：下一代部署</span><span class="sxs-lookup"><span data-stu-id="b79be-148">MSIX: The next generation of deployment</span></span>

<span data-ttu-id="b79be-149">在 .MSIX 之前，可以使用多种打包技术，如安装向导、MSI、ClickOnce、App-v 和脚本撰写。</span><span class="sxs-lookup"><span data-stu-id="b79be-149">Before MSIX, there were several packaging technologies available like setup wizards, MSI, ClickOnce, App-V, and scripting.</span></span> <span data-ttu-id="b79be-150">其中每种技术都有其各自的优势，Microsoft 决定最大程度地选择生成 .MSIX。</span><span class="sxs-lookup"><span data-stu-id="b79be-150">Each of these technologies has their own strengths and Microsoft has decided to pick the best of all to build MSIX.</span></span> <span data-ttu-id="b79be-151">.MSIX 是在这些现有技术的基础上建立的，它们都是最佳选择：</span><span class="sxs-lookup"><span data-stu-id="b79be-151">MSIX is built on the foundations of these existing technologies picking the best of each:</span></span>

- <span data-ttu-id="b79be-152">App-v = \> 容器化</span><span class="sxs-lookup"><span data-stu-id="b79be-152">App-V =\> Containerization</span></span>
- <span data-ttu-id="b79be-153">ClickOnce = \> 自动更新</span><span class="sxs-lookup"><span data-stu-id="b79be-153">ClickOnce =\> Auto updating</span></span>
- <span data-ttu-id="b79be-154">MSI = \> 易于分发</span><span class="sxs-lookup"><span data-stu-id="b79be-154">MSI =\> Easy to distribute</span></span>

<span data-ttu-id="b79be-155">借助 .MSIX，你将获得一项安装程序技术，其中包含所有这些功能。</span><span class="sxs-lookup"><span data-stu-id="b79be-155">With MSIX, you get one installer technology with all these features.</span></span>

![显示对生成 .MSIX 有影响的各种技术的图示](./media/deploy-modern-applications/msix.png)

### <a name="benefits-of-msix"></a><span data-ttu-id="b79be-157">.MSIX 的优点</span><span class="sxs-lookup"><span data-stu-id="b79be-157">Benefits of MSIX</span></span>

#### <a name="never-regret-installing-an-app"></a><span data-ttu-id="b79be-158">从不后悔安装应用</span><span class="sxs-lookup"><span data-stu-id="b79be-158">Never regret installing an app</span></span>

<span data-ttu-id="b79be-159">.MSIX 提供可预测、可靠和安全的部署。</span><span class="sxs-lookup"><span data-stu-id="b79be-159">MSIX provides a predictable, reliable, and safe deployment.</span></span> <span data-ttu-id="b79be-160">包清单中包含的声明性方法使 OS 可以跟踪应用程序所需的每个资产。</span><span class="sxs-lookup"><span data-stu-id="b79be-160">The declarative method contained in the package manifest lets the OS keep track of every asset your application needs.</span></span> <span data-ttu-id="b79be-161">它还提供真正的干净卸载，不会产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="b79be-161">It also provides a true clean uninstall with no side effects.</span></span>

#### <a name="disk-space-optimization"></a><span data-ttu-id="b79be-162">磁盘空间优化</span><span class="sxs-lookup"><span data-stu-id="b79be-162">Disk space optimization</span></span>

<span data-ttu-id="b79be-163">.MSIX 经过优化，可降低应用程序对用户计算机磁盘空间的占用空间。</span><span class="sxs-lookup"><span data-stu-id="b79be-163">MSIX is optimized to reduce the footprint that an application has on the user's machine disk space.</span></span> <span data-ttu-id="b79be-164">它创建文件的单实例存储。</span><span class="sxs-lookup"><span data-stu-id="b79be-164">It creates a single instance storage of your files.</span></span> <span data-ttu-id="b79be-165">也就是说，如果有两个不同于同一个 DLL 的包，则不会两次安装 DLL。</span><span class="sxs-lookup"><span data-stu-id="b79be-165">That is, if you have two different packages with the same DLL, the DLL isn't installed twice.</span></span> <span data-ttu-id="b79be-166">平台会处理该问题，因为它知道某个特定应用程序的所有文件都是根据其声明性性质而安装的。</span><span class="sxs-lookup"><span data-stu-id="b79be-166">The platform takes care of that problem because it knows all the files that a particular app installed thanks to its declarative nature.</span></span> <span data-ttu-id="b79be-167">它还允许并行工作的不同版本的 DLL。</span><span class="sxs-lookup"><span data-stu-id="b79be-167">It also allows you to have different versions of a DLL working side by side.</span></span>

<span data-ttu-id="b79be-168">使用资源包时，可以轻松创建多语言应用，操作系统会安装所使用的应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-168">With the use of resource packages, you can easily create multilingual apps and the OS takes care of installing the ones that are used.</span></span>

#### <a name="network-optimization"></a><span data-ttu-id="b79be-169">网络优化</span><span class="sxs-lookup"><span data-stu-id="b79be-169">Network optimization</span></span>

<span data-ttu-id="b79be-170">.MSIX 检测到字节块级别上的文件之间的差异，启用称为差异更新的功能。</span><span class="sxs-lookup"><span data-stu-id="b79be-170">MSIX detects the differences on the files at the byte block level enabling a feature called differential updates.</span></span> <span data-ttu-id="b79be-171">这意味着在应用程序更新上只下载更新的字节块。</span><span class="sxs-lookup"><span data-stu-id="b79be-171">What this means is that only the updated byte blocks are downloaded on application updates.</span></span>

![显示 .MSIX 如何管理差异更新的关系图](./media/deploy-modern-applications/msix-managing-updates.png)

<span data-ttu-id="b79be-173">使用流式安装，用户可以快速开始使用应用程序，同时在后台下载应用程序的其他部分。</span><span class="sxs-lookup"><span data-stu-id="b79be-173">With streaming installation, the user can quickly start working on your application while other parts of the app are downloaded on the background.</span></span> <span data-ttu-id="b79be-174">此功能可为用户提供丰富的体验。</span><span class="sxs-lookup"><span data-stu-id="b79be-174">This feature contributes to an engaging experience for your users.</span></span>

<span data-ttu-id="b79be-175">利用可选包功能，你可以在应用部署上实现组件化，因此你可以在需要时下载这些包。</span><span class="sxs-lookup"><span data-stu-id="b79be-175">With the optional packages feature, you achieve componentization on your app deployment, so you can download them when needed.</span></span>

#### <a name="simple-packaging-and-deployment"></a><span data-ttu-id="b79be-176">简单打包和部署</span><span class="sxs-lookup"><span data-stu-id="b79be-176">Simple packaging and deployment</span></span>

<span data-ttu-id="b79be-177">AppManifest 声明了版本控制、设备目标，并为每个应用程序确定了标准方式。</span><span class="sxs-lookup"><span data-stu-id="b79be-177">The AppManifest declares the versioning, device targeting and identify in a standard way for every application.</span></span> <span data-ttu-id="b79be-178">它还提供了一种方法来对资产进行签名，从而提供可靠的安全基础。</span><span class="sxs-lookup"><span data-stu-id="b79be-178">It also provides a way to sign your assets providing a solid security foundation.</span></span>

#### <a name="os-managed"></a><span data-ttu-id="b79be-179">操作系统管理</span><span class="sxs-lookup"><span data-stu-id="b79be-179">OS managed</span></span>

<span data-ttu-id="b79be-180">操作系统将处理用于安装、更新和删除应用程序的所有过程。</span><span class="sxs-lookup"><span data-stu-id="b79be-180">The OS handles all the processes for installing, updating, and removing an application.</span></span> <span data-ttu-id="b79be-181">应用程序是按用户安装的，但仅下载一次，从而最大程度地减少磁盘占用。</span><span class="sxs-lookup"><span data-stu-id="b79be-181">Applications are installed per user but downloaded only once, minimizing the disk footprint.</span></span> <span data-ttu-id="b79be-182">Microsoft 正在努力同时提供 Windows 7 上的 .MSIX 体验。</span><span class="sxs-lookup"><span data-stu-id="b79be-182">Microsoft is working on providing the MSIX experience also on Windows 7.</span></span>

#### <a name="windows-provides-integrity-for-the-app"></a><span data-ttu-id="b79be-183">Windows 提供应用的完整性</span><span class="sxs-lookup"><span data-stu-id="b79be-183">Windows provides integrity for the app</span></span>

<span data-ttu-id="b79be-184">使用数字签名，可以确保不会从不受信任的源安装应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-184">With the use of digital signatures, you can guarantee that you don't install an application from untrusted sources.</span></span> <span data-ttu-id="b79be-185">.MSIX 还会阻止篡改，原因如下：</span><span class="sxs-lookup"><span data-stu-id="b79be-185">MSIX also prevents tampering because:</span></span>

- <span data-ttu-id="b79be-186">它保留文件哈希记录。</span><span class="sxs-lookup"><span data-stu-id="b79be-186">It keeps a record of file hashes.</span></span>
- <span data-ttu-id="b79be-187">它检测是否在安装后修改了文件。</span><span class="sxs-lookup"><span data-stu-id="b79be-187">It detects if a file has been modified after installation.</span></span>

#### <a name="works-for-the-entire-app-catalog"></a><span data-ttu-id="b79be-188">适用于整个应用程序目录</span><span class="sxs-lookup"><span data-stu-id="b79be-188">Works for the entire App Catalog</span></span>

<span data-ttu-id="b79be-189">.MSIX 的最酷之一是，它适用于整个应用程序目录、Windows 窗体、WPF、MFC/ATL、Delphi，即使你想要执行 xCopy 部署、ClickOnce 或转到应用商店，你也可以使用相同的 .MSIX 包。</span><span class="sxs-lookup"><span data-stu-id="b79be-189">One of the coolest things about MSIX is that it works for the entire application catalog, Windows Forms, WPF, MFC/ATL, Delphi, even if you want to do xCopy deployment, ClickOnce, or going to the Store, you can use the same MSIX package.</span></span>

### <a name="tools"></a><span data-ttu-id="b79be-190">工具</span><span class="sxs-lookup"><span data-stu-id="b79be-190">Tools</span></span>

#### <a name="windows-application-packaging-project"></a><span data-ttu-id="b79be-191">Windows 应用程序打包项目</span><span class="sxs-lookup"><span data-stu-id="b79be-191">Windows Application Packaging Project</span></span>

<span data-ttu-id="b79be-192">你可以使用 Visual Studio 中的 **Windows 应用程序打包项目** 项目为桌面应用生成程序包。</span><span class="sxs-lookup"><span data-stu-id="b79be-192">You can use the **Windows Application Packaging Project** project in Visual Studio to generate a package for your desktop app.</span></span> <span data-ttu-id="b79be-193">然后，你可以将该包发布到 Microsoft Store 或将其旁加载到一个或多个电脑上。</span><span class="sxs-lookup"><span data-stu-id="b79be-193">Then, you can publish that package to the Microsoft Store or sideload it onto one or more PCs.</span></span>

#### <a name="msix-packaging-tool"></a><span data-ttu-id="b79be-194">MSIX 打包工具</span><span class="sxs-lookup"><span data-stu-id="b79be-194">MSIX Packaging Tool</span></span>

<span data-ttu-id="b79be-195">使用 MSIX 打包工具可将现有的 Win32 应用程序重新打包为 MSIX 格式。</span><span class="sxs-lookup"><span data-stu-id="b79be-195">The MSIX Packaging Tool enables you to repackage your existing Win32 applications to the MSIX format.</span></span> <span data-ttu-id="b79be-196">它同时提供交互式 UI 和用于转换的命令行，并使你能够在不使用源代码的情况下转换应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-196">It offers both an interactive UI and a command line for conversions and gives you the ability to convert an application without having the source code.</span></span>

![MSIX 打包工具](./media/deploy-modern-applications/msix-packaging-tool.png)

#### <a name="package-support-framework"></a><span data-ttu-id="b79be-198">包支持框架</span><span class="sxs-lookup"><span data-stu-id="b79be-198">Package Support Framework</span></span>

<span data-ttu-id="b79be-199">包支持框架是一个开源工具包，可帮助你在无法访问源代码的情况下将修补程序应用于现有的 Win32 应用程序，使其能够在 .MSIX 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="b79be-199">The Package Support Framework is an open-source kit that helps you apply fixes to your existing Win32 application when you don't have access to the source code, so that it can run in an MSIX container.</span></span> <span data-ttu-id="b79be-200">包支持框架可帮助应用程序遵循新式运行时环境的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="b79be-200">The Package Support Framework helps your application follow the best practices of the modern runtime environment.</span></span>

#### <a name="app-installer"></a><span data-ttu-id="b79be-201">应用安装程序</span><span class="sxs-lookup"><span data-stu-id="b79be-201">App Installer</span></span>

<span data-ttu-id="b79be-202">应用安装程序允许通过双击应用程序包来安装 Windows 10 应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-202">App Installer allows Windows 10 apps to be installed by double-clicking the app package.</span></span> <span data-ttu-id="b79be-203">这意味着用户无需使用 PowerShell 或其他开发人员工具来部署 Windows 10 应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-203">This means that users don't need to use PowerShell or other developer tools to deploy Windows 10 apps.</span></span> <span data-ttu-id="b79be-204">应用安装程序还可以从 Web、可选包和相关的集中安装应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-204">The App Installer can also install an app from the web, optional packages, and related sets.</span></span>

## <a name="how-to-create-an-msix-package-from-an-existing-win32-desktop-application"></a><span data-ttu-id="b79be-205">如何从现有 Win32 桌面应用程序创建 .MSIX 包</span><span class="sxs-lookup"><span data-stu-id="b79be-205">How to create an MSIX package from an existing Win32 desktop application</span></span>

<span data-ttu-id="b79be-206">让我们完成从现有 Win32 应用程序创建 .MSIX 包的过程。</span><span class="sxs-lookup"><span data-stu-id="b79be-206">Let's go through the process to create an MSIX package from an existing Win32 application.</span></span> <span data-ttu-id="b79be-207">在此示例中，我们将使用 Windows 窗体应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-207">In this example, we'll use a Windows Forms app.</span></span>

<span data-ttu-id="b79be-208">若要开始，请将新项目添加到解决方案中，选择 Windows 应用程序打包项目，并为其指定名称。</span><span class="sxs-lookup"><span data-stu-id="b79be-208">To start, add a new project to your solution, select the Windows Application Packaging Project, and give it a name.</span></span>

![添加新的 Windows 应用程序打包项目](./media/deploy-modern-applications/add-packaging-project.png)

<span data-ttu-id="b79be-210">你将看到打包项目的结构，并记下名为 " *应用程序*" 的特殊文件夹。</span><span class="sxs-lookup"><span data-stu-id="b79be-210">You'll see the structure of the packaging project and note a special folder called *Applications*.</span></span> <span data-ttu-id="b79be-211">在此文件夹中，可以指定要包含在包中的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-211">Inside this folder, you can specify which applications you want to include in the package.</span></span> <span data-ttu-id="b79be-212">它可以有多个。</span><span class="sxs-lookup"><span data-stu-id="b79be-212">It can be more than one.</span></span>

![打包项目的结构](./media/deploy-modern-applications/packaging-project.png)

<span data-ttu-id="b79be-214">右键单击 " *应用程序* " 文件夹，然后选择要从 Visual Studio 解决方案中打包的 Windows 窗体项目。</span><span class="sxs-lookup"><span data-stu-id="b79be-214">Right-click on the *Applications* folder and select the Windows Forms project you want to package from the Visual Studio solution.</span></span>

![向打包项目添加 Windows 窗体项目](./media/deploy-modern-applications/add-winforms-project.png)

<span data-ttu-id="b79be-216">此时，可以编译和生成包，但我们要检查几个问题。</span><span class="sxs-lookup"><span data-stu-id="b79be-216">At this point, you can compile and generate the package but let's examine a couple of things.</span></span> <span data-ttu-id="b79be-217">为了获得更好的用户体验，Visual Studio 可以自动生成所有视觉对象，新式应用程序需要处理磁贴栏和 "开始" 菜单的图标和磁贴资产。</span><span class="sxs-lookup"><span data-stu-id="b79be-217">To have a better user experience, Visual Studio can autogenerate all the visual assets a modern application needs to handle icons and tile assets for the tile bar and start menu.</span></span> <span data-ttu-id="b79be-218">打开 *appxmanifest.xml* 文件以访问清单设计器。</span><span class="sxs-lookup"><span data-stu-id="b79be-218">Open the *Package.appxmanifest* file to access the Manifest Designer.</span></span> <span data-ttu-id="b79be-219">然后，你可以通过单击 " **创建**"，从项目中的给定映像生成所有视觉资产。</span><span class="sxs-lookup"><span data-stu-id="b79be-219">You can then generate all the visual assets from a given image present on your project just by clicking **Create**.</span></span>

![Visual Studio 中的清单设计器屏幕截图](./media/deploy-modern-applications/manifest-designer.png)

<span data-ttu-id="b79be-221">如果你打开 *appxmanifest.xml* 文件的代码，你会看到一些有趣的事情。</span><span class="sxs-lookup"><span data-stu-id="b79be-221">If you open the code for the *Package.appxmanifest* file, you can see a couple of interesting things.</span></span>

<span data-ttu-id="b79be-222">在 `<Package>` 中，有一个 `<Identity>` 节点。</span><span class="sxs-lookup"><span data-stu-id="b79be-222">Right under `<Package>`, there's an `<Identity>` node.</span></span> <span data-ttu-id="b79be-223">你的打包应用程序将通过它来获取其标识，该标识将由操作系统进行管理。</span><span class="sxs-lookup"><span data-stu-id="b79be-223">This is where your packaged application is going to get its identity, which will be managed by the OS.</span></span>

![标识节点](./media/deploy-modern-applications/identity-node.png)

<span data-ttu-id="b79be-225">在 `<Capabilities>` 节点中，你可以找到应用程序所需的所有需求，特别注意 `<rescap:Capability Name="runFullTrust" \>` ，这会告诉 OS 以完全信任模式运行应用，因为它是 Win32 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-225">In the `<Capabilities>` node, you can find all the requirements the application needs, paying special attention to the `<rescap:Capability Name="runFullTrust" \>`, which tells the OS to run the app in full trust mode since it's a Win32 application.</span></span>

![功能节点](./media/deploy-modern-applications/capabilities-node.png)

<span data-ttu-id="b79be-227">将打包项目设置为解决方案的启动项目，然后选择 " *运行*"。</span><span class="sxs-lookup"><span data-stu-id="b79be-227">Set the packaging project as the startup project for the solution and select *Run*.</span></span> <span data-ttu-id="b79be-228">这将：</span><span class="sxs-lookup"><span data-stu-id="b79be-228">This is going to:</span></span>

- <span data-ttu-id="b79be-229">编译 Windows 窗体应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-229">Compile the Windows Forms application.</span></span>
- <span data-ttu-id="b79be-230">从生成结果中创建 .MSIX 包。</span><span class="sxs-lookup"><span data-stu-id="b79be-230">Create an MSIX package out of the build results.</span></span>
- <span data-ttu-id="b79be-231">部署包。</span><span class="sxs-lookup"><span data-stu-id="b79be-231">Deploy the packages.</span></span>
- <span data-ttu-id="b79be-232">在开发计算机上本地安装它。</span><span class="sxs-lookup"><span data-stu-id="b79be-232">Install it locally on the development machine.</span></span>
- <span data-ttu-id="b79be-233">启动应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-233">Launch the app.</span></span>

![已安装的应用程序](./media/deploy-modern-applications/our-installed-application.png)

<span data-ttu-id="b79be-235">为此，你具有 .MSIX 提供完全集成到 Windows 10 的全新安装和卸载体验。</span><span class="sxs-lookup"><span data-stu-id="b79be-235">With this, you have the clean install and uninstall experience that MSIX provides fully integrated into Windows 10.</span></span>

<span data-ttu-id="b79be-236">最后一阶段介绍如何将 .MSIX 包部署到其他计算机。</span><span class="sxs-lookup"><span data-stu-id="b79be-236">The final stage is about how you deploy the MSIX package to another machine.</span></span>

<span data-ttu-id="b79be-237">右键单击打包项目，选择 " **应用商店** " 菜单，然后选择 " **创建应用包** " 选项。</span><span class="sxs-lookup"><span data-stu-id="b79be-237">Right-click on the packaging project, select the **Store** menu, and then select the **Create App Packages** option.</span></span>

<span data-ttu-id="b79be-238">然后，可以选择是创建要上传到存储的包，还是创建用于旁加载的包。</span><span class="sxs-lookup"><span data-stu-id="b79be-238">Then, you can choose between creating a package to upload to the store or creating packages for sideloading.</span></span> <span data-ttu-id="b79be-239">在大多数现代化情况下，你将选择 " **我想要创建旁加载包**"。</span><span class="sxs-lookup"><span data-stu-id="b79be-239">In most modernization scenarios, you'll choose **I want to create packages for sideloading**.</span></span>

![配置包](./media/deploy-modern-applications/configuring-packages.png)

<span data-ttu-id="b79be-241">你可以选择要作为目标的不同体系结构，因为你可以在同一个 .MSIX 包中包含所需数量。</span><span class="sxs-lookup"><span data-stu-id="b79be-241">There you can select the different architectures you want to target as you can include as many as you want into the same MSIX package.</span></span>

<span data-ttu-id="b79be-242">最后一步是声明要在何处部署最终安装资产。</span><span class="sxs-lookup"><span data-stu-id="b79be-242">The final step is to declare where you want to deploy the final installation assets.</span></span>

![配置更新设置](./media/deploy-modern-applications/configure-update-settings.png)

<span data-ttu-id="b79be-244">你可以选择在企业文件服务器上使用共享 UNC 路径的 web 服务器。</span><span class="sxs-lookup"><span data-stu-id="b79be-244">You can choose to use a web server of a shared UNC path on your enterprise file servers.</span></span> <span data-ttu-id="b79be-245">请注意设置以指定你希望如何更新应用程序。</span><span class="sxs-lookup"><span data-stu-id="b79be-245">Pay attention to the settings to specify how you want to update your application.</span></span> <span data-ttu-id="b79be-246">下一节将介绍应用程序更新。</span><span class="sxs-lookup"><span data-stu-id="b79be-246">We'll cover application updates in the next section.</span></span>

<span data-ttu-id="b79be-247">有关详细的分步指南，请参阅 [使用 Visual Studio 从源代码打包桌面应用](/windows/msix/desktop/desktop-to-uwp-packaging-dot-net)。</span><span class="sxs-lookup"><span data-stu-id="b79be-247">For a detailed step-by-step guide, see [Package a desktop app from source code using Visual Studio](/windows/msix/desktop/desktop-to-uwp-packaging-dot-net).</span></span>

## <a name="auto-updates-in-msix"></a><span data-ttu-id="b79be-248">.MSIX 中的自动更新</span><span class="sxs-lookup"><span data-stu-id="b79be-248">Auto Updates in MSIX</span></span>

<span data-ttu-id="b79be-249">Windows 应用商店使用 Windows 更新具有很好的更新机制。</span><span class="sxs-lookup"><span data-stu-id="b79be-249">The Windows Store has a great updating mechanism using Windows Update.</span></span> <span data-ttu-id="b79be-250">在大多数企业方案中，你不会使用应用商店分发桌面应用。</span><span class="sxs-lookup"><span data-stu-id="b79be-250">In most enterprise scenarios, you don't use the Store to distribute your desktop apps.</span></span> <span data-ttu-id="b79be-251">因此，你需要一种类似的方式来为应用程序配置更新，并将它们拉取给用户。</span><span class="sxs-lookup"><span data-stu-id="b79be-251">So, you need a similar way to configure updates for your application and pull them to your users.</span></span>

<span data-ttu-id="b79be-252">结合使用 Windows 10 功能和 .MSIX 包，你可以为用户提供出色的更新体验。</span><span class="sxs-lookup"><span data-stu-id="b79be-252">Using a combination of Windows 10 features and MSIX packages, you can provide a great updating experience for your users.</span></span> <span data-ttu-id="b79be-253">事实上，用户根本不需要技术，但仍可从无缝应用程序更新体验中获益。</span><span class="sxs-lookup"><span data-stu-id="b79be-253">In fact, the user doesn't need to be technical at all but still benefit from a seamless application update experience.</span></span>

<span data-ttu-id="b79be-254">可以通过两种不同的方式配置更新以与用户交互：</span><span class="sxs-lookup"><span data-stu-id="b79be-254">You can configure your updates to interact with the user in two different ways:</span></span>

- <span data-ttu-id="b79be-255">用户提示更新：操作系统会显示一些自动生成的理想 UI，通知用户有关应用程序即将安装的信息。</span><span class="sxs-lookup"><span data-stu-id="b79be-255">User prompted updates: The OS shows some autogenerated nice UI to notify the user about the application is about to install.</span></span> <span data-ttu-id="b79be-256">它基于你在安装文件中指定的属性生成此 UI。</span><span class="sxs-lookup"><span data-stu-id="b79be-256">It builds this UI based on the properties you specify on your installation files.</span></span>

- <span data-ttu-id="b79be-257">后台无提示更新。</span><span class="sxs-lookup"><span data-stu-id="b79be-257">Silent updates in the background.</span></span> <span data-ttu-id="b79be-258">如果选择此选项，则用户无需知道更新。</span><span class="sxs-lookup"><span data-stu-id="b79be-258">With this option, your users don't need to be aware of the updates.</span></span>

<span data-ttu-id="b79be-259">你还可以配置当应用程序启动或定期执行更新的时间。</span><span class="sxs-lookup"><span data-stu-id="b79be-259">You can also configure when you want to perform updates, when the application launches or on a regular basis.</span></span> <span data-ttu-id="b79be-260">凭借边载功能，您甚至可以在应用程序运行时获取这些更新。</span><span class="sxs-lookup"><span data-stu-id="b79be-260">Thanks to the side-loading features, you can even get these updates while the application is running.</span></span>

<span data-ttu-id="b79be-261">当你使用此类型的部署时，将创建一个名为 *appinstaller* 的特殊文件。</span><span class="sxs-lookup"><span data-stu-id="b79be-261">When you use this type of deployment, a special file is created called *.appinstaller*.</span></span> <span data-ttu-id="b79be-262">此简单文件包含以下部分：</span><span class="sxs-lookup"><span data-stu-id="b79be-262">This simple file contains the following sections:</span></span>

- <span data-ttu-id="b79be-263">*Appinstaller* 文件的位置</span><span class="sxs-lookup"><span data-stu-id="b79be-263">The location of the *.appinstaller* file</span></span>
- <span data-ttu-id="b79be-264">应用程序的主 .MSIX 包属性</span><span class="sxs-lookup"><span data-stu-id="b79be-264">The application's main MSIX package properties</span></span>
- <span data-ttu-id="b79be-265">更新行为</span><span class="sxs-lookup"><span data-stu-id="b79be-265">The update behavior</span></span>

![appinstaller 文件](./media/deploy-modern-applications/appinstaller-file.png)

<span data-ttu-id="b79be-267">与此文件结合使用，Microsoft 设计了一个特殊的 URL 协议，以从链接启动安装过程：</span><span class="sxs-lookup"><span data-stu-id="b79be-267">In combination with this file, Microsoft has designed a special URL protocol to launch the installation process from a link:</span></span>

```xml
<a href="ms-appinstaller:?source=http://mywebservice.azureedge.net/MyApp.msix">Install app package </a>
```

<span data-ttu-id="b79be-268">此协议适用于所有浏览器，并在 Windows 10 上通过出色的用户体验启动安装过程。</span><span class="sxs-lookup"><span data-stu-id="b79be-268">This protocol works on all browsers and launches the installation process with a great user experience on Windows 10.</span></span> <span data-ttu-id="b79be-269">由于 OS 管理安装过程，因此它知道此应用程序的安装位置，并跟踪该进程影响的所有文件。</span><span class="sxs-lookup"><span data-stu-id="b79be-269">Since the OS manages the installation process, it's aware of the location this application was installed from and tracks all the files affected by the process.</span></span>

<span data-ttu-id="b79be-270">.MSIX 创建用于安装的用户界面，该用户界面会自动显示包的某些属性。</span><span class="sxs-lookup"><span data-stu-id="b79be-270">MSIX creates a user interface for installation automatically showing some properties of the package.</span></span> <span data-ttu-id="b79be-271">这允许为每个应用提供常见的安装体验。</span><span class="sxs-lookup"><span data-stu-id="b79be-271">This allows for a common installation experience for every app.</span></span>

<span data-ttu-id="b79be-272">生成新的 .MSIX 包并将其移到部署服务器后，只需编辑 *appinstaller* 文件来反映这些更改，主要是版本和新 .msix 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="b79be-272">Once you've generated the new MSIX package and moved it to the deployment server, you just have to edit the *.appinstaller* file to reflect these changes, mainly the version and the path to the new MSIX file.</span></span> <span data-ttu-id="b79be-273">用户下一次启动应用程序时，系统将检测更改，并在后台下载新版本的文件。</span><span class="sxs-lookup"><span data-stu-id="b79be-273">The next time the user launches the application, the system is going to detect the change and download the files for the new version in the background.</span></span> <span data-ttu-id="b79be-274">完成此操作后，将以透明方式对用户执行安装。</span><span class="sxs-lookup"><span data-stu-id="b79be-274">When this is done, installation will execute on new application launch transparently for your user.</span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="b79be-275">上一页</span><span class="sxs-lookup"><span data-stu-id="b79be-275">Previous</span></span>](example-migration.md)
