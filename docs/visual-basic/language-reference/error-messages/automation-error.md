---
description: 了解详细信息：自动化错误
title: 自动错误
ms.date: 07/20/2015
f1_keywords:
- vbrID440
ms.assetid: 2c4be5c5-2f0d-4a2b-96fe-d1b24f08fc4c
ms.openlocfilehash: e4d283b16b4c54e2488fedfc58d3c881cf6b0218
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797115"
---
# <a name="automation-error"></a><span data-ttu-id="ccfd1-103">自动错误</span><span class="sxs-lookup"><span data-stu-id="ccfd1-103">Automation error</span></span>

<span data-ttu-id="ccfd1-104">执行方法或者获取或设置对象变量的属性时发生错误。</span><span class="sxs-lookup"><span data-stu-id="ccfd1-104">An error occurred while executing a method or getting or setting a property of an object variable.</span></span> <span data-ttu-id="ccfd1-105">错误由创建该对象的应用程序报告。</span><span class="sxs-lookup"><span data-stu-id="ccfd1-105">The error was reported by the application that created the object.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ccfd1-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="ccfd1-106">To correct this error</span></span>  
  
1. <span data-ttu-id="ccfd1-107">检查 `Err` 对象的属性，以确定错误来源和错误性质。</span><span class="sxs-lookup"><span data-stu-id="ccfd1-107">Check the properties of the `Err` object to determine the source and nature of the error.</span></span>  
  
2. <span data-ttu-id="ccfd1-108">在紧邻访问语句之前使用 `On Error Resume Next` 语句，然后检查紧邻访问语句之后是否存在错误。</span><span class="sxs-lookup"><span data-stu-id="ccfd1-108">Use the `On Error Resume Next` statement immediately before the accessing statement, and then check for errors immediately after the accessing statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccfd1-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="ccfd1-109">See also</span></span>

- [<span data-ttu-id="ccfd1-110">错误类型</span><span class="sxs-lookup"><span data-stu-id="ccfd1-110">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
- [<span data-ttu-id="ccfd1-111">与我们交流</span><span class="sxs-lookup"><span data-stu-id="ccfd1-111">Talk to Us</span></span>](/visualstudio/ide/feedback-options)
