---
description: 了解更多： BC30830：不再支持 "Line" 语句
title: 不再支持“Line”语句（Visual Basic 编译器错误）
ms.date: 07/20/2015
f1_keywords:
- bc30830
- vbc30830
helpviewer_keywords:
- BC30830
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
ms.openlocfilehash: 16696856cee365171000e7b0abc206c42d3f3174
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795867"
---
# <a name="bc30830-line-statements-are-no-longer-supported"></a>BC30830：不再支持 "Line" 语句

不再支持行语句。 文件 i/o 功能提供为 `Microsoft.VisualBasic.FileSystem.LineInput` ，图形功能作为提供 `System.Drawing.Graphics.DrawLine` 。

 **错误 ID：** BC30830

## <a name="to-correct-this-error"></a>更正此错误

- 如果执行文件访问，请使用 `Microsoft.VisualBasic.FileSystem.LineInput` 。

- 如果执行图形，则请使用 `System.Drawing.Graphics.Drawline`。

## <a name="see-also"></a>请参阅

- <xref:System.IO>
- <xref:System.Drawing>
- [使用 Visual Basic 访问文件](../../developing-apps/programming/drives-directories-files/file-access.md)
