---
description: '了解有关以下方面的详细信息：程序集 (Visual Basic) '
title: 程序集
ms.date: 07/20/2015
f1_keywords:
- vb.Assembly
- vb.AssemblyAttribute
- Assembly
helpviewer_keywords:
- Assembly modifier
- Assembly keyword [Visual Basic]
- attribute blocks, Assembly keyword
ms.assetid: 925e7471-3bdf-4b51-bb93-cbcfc6efc52f
ms.openlocfilehash: 60b8ce4ed2b8b5cb7deeabb702c33d1e561d765f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701178"
---
# <a name="assembly-visual-basic"></a>程序集 (Visual Basic)

指定源文件开头的属性应用于整个程序集。  
  
## <a name="remarks"></a>备注  

 许多属性都属于单个编程元素，如类或属性。 可以通过将特性块附加到尖括号 (在) 中，将此类特性直接应用于 `< >` 声明语句。  
  
 如果某个特性不仅与以下元素有关，而不属于整个程序集，则可以将特性块放在源文件的开头，并使用关键字标识该特性 `Assembly` 。 如果它适用于当前程序集模块，则使用 [module](module-keyword.md) 关键字。  
  
 你还可以在 AssemblyInfo 文件中将属性应用于程序集，在这种情况下，你不必在主源代码文件中使用属性块。  
  
## <a name="see-also"></a>请参阅

- [模块 \<keyword>](module-keyword.md)
- [属性概述](../../programming-guide/concepts/attributes/index.md)
