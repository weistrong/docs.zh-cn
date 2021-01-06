---
title: Windows 10 迁移
description: Windows 10 功能（如打包和 XAML 孤岛）深入探讨。
ms.date: 09/16/2019
ms.openlocfilehash: cd17088b086a32fd3bb37e617d3a1047acedde0e
ms.sourcegitcommit: 9a4488a3625866335e83a20da5e9c5286b1f034c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2020
ms.locfileid: "97866416"
---
# <a name="windows-10-migration"></a><span data-ttu-id="666df-103">Windows 10 迁移</span><span class="sxs-lookup"><span data-stu-id="666df-103">Windows 10 migration</span></span>

<span data-ttu-id="666df-104">请考虑以下情况：你有在 Windows 7 天内开发的工作桌面应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-104">Consider the following situation: You have a working desktop application that was developed in the Windows 7 days.</span></span> <span data-ttu-id="666df-105">它目前使用 WPF 技术，在 Windows 10 上运行时，它具有过时的 UI 和行为。</span><span class="sxs-lookup"><span data-stu-id="666df-105">It's using WPF technology available at that time and working fine but it has an outdated UI and behaviors when you run it on Windows 10.</span></span> <span data-ttu-id="666df-106">就像观看现在俨然电影（如 Matrix）时，可以使用 Nokia 8110 设备查看 Neo。</span><span class="sxs-lookup"><span data-stu-id="666df-106">It is like when you watch a futuristic movie like Matrix and you see Neo using the Nokia 8110 device.</span></span> <span data-ttu-id="666df-107">此电影在20年后工作良好，但它可以从设备现代化中获益。</span><span class="sxs-lookup"><span data-stu-id="666df-107">The film works great after 20 years but it would rather benefit from a device modernization.</span></span>

<span data-ttu-id="666df-108">随着 Windows 10 的发布，Microsoft 引入了许多创新来支持诸如平板电脑和触摸设备之类的方案，并为 Microsoft 操作系统的用户提供最佳体验。</span><span class="sxs-lookup"><span data-stu-id="666df-108">With the release of Windows 10, Microsoft introduced many innovations to support scenarios like tablets and touch devices and to provide the best experience for users for a Microsoft operating system ever.</span></span> <span data-ttu-id="666df-109">例如，你能够：</span><span class="sxs-lookup"><span data-stu-id="666df-109">For example, you can:</span></span>

- <span data-ttu-id="666df-110">使用 Windows Hello 通过你的面部登录。</span><span class="sxs-lookup"><span data-stu-id="666df-110">Sign in with your face using Windows Hello.</span></span>
- <span data-ttu-id="666df-111">使用笔绘制或手写自动识别和 digitalized 的文本。</span><span class="sxs-lookup"><span data-stu-id="666df-111">Use a pen to draw or handwrite text that is automatically recognized and digitalized.</span></span>
- <span data-ttu-id="666df-112">使用 WinML 运行在云上构建的本地自定义 AI 模型。</span><span class="sxs-lookup"><span data-stu-id="666df-112">Run locally customized AI models built on the cloud using WinML.</span></span>

<span data-ttu-id="666df-113">通过 Windows 运行时 (WinRT) 库为 Windows 开发人员启用所有这些功能。</span><span class="sxs-lookup"><span data-stu-id="666df-113">All these features are enabled for Windows developers through Windows Runtime (WinRT) libraries.</span></span> <span data-ttu-id="666df-114">可以在现有的桌面应用程序中利用这些功能，因为库也同时公开给 .NET Framework 和 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="666df-114">You can take advantage of these features in your existing desktop apps because the libraries are exposed to both the .NET Framework and .NET Core as well.</span></span> <span data-ttu-id="666df-115">你甚至可以使用 XAML 孤岛来现代化 UI，并根据时间改进应用的视觉对象和行为。</span><span class="sxs-lookup"><span data-stu-id="666df-115">You can even modernize your UI with the use of XAML Islands and improve the visuals and behavior of your apps according to the times.</span></span>

<span data-ttu-id="666df-116">此处需要注意的一个重要事项是，无需放弃 .NET Framework 技术来遵循此现代化路径。</span><span class="sxs-lookup"><span data-stu-id="666df-116">One important thing to note here is that you don't need to abandon .NET Framework technology to follow this modernization path.</span></span> <span data-ttu-id="666df-117">您可以安全地停留在那里，并拥有 Windows 10 的所有优点，而无需迁移到 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="666df-117">You can safely stay on there and have all the benefits of Windows 10 without the pressure to migrate to .NET Core.</span></span> <span data-ttu-id="666df-118">因此，您可以获得强大的功能和灵活性来选择您的现代化路径。</span><span class="sxs-lookup"><span data-stu-id="666df-118">So, you get both the power and the flexibility to choose your modernization path.</span></span>

## <a name="winrt-apis"></a><span data-ttu-id="666df-119">WinRT Api</span><span class="sxs-lookup"><span data-stu-id="666df-119">WinRT APIs</span></span>

<span data-ttu-id="666df-120">WinRT Api 是面向对象的、结构良好的应用程序编程接口 (Api) 为 Windows 10 开发人员提供对操作系统必须提供的所有内容的访问权限。</span><span class="sxs-lookup"><span data-stu-id="666df-120">WinRT APIs are object-oriented, well-structured application programming interfaces (APIs) that give Windows 10 developers access to everything the operating system has to offer.</span></span> <span data-ttu-id="666df-121">通过 WinRT Api，你可以将功能（如推送通知、设备 Api、Microsoft Ink 和 WinML）与桌面应用中的其他功能集成。</span><span class="sxs-lookup"><span data-stu-id="666df-121">Through WinRT APIs, you can integrate functionalities like Push Notifications, Device APIs, Microsoft Ink, and WinML, among others on your desktop apps.</span></span>

<span data-ttu-id="666df-122">通常，可以从经典桌面应用程序调用 WinRT Api。</span><span class="sxs-lookup"><span data-stu-id="666df-122">In general, WinRT APIs can be called from a classic desktop app.</span></span> <span data-ttu-id="666df-123">但是，有两个主要方面是此规则的例外情况：</span><span class="sxs-lookup"><span data-stu-id="666df-123">However, two main areas present an exception to this rule:</span></span>

* <span data-ttu-id="666df-124">需要包标识的 Api。</span><span class="sxs-lookup"><span data-stu-id="666df-124">APIs that require a package identity.</span></span>
* <span data-ttu-id="666df-125">需要可视化的 Api，如 XAML 或组合。</span><span class="sxs-lookup"><span data-stu-id="666df-125">APIs that require visualization like XAML or Composition.</span></span>

### <a name="universal-windows-platform-uwp-packages"></a><span data-ttu-id="666df-126">通用 Windows 平台 (UWP) 包</span><span class="sxs-lookup"><span data-stu-id="666df-126">Universal Windows Platform (UWP) packages</span></span>

#### <a name="application-package-identity"></a><span data-ttu-id="666df-127">应用程序包标识</span><span class="sxs-lookup"><span data-stu-id="666df-127">Application Package Identity</span></span>

<span data-ttu-id="666df-128">UWP 应用有一个部署系统，其中操作系统管理应用程序的安装和卸载。</span><span class="sxs-lookup"><span data-stu-id="666df-128">UWP apps have a deployment system where the OS manages the installation and uninstallation of application.</span></span> <span data-ttu-id="666df-129">这要求安装是声明性的，这意味着在安装期间不执行任何用户代码。</span><span class="sxs-lookup"><span data-stu-id="666df-129">That requires the installation to be declarative, meaning that no user code is executed during install.</span></span> <span data-ttu-id="666df-130">相反，应用程序要与系统集成的所有内容（如协议、文件类型和扩展）都是在应用程序清单中声明的。</span><span class="sxs-lookup"><span data-stu-id="666df-130">Instead, everything the app wants to integrate with the system, such as protocols, file types, and extensions, is declared in the application manifest.</span></span> <span data-ttu-id="666df-131">部署管道在部署时配置这些集成点。</span><span class="sxs-lookup"><span data-stu-id="666df-131">At deployment time, the deployment pipeline configures those integration points.</span></span> <span data-ttu-id="666df-132">操作系统管理所有此功能并对其进行跟踪的唯一方式是，每个 "包" 具有标识，这是应用程序的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="666df-132">The only way for the OS to manage all this functionality and keep track of it is for each 'package' to have an identity, a unique identifier for the application.</span></span>

