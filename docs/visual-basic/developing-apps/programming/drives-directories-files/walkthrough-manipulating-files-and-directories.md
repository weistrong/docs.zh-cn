---
description: 详细了解：演练：在 Visual Basic 中操作文件和目录
title: 操作文件和目录
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], reading text
- reading files [Visual Basic], text
- I/O [Visual Basic], walkthroughs
- text, writing to files
- text, reading from files
- reading text from files [Visual Basic], walkthroughs
- Visual Basic code, file access
- files [Visual Basic], writing text
- I/O [Visual Basic], writing text to files
- file access, walkthroughs
- writing to files [Visual Basic], walkthroughs
- I/O [Visual Basic], reading text from files
ms.assetid: cae77565-9f78-4e46-8e42-eb2f9f8e1ffd
ms.openlocfilehash: 315635ee43ee4d4956fc35b7f9bc635b374646f8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99775378"
---
# <a name="walkthrough-manipulating-files-and-directories-in-visual-basic"></a><span data-ttu-id="47e8a-103">演练：在 Visual Basic 中操作文件和目录</span><span class="sxs-lookup"><span data-stu-id="47e8a-103">Walkthrough: Manipulating Files and Directories in Visual Basic</span></span>

<span data-ttu-id="47e8a-104">本演练简单介绍 Visual Basic 中文件 I/O 的基础知识。</span><span class="sxs-lookup"><span data-stu-id="47e8a-104">This walkthrough provides an introduction to the fundamentals of file I/O in Visual Basic.</span></span> <span data-ttu-id="47e8a-105">描述如何创建列出并检查目录中文本文件的小型应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-105">It describes how to create a small application that lists and examines text files in a directory.</span></span> <span data-ttu-id="47e8a-106">对于所选的每个文本文件，该应用程序都会提供文件属性和内容的第一行。</span><span class="sxs-lookup"><span data-stu-id="47e8a-106">For each selected text file, the application provides file attributes and the first line of content.</span></span> <span data-ttu-id="47e8a-107">可以选择将信息写入日志文件中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-107">There is an option to write information to a log file.</span></span>  
  
 <span data-ttu-id="47e8a-108">本演练使用 `My.Computer.FileSystem Object` 的成员，这些成员可从 Visual Basic 中获得。</span><span class="sxs-lookup"><span data-stu-id="47e8a-108">This walkthrough uses members of the `My.Computer.FileSystem Object`, which are available in Visual Basic.</span></span> <span data-ttu-id="47e8a-109">有关详细信息，请参阅<xref:Microsoft.VisualBasic.FileIO.FileSystem>。</span><span class="sxs-lookup"><span data-stu-id="47e8a-109">See <xref:Microsoft.VisualBasic.FileIO.FileSystem> for more information.</span></span> <span data-ttu-id="47e8a-110">本演练结尾部分提供等效示例，该示例使用来自 <xref:System.IO> 命名空间的类。</span><span class="sxs-lookup"><span data-stu-id="47e8a-110">At the end of the walkthrough, an equivalent example is provided that uses classes from the <xref:System.IO> namespace.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-the-project"></a><span data-ttu-id="47e8a-111">创建项目</span><span class="sxs-lookup"><span data-stu-id="47e8a-111">To create the project</span></span>  
  
1. <span data-ttu-id="47e8a-112">在“文件”菜单上，单击“新建项目”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-112">On the **File** menu, click **New Project**.</span></span>  
  
     <span data-ttu-id="47e8a-113">将显示“新建项目”对话框。</span><span class="sxs-lookup"><span data-stu-id="47e8a-113">The **New Project** dialog box appears.</span></span>  
  
2. <span data-ttu-id="47e8a-114">在“已安装的模板”窗格中，展开“Visual Basic”，然后单击“Windows”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-114">In the **Installed Templates** pane, expand **Visual Basic**, and then click **Windows**.</span></span> <span data-ttu-id="47e8a-115">在中间的“模板”窗格中，单击“Windows 窗体应用程序”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-115">In the **Templates** pane in the middle, click **Windows Forms Application**.</span></span>  
  
