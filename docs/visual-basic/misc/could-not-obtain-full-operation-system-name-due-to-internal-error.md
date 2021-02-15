---
description: 了解详细信息：由于内部错误，无法获取完整的操作系统名
title: 由于内部错误，无法获取完整的操作系统名
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: d274a08728b084b21309862de69e2fded5c164da
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100463488"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a>由于内部错误，无法获取完整的操作系统名

由于内部错误，无法获取完整的操作系统名。 这可能由当前计算机上不存在 WMI 导致。  
  
 对 `My.Computer.Info.OSFullName` 属性的调用失败。 此失败的可能原因是当前计算机上是否未安装 Windows Management Instrumentation (WMI)。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 将调用周围的 `Try...Catch` 块添加到 `My.Computer.Info.OSFullName` 属性。  
  
2. 有关 WMI 及其安装方法的详细信息，请参阅和搜索 "Windows Management Instrumentation Core"。  
  
## <a name="see-also"></a>请参阅

- [OSFullName。](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [在 .NET 中处理和引发异常](../../standard/exceptions/index.md)
- [Try...Catch...Finally 语句](../language-reference/statements/try-catch-finally-statement.md)
