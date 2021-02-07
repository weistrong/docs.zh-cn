---
description: '了解有关以下内容的详细信息： Ansi (Visual Basic) '
title: Ansi
ms.date: 07/20/2015
f1_keywords:
- vb.Ansi
helpviewer_keywords:
- Declare statement [Visual Basic], marshaling strings [Visual Basic]
- ANSI, Visual Basic
- ANSI
ms.assetid: 4f1fa6ff-5557-41ab-b6da-90baf4c15917
ms.openlocfilehash: c93472cbf6a8203f05353e0394b52c44686c0070
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701191"
---
# <a name="ansi-visual-basic"></a>Ansi (Visual Basic)

指定 Visual Basic 应将所有字符串封送到美国国家标准学会 (ANSI) 值，而不考虑所声明的外部过程的名称。  
  
 调用在项目外部定义的过程时，Visual Basic 编译器无法访问正确调用过程所需的信息。 此信息包括过程的位置、标识方法、调用序列和返回类型，以及它使用的字符串字符集。 [Declare 语句](../statements/declare-statement.md)创建对外部过程的引用并提供此必要信息。  
  
 `charsetmodifier`语句中的部分 `Declare` 提供在调用外部过程期间封送处理字符串的字符集信息。 它还会影响 Visual Basic 搜索外部文件的外部过程名称的方式。 `Ansi`修饰符指定 Visual Basic 应将所有字符串封送为 ANSI 值，并在搜索过程中查找该过程而不修改其名称。  
  
 如果未指定字符集修饰符， `Ansi` 则默认为。  
  
## <a name="remarks"></a>备注  

 `Ansi`可以在此上下文中使用修饰符：  
  
 [Declare Statement](../statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a>智能设备开发人员说明  

 不支持此关键字。  
  
## <a name="see-also"></a>请参阅

- [Auto](auto.md)
- [Unicode](unicode.md)
- [关键字](../keywords/index.md)
