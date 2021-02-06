---
description: 了解更多：文件太多
title: 文件太多
ms.date: 07/20/2015
f1_keywords:
- vbrID67
ms.assetid: 2ff203e2-bba6-43ae-b72f-8e92a881c98f
ms.openlocfilehash: 85d246c49f765cf618bf889d75dcc9c10b780280
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641220"
---
# <a name="too-many-files"></a><span data-ttu-id="a9dd0-103">文件太多</span><span class="sxs-lookup"><span data-stu-id="a9dd0-103">Too many files</span></span>

<span data-ttu-id="a9dd0-104">在根目录中创建的文件数超过了操作系统允许的数目，或者打开的文件多于 CONFIG.SYS 文件中 " **文件 =** " 设置中指定的数目。</span><span class="sxs-lookup"><span data-stu-id="a9dd0-104">Either more files have been created in the root directory than the operating system permits, or more files have been opened than the number specified in the **files=** setting in your CONFIG.SYS file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a9dd0-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a9dd0-105">To correct this error</span></span>  
  
1. <span data-ttu-id="a9dd0-106">如果程序正在打开、关闭或保存根目录中的文件，请将程序更改为使用子目录。</span><span class="sxs-lookup"><span data-stu-id="a9dd0-106">If your program is opening, closing, or saving files in the root directory, change your program so that it uses a subdirectory.</span></span>  
  
2. <span data-ttu-id="a9dd0-107">增加在文件中指定的文件数 **=** CONFIG.SYS 文件中的设置，然后重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="a9dd0-107">Increase the number of files specified in your **files=** setting in your CONFIG.SYS file, and restart your computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9dd0-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9dd0-108">See also</span></span>

- [<span data-ttu-id="a9dd0-109">错误类型</span><span class="sxs-lookup"><span data-stu-id="a9dd0-109">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
