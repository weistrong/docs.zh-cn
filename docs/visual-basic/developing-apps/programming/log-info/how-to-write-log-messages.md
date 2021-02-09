---
description: 详细了解：操作说明：编写日志消息 (Visual Basic)
title: 如何：写入日志消息
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application.Log object, writing log messages
ms.assetid: 972a3e0c-2996-4623-a7a9-d7ebc4d207f8
ms.openlocfilehash: ed455fdb2cebda908981514bef932942adf499ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797297"
---
# <a name="how-to-write-log-messages-visual-basic"></a><span data-ttu-id="71930-103">如何：编写日志消息 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="71930-103">How to: Write Log Messages (Visual Basic)</span></span>

<span data-ttu-id="71930-104">可以使用 `My.Application.Log` 和 `My.Log` 对象来记录有关应用程序的信息。</span><span class="sxs-lookup"><span data-stu-id="71930-104">You can use the `My.Application.Log` and `My.Log` objects to log information about your application.</span></span> <span data-ttu-id="71930-105">本示例将演示如何使用 `My.Application.Log.WriteEntry` 方法来记录跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="71930-105">This example shows how to use the `My.Application.Log.WriteEntry` method to log tracing information.</span></span>

<span data-ttu-id="71930-106">若要记录异常信息，请使用 `My.Application.Log.WriteException` 方法；请参阅[如何：记录异常](how-to-log-exceptions.md)。</span><span class="sxs-lookup"><span data-stu-id="71930-106">For logging exception information, use the `My.Application.Log.WriteException` method; see [How to: Log Exceptions](how-to-log-exceptions.md).</span></span>

## <a name="example"></a><span data-ttu-id="71930-107">示例</span><span class="sxs-lookup"><span data-stu-id="71930-107">Example</span></span>

<span data-ttu-id="71930-108">本示例将使用 `My.Application.Log.WriteEntry` 方法来写出跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="71930-108">This example uses the `My.Application.Log.WriteEntry` method to write out the trace information.</span></span>

[!code-vb[VbVbalrMyApplicationLog#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/Form1.vb#11)]

## <a name="net-framework-security"></a><span data-ttu-id="71930-109">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="71930-109">.NET Framework Security</span></span>

<span data-ttu-id="71930-110">请确保写入日志的数据不包含敏感信息，如用户密码。</span><span class="sxs-lookup"><span data-stu-id="71930-110">Make sure the data you write to the log does not include sensitive information such as user passwords.</span></span> <span data-ttu-id="71930-111">有关详细信息，请参阅[使用应用程序日志](working-with-application-logs.md)。</span><span class="sxs-lookup"><span data-stu-id="71930-111">For more information, see [Working with Application Logs](working-with-application-logs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="71930-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="71930-112">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [<span data-ttu-id="71930-113">使用应用程序日志</span><span class="sxs-lookup"><span data-stu-id="71930-113">Working with Application Logs</span></span>](working-with-application-logs.md)
- [<span data-ttu-id="71930-114">如何：日志异常</span><span class="sxs-lookup"><span data-stu-id="71930-114">How to: Log Exceptions</span></span>](how-to-log-exceptions.md)
- [<span data-ttu-id="71930-115">演练：确定 My.Application.Log 写入信息的位置</span><span class="sxs-lookup"><span data-stu-id="71930-115">Walkthrough: Determining Where My.Application.Log Writes Information</span></span>](walkthrough-determining-where-my-application-log-writes-information.md)
- [<span data-ttu-id="71930-116">演练：更改 My.Application.Log 写入信息的位置</span><span class="sxs-lookup"><span data-stu-id="71930-116">Walkthrough: Changing Where My.Application.Log Writes Information</span></span>](walkthrough-changing-where-my-application-log-writes-information.md)
- [<span data-ttu-id="71930-117">演练：筛选 My.Application.Log 输出</span><span class="sxs-lookup"><span data-stu-id="71930-117">Walkthrough: Filtering My.Application.Log Output</span></span>](walkthrough-filtering-my-application-log-output.md)
