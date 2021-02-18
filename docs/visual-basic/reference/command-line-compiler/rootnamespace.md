---
description: 详细了解：-rootnamespace
title: -rootnamespace
ms.date: 03/13/2018
f1_keywords:
- /rootnamespace
- rootnamespace
helpviewer_keywords:
- /rootnamespace compiler option [Visual Basic]
- -rootnamespace compiler option [Visual Basic]
- rootnamespace compiler option [Visual Basic]
ms.assetid: e9245edf-6bef-420d-a7c7-324117752783
ms.openlocfilehash: 0e034999a65bf5294e63c8f9cec1a4ce4de39a4b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474078"
---
# <a name="-rootnamespace"></a>-rootnamespace

指定所有类型声明的命名空间。  
  
## <a name="syntax"></a>语法  
  
```console  
-rootnamespace:namespace  
```  
  
## <a name="arguments"></a>自变量  
  
|术语|定义|  
|---|---|  
|`namespace`|命名空间的名称，其中包含当前项目的所有类型声明。|  
  
## <a name="remarks"></a>备注  

 如果使用 Visual Studio 可执行文件 (Devenv.exe) 来编译在 Visual Studio 集成开发环境中创建的项目，请使用 `-rootnamespace` 指定 <xref:VSLangProj80.VBProjectProperties3.RootNamespace%2A> 属性的值。 有关详细信息，请参阅 [Devenv 命令行开关](/visualstudio/ide/reference/devenv-command-line-switches)。  
  
 使用公共语言运行时 MSIL 反汇编程序 (`Ildasm.exe`) 来查看输出文件中的命名空间名称。  
  
|在 Visual Studio 集成开发环境中设置 -rootnamespace|  
|---|  
|1.在 **“解决方案资源管理器”** 中选择一个项目。 在“项目”菜单上，单击“属性”   。 <br />2.单击“应用程序”  选项卡。<br />3.修改“根命名空间”  框中的值。|  
  
## <a name="example"></a>示例  

 下面的代码编译 `In.vb`，并将所有类型声明包含在命名空间 `mynamespace` 中。  
  
```console
vbc -rootnamespace:mynamespace in.vb  
```  
  
## <a name="see-also"></a>请参阅

- [Visual Basic 命令行编译器](index.md)
- [Ildasm.exe（IL 反汇编程序）](../../../framework/tools/ildasm-exe-il-disassembler.md)
- [示例编译命令行](sample-compilation-command-lines.md)
