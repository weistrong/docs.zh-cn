---
description: 了解详细信息： BC42319： XML 注释异常必须具有 "cref" 特性
title: XML 注释异常必须具有“cref”特性
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: e602a2973d95f70d5ab532e6be319a9575d239a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701451"
---
# <a name="bc42319-xml-comment-exception-must-have-a-cref-attribute"></a>BC42319： XML 注释异常必须具有 "cref" 特性

\<exception>标记提供了一种方法来记录可由方法引发的异常。 必需的 `cref` 属性指定由文档生成器检查的成员的名称。 如果该成员存在，则将其转换为文档文件中的规范元素名称。

**错误 ID：** BC42319

## <a name="to-correct-this-error"></a>更正此错误

将 `cref` 属性添加到异常，如下所示：

```xml
<exception cref="member">description</exception>
```

## <a name="see-also"></a>请参阅

- [\<exception>](../xmldoc/exception.md)
- [如何：创建 XML 文档](../../programming-guide/program-structure/how-to-create-xml-documentation.md)
- [XML 注释标记](../xmldoc/index.md)