3. <span data-ttu-id="47e8a-116">在“名称”框中，键入 `FileExplorer` 以设置项目名称，然后单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-116">In the **Name** box, type `FileExplorer` to set the project name, and then click **OK**.</span></span>  
  
     <span data-ttu-id="47e8a-117">Visual Studio 将项目添加到“解决方案资源管理器”中，“Windows 窗体设计器”随即打开。</span><span class="sxs-lookup"><span data-stu-id="47e8a-117">Visual Studio adds the project to **Solution Explorer**, and the Windows Forms Designer opens.</span></span>  
  
4. <span data-ttu-id="47e8a-118">将下表中的控件添加到窗体，并设置控件属性相应的值。</span><span class="sxs-lookup"><span data-stu-id="47e8a-118">Add the controls in the following table to the form, and set the corresponding values for their properties.</span></span>  
  
    |<span data-ttu-id="47e8a-119">控制</span><span class="sxs-lookup"><span data-stu-id="47e8a-119">Control</span></span>|<span data-ttu-id="47e8a-120">属性</span><span class="sxs-lookup"><span data-stu-id="47e8a-120">Property</span></span>|<span data-ttu-id="47e8a-121">值</span><span class="sxs-lookup"><span data-stu-id="47e8a-121">Value</span></span>|  
    |-------------|--------------|-----------|  
    |<span data-ttu-id="47e8a-122">**ListBox**</span><span class="sxs-lookup"><span data-stu-id="47e8a-122">**ListBox**</span></span>|<span data-ttu-id="47e8a-123">**名称**</span><span class="sxs-lookup"><span data-stu-id="47e8a-123">**Name**</span></span>|`filesListBox`|  
    |<span data-ttu-id="47e8a-124">**Button**</span><span class="sxs-lookup"><span data-stu-id="47e8a-124">**Button**</span></span>|<span data-ttu-id="47e8a-125">**名称**</span><span class="sxs-lookup"><span data-stu-id="47e8a-125">**Name**</span></span><br /><br /> <span data-ttu-id="47e8a-126">**Text**</span><span class="sxs-lookup"><span data-stu-id="47e8a-126">**Text**</span></span>|`browseButton`<br /><br /> <span data-ttu-id="47e8a-127">**“浏览”**</span><span class="sxs-lookup"><span data-stu-id="47e8a-127">**Browse**</span></span>|  
    |<span data-ttu-id="47e8a-128">**Button**</span><span class="sxs-lookup"><span data-stu-id="47e8a-128">**Button**</span></span>|<span data-ttu-id="47e8a-129">**名称**</span><span class="sxs-lookup"><span data-stu-id="47e8a-129">**Name**</span></span><br /><br /> <span data-ttu-id="47e8a-130">**Text**</span><span class="sxs-lookup"><span data-stu-id="47e8a-130">**Text**</span></span>|`examineButton`<br /><br /> <span data-ttu-id="47e8a-131">**检查**</span><span class="sxs-lookup"><span data-stu-id="47e8a-131">**Examine**</span></span>|  
    |<span data-ttu-id="47e8a-132">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="47e8a-132">**CheckBox**</span></span>|<span data-ttu-id="47e8a-133">**名称**</span><span class="sxs-lookup"><span data-stu-id="47e8a-133">**Name**</span></span><br /><br /> <span data-ttu-id="47e8a-134">**Text**</span><span class="sxs-lookup"><span data-stu-id="47e8a-134">**Text**</span></span>|`saveCheckBox`<br /><br /> <span data-ttu-id="47e8a-135">**保存结果**</span><span class="sxs-lookup"><span data-stu-id="47e8a-135">**Save Results**</span></span>|  
    |<span data-ttu-id="47e8a-136">**FolderBrowserDialog**</span><span class="sxs-lookup"><span data-stu-id="47e8a-136">**FolderBrowserDialog**</span></span>|<span data-ttu-id="47e8a-137">**名称**</span><span class="sxs-lookup"><span data-stu-id="47e8a-137">**Name**</span></span>|`FolderBrowserDialog1`|  
  