<span data-ttu-id="666df-133">某些 WinRT Api 要求此包标识按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="666df-133">Some WinRT APIs require this package identity to work as expected.</span></span> <span data-ttu-id="666df-134">但是，经典桌面应用（如本机 c + + 或 .NET 应用）使用不需要包标识的不同部署系统。</span><span class="sxs-lookup"><span data-stu-id="666df-134">However, classic desktop apps like native C++ or .NET apps, use different deployment systems that don't require a package identity.</span></span> <span data-ttu-id="666df-135">如果要在桌面应用程序中使用这些 WinRT Api，则需要为其提供包标识。</span><span class="sxs-lookup"><span data-stu-id="666df-135">If you want to use these WinRT APIs in your desktop application, you need to provide them a package identity.</span></span>

<span data-ttu-id="666df-136">继续操作的一种方法是构建附加的打包项目。</span><span class="sxs-lookup"><span data-stu-id="666df-136">One way to proceed is to build an additional packaging project.</span></span> <span data-ttu-id="666df-137">在打包项目中，指向原始源代码项目，并指定要提供的标识信息。</span><span class="sxs-lookup"><span data-stu-id="666df-137">Inside the packaging project, you point to the original source code project and specify the Identity information you want to provide.</span></span><span data-ttu-id="666df-138">如果安装包并运行已安装的应用程序，它会自动获取标识，使代码可以调用需要标识的所有 WinRT Api。</span><span class="sxs-lookup"><span data-stu-id="666df-138"> If you install the package and run the installed app, it will automatically get an identify enabling your code to call all WinRT APIs requiring Identity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
         xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10">
    <Identity Name="YOUR-APP-GUID "
              Publisher="CN=YOUR COMPANY"
              Version="1.x.x.x" />
