---
description: '了解更多相关信息： BC30766： " <functionname> " 未声明 (智能设备/Visual Basic 编译器错误) '
title: 未声明“<functionname>”（智能设备-Visual Basic 编译器错误）
ms.date: 07/20/2015
f1_keywords:
- bc30766
- vbc30766
helpviewer_keywords:
- BC30766
ms.assetid: 13918600-6087-40d7-8134-32aa9d3bfda4
ms.openlocfilehash: 939af146656bc5e5e84b3f0672c730f6a816c043
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796153"
---
# <a name="bc30766-functionname-is-not-declared-smart-devicevisual-basic-compiler-error"></a>BC30766： " \<functionname> " 未声明 (智能设备/Visual Basic 编译器错误) 

<`functionname` 未声明>。 文件 I/O 功能在 `Microsoft.VisualBasic` 命名空间中通常是可用的，但目标版本的 .NET Compact Framewor 不支持它。

 **错误 ID：** BC30766

## <a name="to-correct-this-error"></a>更正此错误

- 利用 `System.IO` 命名空间中定义的函数执行文件操作。

## <a name="see-also"></a>请参阅

- <xref:System.IO>
- [使用 Visual Basic 访问文件](../../developing-apps/programming/drives-directories-files/file-access.md)
