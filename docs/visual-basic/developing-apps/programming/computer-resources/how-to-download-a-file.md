---
description: 详细了解：操作说明：在 Visual Basic 上传文件
title: 如何：下载文件
ms.date: 07/20/2015
helpviewer_keywords:
- downloading Internet resources [Visual Basic], files
- downloading files [Visual Basic]
- remote computers [Visual Basic], downloading from
- files [Visual Basic], downloading
- files [Visual Basic], transferring
ms.assetid: ac479f81-c0e2-4b99-af73-217f446b73da
ms.openlocfilehash: dd296a5958431b74ccc8e0fb41a49073f4847ded
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797687"
---
# <a name="how-to-download-a-file-in-visual-basic"></a><span data-ttu-id="7e579-103">如何：在 Visual Basic 中下载文件</span><span class="sxs-lookup"><span data-stu-id="7e579-103">How to: Download a File in Visual Basic</span></span>

<span data-ttu-id="7e579-104"><xref:Microsoft.VisualBasic.Devices.Network.DownloadFile%2A> 方法可用来下载远程文件并将其存储到特定位置。</span><span class="sxs-lookup"><span data-stu-id="7e579-104">The <xref:Microsoft.VisualBasic.Devices.Network.DownloadFile%2A> method can be used to download a remote file and store it to a specific location.</span></span> <span data-ttu-id="7e579-105">如果 `ShowUI` 参数设置为 `True`，则显示一个对话框，该对话框显示下载进度并允许用户取消该操作。</span><span class="sxs-lookup"><span data-stu-id="7e579-105">If the `ShowUI` parameter is set to `True`, a dialog box is displayed showing the progress of the download and allowing users to cancel the operation.</span></span> <span data-ttu-id="7e579-106">默认情况下，不会覆盖同名的现有文件；如果希望覆盖现有文件，则将 `overwrite` 参数设为 `True`。</span><span class="sxs-lookup"><span data-stu-id="7e579-106">By default, existing files having the same name are not overwritten; if you want to overwrite existing files, set the `overwrite` parameter to `True`.</span></span>

<span data-ttu-id="7e579-107">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="7e579-107">The following conditions may cause an exception:</span></span>

