---
description: 了解详细信息：编码不能设置为 Nothing
title: 编码不能设置为 Nothing。
ms.date: 07/20/2015
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
ms.openlocfilehash: 4fa9cbd9488501b5295da8d8ace41ef06a706c12
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462990"
---
# <a name="encoding-cannot-be-set-to-nothing"></a><span data-ttu-id="22f57-103">编码不能设置为 Nothing。</span><span class="sxs-lookup"><span data-stu-id="22f57-103">Encoding cannot be set to Nothing</span></span>

<span data-ttu-id="22f57-104">尝试读取或写入文件失败，因为已将参数 `encoding` 设置为 `Nothing` ，但需要有效值。</span><span class="sxs-lookup"><span data-stu-id="22f57-104">An attempt to read from or write to a file has failed because the parameter `encoding` has been set to `Nothing` but requires a valid value.</span></span>  
  
 <span data-ttu-id="22f57-105"><xref:System.Text.Encoding> 用于确定写入文件时使用何种编码。</span><span class="sxs-lookup"><span data-stu-id="22f57-105"><xref:System.Text.Encoding> is used to determine what encoding to use when writing to a file.</span></span> <span data-ttu-id="22f57-106">默认为 UTF-8。</span><span class="sxs-lookup"><span data-stu-id="22f57-106">The default is UTF-8.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="22f57-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="22f57-107">To correct this error</span></span>  
  
- <span data-ttu-id="22f57-108">为 `encoding` 参数提供有效值。</span><span class="sxs-lookup"><span data-stu-id="22f57-108">Supply a valid value for the `encoding` parameter.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22f57-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="22f57-109">See also</span></span>

- [<span data-ttu-id="22f57-110">文件编码</span><span class="sxs-lookup"><span data-stu-id="22f57-110">File Encodings</span></span>](../developing-apps/programming/drives-directories-files/file-encodings.md)
- [<span data-ttu-id="22f57-111">从文件读取</span><span class="sxs-lookup"><span data-stu-id="22f57-111">Reading from Files</span></span>](../developing-apps/programming/drives-directories-files/reading-from-files.md)
- [<span data-ttu-id="22f57-112">写入文件</span><span class="sxs-lookup"><span data-stu-id="22f57-112">Writing to Files</span></span>](../developing-apps/programming/drives-directories-files/writing-to-files.md)
- [<span data-ttu-id="22f57-113">文件 System.io.file.readalltext</span><span class="sxs-lookup"><span data-stu-id="22f57-113">My.Computer.FileSystem.ReadAllText</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A)
- [<span data-ttu-id="22f57-114">文件 Microsoft.visualbasic.fileio.filesystem.writealltext</span><span class="sxs-lookup"><span data-stu-id="22f57-114">My.Computer.FileSystem.WriteAllText</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A)
