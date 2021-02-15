---
description: 了解详细信息：不存在鼠标
title: 没有鼠标
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoMouseIsPresent
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
ms.openlocfilehash: 1964f1def655a1e38ce2b8919a69ab2e6ac929a7
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100479122"
---
# <a name="no-mouse-is-present"></a>没有鼠标

调用了 `My.Computer.Mouse` 对象的一个属性，但是计算机未安装鼠标或鼠标端口。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
- 在调用周围将 `Try...Catch` 块添加到 `My.Computer.Mouse` 对象的属性。  
  
     — 或 —  
  
- 在计算机上安装鼠标。  
  
## <a name="see-also"></a>请参阅

- [My.Computer.Mouse](xref:Microsoft.VisualBasic.Devices.Mouse)
- [在 .NET 中处理和引发异常](../../standard/exceptions/index.md)
- [Try...Catch...Finally 语句](../language-reference/statements/try-catch-finally-statement.md)
