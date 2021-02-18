---
description: 详细了解：-nologo (Visual Basic)
title: -nologo
ms.date: 03/13/2018
helpviewer_keywords:
- -nologo compiler option [Visual Basic]
- banners [Visual Basic], suppressing startup
- nologo compiler option [Visual Basic]
- /nologo compiler option [Visual Basic]
ms.assetid: 25ef54b6-d676-4639-a2d2-a747a158bc07
ms.openlocfilehash: 370889fbd5d4e499ba27ff8bee4adc16a7a71876
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434883"
---
# <a name="-nologo-visual-basic"></a>-nologo (Visual Basic)

在编译期间禁止显示版权标志和信息性消息。  
  
## <a name="syntax"></a>语法  
  
```console  
-nologo  
```  
  
## <a name="remarks"></a>备注  

 如果指定 `-nologo`，编译器不会显示版权标志。 默认情况，`-nologo` 是无效的。  
  
> [!NOTE]
> `-nologo` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。  
  
## <a name="example"></a>示例  

 以下代码编译 `T2.vb` 并且不显示任何版权标志。  
  
```console
vbc -nologo t2.vb  
```  
  
## <a name="see-also"></a>请参阅

- [Visual Basic 命令行编译器](index.md)
- [示例编译命令行](sample-compilation-command-lines.md)
