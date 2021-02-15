---
description: 了解详细信息：无法完成操作，因为目标目录位于源目录下
title: 未能完成操作，因为目标目录位于源目录下
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: 5fb0bf1d761faf9d3d0c64e8815e28e14841b1fd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100463515"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a>未能完成操作，因为目标目录位于源目录下

循环操作已失败。 循环操作正在循环，因此无法完成。 例如，对象 A 可能会尝试从对象 B 中继承，而后者反之从对象 A 中继承。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
- 继承时，请确保没有任何循环引用。  
  
## <a name="see-also"></a>请参阅

- [错误类型](../programming-guide/language-features/error-types.md)
- [在 Visual Studio 调试器中使用断点](/visualstudio/debugger/using-breakpoints)
