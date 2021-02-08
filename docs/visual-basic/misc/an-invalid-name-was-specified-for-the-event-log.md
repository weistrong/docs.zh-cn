---
description: 了解详细信息：为事件日志指定了无效名称
title: 为事件日志指定了无效名称
ms.date: 07/20/2015
ms.assetid: b1b158bd-f13f-4371-a8af-31c0e86ae6be
ms.openlocfilehash: 4786483fe0b1ae32a16b67bfb4f406587719011b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787365"
---
# <a name="an-invalid-name-was-specified-for-the-event-log"></a><span data-ttu-id="da6cb-103">为事件日志指定了无效名称</span><span class="sxs-lookup"><span data-stu-id="da6cb-103">An invalid name was specified for the event log</span></span>

<span data-ttu-id="da6cb-104">为事件日志指定了无效名称。</span><span class="sxs-lookup"><span data-stu-id="da6cb-104">An invalid name was specified for the event log.</span></span> <span data-ttu-id="da6cb-105">通常名称中存在无效字符、文件名太长或空白文件名会导致此结果。</span><span class="sxs-lookup"><span data-stu-id="da6cb-105">Usually this is a result of invalid characters in the name, a blank file name, or a file name that is too long.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="da6cb-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="da6cb-106">To correct this error</span></span>  
  
- <span data-ttu-id="da6cb-107">如果指定的名称多于 8 个字符，请确保与其他事件日志名称之间不存在冲突。</span><span class="sxs-lookup"><span data-stu-id="da6cb-107">If the specified name is more than eight characters, make sure there is no conflict with the names of other event logs.</span></span> <span data-ttu-id="da6cb-108">当确定名称是否唯一时，将仅计算前八个字符。</span><span class="sxs-lookup"><span data-stu-id="da6cb-108">Only the first eight characters are evaluated when determining if the name is unique.</span></span>  
  
- <span data-ttu-id="da6cb-109">如果提供路径，请确保它被正确解析。</span><span class="sxs-lookup"><span data-stu-id="da6cb-109">If supplying a path, make sure it is parsed correctly.</span></span>  
  
- <span data-ttu-id="da6cb-110">检查此名称中是否不存在任何无效字符。</span><span class="sxs-lookup"><span data-stu-id="da6cb-110">Check that there are no invalid characters in the name.</span></span> <span data-ttu-id="da6cb-111">不能在文件名中使用的字符包括 `<`、 `>`、 `:`、 `"`、 `/`、 `\`和 `|`。</span><span class="sxs-lookup"><span data-stu-id="da6cb-111">Characters that cannot be used in a file name include `<`, `>`, `:`, `"`, `/`, `\`, and `|`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da6cb-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="da6cb-112">See also</span></span>

- [<span data-ttu-id="da6cb-113">如何：分析文件路径</span><span class="sxs-lookup"><span data-stu-id="da6cb-113">How to: Parse File Paths</span></span>](../developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
- [<span data-ttu-id="da6cb-114">如何：重命名文件</span><span class="sxs-lookup"><span data-stu-id="da6cb-114">How to: Rename a File</span></span>](../developing-apps/programming/drives-directories-files/how-to-rename-a-file.md)
