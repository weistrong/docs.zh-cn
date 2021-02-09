---
description: 详细了解：<inheritdoc>（C# 编程指南）
title: <inheritdoc> - C# 编程指南
ms.date: 01/21/2020
f1_keywords:
- inheritdoc
- <inheritdoc>
helpviewer_keywords:
- <inheritdoc> C# XML tag
- inheritdoc C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 960bdfbcec1e3f6a89675273f63b6d398e44947e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719391"
---
# <a name="inheritdoc-c-programming-guide"></a>\<inheritdoc>（C# 编程指南）

## <a name="syntax"></a>语法  
  
```xml  
<inheritdoc/>
```  

## <a name="inheritdoc"></a>InheritDoc

继承基类、接口和类似方法中的 XML 注释。 这样不必复制和粘贴重复的 XML 注释，并自动保持 XML 注释同步。
  
## <a name="remarks"></a>备注  

在基类或接口中添加 XML 注释，并让 InheritDoc 将注释复制到实现类中。

向同步方法添加 XML 注释，并让 InheritDoc 将注释复制到相同方法的异步版本中。  

如果要从特定成员复制注释，可以使用 `cref` 特性来指定成员。
  
## <a name="examples"></a>示例

[!code-csharp[csProgGuideDocComments#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#16)]  

[!code-csharp[csProgGuideDocComments#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#17)]  

## <a name="see-also"></a>另请参阅

- [C# 编程指南](../index.md)
- [建议的文档注释标记](./recommended-tags-for-documentation-comments.md)