### <a name="to-select-a-folder-and-list-files-in-a-folder"></a><span data-ttu-id="47e8a-138">选择一个文件夹，并列出文件夹中的文件</span><span class="sxs-lookup"><span data-stu-id="47e8a-138">To select a folder, and list files in a folder</span></span>  
  
1. <span data-ttu-id="47e8a-139">通过双击窗体上的控件，创建 `browseButton` 的 `Click` 事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-139">Create a `Click` event handler for `browseButton` by double-clicking the control on the form.</span></span> <span data-ttu-id="47e8a-140">代码编辑器随即打开。</span><span class="sxs-lookup"><span data-stu-id="47e8a-140">The Code Editor opens.</span></span>  
  
2. <span data-ttu-id="47e8a-141">将以下代码添加到 `Click` 事件处理程序中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-141">Add the following code to the `Click` event handler.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#103](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#103)]  
  
     <span data-ttu-id="47e8a-142">`FolderBrowserDialog1.ShowDialog` 调用将打开“浏览文件夹”对话框。</span><span class="sxs-lookup"><span data-stu-id="47e8a-142">The `FolderBrowserDialog1.ShowDialog` call opens the **Browse For Folder** dialog box.</span></span> <span data-ttu-id="47e8a-143">用户单击“确定”后，<xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> 属性作为参数发送给在下一步中添加的 `ListFiles` 方法。</span><span class="sxs-lookup"><span data-stu-id="47e8a-143">After the user clicks **OK**, the <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> property is sent as an argument to the `ListFiles` method, which is added in the next step.</span></span>  
  
3. <span data-ttu-id="47e8a-144">添加以下 `ListFiles` 方法。</span><span class="sxs-lookup"><span data-stu-id="47e8a-144">Add the following `ListFiles` method.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#104](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#104)]  
  
     <span data-ttu-id="47e8a-145">此代码首先会清除“ListBox”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-145">This code first clears the **ListBox**.</span></span>  
  
     <span data-ttu-id="47e8a-146"><xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A> 方法然后检索字符串集合，一个字符串对应目录中的一个文件。</span><span class="sxs-lookup"><span data-stu-id="47e8a-146">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A> method then retrieves a collection of strings, one for each file in the directory.</span></span> <span data-ttu-id="47e8a-147">`GetFiles` 方法接受一个搜索模式参数来检索与特定模式匹配的文件。</span><span class="sxs-lookup"><span data-stu-id="47e8a-147">The `GetFiles` method accepts a search pattern argument to retrieve files that match a particular pattern.</span></span> <span data-ttu-id="47e8a-148">在此示例中，仅返回具有 .txt 扩展名的文件。</span><span class="sxs-lookup"><span data-stu-id="47e8a-148">In this example, only files that have the extension .txt are returned.</span></span>  
  
     <span data-ttu-id="47e8a-149">通过 `GetFiles` 方法返回的字符串随后将添加到“ListBox”中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-149">The strings that are returned by the `GetFiles` method are then added to the **ListBox**.</span></span>  
  
4. <span data-ttu-id="47e8a-150">运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-150">Run the application.</span></span> <span data-ttu-id="47e8a-151">单击“浏览”按钮。 </span><span class="sxs-lookup"><span data-stu-id="47e8a-151">Click the **Browse** button.</span></span> <span data-ttu-id="47e8a-152">在“浏览文件夹”对话框中，浏览到包含 .txt 文件的文件夹，然后选择该文件夹，并单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-152">In the **Browse For Folder** dialog box, browse to a folder that contains .txt files, and then select the folder and click **OK**.</span></span>  
  
     <span data-ttu-id="47e8a-153">`ListBox` 包含所选文件夹中 .txt 文件的列表。</span><span class="sxs-lookup"><span data-stu-id="47e8a-153">The `ListBox` contains a list of .txt files in the selected folder.</span></span>  
  
5. <span data-ttu-id="47e8a-154">停止运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-154">Stop running the application.</span></span>  
  