</Package>
```

<span data-ttu-id="666df-139">通过检查包含 API 的类型是否使用 [DualApiPartition](xref:Windows.Foundation.Metadata.DualApiPartitionAttribute) 属性进行标记，可以检查哪些 api 需要打包的应用程序标识。</span><span class="sxs-lookup"><span data-stu-id="666df-139">You can check which APIs need a packaged application identity by inspecting if the type that contains the API is marked with the [DualApiPartition](xref:Windows.Foundation.Metadata.DualApiPartitionAttribute) attribute.</span></span><span data-ttu-id="666df-140">如果是，则可以从未打包的传统桌面应用程序调用。</span><span class="sxs-lookup"><span data-stu-id="666df-140"> If it is, you can call if from an unpackaged traditional desktop app.</span></span> <span data-ttu-id="666df-141">否则，必须使用打包项目的帮助将经典桌面应用转换为 UWP。</span><span class="sxs-lookup"><span data-stu-id="666df-141">Otherwise, you must convert your classic desktop app to a UWP with the help of a packaging project.</span></span>

<https://docs.microsoft.com/windows/desktop/apiindex/uwp-apis-callable-from-a-classic-desktop-app>

#### <a name="benefits-of-packaging"></a><span data-ttu-id="666df-142">打包的优点</span><span class="sxs-lookup"><span data-stu-id="666df-142">Benefits of packaging</span></span>

<span data-ttu-id="666df-143">除了允许您访问这些 Api 之外，您还可以通过为桌面应用程序创建 Windows 应用包来获得一些额外的好处，包括：</span><span class="sxs-lookup"><span data-stu-id="666df-143">Besides giving you access to these APIs, you get some additional benefits by creating a Windows App package for your desktop application including:</span></span>

* <span data-ttu-id="666df-144">**简化的部署**。</span><span class="sxs-lookup"><span data-stu-id="666df-144">**Streamlined deployment**.</span></span> <span data-ttu-id="666df-145">应用具有良好的部署体验，确保用户可以放心地安装应用程序并对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="666df-145">Apps have a great deployment experience ensuring that users can confidently install an application and update it.</span></span> <span data-ttu-id="666df-146">如果用户选择卸载应用程序，则会完全删除该应用程序，而不留下任何跟踪来阻止 Windows rot 问题。</span><span class="sxs-lookup"><span data-stu-id="666df-146">If a user chooses to uninstall the app, it's removed completely with no trace left behind preventing the Windows rot problem.</span></span>

* <span data-ttu-id="666df-147">**自动更新和许可**。</span><span class="sxs-lookup"><span data-stu-id="666df-147">**Automatic updates and licensing**.</span></span> <span data-ttu-id="666df-148">你的应用程序可以参与 Microsoft Store 的内置许可和自动更新功能。</span><span class="sxs-lookup"><span data-stu-id="666df-148">Your application can participate in the Microsoft Store's built-in licensing and automatic update facilities.</span></span> <span data-ttu-id="666df-149">自动更新是高度可靠和高效的机制，因为仅下载文件的已更改部分。</span><span class="sxs-lookup"><span data-stu-id="666df-149">Automatic update is a highly reliable and efficient mechanism, because only the changed parts of files are downloaded.</span></span>

* <span data-ttu-id="666df-150">**扩大了覆盖范围，并简化了盈利**。</span><span class="sxs-lookup"><span data-stu-id="666df-150">**Increased reach and simplified monetization**.</span></span> <span data-ttu-id="666df-151">您可能不是您的情况，但如果您选择通过 Microsoft Store 将您的应用程序分发给数百万个 Windows 10 用户。</span><span class="sxs-lookup"><span data-stu-id="666df-151">Maybe not your case but if you choose to distribute your application through the Microsoft Store you reach millions of Windows 10 users.</span></span>

* <span data-ttu-id="666df-152">**添加 UWP 功能**。</span><span class="sxs-lookup"><span data-stu-id="666df-152">**Add UWP features**.</span></span> <span data-ttu-id="666df-153">您可以按自己的节奏将 UWP 功能添加到应用程序包。</span><span class="sxs-lookup"><span data-stu-id="666df-153">You can add UWP features to your app's package at your own pace.</span></span>

#### <a name="prepare-for-packaging"></a><span data-ttu-id="666df-154">准备打包</span><span class="sxs-lookup"><span data-stu-id="666df-154">Prepare for packaging</span></span>

<span data-ttu-id="666df-155">在开始打包桌面应用程序之前，必须先解决一些要点，然后才能开始此过程。</span><span class="sxs-lookup"><span data-stu-id="666df-155">Before proceeding to package your desktop application, there are some points you have to address before starting the process.</span></span> <span data-ttu-id="666df-156">应用程序必须遵守 Microsoft Store 的规则和策略，并在 UWP 应用程序模型中运行。</span><span class="sxs-lookup"><span data-stu-id="666df-156">Your application must respect any of the Microsoft Store rules and policies and run in the UWP application model.</span></span> <span data-ttu-id="666df-157">例如，必须在 .NET Framework 4.6.2 或更高版本上运行，并写入 `HKEY_CURRENT_USER` 注册表配置单元，并将 AppData 文件夹虚拟化到特定于用户的本地位置。</span><span class="sxs-lookup"><span data-stu-id="666df-157">For example, it has to run on the .NET Framework 4.6.2 or later and writes to the `HKEY_CURRENT_USER` registry hive and the AppData folders will be virtualized to a user-specific app-local location.</span></span>

<span data-ttu-id="666df-158">打包的设计目标是将应用程序状态与系统状态分开，同时保持与其他应用的兼容性。</span><span class="sxs-lookup"><span data-stu-id="666df-158">The design goal for packaging is to separate the application state from system state while maintaining compatibility with other apps.</span></span> <span data-ttu-id="666df-159">Windows 10 通过将应用程序置于 UWP 包内来实现此目标。</span><span class="sxs-lookup"><span data-stu-id="666df-159">Windows 10 accomplishes this goal by placing the application inside a UWP package.</span></span> <span data-ttu-id="666df-160">它在运行时检测并重定向对文件系统和注册表的一些更改，以满足打包提供的应用程序的受信任的干净安装和卸载行为。</span><span class="sxs-lookup"><span data-stu-id="666df-160">It detects and redirects some changes to the file system and registry at run time to fulfill the promise of a trusted and clean install and uninstall behavior of an application provided by packaging.</span></span>

<span data-ttu-id="666df-161">你为桌面应用程序创建的包是仅限桌面的完全信任应用程序，它们不会进行沙盒处理，不过，在应用中应用了轻型虚拟化以写入到 `HKCU` 和 `AppData` 。</span><span class="sxs-lookup"><span data-stu-id="666df-161">Packages that you create for your desktop application are desktop-only, full-trust applications that aren't sandboxed, although there's lightweight virtualization applied to the app for writes to `HKCU` and `AppData`.</span></span> <span data-ttu-id="666df-162">此虚拟化可让他们与经典桌面应用程序相同的方式与其他应用交互。</span><span class="sxs-lookup"><span data-stu-id="666df-162">This virtualization allows them to interact with other apps the same way classic desktop applications do.</span></span>

##### <a name="installation"></a><span data-ttu-id="666df-163">安装</span><span class="sxs-lookup"><span data-stu-id="666df-163">Installation</span></span>

<span data-ttu-id="666df-164">应用包安装在 *% ProgramFiles% \\ WindowsApps \\ package_name* 下，其中包含名为的可执行文件  `app_name.exe` 。</span><span class="sxs-lookup"><span data-stu-id="666df-164">App packages are installed under *%ProgramFiles%\\WindowsApps\\package_name*, with the executable titled `app_name.exe`.</span></span> <span data-ttu-id="666df-165">每个包文件夹都包含一个名为 `AppxManifest.xml`) 的清单 (，其中包含打包应用程序的特殊 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="666df-165">Each package folder contains a manifest (named `AppxManifest.xml`) that contains a special XML namespace for packaged apps.</span></span> <span data-ttu-id="666df-166">在该清单文件中，是一个  `<EntryPoint>`   元素，它引用完全信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-166">Inside that manifest file is an `<EntryPoint>` element, which references the full-trust app.</span></span> <span data-ttu-id="666df-167">当该应用程序启动时，它不会在应用程序容器内运行，而是以用户通常的方式运行。</span><span class="sxs-lookup"><span data-stu-id="666df-167">When that application is launched, it doesn't run inside an app container, but instead it runs as the user as it normally would.</span></span>

<span data-ttu-id="666df-168">部署后，软件包文件由操作系统标记为只读并严格锁定。</span><span class="sxs-lookup"><span data-stu-id="666df-168">After deployment, package files are marked read-only and heavily locked down by the operating system.</span></span> <span data-ttu-id="666df-169">如果这些文件遭到篡改，Windows 将阻止应用启动。</span><span class="sxs-lookup"><span data-stu-id="666df-169">Windows prevents apps from launching if these files are tampered with.</span></span>

##### <a name="file-system"></a><span data-ttu-id="666df-170">文件系统</span><span class="sxs-lookup"><span data-stu-id="666df-170">File system</span></span>

<span data-ttu-id="666df-171">对于打包的桌面应用程序，操作系统支持不同级别的文件系统操作，具体取决于文件夹位置。</span><span class="sxs-lookup"><span data-stu-id="666df-171">The OS supports different levels of file system operations for packaged desktop applications, depending on the folder location.</span></span>

<span data-ttu-id="666df-172">当尝试访问用户的 *AppData* 文件夹时，系统将创建一个专用的每用户、每个应用在幕后的位置。</span><span class="sxs-lookup"><span data-stu-id="666df-172">When trying to access the user's *AppData* folder, the system creates a private per-user, per-app location behind the scenes.</span></span> <span data-ttu-id="666df-173">这将创建打包后的应用程序在实际修改专用副本时编辑真正 *AppData* 的假象。</span><span class="sxs-lookup"><span data-stu-id="666df-173">This creates the illusion that the packaged application is editing the real *AppData* when it's actually modifying a private copy.</span></span> <span data-ttu-id="666df-174">通过以这种方式重定向写入，系统可以跟踪应用所作的所有文件修改。</span><span class="sxs-lookup"><span data-stu-id="666df-174">By redirecting writes this way, the system can track all file modifications made by the app.</span></span> <span data-ttu-id="666df-175">然后，它可以在卸载减少系统 "rot" 时清除所有这些文件，并为用户提供更好的应用程序删除体验。</span><span class="sxs-lookup"><span data-stu-id="666df-175">It can then clean all those files when uninstalling reducing system "rot" and providing a better application removal experience for the user.</span></span>

##### <a name="registry"></a><span data-ttu-id="666df-176">注册表</span><span class="sxs-lookup"><span data-stu-id="666df-176">Registry</span></span>

<span data-ttu-id="666df-177">应用包包含注册表 .dat 文件，该文件  `HKLM\Software`   在实际注册表中充当的逻辑等效项。</span><span class="sxs-lookup"><span data-stu-id="666df-177">App packages contain a registry.dat file, which serves as the logical equivalent of `HKLM\Software` in the real registry.</span></span> <span data-ttu-id="666df-178">在运行时，此虚拟注册表将此配置单元的内容合并到原生系统配置单元，以提供两者的单一视图。</span><span class="sxs-lookup"><span data-stu-id="666df-178">At runtime, this virtual registry merges the contents of this hive into the native system hive to provide a singular view of both.</span></span>

<span data-ttu-id="666df-179">所有写入都将保留在包升级过程中，仅在卸载应用程序时删除。</span><span class="sxs-lookup"><span data-stu-id="666df-179">All writes are kept during package upgrade and only deleted when the application is uninstalled.</span></span>

##### <a name="uninstallation"></a><span data-ttu-id="666df-180">卸载</span><span class="sxs-lookup"><span data-stu-id="666df-180">Uninstallation</span></span>

<span data-ttu-id="666df-181">当用户卸载包时，将删除位于下的所有文件和文件夹  `C:\Program Files\WindowsApps\package_name` ，以及对 AppData 或在该过程中捕获的注册表进行的任何重定向写入操作。</span><span class="sxs-lookup"><span data-stu-id="666df-181">When the user uninstalls a package, all files and folders located under `C:\Program Files\WindowsApps\package_name` are removed, as well as any redirected writes to AppData or the registry that were captured during the process.</span></span>

<span data-ttu-id="666df-182">有关打包应用程序如何处理安装、文件访问、注册表和卸载的详细信息，请参阅 <https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-behind-the-scenes> 。</span><span class="sxs-lookup"><span data-stu-id="666df-182">For details about how a packaged application handles installation, file access, registry, and uninstallation, see <https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-behind-the-scenes>.</span></span>

<span data-ttu-id="666df-183">您可以获取要检查的项目的完整列表 <https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-prepare> 。</span><span class="sxs-lookup"><span data-stu-id="666df-183">You can get a complete list of things to check on <https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-prepare>.</span></span>

## <a name="how-to-add-winrt-apis-to-your-desktop-project"></a><span data-ttu-id="666df-184">如何将 WinRT Api 添加到桌面项目</span><span class="sxs-lookup"><span data-stu-id="666df-184">How to add WinRT APIs to your desktop project</span></span>

<span data-ttu-id="666df-185">在本部分中，可以找到有关如何在现有 WPF 应用程序中集成 Toast 通知的演练。</span><span class="sxs-lookup"><span data-stu-id="666df-185">In this section, you can find a walkthrough on how to integrate Toast Notifications in an existing WPF application.</span></span> <span data-ttu-id="666df-186">尽管代码的观点很简单，但它有助于阐释整个过程。</span><span class="sxs-lookup"><span data-stu-id="666df-186">Although it's simple from the code perspective, it helps illustrate the whole process.</span></span> <span data-ttu-id="666df-187">通知是可在 .NET 应用中使用的众多可用 WinRT Api 之一。</span><span class="sxs-lookup"><span data-stu-id="666df-187">Notifications are one of the many available WinRT APIs available that you can use in .NET app.</span></span> <span data-ttu-id="666df-188">在这种情况下，API 需要包标识。</span><span class="sxs-lookup"><span data-stu-id="666df-188">In this case, the API requires a Package Identity.</span></span> <span data-ttu-id="666df-189">如果 Api 不需要包标识，此过程更加简单。</span><span class="sxs-lookup"><span data-stu-id="666df-189">This process is more straightforward if the APIs don't require Package Identity.</span></span>

<span data-ttu-id="666df-190">让我们使用一个现有的 WPF 示例应用程序，它读取文件并在屏幕上显示其内容。</span><span class="sxs-lookup"><span data-stu-id="666df-190">Let's take an existing WPF sample app that reads files and shows its contents on the screen.</span></span> <span data-ttu-id="666df-191">目标是在应用程序启动时显示 Toast 通知。</span><span class="sxs-lookup"><span data-stu-id="666df-191">The goal is to display a Toast Notification when the application starts.</span></span>

![运行的示例应用程序的屏幕截图](./media/windows-migration/sample-application.png)

<span data-ttu-id="666df-193">首先，应签入以下链接，以确定要使用的 Windows 10 API 是否需要包标识：</span><span class="sxs-lookup"><span data-stu-id="666df-193">First, you should check in the following link whether the Windows 10 API that you'll use requires a Package Identity:</span></span>

<https://docs.microsoft.com/windows/apps/desktop/modernize/desktop-to-uwp-supported-api>

<span data-ttu-id="666df-194">示例将使用 <xref:Windows.UI.Notifications.Notification?displayProperty=nameWithType> 需要打包标识的 API：</span><span class="sxs-lookup"><span data-stu-id="666df-194">Our sample will use the <xref:Windows.UI.Notifications.Notification?displayProperty=nameWithType> API that requires a packaged identity:</span></span>

![Microsoft 文档中的通知类](./media/windows-migration/notification-class-documentation.png)

<span data-ttu-id="666df-196">若要访问 WinRT API，请添加对 NuGet 包的引用， `Microsoft.Windows.SDK.Contracts`   此包将在幕后执行神奇 (查看) 的详细信息 <https://blogs.windows.com/windowsdeveloper/2019/04/30/calling-windows-10-apis-from-a-desktop-application-just-got-easier/> 。</span><span class="sxs-lookup"><span data-stu-id="666df-196">To access the WinRT API, add a reference to the `Microsoft.Windows.SDK.Contracts` NuGet package and this package will do the magic behind the scenes (see details at <https://blogs.windows.com/windowsdeveloper/2019/04/30/calling-windows-10-apis-from-a-desktop-application-just-got-easier/>).</span></span>

<span data-ttu-id="666df-197">你现在已准备好开始添加一些代码。</span><span class="sxs-lookup"><span data-stu-id="666df-197">You're now prepared to start adding some code.</span></span>

<span data-ttu-id="666df-198">创建 `ShowToastNotification` 将在应用程序启动时调用的方法。</span><span class="sxs-lookup"><span data-stu-id="666df-198">Create a `ShowToastNotification` method that will be called on application startup.</span></span> <span data-ttu-id="666df-199">它只是从 XML 模式生成 toast 通知：</span><span class="sxs-lookup"><span data-stu-id="666df-199">It just builds a toast notification from an XML pattern:</span></span>

```csharp
private void ShowNotification(string title, string content, string image)
{
    string xmlString = $@"<toast><visual><binding template = 'ToastGeneric'><text>{title}</text><text>{content}</text><image src=>'{image}'</image></binding></visual></toast>";
    XmlDocument toastXml = new XmlDocument();
    toastXml.LoadXml(xmlString);
    ToastNotification toast = new ToastNotification(toastXml);
    ToastNotificationManager.CreateToastNotifier().Show(toast);
}
```

<span data-ttu-id="666df-200">尽管项目会生成，但会出现错误，因为通知 API 需要包标识，而你未提供。</span><span class="sxs-lookup"><span data-stu-id="666df-200">Although the project builds, there are errors because the Notifications API requires a Package Identity and you didn't provide it.</span></span> <span data-ttu-id="666df-201">将 Windows 打包项目添加到解决方案可以解决此问题：</span><span class="sxs-lookup"><span data-stu-id="666df-201">Adding a Windows Packaging Project to the solution will fix the issue:</span></span>

![Visual Studio 中的 "添加新项目" 对话框的屏幕截图](./media/windows-migration/add-packaging-project.png)

<span data-ttu-id="666df-203">选择要支持的最低 Windows 版本和目标版本。</span><span class="sxs-lookup"><span data-stu-id="666df-203">Select the minimum Windows version you want to support and the version you're targeting.</span></span> <span data-ttu-id="666df-204">并非所有的 WinRT Api 在所有 Windows 10 版本中都受支持。</span><span class="sxs-lookup"><span data-stu-id="666df-204">Not all the WinRT APIs are supported in all Windows 10 versions.</span></span> <span data-ttu-id="666df-205">每个 Windows 10 更新会添加仅在此版本中可用的新 Api;下层支持不可用。</span><span class="sxs-lookup"><span data-stu-id="666df-205">Each Windows 10 update adds new APIs that are only available from this version; down-level support isn't available.</span></span>

![选择最低 Windows 版本](./media/windows-migration/select-versions.png)

<span data-ttu-id="666df-207">下一步是通过添加项目引用将 WPF 应用程序添加到 Windows 打包项目：</span><span class="sxs-lookup"><span data-stu-id="666df-207">Next step is to add the WPF application to the Windows Packaging Project by adding a project reference:</span></span>

![将 WPF 应用程序添加到 Windows 打包项目](./media/windows-migration/add-application.png)

![引用管理器](./media/windows-migration/reference-manager.png)

<span data-ttu-id="666df-210">Windows 打包项目可以打包多个应用，因此应将其设置为入口点：</span><span class="sxs-lookup"><span data-stu-id="666df-210">A Windows Packaging Project can package several apps so you should set which one is the Entry Point:</span></span>

![设置入口点](./media/windows-migration/set-entry-point.png)

<span data-ttu-id="666df-212">下一步是将 WPF 项目设置为解决方案配置中的启动项目。</span><span class="sxs-lookup"><span data-stu-id="666df-212">Next step is to set the WPF Project as the startup Project in the solution configuration.</span></span> <span data-ttu-id="666df-213">可以按 F5 编译并生成并查看结果。</span><span class="sxs-lookup"><span data-stu-id="666df-213">You can press F5 to compile and build and see the results.</span></span>

![运行和显示结果的示例应用程序](./media/windows-migration/sample-app-result.png)

<span data-ttu-id="666df-215">让我们生成包，以便可以安装应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-215">Let's generate the package so you can install your app.</span></span> <span data-ttu-id="666df-216">右键单击 "**存储**  >  **创建应用包**"。</span><span class="sxs-lookup"><span data-stu-id="666df-216">Right click on **Store** > **Create App Packages**.</span></span>

!["创建应用包" 对话框](./media/windows-migration/create-app-packages.png)

<span data-ttu-id="666df-218">选择 "旁加载" 选项以从计算机部署应用：</span><span class="sxs-lookup"><span data-stu-id="666df-218">Select the sideloading option to deploy the app from your machine:</span></span>

![选择旁加载选项](./media/windows-migration/select-sideloading-option.png)

<span data-ttu-id="666df-220">选择应用的应用程序体系结构：</span><span class="sxs-lookup"><span data-stu-id="666df-220">Select the application architecture of your app:</span></span>

![选择应用程序体系结构](./media/windows-migration/select-app-architecture.png)

<span data-ttu-id="666df-222">最后，单击 " **创建**" 创建包。</span><span class="sxs-lookup"><span data-stu-id="666df-222">Finally, create the package by clicking on **Create**.</span></span>

## <a name="xaml-islands"></a><span data-ttu-id="666df-223">XAML 岛</span><span class="sxs-lookup"><span data-stu-id="666df-223">XAML Islands</span></span>

<span data-ttu-id="666df-224">XAML 孤岛是一组组件，使 Windows 桌面开发人员能够在其现有 Win32 应用程序（包括 Windows 窗体和 WPF）上使用 UWP XAML 控件。</span><span class="sxs-lookup"><span data-stu-id="666df-224">XAML Islands are a set of components that enable Windows desktop developers to use UWP XAML controls on their existing Win32 applications, including Windows Forms and WPF.</span></span>

![XAML 孤岛的结构](./media/windows-migration/xaml-islands.png)

<span data-ttu-id="666df-226">你可以使用标准控件以及从现代世界中包含控件的 UWP UI 的 "孤岛" 来图像 Win32 应用。</span><span class="sxs-lookup"><span data-stu-id="666df-226">You can image your Win32 app with your standard controls and among them an "island" of UWP UI containing controls from the modern world.</span></span> <span data-ttu-id="666df-227">此概念类似于在网页中具有显示来自 `different page.`</span><span class="sxs-lookup"><span data-stu-id="666df-227">The concept is similar as having an iFrame inside a web page that shows content from a `different page.`</span></span>

<span data-ttu-id="666df-228">除了从 Windows 10 Api 添加功能外，还可以使用 XAML 孤岛在应用内添加 UWP XAML 片段。</span><span class="sxs-lookup"><span data-stu-id="666df-228">Besides adding functionality from the Windows 10 APIs, you can add pieces of UWP XAML inside of your app using XAML Islands.</span></span>

<span data-ttu-id="666df-229">Windows 10 1903 更新引入了一组 Api，可用于在 Win32 窗口中承载 UWP XAML 内容。</span><span class="sxs-lookup"><span data-stu-id="666df-229">Windows 10 1903 update introduces a set of APIs that allows hosting UWP XAML content in Win32 windows.</span></span> <span data-ttu-id="666df-230">只有在 Windows 10 1903 上运行的应用才能使用 XAML 孤岛。</span><span class="sxs-lookup"><span data-stu-id="666df-230">Only apps running on Windows 10 1903 can use XAML Islands.</span></span>

### <a name="the-road-to-xaml-islands"></a><span data-ttu-id="666df-231">XAML 孤岛的道路</span><span class="sxs-lookup"><span data-stu-id="666df-231">The road to XAML Islands</span></span>

<span data-ttu-id="666df-232">当 Microsoft 引入了 WinRT Api 作为框架，以便在)  (Windows 窗体、WPF 和本机 Win32 应用程序中实现 Win32 应用的现代化时，从2012开始开始 XAML 孤岛。</span><span class="sxs-lookup"><span data-stu-id="666df-232">The road to XAML Islands started in 2012 when Microsoft introduced the WinRT APIs as a framework to modernize the Win32 apps (Windows Forms, WPF, and native Win32 apps).</span></span> <span data-ttu-id="666df-233">但是，WinRT 中的新 UI 控件可用于新应用程序，但不能用于现有应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-233">However, the new UI controls inside WinRT were available for new applications but not for existing ones.</span></span>

<span data-ttu-id="666df-234">在2015和 Windows 10 中，UWP 是出生的。</span><span class="sxs-lookup"><span data-stu-id="666df-234">In 2015, along with Windows 10, UWP was born.</span></span> <span data-ttu-id="666df-235">UWP 允许您创建可跨 Windows 设备（如 XBox、移动和桌面）运行的应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-235">UWP allows you to create apps that work across Windows devices like XBox, Mobile, and Desktop.</span></span> <span data-ttu-id="666df-236">一年后，Microsoft 宣布桌面桥 (以前称为 Project Centennial) 。</span><span class="sxs-lookup"><span data-stu-id="666df-236">One year later, Microsoft announced Desktop Bridge (formerly known as Project Centennial).</span></span> <span data-ttu-id="666df-237">桌面桥是一组工具，使开发人员能够将现有的 Win32 应用程序引入 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="666df-237">Desktop Bridge is a set of tools that allowed developers to bring their existing Win32 apps to the Microsoft Store.</span></span> <span data-ttu-id="666df-238">2017中添加了更多功能，使开发人员能够利用一些新的 Windows 10 Api （例如操作中心的活动磁贴和通知）增强其 Win32 应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-238">More capabilities were added in 2017, allowing developers to enhance their Win32 apps leveraging some of the new Windows 10 APIs, like live tiles and notifications on the action center.</span></span> <span data-ttu-id="666df-239">但仍不存在新的 UI 控件。</span><span class="sxs-lookup"><span data-stu-id="666df-239">But still, no new UI controls.</span></span>

<span data-ttu-id="666df-240">在版本2018中，Microsoft 宣布了一种方法，使开发人员能够将新的 Windows 10 XAML 控件使用到当前的 Win32 应用程序中，而无需将其应用完全迁移到 UWP。</span><span class="sxs-lookup"><span data-stu-id="666df-240">At Build 2018, Microsoft announced a way for developers to use the new Windows 10 XAML controls into their current Win32 apps, without fully migrating their apps to UWP.</span></span> <span data-ttu-id="666df-241">它被标记为 UWP XAML 孤岛。</span><span class="sxs-lookup"><span data-stu-id="666df-241">It was branded as UWP XAML Islands.</span></span>

### <a name="how-it-works"></a><span data-ttu-id="666df-242">工作原理</span><span class="sxs-lookup"><span data-stu-id="666df-242">How it works</span></span>

<span data-ttu-id="666df-243">Windows 10 1903 更新引入了几个 XAML 宿主 Api。</span><span class="sxs-lookup"><span data-stu-id="666df-243">The Windows 10 1903 update introduces several XAML hosting APIs.</span></span> <span data-ttu-id="666df-244">其中两个是 `WindowsXamlManager`   和  `DesktopWindowXamlSource` 。</span><span class="sxs-lookup"><span data-stu-id="666df-244">Two of them are `WindowsXamlManager` and `DesktopWindowXamlSource`.</span></span>

<span data-ttu-id="666df-245"> `WindowsXamlManager`   类处理 UWP XAML 框架。</span><span class="sxs-lookup"><span data-stu-id="666df-245">The `WindowsXamlManager` class handles the UWP XAML Framework.</span></span> <span data-ttu-id="666df-246">它的 `InitializeForCurrentThread` 方法将 UWP XAML 框架加载到 Win32 应用程序的当前线程中。</span><span class="sxs-lookup"><span data-stu-id="666df-246">Its `InitializeForCurrentThread` method loads the UWP XAML Framework inside the current thread of the Win32 app.</span></span>

<span data-ttu-id="666df-247"> `DesktopWindowXamlSource`   是 XAML 岛内容的实例。</span><span class="sxs-lookup"><span data-stu-id="666df-247">The `DesktopWindowXamlSource` is the instance of your XAML Island content.</span></span> <span data-ttu-id="666df-248">它具有 `Content` 用于实例化和设置的属性。</span><span class="sxs-lookup"><span data-stu-id="666df-248">It has the `Content` property, which you're responsible for instantiating and setting.</span></span> <span data-ttu-id="666df-249">`DesktopWindowXamlSource`   呈现并从 HWND 获取其输入。</span><span class="sxs-lookup"><span data-stu-id="666df-249">The `DesktopWindowXamlSource` renders and gets its input from an HWND.</span></span> <span data-ttu-id="666df-250">它需要知道将 XAML 岛附加到哪些其他 HWND，并负责调整和定位父级的 HWND。</span><span class="sxs-lookup"><span data-stu-id="666df-250">It needs to know to which other HWND it will attach the XAML Island's one, and you're responsible for sizing and positioning the parent's HWND.</span></span>

<span data-ttu-id="666df-251">WPF 或 Windows 窗体开发人员通常不会处理其代码中的 HWND，因此，很难理解并处理 HWND 指针和基础布线材料来与 Win32 和 UWP 的世界通信。</span><span class="sxs-lookup"><span data-stu-id="666df-251">WPF or Windows Forms developers don't usually deal with HWND inside their code, so it may be hard to understand and handle HWND pointers and the underlying wiring stuff to communicate Win32 and UWP worlds.</span></span>

#### <a name="the-xaml-islands-net-wrappers"></a><span data-ttu-id="666df-252">XAML 孤岛 .NET 包装</span><span class="sxs-lookup"><span data-stu-id="666df-252">The XAML Islands .NET Wrappers</span></span>

<span data-ttu-id="666df-253">Windows 社区工具包为 WPF 或 Windows 窗体设置了 XAML 孤岛 .NET 包装，使其更易于使用。</span><span class="sxs-lookup"><span data-stu-id="666df-253">The Windows Community Toolkit has a set the XAML Islands .NET wrappers for WPF or Windows Forms that make easier to use XAML Islands.</span></span> <span data-ttu-id="666df-254">这些包装管理 Hwnd、焦点管理和其他功能。</span><span class="sxs-lookup"><span data-stu-id="666df-254">These wrappers manage the HWNDs, the focus management, among other things.</span></span> <span data-ttu-id="666df-255">Windows 窗体和 WPF 开发人员应使用这些包装。</span><span class="sxs-lookup"><span data-stu-id="666df-255">Windows Forms and WPF developers should use these wrappers.</span></span>

<span data-ttu-id="666df-256">Windows 社区工具包提供了两种类型的控件：包装控件和宿主控件。</span><span class="sxs-lookup"><span data-stu-id="666df-256">The Windows Community Toolkit offers two types of controls: Wrapped Controls and Hosting Controls.</span></span>

##### <a name="wrapped-controls"></a><span data-ttu-id="666df-257">包装控件</span><span class="sxs-lookup"><span data-stu-id="666df-257">Wrapped Controls</span></span>

<span data-ttu-id="666df-258">这些包装控件将某些 UWP 控件包装到 Windows 窗体或 WPF 控件中，为这些开发人员隐藏 UWP 概念。</span><span class="sxs-lookup"><span data-stu-id="666df-258">These wrapped controls wrap some UWP controls into Windows Forms or WPF controls, hiding UWP concepts for those developers.</span></span> <span data-ttu-id="666df-259">这些控件包括：</span><span class="sxs-lookup"><span data-stu-id="666df-259">These controls are:</span></span>

* <span data-ttu-id="666df-260">Web 视图和 WebViewCompatible</span><span class="sxs-lookup"><span data-stu-id="666df-260">WebView and WebViewCompatible</span></span>
* <span data-ttu-id="666df-261">InkCanvas 和 InkToolbar</span><span class="sxs-lookup"><span data-stu-id="666df-261">InkCanvas and InkToolbar</span></span>
* <span data-ttu-id="666df-262">MediaPlayerElement</span><span class="sxs-lookup"><span data-stu-id="666df-262">MediaPlayerElement</span></span>
* <span data-ttu-id="666df-263">MapControl</span><span class="sxs-lookup"><span data-stu-id="666df-263">MapControl</span></span>

<span data-ttu-id="666df-264">将 `Microsoft.Toolkit.Wpf.UI.Controls` 包添加到项目中，包括对命名空间的引用，并开始使用。</span><span class="sxs-lookup"><span data-stu-id="666df-264">Add the `Microsoft.Toolkit.Wpf.UI.Controls` package to your project, include the reference to the namespace, and start using them.</span></span>

```xml
<Window
        ...
        xmlns:uwpControls="clr-namespace:Microsoft.Toolkit.Wpf.UI.Controls;assembly=Microsoft.Toolkit.Wpf.UI.Controls">
