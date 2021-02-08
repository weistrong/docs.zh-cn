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
# <a name="automation-error"></a>自动错误

执行方法或者获取或设置对象变量的属性时发生错误。 错误由创建该对象的应用程序报告。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 检查 `Err` 对象的属性，以确定错误来源和错误性质。  
  
2. 在紧邻访问语句之前使用 `On Error Resume Next` 语句，然后检查紧邻访问语句之后是否存在错误。  
  
## <a name="see-also"></a>请参阅

- [错误类型](../../programming-guide/language-features/error-types.md)
- [与我们交流](/visualstudio/ide/feedback-options)
