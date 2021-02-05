---
title: 选择 Visual Basic 语言版本
description: 将编译器配置为使用特定编译器版本执行语法验证。
ms.date: 05/24/2018
ms.openlocfilehash: 09503db726f9d993bc986860c57aa98652b696d1
ms.sourcegitcommit: 65af0f0ad316858882845391d60ef7e303b756e8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "99585450"
---
# <a name="select-the-visual-basic-language-version"></a>选择 Visual Basic 语言版本

Visual Basic 编译器默认为已发布语言的最新主版本。 你可以选择使用该语言的新单点版本编译任何项目。 选择语言的较新版本，让你的项目可以使用最新的语言功能。 在其他情况下，可能需要在使用较旧的语言版本时验证项目的编译内容是否整齐。

借助此功能，在开发环境中安装新版本的 SDK 和工具时，不必选择在项目中引入新的语言功能。 可以在生成计算机上安装最新的 SDK 和工具。 每个项目可以配置为对其生成使用该语言的特定版本。

有三种方法可设置语言版本：

- 手动编辑 [ **.vbproj** 文件](#edit-the-vbproj-file)
- [为子目录中的多个项目](#configure-multiple-projects)设置语言版本
- 配置[ `-langversion` 编译器选项](#set-the-langversion-compiler-option)

## <a name="edit-the-vbproj-file"></a>编辑 .vbproj 文件

您可以在 **.vbproj** 文件中设置语言版本。 添加以下元素：

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

该值 `latest` 使用 Visual Basic 语言的最新次要版本。 有效值是：

|值|含义|
|------------|-------------|
|default|编译器接受它可支持的最新主版本中的所有有效语言语法。|
|9|编译器仅接受 Visual Basic 9.0 或更低版本中所含的语法。|
|10|编译器仅接受 Visual Basic 10.0 或更低版本中所含的语法。|
|11|编译器仅接受 Visual Basic 11.0 或更低版本中所含的语法。|
|12|编译器仅接受 Visual Basic 12.0 或更低版本中所含的语法。|
|14|编译器仅接受 Visual Basic 14.0 或更低版本中所含的语法。|
|15|编译器仅接受 Visual Basic 15.0 或更低版本中所含的语法。|
|15.3|编译器仅接受 Visual Basic 15.3 或更低版本中所含的语法。|
|15.5|编译器仅接受 Visual Basic 15.5 或更低版本中所含的语法。|
|16|编译器仅接受 Visual Basic 16 或更低版本中包含的语法。|
|16.9|编译器仅接受 Visual Basic 16.9 或更低版本中所含的语法。|
|最新|编译器接受它可支持的所有有效语言语法。|

特殊字符串 `default` 和 `latest` 分别解析为生成计算机上安装的最新主要和次要语言版本。

## <a name="configure-multiple-projects"></a>配置多个项目

你可以创建一个 **属性** 文件，其中包含 `<LangVersion>` 用于配置多个目录的元素。 通常是在解决方案目录中完成这件事。 将以下内容添加到你的解决方案目录中的 **属性** 文件：

```xml
<Project>
 <PropertyGroup>
   <LangVersion>15.5</LangVersion>
 </PropertyGroup>
</Project>
```

现在，包含该文件的目录的每个子目录中的生成将使用 Visual Basic 版本15.5 语法。 有关详细信息，请参阅关于[自定义生成](/visualstudio/msbuild/customize-your-build)的文章。

## <a name="set-the-langversion-compiler-option"></a>选择 langversion 编译器选项

你可以使用 `-langversion` 命令行选项。 有关详细信息，请参阅关于 [/langversion](../reference/command-line-compiler/langversion.md) 编译器选项的文章。 您可以通过键入来查看有效值的列表  `vbc -langversion:?` 。