<Grid>
    <Grid.RowDefinitions>
        <RowDefinition Height="Auto"/>
        <RowDefinition Height="\*"/>
    </Grid.RowDefinitions>
    <uwpControls:InkToolbar TargetInkCanvas="{x:Reference Name=inkCanvas}"/>
    <uwpControls:InkCanvas Grid.Row="1" x:Name="inkCanvas" />
</Grid>
```

##### <a name="hosting-controls"></a><span data-ttu-id="666df-265">宿主控件</span><span class="sxs-lookup"><span data-stu-id="666df-265">Hosting controls</span></span>

<span data-ttu-id="666df-266">XAML 孤岛的强大功能延伸到了多数第一方控件、第三方控件以及为 UWP 开发的自定义控件，这些控件可作为 "孤岛" 集成到 Windows 窗体和 WPF，并具有完整功能的 UI。</span><span class="sxs-lookup"><span data-stu-id="666df-266">The power of XAML Islands extends to most first-party controls, third-party controls, and custom controls developed for UWP, which can be integrated into Windows Forms and WPF as "Islands" with fully functional UI.</span></span> <span data-ttu-id="666df-267">`WindowsXamlHost`WPF 和 Windows 窗体的控件允许执行此操作。</span><span class="sxs-lookup"><span data-stu-id="666df-267">The `WindowsXamlHost` control for WPF and Windows Forms allows doing this.</span></span>

<span data-ttu-id="666df-268">例如，若要 `WindowsXamlHost` 在 WPF 中使用控件，请添加对 `Microsoft.Toolkit.Wpf.UI.XamlHost` Windows 社区工具包提供的包的引用。</span><span class="sxs-lookup"><span data-stu-id="666df-268">For example, to use the `WindowsXamlHost` control in WPF, add a reference to the `Microsoft.Toolkit.Wpf.UI.XamlHost` package provided by the Windows Community Toolkit.</span></span>

<span data-ttu-id="666df-269">将放 `WindowsXamlHost` 入 UI 代码后，指定要加载的 UWP 类型。</span><span class="sxs-lookup"><span data-stu-id="666df-269">Once you've placed your `WindowsXamlHost` into your UI code, specify which UWP type you want to load.</span></span> <span data-ttu-id="666df-270">您可以选择使用被包装的控件，如 `Button` 或由多个不同控件（自定义 UWP 控件）组成的更复杂的控件。</span><span class="sxs-lookup"><span data-stu-id="666df-270">You can choose to use a wrapped control like a `Button` or a more complex one composed by several different controls, which are a custom UWP control.</span></span>

<span data-ttu-id="666df-271">下面的示例演示如何添加 UWP `Button` ：</span><span class="sxs-lookup"><span data-stu-id="666df-271">The following example shows how to add a UWP `Button`:</span></span>

```xml
<Window
        ...
        xmlns:xamlhost="clr-namespace:Microsoft.Toolkit.Wpf.UI.XamlHost;assembly=Microsoft.Toolkit.Wpf.UI.XamlHost">