### <a name="to-obtain-attributes-of-a-file-and-content-from-a-text-file"></a><span data-ttu-id="47e8a-155">从文本文件获取文件的属性和内容</span><span class="sxs-lookup"><span data-stu-id="47e8a-155">To obtain attributes of a file, and content from a text file</span></span>  
  
1. <span data-ttu-id="47e8a-156">通过双击窗体上的控件，创建 `examineButton` 的 `Click` 事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-156">Create a `Click` event handler for `examineButton` by double-clicking the control on the form.</span></span>  
  
2. <span data-ttu-id="47e8a-157">将以下代码添加到 `Click` 事件处理程序中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-157">Add the following code to the `Click` event handler.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#105](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#105)]  
  
     <span data-ttu-id="47e8a-158">该代码验证是否在 `ListBox` 中选中某项。</span><span class="sxs-lookup"><span data-stu-id="47e8a-158">The code verifies that an item is selected in the `ListBox`.</span></span> <span data-ttu-id="47e8a-159">然后，将从 `ListBox` 获取文件路径项。</span><span class="sxs-lookup"><span data-stu-id="47e8a-159">It then obtains the file path entry from the `ListBox`.</span></span> <span data-ttu-id="47e8a-160"><xref:Microsoft.VisualBasic.FileIO.FileSystem.FileExists%2A> 方法用于检查文件是否仍然存在。</span><span class="sxs-lookup"><span data-stu-id="47e8a-160">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.FileExists%2A> method is used to check whether the file still exists.</span></span>  
  
     <span data-ttu-id="47e8a-161">该文件路径作为参数发送给下一步中添加的 `GetTextForOutput` 方法。</span><span class="sxs-lookup"><span data-stu-id="47e8a-161">The file path is sent as an argument to the `GetTextForOutput` method, which is added in the next step.</span></span> <span data-ttu-id="47e8a-162">此方法返回一个包含文件信息字符串。</span><span class="sxs-lookup"><span data-stu-id="47e8a-162">This method returns a string that contains file information.</span></span> <span data-ttu-id="47e8a-163">该文件信息将出现在“MessageBox”中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-163">The file information appears in a **MessageBox**.</span></span>  
  
3. <span data-ttu-id="47e8a-164">添加以下 `GetTextForOutput` 方法。</span><span class="sxs-lookup"><span data-stu-id="47e8a-164">Add the following `GetTextForOutput` method.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#107](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#107)]  
  
     <span data-ttu-id="47e8a-165">该代码使用 <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A> 方法来获取文件参数。</span><span class="sxs-lookup"><span data-stu-id="47e8a-165">The code uses the <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFileInfo%2A> method to obtain file parameters.</span></span> <span data-ttu-id="47e8a-166">文件参数添加到 <xref:System.Text.StringBuilder>。</span><span class="sxs-lookup"><span data-stu-id="47e8a-166">The file parameters are added to a <xref:System.Text.StringBuilder>.</span></span>  
  
     <span data-ttu-id="47e8a-167"><xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileReader%2A> 方法将文件内容读取到 <xref:System.IO.StreamReader>。</span><span class="sxs-lookup"><span data-stu-id="47e8a-167">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileReader%2A> method reads the file contents into a <xref:System.IO.StreamReader>.</span></span> <span data-ttu-id="47e8a-168">该内容的第一行是从 `StreamReader` 获取的，然后将添加到 `StringBuilder`。</span><span class="sxs-lookup"><span data-stu-id="47e8a-168">The first line of the contents is obtained from the `StreamReader` and is added to the `StringBuilder`.</span></span>  
  
4. <span data-ttu-id="47e8a-169">运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-169">Run the application.</span></span> <span data-ttu-id="47e8a-170">单击“浏览”，然后浏览到包含 .txt 文件的文件夹。</span><span class="sxs-lookup"><span data-stu-id="47e8a-170">Click **Browse**, and browse to a folder that contains .txt files.</span></span> <span data-ttu-id="47e8a-171">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-171">Click **OK**.</span></span>  
  
     <span data-ttu-id="47e8a-172">在 `ListBox` 中选择一个文件，然后单击“检查”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-172">Select a file in the `ListBox`, and then click **Examine**.</span></span> <span data-ttu-id="47e8a-173">`MessageBox` 显示文件信息。</span><span class="sxs-lookup"><span data-stu-id="47e8a-173">A `MessageBox` shows the file information.</span></span>  
  
