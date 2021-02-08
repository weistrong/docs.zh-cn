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
# <a name="resume-without-error"></a>无错误继续执行

`Resume`语句出现在错误处理代码之外，或代码跳转到错误处理程序，即使没有出错。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 将 `Resume` 语句移动到错误处理程序中，或将其删除。  
  
2. 跳转到标签不能跨过程出现，因此请在过程中搜索标识错误处理程序的标签。 如果找到指定为不是语句的语句目标的重复标签 `GoTo` `On Error GoTo` ，则更改行标签以同意其预期目标。  
  
## <a name="see-also"></a>请参阅

- [Resume 语句](../statements/resume-statement.md)
- [On Error 语句](../statements/on-error-statement.md)
