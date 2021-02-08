---
description: 了解详细信息：恢复而不出错
title: 无错误继续执行
ms.date: 07/20/2015
f1_keywords:
- vbrID20
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
ms.openlocfilehash: a2284484be65ae975c6e09499ec19e3cfd8d4a04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792006"
---
# <a name="resume-without-error"></a><span data-ttu-id="e76ab-103">无错误继续执行</span><span class="sxs-lookup"><span data-stu-id="e76ab-103">Resume without error</span></span>

<span data-ttu-id="e76ab-104">`Resume`语句出现在错误处理代码之外，或代码跳转到错误处理程序，即使没有出错。</span><span class="sxs-lookup"><span data-stu-id="e76ab-104">A `Resume` statement appeared outside error-handling code, or the code jumped into an error handler even though there was no error.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e76ab-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="e76ab-105">To correct this error</span></span>  
  
1. <span data-ttu-id="e76ab-106">将 `Resume` 语句移动到错误处理程序中，或将其删除。</span><span class="sxs-lookup"><span data-stu-id="e76ab-106">Move the `Resume` statement into an error handler, or delete it.</span></span>  
  
2. <span data-ttu-id="e76ab-107">跳转到标签不能跨过程出现，因此请在过程中搜索标识错误处理程序的标签。</span><span class="sxs-lookup"><span data-stu-id="e76ab-107">Jumps to labels cannot occur across procedures, so search the procedure for the label that identifies the error handler.</span></span> <span data-ttu-id="e76ab-108">如果找到指定为不是语句的语句目标的重复标签 `GoTo` `On Error GoTo` ，则更改行标签以同意其预期目标。</span><span class="sxs-lookup"><span data-stu-id="e76ab-108">If you find a duplicate label specified as the target of a `GoTo` statement that isn't an `On Error GoTo` statement, change the line label to agree with its intended target.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e76ab-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="e76ab-109">See also</span></span>

- [<span data-ttu-id="e76ab-110">Resume 语句</span><span class="sxs-lookup"><span data-stu-id="e76ab-110">Resume Statement</span></span>](../statements/resume-statement.md)
- [<span data-ttu-id="e76ab-111">On Error 语句</span><span class="sxs-lookup"><span data-stu-id="e76ab-111">On Error Statement</span></span>](../statements/on-error-statement.md)
