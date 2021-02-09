---
description: 详细了解：操作说明：在 Visual Basic 中检索“我的文档”目录中的内容
title: 如何：检索“我的文档”目录中的内容
ms.date: 07/20/2015
helpviewer_keywords:
- My Documents directory
ms.assetid: 26560d01-7dda-4457-8e95-21db23d71aea
ms.openlocfilehash: e9e6ffc202332bd8d1849ef886fd4e7d6cc46a54
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797388"
---
# <a name="how-to-retrieve-the-contents-of-the-my-documents-directory-in-visual-basic"></a><span data-ttu-id="2ad4d-103">如何：在 Visual Basic 中检索“我的文档”目录中的内容</span><span class="sxs-lookup"><span data-stu-id="2ad4d-103">How to: Retrieve the Contents of the My Documents Directory in Visual Basic</span></span>

<span data-ttu-id="2ad4d-104">可以使用 <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> 对象读取许多“所有用户”目录，例如“我的文档”或“桌面”。</span><span class="sxs-lookup"><span data-stu-id="2ad4d-104">The <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories> object can be used to read from many of the **All Users** directories, such as **My Documents** or **Desktop**.</span></span>  
  
### <a name="to-read-from-the-my-documents-folder"></a><span data-ttu-id="2ad4d-105">读取“我的文档”文件夹</span><span class="sxs-lookup"><span data-stu-id="2ad4d-105">To read from the My Documents folder</span></span>  
  
- <span data-ttu-id="2ad4d-106">可以使用 `ReadAllText`方法从特定目录中的每个文件中读取文本。</span><span class="sxs-lookup"><span data-stu-id="2ad4d-106">Use the `ReadAllText` method to read the text from each file in a specific directory.</span></span> <span data-ttu-id="2ad4d-107">以下代码指定一个目录和文件，然后使用 `ReadAllText` 将它们读入名为 `patients` 的字符串。</span><span class="sxs-lookup"><span data-stu-id="2ad4d-107">The following code specifies a directory and file and then uses `ReadAllText` to read them into the string named `patients`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="2ad4d-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ad4d-108">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A>
