---
description: 了解详细信息： <seealso> (Visual Basic)
title: <seealso>
ms.date: 07/20/2015
helpviewer_keywords:
- <seealso> XML tag
- seealso XML tag
ms.assetid: 36050c95-1af2-4284-b9b6-1a70691ed978
ms.openlocfilehash: 0bf6fa69ad63db016b42e31f717f521f82bbe20e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640311"
---
# <a name="seealso-visual-basic"></a>\<seealso> (Visual Basic)

指定显示在 "另请参见" 部分中的链接。  
  
## <a name="syntax"></a>语法  
  
```xml  
<seealso cref="member"/>  
```  
  
## <a name="parameters"></a>参数  

 `member`  
 对可从当前编译环境调用的成员或字段的引用。 编译器检查是否存在给定的码位元素，并将 `member` 传递到输出 XML 中的元素名称。 `member` 必须出现在双引号 (" ") 内。  
  
## <a name="remarks"></a>备注  

 使用 `<seealso>` 标记来指定要在 "另请参见" 部分中显示的文本。 使用 [\<see>](see.md) 从文本内指定链接。  
  
 使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。  
  
## <a name="example"></a>示例  

 此示例使用 " `<seealso>` 备注" 部分中的标记 `DoesRecordExist` 来引用 `UpdateRecord` 方法。  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>请参阅

- [XML 注释标记](index.md)
