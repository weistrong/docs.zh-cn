---
description: 了解详细信息： <returns> (Visual Basic)
title: <returns>
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: ba5f1e231502a67e86ffbb92cf8868c3aecb05d2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640376"
---
# <a name="returns-visual-basic"></a>\<returns> (Visual Basic)

指定属性或函数的返回值。  
  
## <a name="syntax"></a>语法  
  
```xml  
<returns>description</returns>  
```  
  
## <a name="parameters"></a>参数  

 `description`  
 返回值的说明。  
  
## <a name="remarks"></a>备注  

 `<returns>`在方法声明的注释中使用标记来描述返回值。  
  
 使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。  
  
## <a name="example"></a>示例  

 此示例使用 `<returns>` 标记解释函数返回的内容 `DoesRecordExist` 。  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>请参阅

- [XML 注释标记](index.md)
