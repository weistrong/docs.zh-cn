---
description: 了解详细信息： BC30663： <attributename> 不能多次应用特性 ""
title: 特性“<attributename>”不能应用多次
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: 84b77111a7401eb6f30eb7cd167f4b5689f33e77
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797141"
---
# <a name="bc30663-attribute-attributename-cannot-be-applied-multiple-times"></a>BC30663：特性 " \<attributename> " 不能应用多次

特性只能应用一次。 `AttributeUsage`特性确定特性是否可以应用多次。

 **错误 ID：** BC30663

## <a name="to-correct-this-error"></a>更正此错误

1. 请确保属性仅应用一次。

2. 如果使用的是你开发的自定义特性，请考虑将其 `AttributeUsage` 特性更改为允许使用多种特性，如下面的示例所示。

```vb
<AttributeUsage(AllowMultiple := True)>
```

## <a name="see-also"></a>请参阅

- <xref:System.AttributeUsageAttribute>
- [创建自定义特性](../../programming-guide/concepts/attributes/creating-custom-attributes.md)
- [AttributeUsage](../../programming-guide/concepts/attributes/attributeusage.md)
