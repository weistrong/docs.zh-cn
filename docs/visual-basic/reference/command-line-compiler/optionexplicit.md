---
description: 详细了解：-optionexplicit
title: -optionexplicit
ms.date: 07/20/2015
f1_keywords:
- /optionexplicit
- -optionexplicit
helpviewer_keywords:
- /optionexplicit compiler option [Visual Basic]
- optionexplicit compiler option [Visual Basic]
- -optionexplicit compiler option [Visual Basic]
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
ms.openlocfilehash: 4d1ab14bbf9de176de17fb5077f4bb919f5472b4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433557"
---
# <a name="-optionexplicit"></a>-optionexplicit

如果变量在使用之前未被声明，则会导致编译器报告错误。  
  
## <a name="syntax"></a>语法  
  
```console  
-optionexplicit[+ | -]  
```  
  
## <a name="arguments"></a>自变量  

 `+` &#124; `-`  
 可选。 指定 `-optionexplicit+` 可要求显式声明变量。 `-optionexplicit+` 选项是默认选项，与 `-optionexplicit` 相同。 `-optionexplicit-` 选项启用变量的隐式声明。  
  
## <a name="remarks"></a>备注  

 如果源代码文件包含 [Option Explicit 语句](../../language-reference/statements/option-explicit-statement.md)，则语句将重写 `-optionexplicit` 命令行编译器设置。  
  
### <a name="to-set--optionexplicit-in-the-visual-studio-ide"></a>若要在 Visual Studio IDE 中设置 -optionexplicit  
  
1. 在 **“解决方案资源管理器”** 中选择一个项目。 在“项目”菜单上，单击“属性”   。
  
2. 单击“编译”  选项卡。  
  
3. 修改“Option Explicit”框中的值。   
  
## <a name="example"></a>示例  

 以下代码在使用 `-optionexplicit-` 时进行编译。  
  
 [!code-vb[VbVbalrCompiler#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionExplicitOff.vb#5)]  
  
## <a name="see-also"></a>请参阅

- [Visual Basic 命令行编译器](index.md)
- [-optioncompare](optioncompare.md)
- [-optionstrict](optionstrict.md)
- [-optioninfer](optioninfer.md)
- [示例编译命令行](sample-compilation-command-lines.md)
- [Option Explicit 语句](../../language-reference/statements/option-explicit-statement.md)
- [“选项”对话框 ->“项目”->“Visual Basic 默认值”](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
