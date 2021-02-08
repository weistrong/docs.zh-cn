---
description: 了解详细信息：无法创建必要的临时文件
title: 无法建立必要的临时文件。
ms.date: 07/20/2015
f1_keywords:
- vbrID322
ms.assetid: 53617b5b-eb06-4188-b4c2-8607cb9fbc79
ms.openlocfilehash: 52d68b720d9f8797183cf773da45f02ceca0224d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796816"
---
# <a name="cant-create-necessary-temporary-file"></a><span data-ttu-id="a2613-103">无法建立必要的临时文件。</span><span class="sxs-lookup"><span data-stu-id="a2613-103">Can't create necessary temporary file</span></span>

<span data-ttu-id="a2613-104">驱动器已满，包含 TEMP 环境变量指定的目录，或者 TEMP 环境变量指定了无效或只读的驱动器或目录。</span><span class="sxs-lookup"><span data-stu-id="a2613-104">Either the drive is full that contains the directory specified by the TEMP environment variable, or the TEMP environment variable specifies an invalid or read-only drive or directory.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a2613-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a2613-105">To correct this error</span></span>  
  
1. <span data-ttu-id="a2613-106">删除驱动器中的文件（如果已满）。</span><span class="sxs-lookup"><span data-stu-id="a2613-106">Delete files from the drive, if full.</span></span>  
  
2. <span data-ttu-id="a2613-107">在 TEMP 环境变量中指定其他驱动器。</span><span class="sxs-lookup"><span data-stu-id="a2613-107">Specify a different drive in the TEMP environment variable.</span></span>  
  
3. <span data-ttu-id="a2613-108">为 TEMP 环境变量指定有效的驱动器。</span><span class="sxs-lookup"><span data-stu-id="a2613-108">Specify a valid drive for the TEMP environment variable.</span></span>  
  
4. <span data-ttu-id="a2613-109">从当前指定的驱动器或目录中删除只读限制。</span><span class="sxs-lookup"><span data-stu-id="a2613-109">Remove the read-only restriction from the currently specified drive or directory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2613-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2613-110">See also</span></span>

- [<span data-ttu-id="a2613-111">错误类型</span><span class="sxs-lookup"><span data-stu-id="a2613-111">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
