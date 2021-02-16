---
description: 了解详细信息：参数 BasePath 必须是文件夹的路径
title: 参数 BasePath 必须是一个文件夹的路径
ms.date: 07/20/2015
ms.assetid: b180ce60-ad57-41a6-a313-491d86d84cc7
ms.openlocfilehash: 314ccd8510a286fc7f01518600a625cac48e10af
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472300"
---
# <a name="argument-basepath-must-be-a-path-to-a-folder"></a><span data-ttu-id="28259-103">参数 BasePath 必须是一个文件夹的路径</span><span class="sxs-lookup"><span data-stu-id="28259-103">Argument BasePath must be a path to a folder</span></span>

<span data-ttu-id="28259-104">参数 `BasePath` 必须包含文件夹的路径。</span><span class="sxs-lookup"><span data-stu-id="28259-104">The argument `BasePath` must consist of a path to a folder.</span></span> <span data-ttu-id="28259-105">你可能会错误地解析字符串，并提供一个未被识别为有效路径的值。</span><span class="sxs-lookup"><span data-stu-id="28259-105">You may be parsing a string incorrectly and supplying a value that is not recognized as a valid path.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="28259-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="28259-106">To correct this error</span></span>  
  
- <span data-ttu-id="28259-107">检查为 `BasePath` 提供的值，确保它是一个文件夹的有效路径。</span><span class="sxs-lookup"><span data-stu-id="28259-107">Check the value you are supplying for `BasePath` to make sure it is a valid path to a folder.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28259-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="28259-108">See also</span></span>

- <xref:System.CodeDom.Compiler.TempFileCollection.BasePath%2A>
- <xref:System.Resources.ResXResourceWriter.BasePath%2A>
- <xref:System.Resources.ResXResourceReader.BasePath%2A>
- [<span data-ttu-id="28259-109">如何：分析文件路径</span><span class="sxs-lookup"><span data-stu-id="28259-109">How to: Parse File Paths</span></span>](../developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
