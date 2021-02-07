---
description: 了解详细信息： <para> (Visual Basic)
title: <para>
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: 51dd9ff300d980b4c0576566cad5d17375889ba1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740764"
---
# <a name="para-visual-basic"></a>\<para> (Visual Basic)

指定将内容的格式设置为段落。  
  
## <a name="syntax"></a>语法  
  
```xml  
<para>content</para>  
```  
  
## <a name="parameters"></a>参数  

 `content`  
 段落文本。  
  
## <a name="remarks"></a>备注  

 `<para>` 标记用于标记内，例如 [\<summary>](summary.md)、[\<remarks>](remarks.md) 或 [\<returns>](returns.md)，允许向文本添加结构。  
  
 使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。  
  
## <a name="example"></a>示例  

 此示例使用 `<para>` 标记将方法的 "备注" 部分拆分为 `UpdateRecord` 两个段落。  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>请参阅

- [XML 注释标记](index.md)