- <span data-ttu-id="7e579-108">驱动器名称无效 (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="7e579-108">Drive name is not valid (<xref:System.ArgumentException>).</span></span>

- <span data-ttu-id="7e579-109">尚未提供必要的身份验证（<xref:System.UnauthorizedAccessException> 或 <xref:System.Security.SecurityException>）。</span><span class="sxs-lookup"><span data-stu-id="7e579-109">Necessary authentication has not been supplied (<xref:System.UnauthorizedAccessException> or <xref:System.Security.SecurityException>).</span></span>

- <span data-ttu-id="7e579-110">服务器未在指定的 `connectionTimeout` (<xref:System.TimeoutException>) 内响应。</span><span class="sxs-lookup"><span data-stu-id="7e579-110">The server does not respond within the specified `connectionTimeout` (<xref:System.TimeoutException>).</span></span>

- <span data-ttu-id="7e579-111">请求被网站 (<xref:System.Net.WebException>) 拒绝。</span><span class="sxs-lookup"><span data-stu-id="7e579-111">The request is denied by the Web site (<xref:System.Net.WebException>).</span></span>

[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]

> [!IMPORTANT]
> <span data-ttu-id="7e579-112">不要根据文件的名称来判断文件的内容。</span><span class="sxs-lookup"><span data-stu-id="7e579-112">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="7e579-113">例如，文件 Form1.vb 可能不是 Visual Basic 源文件。</span><span class="sxs-lookup"><span data-stu-id="7e579-113">For example, the file Form1.vb may not be a Visual Basic source file.</span></span> <span data-ttu-id="7e579-114">在应用程序中使用输入的数据之前，需验证所有的输入内容。</span><span class="sxs-lookup"><span data-stu-id="7e579-114">Verify all inputs before using the data in your application.</span></span> <span data-ttu-id="7e579-115">文件的内容可能不是预期内容，并且用来读取该文件的方法可能失败。</span><span class="sxs-lookup"><span data-stu-id="7e579-115">The contents of the file may not be what is expected, and methods to read from the file may fail.</span></span>

### <a name="to-download-a-file"></a><span data-ttu-id="7e579-116">下载文件</span><span class="sxs-lookup"><span data-stu-id="7e579-116">To download a file</span></span>

- <span data-ttu-id="7e579-117">使用 `DownloadFile` 方法下载文件，同时将目标文件的位置指定为字符串或 URI 并指定要存储该文件的位置。</span><span class="sxs-lookup"><span data-stu-id="7e579-117">Use the `DownloadFile` method to download the file, specifying the target file's location as a string or URI and specifying the location at which to store the file.</span></span> <span data-ttu-id="7e579-118">此示例从 `http://www.cohowinery.com/downloads` 下载 `WineList.txt` 文件，并将其保存到 `C:\Documents and Settings\All Users\Documents` 中：</span><span class="sxs-lookup"><span data-stu-id="7e579-118">This example downloads the file `WineList.txt` from `http://www.cohowinery.com/downloads` and saves it to `C:\Documents and Settings\All Users\Documents`:</span></span>

  [!code-vb[VbResourceTasks#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#9)]

### <a name="to-download-a-file-specifying-a-time-out-interval"></a><span data-ttu-id="7e579-119">下载文件，并指定超时间隔</span><span class="sxs-lookup"><span data-stu-id="7e579-119">To download a file, specifying a time-out interval</span></span>

- <span data-ttu-id="7e579-120">使用 `DownloadFile` 方法下载文件，同时将目标文件的位置指定为字符串或 URI，指定要存储该文件的位置，并以毫秒为单位指定超时间隔（默认值为 1000 毫秒）。</span><span class="sxs-lookup"><span data-stu-id="7e579-120">Use the `DownloadFile` method to download the file, specifying the target file's location as a string or URI, specifying the location at which to store the file, and specifying the time-out interval in milliseconds (the default is 1000).</span></span> <span data-ttu-id="7e579-121">此示例从 `http://www.cohowinery.com/downloads` 下载 `WineList.txt` 文件，然后将该文件保存到 `C:\Documents and Settings\All Users\Documents`，同时将超时间隔指定为 500 毫秒：</span><span class="sxs-lookup"><span data-stu-id="7e579-121">This example downloads the file `WineList.txt` from `http://www.cohowinery.com/downloads` and saves it to `C:\Documents and Settings\All Users\Documents`, specifying a time-out interval of 500 milliseconds:</span></span>

  [!code-vb[VbResourceTasks#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#10)]

### <a name="to-download-a-file-supplying-a-user-name-and-password"></a><span data-ttu-id="7e579-122">提供用户名和密码下载文件</span><span class="sxs-lookup"><span data-stu-id="7e579-122">To download a file, supplying a user name and password</span></span>

- <span data-ttu-id="7e579-123">使用 `DownLoadFile` 方法下载文件，同时将目标文件的位置指定为字符串或 URI，并指定要存储该文件的位置、用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="7e579-123">Use the `DownLoadFile` method to download the file, specifying the target file's location as a string or URI and specifying the location at which to store the file, the user name, and the password.</span></span> <span data-ttu-id="7e579-124">此示例使用用户名 `anonymous` 和空密码从 `http://www.cohowinery.com/downloads` 下载 `WineList.txt` 文件，然后将该文件保存到 `C:\Documents and Settings\All Users\Documents`。</span><span class="sxs-lookup"><span data-stu-id="7e579-124">This example downloads the file `WineList.txt` from `http://www.cohowinery.com/downloads` and saves it to `C:\Documents and Settings\All Users\Documents`, with the user name `anonymous` and a blank password.</span></span>

  [!code-vb[VbResourceTasks#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#11)]

  > [!IMPORTANT]
  > <span data-ttu-id="7e579-125">`DownLoadFile` 方法使用的 FTP 协议以纯文本方式发送信息（包括密码），因此不应用于传送敏感信息。</span><span class="sxs-lookup"><span data-stu-id="7e579-125">The FTP protocol used by the `DownLoadFile` method sends information, including passwords, in plain text and should not be used for transmitting sensitive information.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e579-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e579-126">See also</span></span>

- <xref:Microsoft.VisualBasic.Devices.Network>
- <xref:Microsoft.VisualBasic.Devices.Network.DownloadFile%2A>
- [<span data-ttu-id="7e579-127">如何：上传文件</span><span class="sxs-lookup"><span data-stu-id="7e579-127">How to: Upload a File</span></span>](how-to-upload-a-file.md)
- [<span data-ttu-id="7e579-128">如何：分析文件路径</span><span class="sxs-lookup"><span data-stu-id="7e579-128">How to: Parse File Paths</span></span>](../drives-directories-files/how-to-parse-file-paths.md)
