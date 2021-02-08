---
description: 了解有关以下内容的详细信息：已打开文件
title: 文件已打开
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 2f3345c15f4a3095a8e733c2c8424edb25b4dee6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796296"
---
# <a name="file-already-open"></a>文件已打开

有时，必须先关闭文件，然后才能 `FileOpen` 进行其他或其他操作。 此错误的可能原因包括：

- `FileOpen`为已打开的文件执行了顺序输出模式操作

- 语句引用打开的文件。

## <a name="to-correct-this-error"></a>更正此错误

- 在执行语句前关闭文件。

## <a name="see-also"></a>请参阅

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
