---
description: '了解有关以下方面的详细信息：权限被拒绝 (Visual Basic) '
title: 权限被拒绝
ms.date: 07/20/2015
f1_keywords:
- vbrID70
ms.assetid: 71f46756-f522-4814-aab4-492bf9924245
ms.openlocfilehash: dcd7f69c1294d22510a3600a3feb045da30faf17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795412"
---
# <a name="permission-denied-visual-basic"></a>权限被拒绝 (Visual Basic)

尝试写入到写保护的磁盘或访问锁定的文件。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 若要打开写保护的文件，请更改文件的写保护特性。  
  
2. 请确保其他进程未锁定该文件，并等待打开该文件，直到另一个进程释放它。  
  
3. 若要访问注册表，请检查你的用户权限是否包括此类型的注册表访问权限。  
  
## <a name="see-also"></a>请参阅

- [错误类型](../../programming-guide/language-features/error-types.md)
