---
description: 了解详细信息：无法写入日志文件，因为写入日志文件会使可用磁盘空间低于 ReservedSpace 值
title: 无法写入日志文件，因为写入日志文件会使可用磁盘空间低于 ReservedSpace 值
ms.date: 07/20/2015
f1_keywords:
- vbrApplicationLog_ReservedSpaceEncroached
ms.assetid: 95832e70-4ecc-47aa-90c1-f35c4d468151
ms.openlocfilehash: e02fa9527539169da3ea99f89246dafe82646cff
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100456947"
---
# <a name="unable-to-write-to-log-file-because-writing-to-it-would-reduce-free-disk-space-below-reservedspace-value"></a><span data-ttu-id="d598b-103">无法写入日志文件，因为写入日志文件会使可用磁盘空间低于 ReservedSpace 值</span><span class="sxs-lookup"><span data-stu-id="d598b-103">Unable to write to log file because writing to it would reduce free disk space below ReservedSpace value</span></span>

<span data-ttu-id="d598b-104"><xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> 类无法写入日志文件，原因如下：</span><span class="sxs-lookup"><span data-stu-id="d598b-104">The <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> class could not write to the log file because:</span></span>  
  
- <span data-ttu-id="d598b-105">可用磁盘空间量（以字节为单位）小于 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> 属性的值</span><span class="sxs-lookup"><span data-stu-id="d598b-105">The amount of free disk space (in bytes) is less than the value of the <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> property</span></span>  
  
     <span data-ttu-id="d598b-106">—并且—</span><span class="sxs-lookup"><span data-stu-id="d598b-106">—and—</span></span>  
  
- <span data-ttu-id="d598b-107"><xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> 属性的值为 <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.ThrowException>。</span><span class="sxs-lookup"><span data-stu-id="d598b-107">The value of the <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> property was <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.ThrowException>.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d598b-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="d598b-108">To correct this error</span></span>  
  
1. <span data-ttu-id="d598b-109">将现有日志存档后将其从计算机中删除，以允许 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> 对象创建新日志。</span><span class="sxs-lookup"><span data-stu-id="d598b-109">Archive the existing logs and remove them from the computer to allow the <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> object to create new logs.</span></span>  
  
2. <span data-ttu-id="d598b-110">将 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> 属性的值更改为一个较小的数字，以保留更少的磁盘空间。</span><span class="sxs-lookup"><span data-stu-id="d598b-110">Change the value of the <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> property to a smaller number to reserve less disk space.</span></span>  
  
3. <span data-ttu-id="d598b-111">如果没有足够的可用磁盘空间，则将 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> 属性设置为 <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.DiscardMessages> 以放弃消息而不发出警告消息。</span><span class="sxs-lookup"><span data-stu-id="d598b-111">Set the <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> property to <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.DiscardMessages> to discard messages without warning if there is not enough free disk space.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d598b-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="d598b-112">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A>
- <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A>
- <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener>
- [<span data-ttu-id="d598b-113">My. .Log</span><span class="sxs-lookup"><span data-stu-id="d598b-113">My.Application.Log</span></span>](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
- [<span data-ttu-id="d598b-114">DirectoryPath。</span><span class="sxs-lookup"><span data-stu-id="d598b-114">My.Application.Info.DirectoryPath</span></span>](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
