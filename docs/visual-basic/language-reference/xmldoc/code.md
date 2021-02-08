---
description: 了解详细信息： <code>(Visual Basic)
title: <code>
ms.date: 07/20/2015
helpviewer_keywords:
- code XML tag
- <code> XML tag
ms.assetid: 925e5342-be05-45f2-bf66-7398bbd6710e
ms.openlocfilehash: 80fc0988f60d9d82b9c88734f86b20ebccc80b7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787495"
---
# <a name="code-visual-basic"></a>\<code> (Visual Basic)

指示文本为多行代码。  
  
## <a name="syntax"></a>语法  
  
```xml  
<code>content</code>  
```  
  
## <a name="parameters"></a>参数  

 `content`  
 要标记为代码的文本。  
  
## <a name="remarks"></a>备注  

 使用 `<code>` 标记将多行指示为代码。 用于 [\<c>](c.md) 指示应将说明内的文本标记为代码。  
  
 使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。  
  
## <a name="example"></a>示例  

 此示例使用 \<code> 标记来包含用于使用字段的示例代码 `ID` 。  
  
 [!code-vb[VbVbcnXmlDocComments#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#2)]  
  
## <a name="see-also"></a>请参阅

- [XML 注释标记](index.md)
