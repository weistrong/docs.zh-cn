---
description: 详细了解：操作说明：在 Visual Basic 中保存用户设置
title: 如何：永久保存用户设置
ms.date: 07/20/2015
helpviewer_keywords:
- My.Settings object [Visual Basic], persisting user settings
- persistence [Visual Basic], persisting user settings [Visual Basic]
- user settings [Visual Basic], persisting
ms.assetid: 0e5e6415-b6e2-4602-9be0-a65fa167d007
ms.openlocfilehash: 43ca82442678356afacb8e05149a35d485603059
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797830"
---
# <a name="how-to-persist-user-settings-in-visual-basic"></a>如何：在 Visual Basic 中保存用户设置

可以使用 `My.Settings.Save` 方法来保存对用户设置的更改。  
  
 通常情况下，将应用程序设计为在应用程序关闭时保存用户设置的更改。 这是因为保存设置需要几秒钟，具体取决于多种因素。  
  
 有关详细信息，请参阅 [My.Settings 对象](../../../language-reference/objects/my-settings-object.md)。  
  
> [!NOTE]
> 虽然可以在运行时更改并保存用户范围设置的值，但是应用程序范围设置是只读的，不能以编程方式进行更改。 可以在创建应用程序时通过 **项目设计器**，或者编辑应用程序的配置文件来更改应用程序范围设置。 有关详细信息，请参阅[管理应用程序设置 (.NET)](/visualstudio/ide/managing-application-settings-dotnet)。  
  
## <a name="example"></a>示例  

 本示例更改 `LastChanged` 用户设置的值，并通过调用 `My.Settings.Save` 方法来保存此更改。  
  
 [!code-vb[VbVbalrMyResources#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyResources/VB/Form1.vb#5)]  
  
 若要使用本示例，应用程序必须具有类型为 `Date` 的 `LastChanged` 用户设置。 有关详细信息，请参阅[管理应用程序设置 (.NET)](/visualstudio/ide/managing-application-settings-dotnet)。  
  
## <a name="see-also"></a>另请参阅

- [My.Settings 对象](../../../language-reference/objects/my-settings-object.md)
- [如何：在 Visual Basic 中读取应用程序设置](how-to-read-application-settings.md)
- [如何：在 Visual Basic 中更改用户设置](how-to-change-user-settings.md)
- [如何：在 Visual Basic 中为用户设置创建属性网格](how-to-create-property-grids-for-user-settings.md)
- [管理应用程序设置 (.NET)](/visualstudio/ide/managing-application-settings-dotnet)
