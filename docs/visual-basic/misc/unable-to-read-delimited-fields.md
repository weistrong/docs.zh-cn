---
description: 了解详细信息：无法读取分隔字段，因为当 EscapeQuotes 设置为 True 时，双引号不是合法的分隔符
title: 无法读取分隔字段，因为当 EscapeQuotes 设置为 True 时，双引号不是合法的分隔符
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_IllegalDelimiter
ms.assetid: ab8a0c3a-b89c-4617-9e31-7e81f5dca433
ms.openlocfilehash: 066b5110eaddad74b64f1d86683d7ca2a0a619f7
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474390"
---
# <a name="unable-to-read-delimited-fields-because-a-double-quote-is-not-a-legal-delimiter-when-escapequotes-is-set-to-true"></a>无法读取分隔字段，因为当 EscapeQuotes 设置为 True 时，双引号不是合法的分隔符

`TextFieldParser` 无法从文件中读取，因为引号 (") 以分隔符形式提供，且 `EscapeQuotes` 设置为 `True`。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
- 将 `EscapeQuotes` 设置为 `False`。  
  
## <a name="see-also"></a>请参阅

- [TextFieldParser.SetDelimiters 方法](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters%2A)
- [TextFieldParser.Delimiters 属性](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters%2A)
- [如何：读取逗号分隔的文本文件](../developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)
- [TextFieldParser Object](../language-reference/objects/textfieldparser-object.md)
