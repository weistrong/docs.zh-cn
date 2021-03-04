---
description: 了解详细信息：自动化错误
title: 自动错误
ms.date: 07/20/2015
f1_keywords:
- vbrID440
ms.assetid: 2c4be5c5-2f0d-4a2b-96fe-d1b24f08fc4c
ms.openlocfilehash: bf3e61bb9b8fec9a831d211b70abdca322c1fe06
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106600"
---
# <a name="automation-error"></a><span data-ttu-id="dcb9d-103">自动错误</span><span class="sxs-lookup"><span data-stu-id="dcb9d-103">Automation error</span></span>

<span data-ttu-id="dcb9d-104">执行方法或者获取或设置对象变量的属性时发生错误。</span><span class="sxs-lookup"><span data-stu-id="dcb9d-104">An error occurred while executing a method or getting or setting a property of an object variable.</span></span> <span data-ttu-id="dcb9d-105">错误由创建该对象的应用程序报告。</span><span class="sxs-lookup"><span data-stu-id="dcb9d-105">The error was reported by the application that created the object.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dcb9d-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="dcb9d-106">To correct this error</span></span>  
  
1. <span data-ttu-id="dcb9d-107">检查 `Err` 对象的属性，以确定错误来源和错误性质。</span><span class="sxs-lookup"><span data-stu-id="dcb9d-107">Check the properties of the `Err` object to determine the source and nature of the error.</span></span>  
  
2. <span data-ttu-id="dcb9d-108">在紧邻访问语句之前使用 `On Error Resume Next` 语句，然后检查紧邻访问语句之后是否存在错误。</span><span class="sxs-lookup"><span data-stu-id="dcb9d-108">Use the `On Error Resume Next` statement immediately before the accessing statement, and then check for errors immediately after the accessing statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dcb9d-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dcb9d-109">See also</span></span>

- [<span data-ttu-id="dcb9d-110">错误类型</span><span class="sxs-lookup"><span data-stu-id="dcb9d-110">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
- [<span data-ttu-id="dcb9d-111">Visual Studio 反馈选项</span><span class="sxs-lookup"><span data-stu-id="dcb9d-111">Visual Studio feedback options</span></span>](/visualstudio/ide/feedback-options)