5. <span data-ttu-id="47e8a-174">停止运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-174">Stop running the application.</span></span>  
  
### <a name="to-add-a-log-entry"></a><span data-ttu-id="47e8a-175">添加日志项目</span><span class="sxs-lookup"><span data-stu-id="47e8a-175">To add a log entry</span></span>  
  
1. <span data-ttu-id="47e8a-176">将以下代码添加到 `examineButton_Click` 事件处理程序末尾。</span><span class="sxs-lookup"><span data-stu-id="47e8a-176">Add the following code to the end of the `examineButton_Click` event handler.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#106](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#106)]  
  
     <span data-ttu-id="47e8a-177">该代码设置日志文件路径以便将日志文件放在与所选文件相同的目录中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-177">The code sets the log file path to put the log file in the same directory as that of the selected file.</span></span> <span data-ttu-id="47e8a-178">日志项目的文本设置为当前日期和文件信息后的时间。</span><span class="sxs-lookup"><span data-stu-id="47e8a-178">The text of the log entry is set to the current date and time followed by the file information.</span></span>  
  
     <span data-ttu-id="47e8a-179"><xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> 方法，其 `append` 参数设置为 `True`，用于创建日志条目。</span><span class="sxs-lookup"><span data-stu-id="47e8a-179">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> method, with the `append` argument set to `True`, is used to create the log entry.</span></span>  
  
2. <span data-ttu-id="47e8a-180">运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-180">Run the application.</span></span> <span data-ttu-id="47e8a-181">浏览到一个文本文件，在 `ListBox` 中选中它，选择“保存结果”复选框，然后再单击“检查”。</span><span class="sxs-lookup"><span data-stu-id="47e8a-181">Browse to a text file, select it in the `ListBox`, select the **Save Results** check box, and then click **Examine**.</span></span> <span data-ttu-id="47e8a-182">验证日志条目是否写入 `log.txt` 文件。</span><span class="sxs-lookup"><span data-stu-id="47e8a-182">Verify that the log entry is written to the `log.txt` file.</span></span>  
  
3. <span data-ttu-id="47e8a-183">停止运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-183">Stop running the application.</span></span>  
  
### <a name="to-use-the-current-directory"></a><span data-ttu-id="47e8a-184">使用当前目录</span><span class="sxs-lookup"><span data-stu-id="47e8a-184">To use the current directory</span></span>  
  
1. <span data-ttu-id="47e8a-185">通过双击窗体，创建 `Form1_Load` 的事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-185">Create an event handler for `Form1_Load` by double-clicking the form.</span></span>  
  
2. <span data-ttu-id="47e8a-186">将以下代码添加到该事件处理程序中。</span><span class="sxs-lookup"><span data-stu-id="47e8a-186">Add the following code to the event handler.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#102](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#102)]  
  
     <span data-ttu-id="47e8a-187">此代码将文件夹浏览器的默认目录设置为当前目录。</span><span class="sxs-lookup"><span data-stu-id="47e8a-187">This code sets the default directory of the folder browser to the current directory.</span></span>  
  
3. <span data-ttu-id="47e8a-188">运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-188">Run the application.</span></span> <span data-ttu-id="47e8a-189">第一次单击“浏览”时，“浏览文件夹”对话框将打开到当前目录。</span><span class="sxs-lookup"><span data-stu-id="47e8a-189">When you click **Browse** the first time, the **Browse For Folder** dialog box opens to the current directory.</span></span>  
  
4. <span data-ttu-id="47e8a-190">停止运行该应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-190">Stop running the application.</span></span>  
  
### <a name="to-selectively-enable-controls"></a><span data-ttu-id="47e8a-191">有选择地启用控件</span><span class="sxs-lookup"><span data-stu-id="47e8a-191">To selectively enable controls</span></span>  
  
