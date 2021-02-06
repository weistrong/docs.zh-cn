---
description: '了解详细信息： <see> (Visual Basic) '
title: <see>
ms.date: 07/20/2015
helpviewer_keywords:
- see XML tag
- <see> XML tag
ms.assetid: 7e18f60b-ef4a-4678-a797-5eb918635ca9
ms.openlocfilehash: 46dd67710f83d6c4549ddfeb6b7bbc1503b7aa1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640337"
---
# <a name="see-visual-basic"></a>\<see> (Visual Basic)

指定指向另一个成员的链接。  
  
## <a name="syntax"></a>语法  
  
```xml  
<see cref="member"/>  
```  
  
## <a name="parameters"></a>参数  

 `member`  
 对可从当前编译环境调用的成员或字段的引用。 编译器检查是否存在给定的码位元素，并将 `member` 传递到输出 XML 中的元素名称。 `member` 必须出现在双引号 (" ") 内。  
  
## <a name="remarks"></a>备注  

 使用 `<see>` 标记可以指定文本内的链接。 用于 [\<seealso>](seealso.md) 指示你可能希望在 "另请参见" 部分中显示的文本。  
  
 使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。  
  
## <a name="example"></a>示例  

 此示例使用 " `<see>` 备注" 部分中的标记 `UpdateRecord` 来引用 `DoesRecordExist` 方法。  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>请参阅

- [XML 注释标记](index.md)
