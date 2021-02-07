---
description: '了解详细信息： Unicode (Visual Basic) '
title: Unicode
ms.date: 07/20/2015
f1_keywords:
- vb.Unicode
helpviewer_keywords:
- Unicode, external references
- Declare statement [Visual Basic], marshaling strings
- Unicode keyword [Visual Basic]
- Unicode, marshaling strings
ms.assetid: 0021d5ff-3209-444e-8497-420f3e6ee075
ms.openlocfilehash: b0c71d8fdefe3f0d240201e0d57265e5c6081d50
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700710"
---
# <a name="unicode-visual-basic"></a>Unicode (Visual Basic)

指定 Visual Basic 应将所有字符串封送到 Unicode 值，而不考虑所声明的外部过程的名称。  
  
 调用在项目外部定义的过程时，Visual Basic 编译器无权访问它必须具有的信息，以便正确调用过程。 此信息包括过程的位置、标识方法、调用序列和返回类型，以及它使用的字符串字符集。 [Declare 语句](../statements/declare-statement.md)创建对外部过程的引用并提供此必要信息。  
  
 `charsetmodifier`语句中的部分 `Declare` 提供了字符集信息以在调用外部过程的过程中封送字符串。 它还会影响 Visual Basic 搜索外部文件的外部过程名称的方式。 `Unicode`修饰符指定 Visual Basic 应将所有字符串封送为 Unicode 值，并且应在搜索过程中查找过程而不修改其名称。  
  
 如果未指定字符集修饰符， `Ansi` 则默认为。  
  
## <a name="remarks"></a>备注  

 `Unicode`可以在此上下文中使用修饰符：  
  
 [Declare Statement](../statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a>智能设备开发人员说明  

 不支持此关键字。  
  
## <a name="see-also"></a>请参阅

- [Ansi](ansi.md)
- [Auto](auto.md)
- [关键字](../keywords/index.md)
