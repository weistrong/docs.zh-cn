---
description: 详细了解：演练：创建自定义日志侦听器 (Visual Basic)
title: 创建自定义日志侦听器
ms.date: 07/20/2015
helpviewer_keywords:
- custom log listeners
- My.Application.Log object, custom log listeners
ms.assetid: 0e019115-4b25-4820-afb1-af8c6e391698
ms.openlocfilehash: bc5e1743eeaec427adf909ca95aa1979ce61a993
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792292"
---
# <a name="walkthrough-creating-custom-log-listeners-visual-basic"></a><span data-ttu-id="cb6cc-103">演练：创建自定义日志侦听器 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cb6cc-103">Walkthrough: Creating Custom Log Listeners (Visual Basic)</span></span>

<span data-ttu-id="cb6cc-104">本演练演示如何创建自定义日志侦听器，并将其配置为侦听 `My.Application.Log` 对象的输出。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-104">This walkthrough demonstrates how to create a custom log listener and configure it to listen to the output of the `My.Application.Log` object.</span></span>

## <a name="getting-started"></a><span data-ttu-id="cb6cc-105">入门</span><span class="sxs-lookup"><span data-stu-id="cb6cc-105">Getting Started</span></span>

<span data-ttu-id="cb6cc-106">日志侦听器必须继承自 <xref:System.Diagnostics.TraceListener> 类。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-106">Log listeners must inherit from the <xref:System.Diagnostics.TraceListener> class.</span></span>

#### <a name="to-create-the-listener"></a><span data-ttu-id="cb6cc-107">创建侦听器</span><span class="sxs-lookup"><span data-stu-id="cb6cc-107">To create the listener</span></span>

