---
description: 了解详细信息： BC31019：无法写入输出文件 " <filename> "： <error>
title: 无法写入输出文件“<filename>”：<error>
ms.date: 07/20/2015
f1_keywords:
- vbc31019
- bc31019
helpviewer_keywords:
- BC31019
ms.assetid: 0845b245-11bb-46fd-95ca-f6cef3c318ef
ms.openlocfilehash: 86ddd01764d51c3050186e99e047edb8aba158eb
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102104793"
---
# <a name="bc31019-unable-to-write-to-output-file-filename-error"></a><span data-ttu-id="0772f-103">BC31019：无法写入输出文件 " \<filename> "： \<error></span><span class="sxs-lookup"><span data-stu-id="0772f-103">BC31019: Unable to write to output file '\<filename>': \<error></span></span>

<span data-ttu-id="0772f-104">创建文件时出现问题。</span><span class="sxs-lookup"><span data-stu-id="0772f-104">There was a problem creating the file.</span></span>

 <span data-ttu-id="0772f-105">无法打开输出文件以进行写入。</span><span class="sxs-lookup"><span data-stu-id="0772f-105">An output file cannot be opened for writing.</span></span> <span data-ttu-id="0772f-106">文件（或包含该文件的文件夹）可能由另一个进程打开以供独占使用，或者可能设置了只读特性。</span><span class="sxs-lookup"><span data-stu-id="0772f-106">The file (or the folder containing the file) may be opened for exclusive use by another process, or it may have its read-only attribute set.</span></span>

 <span data-ttu-id="0772f-107">文件以独占形式打开的常见情形是：</span><span class="sxs-lookup"><span data-stu-id="0772f-107">Common situations where a file is opened exclusively are:</span></span>

- <span data-ttu-id="0772f-108">应用程序已经在运行并使用它的文件。</span><span class="sxs-lookup"><span data-stu-id="0772f-108">The application is already running and using its files.</span></span> <span data-ttu-id="0772f-109">若要解决此问题，请确保应用程序没有运行。</span><span class="sxs-lookup"><span data-stu-id="0772f-109">To solve this problem, make sure that the application is not running.</span></span>

- <span data-ttu-id="0772f-110">其他应用程序已经打开了该文件。</span><span class="sxs-lookup"><span data-stu-id="0772f-110">Another application has opened the file.</span></span> <span data-ttu-id="0772f-111">若要解决此问题，请确保其他应用程序没有访问这些文件。</span><span class="sxs-lookup"><span data-stu-id="0772f-111">To solve this problem, make sure that no other application is accessing the files.</span></span> <span data-ttu-id="0772f-112">是哪个应用程序在访问你的文件并不总是很明显；在这种情况下，重新启动计算机可能是终止该应用程序的最简单的方式。</span><span class="sxs-lookup"><span data-stu-id="0772f-112">It is not always obvious which application is accessing your files; in that case, restarting the computer might be the easiest way to terminate the application.</span></span>

 <span data-ttu-id="0772f-113">即使是项目输出文件中只有一个被标记为只读，也将会引发此异常。</span><span class="sxs-lookup"><span data-stu-id="0772f-113">If even one of the project output files is marked as read-only, this exception will be thrown.</span></span>

 <span data-ttu-id="0772f-114">**错误 ID：** BC31019</span><span class="sxs-lookup"><span data-stu-id="0772f-114">**Error ID:** BC31019</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="0772f-115">更正此错误</span><span class="sxs-lookup"><span data-stu-id="0772f-115">To correct this error</span></span>

1. <span data-ttu-id="0772f-116">再次编译此程序以查看错误是否重复出现。</span><span class="sxs-lookup"><span data-stu-id="0772f-116">Compile the program again to see if the error recurs.</span></span>

2. <span data-ttu-id="0772f-117">如果错误仍然存在，请保存你的工作并重启 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="0772f-117">If the error continues, save your work and restart Visual Studio.</span></span>

3. <span data-ttu-id="0772f-118">如果仍出现错误，请重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="0772f-118">If the error continues, restart the computer.</span></span>

4. <span data-ttu-id="0772f-119">如果错误重复出现，请重新安装 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="0772f-119">If the error recurs, reinstall Visual Basic.</span></span>

5. <span data-ttu-id="0772f-120">如果在重新安装之后依然出现错误，请通知 Microsoft 产品支持服务。</span><span class="sxs-lookup"><span data-stu-id="0772f-120">If the error persists after reinstallation, notify Microsoft Product Support Services.</span></span>

### <a name="to-check-file-attributes-in-file-explorer"></a><span data-ttu-id="0772f-121">在“文件资源管理器”中检查文件特性</span><span class="sxs-lookup"><span data-stu-id="0772f-121">To check file attributes in File Explorer</span></span>

1. <span data-ttu-id="0772f-122">打开你感兴趣的文件夹。</span><span class="sxs-lookup"><span data-stu-id="0772f-122">Open the folder you are interested in.</span></span>

2. <span data-ttu-id="0772f-123">单击 " **视图** " 图标，然后选择 " **详细信息**"。</span><span class="sxs-lookup"><span data-stu-id="0772f-123">Click the **Views** icon and choose **Details**.</span></span>

3. <span data-ttu-id="0772f-124">右键单击列标题，然后从下拉列表中选择 " **属性** "。</span><span class="sxs-lookup"><span data-stu-id="0772f-124">Right-click the column header, and choose **Attributes** from the drop-down list.</span></span>

### <a name="to-change-the-attributes-of-a-file-or-folder"></a><span data-ttu-id="0772f-125">更改文件或文件夹的特性</span><span class="sxs-lookup"><span data-stu-id="0772f-125">To change the attributes of a file or folder</span></span>

1. <span data-ttu-id="0772f-126">在 **文件资源管理器** 中，右键单击文件或文件夹，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="0772f-126">In **File Explorer**, right-click the file or folder and choose **Properties**.</span></span>

2. <span data-ttu-id="0772f-127">在 "**常规**" 选项卡的 "**属性**" 部分中，清除 "**只读**" 复选框。</span><span class="sxs-lookup"><span data-stu-id="0772f-127">In the **Attributes** section of the **General** tab, clear the **Read-only** box.</span></span>

3. <span data-ttu-id="0772f-128">按“确定”。</span><span class="sxs-lookup"><span data-stu-id="0772f-128">Press **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0772f-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="0772f-129">See also</span></span>

- [<span data-ttu-id="0772f-130">Visual Studio 反馈选项</span><span class="sxs-lookup"><span data-stu-id="0772f-130">Visual Studio feedback options</span></span>](/visualstudio/ide/feedback-options)
