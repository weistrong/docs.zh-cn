---
description: 了解有关详细信息，请参阅如何：使用 EdmGen.exe 生成 Object-Layer 代码
title: 如何：使用 EdmGen.exe 生成对象层代码
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: 1c1f614247f10c8819709b9494fb1ec04271b634
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697460"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a>如何：使用 EdmGen.exe 生成对象层代码

本主题演示如何使用 [EDM 生成器 ( # A0) ](edm-generator-edmgen-exe.md) 工具根据 csdl 文件生成对象层代码。  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a>使用 EdmGen.exe 为 Visual Basic 项目的 School 模型生成对象层代码  
  
1. 创建 School 数据库。 有关详细信息，请参阅 [创建 School 示例数据库](/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100))。  
  
2. 生成 School 模型或获取 School.csdl 文件。 有关详细信息，请参阅 [如何：使用 EdmGen.exe 生成模型和映射文件](how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)。  
  
3. 在命令提示符下执行以下命令（无换行符）：  
  
    ```console  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a>使用 EdmGen.exe 为 C# 项目的 School 模型生成对象层代码  
  
1. 创建 School 数据库。 有关详细信息，请参阅 [创建 School 示例数据库](/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100))。  
  
2. 生成 School 模型或获取 School.csdl 文件。 有关详细信息，请参阅 [如何：使用 EdmGen.exe 生成模型和映射文件](how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)。  
  
3. 在命令提示符下执行以下命令（无换行符）：  
  
    ```console  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a>请参阅

- [建模和映射](modeling-and-mapping.md)
- [如何：手动配置实体框架项目](/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))
- [ADO.NET 实体数据模型工具](/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))
- [如何：预生成视图以改进查询性能](/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))
- [如何：使用 EdmGen.exe 生成模型和映射文件](how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
