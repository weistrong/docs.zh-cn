---
description: '了解详细信息： #Const 指令'
title: '#Const 指令'
ms.date: 07/20/2015
f1_keywords:
- vb.#Const
- '#vb.Const'
- '#Const'
helpviewer_keywords:
- '#Const directive'
- conditional compilation [Visual Basic], directives
- Const directive (#Const)
- Visual Basic compiler, compiler directives
- constants [Visual Basic], Const directive
- constants [Visual Basic], declaring
- Const statement [Visual Basic], directive (#Const)
- 'declaring constants [Visual Basic], #const directive'
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
ms.openlocfilehash: 9597666ee1320f5dfda226040f93a84eb60a3deb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797271"
---
# <a name="const-directive"></a>#Const 指令

为 Visual Basic 定义条件编译器常量。  
  
## <a name="syntax"></a>语法  
  
```vb  
#Const constname = expression  
```  
  
## <a name="parts"></a>组成部分  

 `constname`  
 必需。 要定义的常数的名称。  
  
 `expression`  
 必需。 文本、其他条件编译器常量或包含除以外的任何或所有算术或逻辑运算符的任意组合 `Is` 。  
  
## <a name="remarks"></a>备注  

 条件编译器常量总是专用于它们所在的文件。 不能使用指令创建公共编译器常量 `#Const` ; 只能在用户界面中或使用 `/define` 编译器选项创建它们。  
  
 只能在中使用条件编译器常量和文本 `expression` 。 使用定义的标准常数 `Const` 会导致错误。 相反，您可以使用只使用关键字定义 `#Const` 的常量进行条件编译。 常数也可以是未定义的，在这种情况下，它们的值为 `Nothing` 。  
  
## <a name="example"></a>示例  

 此示例使用 `#Const` 指令。  
  
 [!code-vb[VbVbalrConditionalComp#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#3)]  
  
## <a name="see-also"></a>请参阅

- [-define (Visual Basic)](../../reference/command-line-compiler/define.md)
- [#If...Then...#Else 指令](if-then-else-directives.md)
- [Const 语句](../statements/const-statement.md)
- [条件编译](../../programming-guide/program-structure/conditional-compilation.md)
- [If...Then...Else 语句](../statements/if-then-else-statement.md)
