---
description: 了解更多相关信息：使用 "Object" 类型的参数时，请使用 "FilePutObject" 而不是 "FilePut"
title: 在使用 "Object" 类型的自变量时，请使用 "FilePutObject"，而不要使用 "FilePut"
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: 5e5822999aa39bff4d43f83a2719341034cdcadc
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100460093"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a>在使用 "Object" 类型的自变量时，请使用 "FilePutObject"，而不要使用 "FilePut"

`FilePut` 方法包含 `Object`类型的参数。 应使用`FilePutObject` 替代 `FilePut` ，以避免多义性。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
- 将 `FilePut` 替换为 `FilePutObject`。  
  
- 将 `Object` 参数强制转换为一个更明确的类型。  
  
- 使用 `My.Computer.FileSystem` 对象中的可用功能。  
  
## <a name="see-also"></a>请参阅

- [文件系统文件](xref:Microsoft.VisualBasic.FileIO.FileSystem)
- [文件 My.computer.filesystem.writeallbytes](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