- <span data-ttu-id="cb6cc-108">在应用程序中，创建继承自 <xref:System.Diagnostics.TraceListener> 的类，其名称为 `SimpleListener`。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-108">In your application, create a class named `SimpleListener` that inherits from <xref:System.Diagnostics.TraceListener>.</span></span>

     [!code-vb[VbVbalrMyApplicationLog#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/Form1.vb#16)]

     <span data-ttu-id="cb6cc-109">基类所需的 <xref:System.Diagnostics.TraceListener.Write%2A> 和 <xref:System.Diagnostics.TraceListener.WriteLine%2A> 方法调用 `MsgBox`，以显示其输入。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-109">The <xref:System.Diagnostics.TraceListener.Write%2A> and <xref:System.Diagnostics.TraceListener.WriteLine%2A> methods, required by the base class, call `MsgBox` to display their input.</span></span>

     <span data-ttu-id="cb6cc-110"><xref:System.Security.Permissions.HostProtectionAttribute> 特性应用于 <xref:System.Diagnostics.TraceListener.Write%2A> 和 <xref:System.Diagnostics.TraceListener.WriteLine%2A> 方法，使其特性与基类方法匹配。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-110">The <xref:System.Security.Permissions.HostProtectionAttribute> attribute is applied to the <xref:System.Diagnostics.TraceListener.Write%2A> and <xref:System.Diagnostics.TraceListener.WriteLine%2A> methods so that their attributes match the base class methods.</span></span> <span data-ttu-id="cb6cc-111"><xref:System.Security.Permissions.HostProtectionAttribute> 特性使运行代码的主机能够确定代码会公开主机保护同步。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-111">The <xref:System.Security.Permissions.HostProtectionAttribute> attribute allows the host that runs the code to determine that the code exposes host-protection synchronization.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb6cc-112"><xref:System.Security.Permissions.HostProtectionAttribute> 特性仅在可托管公共语言运行时且实现主机保护的非托管应用程序上有效，如 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-112">The <xref:System.Security.Permissions.HostProtectionAttribute> attribute is effective only on unmanaged applications that host the common language runtime and that implement host protection, such as SQL Server.</span></span>

<span data-ttu-id="cb6cc-113">若要确保 `My.Application.Log` 使用日志侦听器，应对包含日志侦听器的程序集执行强名称。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-113">To ensure that `My.Application.Log` uses your log listener, you should strongly name the assembly that contains your log listener.</span></span>

<span data-ttu-id="cb6cc-114">接下来的过程提供一些用于创建强名称日志侦听器程序集的简单步骤。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-114">The next procedure provides some simple steps for creating a strongly named log-listener assembly.</span></span> <span data-ttu-id="cb6cc-115">有关详细信息，请参阅[创建和使用具有强名称的程序集](../../../../standard/assembly/create-use-strong-named.md)。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-115">For more information, see [Creating and Using Strong-Named Assemblies](../../../../standard/assembly/create-use-strong-named.md).</span></span>

#### <a name="to-strongly-name-the-log-listener-assembly"></a><span data-ttu-id="cb6cc-116">对日志侦听器程序集执行强名称</span><span class="sxs-lookup"><span data-stu-id="cb6cc-116">To strongly name the log-listener assembly</span></span>

1. <span data-ttu-id="cb6cc-117">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-117">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="cb6cc-118">在 **“项目”** 菜单上，选择 **“属性”** 。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-118">On the **Project** menu, choose **Properties**.</span></span>

2. <span data-ttu-id="cb6cc-119">单击“签名”选项卡。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-119">Click the **Signing** tab.</span></span>

3. <span data-ttu-id="cb6cc-120">选择“为程序集签名”框。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-120">Select the **Sign the assembly** box.</span></span>

4. <span data-ttu-id="cb6cc-121">在“选择强名称密钥文件”下拉列表中，选择“\<New>”。 </span><span class="sxs-lookup"><span data-stu-id="cb6cc-121">Select **\<New>** from the **Choose a strong name key file** drop-down list.</span></span>

     <span data-ttu-id="cb6cc-122">将打开“创建强名称密钥”对话框。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-122">The **Create Strong Name Key** dialog box opens.</span></span>

5. <span data-ttu-id="cb6cc-123">在“密钥文件名”框中提供密钥文件的名称。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-123">Provide a name for the key file in the **Key file name** box.</span></span>

6. <span data-ttu-id="cb6cc-124">在“输入密码”和“确认密码”框中输入密码。 </span><span class="sxs-lookup"><span data-stu-id="cb6cc-124">Enter a password in the **Enter password** and **Confirm password** boxes.</span></span>

7. <span data-ttu-id="cb6cc-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-125">Click **OK**.</span></span>

8. <span data-ttu-id="cb6cc-126">重新生成应用程序。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-126">Rebuild the application.</span></span>

## <a name="adding-the-listener"></a><span data-ttu-id="cb6cc-127">添加侦听器</span><span class="sxs-lookup"><span data-stu-id="cb6cc-127">Adding the Listener</span></span>

<span data-ttu-id="cb6cc-128">现在程序集已具有强名称，需要确定侦听器的强名称，以便 `My.Application.Log` 使用日志侦听器。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-128">Now that the assembly has a strong name, you need to determine the strong name of the listener so that `My.Application.Log` uses your log listener.</span></span>

<span data-ttu-id="cb6cc-129">强名称类型的格式如下所示。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-129">The format of a strongly named type is as follows.</span></span>

<span data-ttu-id="cb6cc-130">\<type name>, \<assembly name>, \<version number>, \<culture>, \<strong name></span><span class="sxs-lookup"><span data-stu-id="cb6cc-130">\<type name>, \<assembly name>, \<version number>, \<culture>, \<strong name></span></span>

#### <a name="to-determine-the-strong-name-of-the-listener"></a><span data-ttu-id="cb6cc-131">确定侦听器的强名称</span><span class="sxs-lookup"><span data-stu-id="cb6cc-131">To determine the strong name of the listener</span></span>

- <span data-ttu-id="cb6cc-132">以下代码演示如何确定 `SimpleListener` 的强名称类型名称。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-132">The following code shows how to determine the strongly named type name for `SimpleListener`.</span></span>

     [!code-vb[VbVbalrMyApplicationLog#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/Form1.vb#17)]

     <span data-ttu-id="cb6cc-133">该类型的强名称取决于项目。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-133">The strong name of the type depends on your project.</span></span>

<span data-ttu-id="cb6cc-134">借助强名称，可以将侦听器添加到 `My.Application.Log` 日志侦听器集合中。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-134">With the strong name, you can add the listener to the `My.Application.Log` log-listener collection.</span></span>

#### <a name="to-add-the-listener-to-myapplicationlog"></a><span data-ttu-id="cb6cc-135">将侦听器添加到 My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="cb6cc-135">To add the listener to My.Application.Log</span></span>

1. <span data-ttu-id="cb6cc-136">在“解决方案资源管理器”中右键单击 app.config，然后选择“打开”。 </span><span class="sxs-lookup"><span data-stu-id="cb6cc-136">Right-click on app.config in the **Solution Explorer** and choose **Open**.</span></span>

     <span data-ttu-id="cb6cc-137">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="cb6cc-137">-or-</span></span>

     <span data-ttu-id="cb6cc-138">如果其中有 app.config 文件：</span><span class="sxs-lookup"><span data-stu-id="cb6cc-138">If there is an app.config file:</span></span>

    1. <span data-ttu-id="cb6cc-139">在 **“项目”** 菜单上选择 **“添加新项”** 。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-139">On the **Project** menu, choose **Add New Item**.</span></span>

    2. <span data-ttu-id="cb6cc-140">在“添加新项”  对话框中，选择“应用程序配置文件”  。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-140">From the **Add New Item** dialog box, choose **Application Configuration File**.</span></span>

    3. <span data-ttu-id="cb6cc-141">单击 **添加**。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-141">Click **Add**.</span></span>

2. <span data-ttu-id="cb6cc-142">找到 `<listeners>` 部分，该部分位于 `<source>` 属性为“DefaultSource”的 `name` 部分当中，后者又位于 `<sources>` 部分之下。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-142">Locate the `<listeners>` section, in the `<source>` section with the `name` attribute "DefaultSource", located in the `<sources>` section.</span></span> <span data-ttu-id="cb6cc-143">`<sources>` 部分位于 `<system.diagnostics>` 部分当中，后者又位于顶级 `<configuration>` 部分之下。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-143">The `<sources>` section is located in the `<system.diagnostics>` section, in the top-level `<configuration>` section.</span></span>

3. <span data-ttu-id="cb6cc-144">将此元素添加到 `<listeners>` 部分：</span><span class="sxs-lookup"><span data-stu-id="cb6cc-144">Add this element to the `<listeners>` section:</span></span>

    ```xml
    <add name="SimpleLog" />
    ```

4. <span data-ttu-id="cb6cc-145">找到 `<sharedListeners>` 部分，该部分位于 `<system.diagnostics>` 部分当中，后者又位于顶级 `<configuration>` 部分之下。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-145">Locate the `<sharedListeners>` section, in the `<system.diagnostics>` section, in the top-level `<configuration>` section.</span></span>

5. <span data-ttu-id="cb6cc-146">将此元素添加到该 `<sharedListeners>` 部分：</span><span class="sxs-lookup"><span data-stu-id="cb6cc-146">Add this element to that `<sharedListeners>` section:</span></span>

    ```xml
    <add name="SimpleLog" type="SimpleLogStrongName" />
    ```

     <span data-ttu-id="cb6cc-147">将 `SimpleLogStrongName` 的值更改为该侦听器的强名称。</span><span class="sxs-lookup"><span data-stu-id="cb6cc-147">Change the value of `SimpleLogStrongName` to be the strong name of the listener.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb6cc-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb6cc-148">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- [<span data-ttu-id="cb6cc-149">使用应用程序日志</span><span class="sxs-lookup"><span data-stu-id="cb6cc-149">Working with Application Logs</span></span>](working-with-application-logs.md)
- [<span data-ttu-id="cb6cc-150">如何：日志异常</span><span class="sxs-lookup"><span data-stu-id="cb6cc-150">How to: Log Exceptions</span></span>](how-to-log-exceptions.md)
- [<span data-ttu-id="cb6cc-151">如何：写入日志消息</span><span class="sxs-lookup"><span data-stu-id="cb6cc-151">How to: Write Log Messages</span></span>](how-to-write-log-messages.md)
- [<span data-ttu-id="cb6cc-152">演练：更改 My.Application.Log 在哪里写入信息</span><span class="sxs-lookup"><span data-stu-id="cb6cc-152">Walkthrough: Changing Where My.Application.Log Writes Information</span></span>](walkthrough-changing-where-my-application-log-writes-information.md)
