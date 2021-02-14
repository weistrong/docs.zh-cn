---
description: 了解详细信息：无法删除系统事件日志
title: 不能删除系统事件日志
ms.date: 07/20/2015
ms.assetid: 26ca8819-4ce5-49c6-98f3-27fe9e2e8e3d
ms.openlocfilehash: 5cf64303c9b4d3b4a03a5f224c1a97859d49d3d1
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100455374"
---
# <a name="system-event-log-cannot-be-deleted"></a><span data-ttu-id="a8800-103">不能删除系统事件日志</span><span class="sxs-lookup"><span data-stu-id="a8800-103">System event log cannot be deleted</span></span>

<span data-ttu-id="a8800-104">试图删除系统事件日志（该日志是不能被删除的）。</span><span class="sxs-lookup"><span data-stu-id="a8800-104">An attempt has been made to delete the system event log, which cannot be deleted.</span></span> <span data-ttu-id="a8800-105">系统日志跟踪系统事件（如系统启动和硬件故障）。</span><span class="sxs-lookup"><span data-stu-id="a8800-105">The system log tracks system events such as system startup and hardware failures.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a8800-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a8800-106">To correct this error</span></span>  
  
- <span data-ttu-id="a8800-107">请考虑让应用程序写入应用程序或自定义日志，而不是系统事件日志。</span><span class="sxs-lookup"><span data-stu-id="a8800-107">Consider having your application write to an application or custom log, rather than the system event log.</span></span>  
  
- <span data-ttu-id="a8800-108">请勿试图删除系统事件日志。</span><span class="sxs-lookup"><span data-stu-id="a8800-108">Do not attempt to delete the system event log.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8800-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="a8800-109">See also</span></span>

- <span data-ttu-id="a8800-110">[管理事件日志](/previous-versions/visualstudio/visual-studio-2008/4f69axw4(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a8800-110">[Administering Event Logs](/previous-versions/visualstudio/visual-studio-2008/4f69axw4(v=vs.90))</span></span>
- <span data-ttu-id="a8800-111">[如何：创建和移除自定义事件日志](/previous-versions/visualstudio/visual-studio-2008/49dwckkz(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a8800-111">[How to: Create and Remove Custom Event Logs](/previous-versions/visualstudio/visual-studio-2008/49dwckkz(v=vs.90))</span></span>
