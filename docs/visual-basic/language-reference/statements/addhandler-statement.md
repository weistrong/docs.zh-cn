---
description: 了解详细信息： AddHandler 语句
title: AddHandler 语句
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: c0c34abd7ff225765ab36278825a555e2b84b0d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674098"
---
# <a name="addhandler-statement"></a>AddHandler 语句

在运行时将事件与事件处理程序相关联。  
  
## <a name="syntax"></a>语法  
  
```vb  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a>组成部分  

|||
|---|---|
|event|要处理的事件的名称。|  
|`eventhandler`|处理事件的过程的名称。|
|||
  
## <a name="remarks"></a>备注  

 `AddHandler`和 `RemoveHandler` 语句允许您在程序执行过程中随时启动和停止事件处理。  
  
 过程的签名 `eventhandler` 必须与事件的签名相匹配 `event` 。  
  
 `Handles` 关键字和 `AddHandler` 语句都允许你指定特定过程处理特定事件，但存在差异。 `AddHandler` 语句在运行时将过程连接到事件。 定义过程时使用 `Handles` 关键字，以指定它处理特定事件。 有关详细信息，请参阅 [句柄](handles-clause.md)。  
  
> [!NOTE]
> 对于自定义事件，该 `AddHandler` 语句将调用事件的 `AddHandler` 访问器。 有关自定义事件的详细信息，请参阅 [Event 语句](event-statement.md)。  
  
## <a name="example"></a>示例  

 [!code-vb[VbVbalrEvents#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#17)]  
  
## <a name="see-also"></a>请参阅

- [RemoveHandler 语句](removehandler-statement.md)
- [句柄数](handles-clause.md)
- [Event 语句](event-statement.md)
- [事件](../../programming-guide/language-features/events/index.md)
