---
description: '了解详细信息：此数组是固定的或临时锁定的 (Visual Basic) '
title: 此数组是固定数组或被临时锁定
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: 034bcc23055f7fb3f707e1105589a4526e6f9009
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641208"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a>此数组被固定或临时锁定 (Visual Basic)

此错误具有以下可能的原因：  
  
- 使用 `ReDim` 更改固定大小数组的元素数。  
  
- Redimensioning 模块级动态数组，其中一个元素已作为参数传递给过程。 如果传递了某个元素，则会锁定数组，以防在过程中为引用参数释放内存。  
  
- 尝试向 `Variant` 包含数组的变量赋值，但 `Variant` 当前已锁定。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 如果数组是在) 过程中声明的，则通过使用 (进行声明来使原始数组成为动态的（而不是固定的 `ReDim` ）; 或者，如果数组是在模块级别声明的，则通过在不指定元素数目的情况下声明，而不指定 (元素数  
  
2. 确定是否确实需要传递元素，因为它在模块中的所有过程中可见。  
  
3. 确定锁定 `Variant` 和更正的内容。  
  
## <a name="see-also"></a>请参阅

- [数组](../../programming-guide/language-features/arrays/index.md)