<xamlhost:WindowsXamlHost x:Name="myUwpButton"
                          InitialTypeName="Windows.UI.Xaml.Controls.Button" />
```

<span data-ttu-id="666df-272">对于如何实现此操作，有一个清晰的建议，更好的是，有一个包含自定义复合控件的单个和更大的 XAML 岛，而不是每个都有一个控件。</span><span class="sxs-lookup"><span data-stu-id="666df-272">There's a clear recommendation on how to approach this and it's better to have one single and bigger XAML Island containing a custom composite control than to have several islands with one control on each.</span></span>

<span data-ttu-id="666df-273">XAML 的核心功能之一是绑定，它在 Win32 代码和岛之间有效。</span><span class="sxs-lookup"><span data-stu-id="666df-273">One of the core features of XAML is binding and it works between your Win32 code and the island.</span></span> <span data-ttu-id="666df-274">因此，您可以绑定 `Textbox` 具有 UWP 的 Win32 `Textbox` 。</span><span class="sxs-lookup"><span data-stu-id="666df-274">So, you can bind, for instance, a Win32 `Textbox` with a UWP `Textbox`.</span></span> <span data-ttu-id="666df-275">需要考虑的一个重要事项是，这些绑定是从 UWP 到 Win32 的单向绑定，因此，如果在 `Textbox` XAML 岛内部更新，Win32 文本框将会更新，但不会被更新。</span><span class="sxs-lookup"><span data-stu-id="666df-275">One important thing to consider is that these bindings are one-way bindings, from UWP to Win32, so if you update the `Textbox` inside the XAML Island the Win32 Textbox will be updated, but not the other way around.</span></span>

<span data-ttu-id="666df-276">若要查看有关如何使用 XAML 孤岛的演练，请参阅：</span><span class="sxs-lookup"><span data-stu-id="666df-276">To see a walkthrough about how to use XAML Islands, see:</span></span>

<https://docs.microsoft.com/windows/apps/desktop/modernize/host-standard-control-with-xaml-islands>

#### <a name="adding-uwp-xaml-custom-controls"></a><span data-ttu-id="666df-277">添加 UWP XAML 自定义控件</span><span class="sxs-lookup"><span data-stu-id="666df-277">Adding UWP XAML custom controls</span></span>

<span data-ttu-id="666df-278">XAML 自定义控件是由你或第三方) 创建的控件 (或用户控件， (包括 WinUI 1.x 控件) 。</span><span class="sxs-lookup"><span data-stu-id="666df-278">A XAML custom control is a control (or user control) created by you or by third parties (including WinUI 2.x controls).</span></span> <span data-ttu-id="666df-279">若要在 Windows 窗体或 WPF 应用程序中托管自定义 UWP 控件，你将需要：</span><span class="sxs-lookup"><span data-stu-id="666df-279">To host a custom UWP control in a Windows Forms or WPF app, you'll need:</span></span>

- <span data-ttu-id="666df-280">`WindowsXamlHost`在 .Net Core 2.x 应用中使用 UWP 控件。</span><span class="sxs-lookup"><span data-stu-id="666df-280">To use the `WindowsXamlHost` UWP control in your .NET Core 3.x app.</span></span>
- <span data-ttu-id="666df-281">若要创建定义对象的 UWP 应用项目，则为 `XamlApplication` 。</span><span class="sxs-lookup"><span data-stu-id="666df-281">To create a UWP app project that defines a `XamlApplication` object.</span></span>

<span data-ttu-id="666df-282">WPF 或 Windows 窗体项目必须有权访问 `Microsoft.Toolkit.Win32.UI.XamlHost.XamlApplication` Windows 社区工具包提供的类的实例。</span><span class="sxs-lookup"><span data-stu-id="666df-282">Your WPF or Windows Forms project must have access to an instance of the `Microsoft.Toolkit.Win32.UI.XamlHost.XamlApplication` class provided by the Windows Community Toolkit.</span></span> <span data-ttu-id="666df-283">此对象用作根元数据提供程序，用于为应用程序的当前目录中的程序集中的自定义 UWP XAML 类型加载元数据。</span><span class="sxs-lookup"><span data-stu-id="666df-283">This object acts as a root metadata provider for loading metadata for custom UWP XAML types in assemblies in the current directory of your application.</span></span> <span data-ttu-id="666df-284">执行此操作的建议方法是将 (通用 Windows) 项目的空白应用添加到与 WPF 或 Windows 窗体项目相同的解决方案，然后修改此项目中的默认应用类。</span><span class="sxs-lookup"><span data-stu-id="666df-284">The recommended way to do this is to add a Blank App (Universal Windows) project to the same solution as your WPF or Windows Forms project and revise the default App class in this project.</span></span>

<span data-ttu-id="666df-285">自定义 UWP XAML 控件可包含在此 UWP 应用或独立 UWP 类库项目中，您可以在与 WPF 或 Windows 窗体项目相同的解决方案中引用该项目。</span><span class="sxs-lookup"><span data-stu-id="666df-285">The custom UWP XAML control can be included on this UWP app or in an independent UWP Class Library project that you reference in the same solution as your WPF or Windows Forms project.</span></span>

<span data-ttu-id="666df-286">可以在以下位置查看详细的分步过程说明：</span><span class="sxs-lookup"><span data-stu-id="666df-286">You can check a detailed step-by-step process description at:</span></span>

<https://docs.microsoft.com/windows/apps/desktop/modernize/host-custom-control-with-xaml-islands>

#### <a name="the-windows-ui-library-winui-2"></a><span data-ttu-id="666df-287">Windows UI 库 (WinUI 2) </span><span class="sxs-lookup"><span data-stu-id="666df-287">The Windows UI Library (WinUI 2)</span></span>

<span data-ttu-id="666df-288">除了操作系统附带的收件箱 Windows 10 控件外，同一 UWP XAML 团队还在 Windows UI 库中提供了其他控件， (**WinUI 2**) 。</span><span class="sxs-lookup"><span data-stu-id="666df-288">Besides the inbox Windows 10 controls that comes with the OS, the same UWP XAML team also deliver additional controls in the Windows UI Library (**WinUI 2**).</span></span> <span data-ttu-id="666df-289">WinUI 2 为 Windows UWP 应用提供官方的本机 Microsoft UI 控件和功能，这些控件可以在 XAML 孤岛内使用。</span><span class="sxs-lookup"><span data-stu-id="666df-289">WinUI 2 provides official native Microsoft UI controls and features for Windows UWP apps and these controls can be used inside of XAML Islands.</span></span>

<span data-ttu-id="666df-290">WinUI 2 是开源的，你可以在中找到信息 <https://github.com/microsoft/microsoft-ui-xaml> 。</span><span class="sxs-lookup"><span data-stu-id="666df-290">WinUI 2 is open source and you can find information at <https://github.com/microsoft/microsoft-ui-xaml>.</span></span>

<span data-ttu-id="666df-291">以下文章演示了如何从 WinUI 2 库承载 UWP XAML 控件： <https://docs.microsoft.com/windows/apps/desktop/modernize/host-custom-control-with-xaml-islands></span><span class="sxs-lookup"><span data-stu-id="666df-291">The following article demonstrates how to host a UWP XAML control from the WinUI 2 library: <https://docs.microsoft.com/windows/apps/desktop/modernize/host-custom-control-with-xaml-islands></span></span>

### <a name="do-you-need-xaml-islands"></a><span data-ttu-id="666df-292">是否需要 XAML 孤岛</span><span class="sxs-lookup"><span data-stu-id="666df-292">Do you need XAML Islands</span></span>

<span data-ttu-id="666df-293">XAML 孤岛适用于那些希望通过利用新的 UWP 控件和行为而无需完全重写应用程序来改善用户体验的现有 Win32 应用程序。</span><span class="sxs-lookup"><span data-stu-id="666df-293">XAML Islands are intended for existing Win32 apps that want to improve their user experience by leveraging new UWP controls and behaviors without a full rewrite of the app.</span></span> <span data-ttu-id="666df-294">你可以使用 [Windows 10 api](/windows/uwp/porting/desktop-to-uwp-enhance)，但在 XAML 孤岛之前，只需要使用非 UI 相关的 api。</span><span class="sxs-lookup"><span data-stu-id="666df-294">You could already [leverage Windows 10 APIs](/windows/uwp/porting/desktop-to-uwp-enhance), but up until XAML Islands, only non-UI related APIs.</span></span>

<span data-ttu-id="666df-295">如果要开发新的 Windows 应用程序， [UWP 应用程序](/windows/uwp/get-started/universal-application-platform-guide)   可能是正确的方法。</span><span class="sxs-lookup"><span data-stu-id="666df-295">If you're developing a new Windows App, a [UWP App](/windows/uwp/get-started/universal-application-platform-guide) is probably the right approach.</span></span>

### <a name="the-road-ahead-xaml-islands-winui-30"></a><span data-ttu-id="666df-296">更快的 XAML 孤岛： WinUI 3。0</span><span class="sxs-lookup"><span data-stu-id="666df-296">The road ahead XAML Islands: WinUI 3.0</span></span>

<span data-ttu-id="666df-297">自 Windows 8 起，Windows UI 平台（包括 XAML UI 框架、视觉组合层和输入处理）已作为 Windows 的一个有机组成部分提供。</span><span class="sxs-lookup"><span data-stu-id="666df-297">Since Windows 8, the Windows UI platform, including the XAML UI framework, visual composition layer, and input processing has been shipped as an integral part of Windows.</span></span> <span data-ttu-id="666df-298">这意味着，若要从对 UI 技术的最新改进中受益，你必须升级到最新版本的 UI，并在开发应用时降低创新速度。</span><span class="sxs-lookup"><span data-stu-id="666df-298">This means that to benefit from the latest improvements on UI technologies, you must upgrade to the latest version of the UI, slowing down the pace of innovation when you develop your apps.</span></span> <span data-ttu-id="666df-299">为了使这两个发展周期和促进创新，Microsoft 正在积极处理 WinUI 项目。</span><span class="sxs-lookup"><span data-stu-id="666df-299">To decouple these two evolution cycles and foster innovation, Microsoft is actively working on the WinUI project.</span></span>

<span data-ttu-id="666df-300">从2018中的 WinUI 2 开始，Microsoft 已开始将一些新的 XAML UI 控件和功能作为构建于 UWP SDK 顶层的单独 NuGet 包交付。</span><span class="sxs-lookup"><span data-stu-id="666df-300">Starting with WinUI 2 in 2018, Microsoft started shipping some new XAML UI controls and features as separate NuGet packages that build on top of the UWP SDK.</span></span>

![WinUI 2.0 的结构](./media/windows-migration/winui2.png)

<span data-ttu-id="666df-302">WinUI 3 处于积极开发阶段，将极大地扩展 WinUI 的作用域，以包括完全与 UWP SDK 完全分离的完整 UI 平台：</span><span class="sxs-lookup"><span data-stu-id="666df-302">WinUI 3 is under active development and will greatly expand the scope of WinUI to include the full UI platform, which will be fully decoupled from the UWP SDK:</span></span>

![WinUI 3.0 的结构](./media/windows-migration/winui3.png)

<span data-ttu-id="666df-304">XAML 框架现在将在 GitHub 上开发，并以 [NuGet](/nuget/what-is-nuget)包的形式提供   。</span><span class="sxs-lookup"><span data-stu-id="666df-304">XAML framework will now be developed on GitHub and shipped out of band as [NuGet](/nuget/what-is-nuget) packages.</span></span>

<span data-ttu-id="666df-305">作为 OS 的一部分发布的现有 UWP XAML API 将不会再收到新的功能更新。</span><span class="sxs-lookup"><span data-stu-id="666df-305">The existing UWP XAML APIs that ship as part of the OS will no longer receive new feature updates.</span></span> <span data-ttu-id="666df-306">它们仍将根据 Windows 10 支持生命周期收到安全更新和关键修复程序。</span><span class="sxs-lookup"><span data-stu-id="666df-306">They will still receive security updates and critical fixes according to the Windows 10 support lifecycle.</span></span>

<span data-ttu-id="666df-307">通用 Windows 平台包含的不仅仅是 XAML 框架 (例如，应用程序和安全模型、媒体管道、Xbox 和 Windows 10 shell 集成、广泛的设备支持) 并将继续发展。</span><span class="sxs-lookup"><span data-stu-id="666df-307">The Universal Windows Platform contains more than just the XAML framework (for example, application and security model, media pipeline, Xbox and Windows 10 shell integrations, broad device support) and will continue to evolve.</span></span> <span data-ttu-id="666df-308">所有新的 XAML 功能都将作为 WinUI 的一部分进行开发和交付。</span><span class="sxs-lookup"><span data-stu-id="666df-308">All new XAML features will just be developed and ship as part of WinUI instead.</span></span>

#### <a name="winui-3-in-desktop-app-and-winui-xaml-islands"></a><span data-ttu-id="666df-309">桌面应用中的 WinUI 3 和 WinUI XAML 孤岛</span><span class="sxs-lookup"><span data-stu-id="666df-309">WinUI 3 in desktop app and WinUI XAML Islands</span></span>

<span data-ttu-id="666df-310">正如您所看到的，WinUI 3 是 UWP XAML 的演变，它在 UWP 应用模型中自然运行，并且其所有要求都 (.MSIX 打包 ID、沙箱、CoreWindow 等。</span><span class="sxs-lookup"><span data-stu-id="666df-310">As you can see, WinUI 3 is the evolution of UWP XAML and it works naturally within the UWP app model and all its requirements (MSIX packaged ID, sandbox, CoreWindow, and so on.</span></span> <span data-ttu-id="666df-311">若要仅在 Win32 应用模型中使用 WinUI 3，WinUI 内容应由另一个 UI 框架承载 (Windows 窗体、WPF 等) 使用 **WINUI XAML 孤岛**。</span><span class="sxs-lookup"><span data-stu-id="666df-311">To use just WinUI 3 in a Win32 app model, the WinUI content should be hosted by another UI Framework (Windows Forms, WPF, and so on) using **WinUI XAML Islands**.</span></span> <span data-ttu-id="666df-312">如果要改进应用和混合技术，这是正确的路径。</span><span class="sxs-lookup"><span data-stu-id="666df-312">This is the right path if you want to evolve your app and mix technologies.</span></span> <span data-ttu-id="666df-313">但是，如果要替换 WinUI 的整个旧 UI，应用程序不应加载 UI 框架，只需托管 WinUI 即可。</span><span class="sxs-lookup"><span data-stu-id="666df-313">However, if you want to replace your entire old UI for WinUI, your app shouldn't load UI Frameworks for just hosting WinUI.</span></span>

<span data-ttu-id="666df-314">WinUI 3 将解决 **在桌面应用中添加 WinUI 的** 关键反馈。</span><span class="sxs-lookup"><span data-stu-id="666df-314">WinUI 3 will address this critical feedback adding **WinUI in desktop apps**.</span></span> <span data-ttu-id="666df-315">这将允许 Win32 应用程序使用 WinUI 3 作为独立 UI 框架;无需加载 Windows 窗体或 WPF。</span><span class="sxs-lookup"><span data-stu-id="666df-315">This will allow that Win32 apps can use WinUI 3 as standalone UI Framework; no need to load Windows Forms or WPF.</span></span>

<span data-ttu-id="666df-316">在此聚合内，WinUI 3 将让开发人员轻松地混合和匹配的正确组合：</span><span class="sxs-lookup"><span data-stu-id="666df-316">Within this aggregation, WinUI 3 will let developers easily mix and match the right combination of:</span></span>

* <span data-ttu-id="666df-317">应用模型： UWP，Win32</span><span class="sxs-lookup"><span data-stu-id="666df-317">App model: UWP, Win32</span></span>
* <span data-ttu-id="666df-318">平台： .NET Core 或本机</span><span class="sxs-lookup"><span data-stu-id="666df-318">Platform: .NET Core or Native</span></span>
* <span data-ttu-id="666df-319">语言： .NET (C \# ，Visual Basic) ，标准 c + +</span><span class="sxs-lookup"><span data-stu-id="666df-319">Language: .NET (C\#, Visual Basic), standard C++</span></span>
* <span data-ttu-id="666df-320">打包： .MSIX，AppX 用于 Microsoft Store，未打包</span><span class="sxs-lookup"><span data-stu-id="666df-320">Packaging: MSIX, AppX for the Microsoft Store, unpackaged</span></span>
* <span data-ttu-id="666df-321">互操作：使用 WinUI 3，使用 WinUI XAML 孤岛扩展现有 WPF、WinForms 和 MFC 应用。</span><span class="sxs-lookup"><span data-stu-id="666df-321">Interop: use WinUI 3 to extend existing WPF, WinForms, and MFC apps using WinUI XAML Islands.</span></span>

<span data-ttu-id="666df-322">如果希望了解更多详细信息，Microsoft 将在中共享此路线图 <https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md> 。</span><span class="sxs-lookup"><span data-stu-id="666df-322">If you want to know more details, Microsoft is sharing this roadmap in <https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md>.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="666df-323">[上一页](migrate-modern-applications.md)
>[下一页](example-migration-core.md)</span><span class="sxs-lookup"><span data-stu-id="666df-323">[Previous](migrate-modern-applications.md)
[Next](example-migration-core.md)</span></span>