1. <span data-ttu-id="47e8a-192">添加以下 `SetEnabled` 方法。</span><span class="sxs-lookup"><span data-stu-id="47e8a-192">Add the following `SetEnabled` method.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#108](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#108)]  
  
     <span data-ttu-id="47e8a-193">`SetEnabled` 方法启用还是禁用控件是由是否选中 `ListBox` 中的项决定的。</span><span class="sxs-lookup"><span data-stu-id="47e8a-193">The `SetEnabled` method enables or disables controls depending on whether an item is selected in the `ListBox`.</span></span>  
  
2. <span data-ttu-id="47e8a-194">通过双击窗体上的 `ListBox` 控件，创建 `filesListBox` 的 `SelectedIndexChanged` 事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-194">Create a `SelectedIndexChanged` event handler for `filesListBox` by double-clicking the `ListBox` control on the form.</span></span>  
  
3. <span data-ttu-id="47e8a-195">在新的 `filesListBox_SelectedIndexChanged` 事件处理程序中添加对 `SetEnabled` 的调用。</span><span class="sxs-lookup"><span data-stu-id="47e8a-195">Add a call to `SetEnabled` in the new `filesListBox_SelectedIndexChanged` event handler.</span></span>  
  
4. <span data-ttu-id="47e8a-196">在 `browseButton_Click` 事件处理程序末尾添加对 `SetEnabled` 的调用。</span><span class="sxs-lookup"><span data-stu-id="47e8a-196">Add a call to `SetEnabled` at the end of the `browseButton_Click` event handler.</span></span>  
  
5. <span data-ttu-id="47e8a-197">在 `Form1_Load` 事件处理程序末尾添加对 `SetEnabled` 的调用。</span><span class="sxs-lookup"><span data-stu-id="47e8a-197">Add a call to `SetEnabled` at the end of the `Form1_Load` event handler.</span></span>  
  
6. <span data-ttu-id="47e8a-198">运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="47e8a-198">Run the application.</span></span> <span data-ttu-id="47e8a-199">如果在 `ListBox` 中未选中任何项，将禁用“保存结果”复选框和“检查”按钮。</span><span class="sxs-lookup"><span data-stu-id="47e8a-199">The **Save Results** check box and the **Examine** button are disabled if an item is not selected in the `ListBox`.</span></span>  
  
## <a name="full-example-using-mycomputerfilesystem"></a><span data-ttu-id="47e8a-200">使用 My.Computer.FileSystem 的完整示例</span><span class="sxs-lookup"><span data-stu-id="47e8a-200">Full example using My.Computer.FileSystem</span></span>  

 <span data-ttu-id="47e8a-201">以下是完整示例。</span><span class="sxs-lookup"><span data-stu-id="47e8a-201">Following is the complete example.</span></span>  
  
 [!code-vb[VbVbcnMyFileSystem#101](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class2.vb#101)]  
  
## <a name="full-example-using-systemio"></a><span data-ttu-id="47e8a-202">使用 System.IO 的完整示例</span><span class="sxs-lookup"><span data-stu-id="47e8a-202">Full example using System.IO</span></span>  

 <span data-ttu-id="47e8a-203">以下等效示例使用来自 <xref:System.IO> 命名空间的类，而不使用 `My.Computer.FileSystem` 对象。</span><span class="sxs-lookup"><span data-stu-id="47e8a-203">The following equivalent example uses classes from the <xref:System.IO> namespace instead of using `My.Computer.FileSystem` objects.</span></span>  
  
 [!code-vb[VbVbcnMyFileSystem#111](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/class3.vb#111)]  
  
## <a name="see-also"></a><span data-ttu-id="47e8a-204">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47e8a-204">See also</span></span>

- <xref:System.IO>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CurrentDirectory%2A>
- [<span data-ttu-id="47e8a-205">演练：使用 .NET Framework 方法操作文件</span><span class="sxs-lookup"><span data-stu-id="47e8a-205">Walkthrough: Manipulating Files by Using .NET Framework Methods</span></span>](walkthrough-manipulating-files-by-using-net-framework-methods.md)
