---
description: 了解有关以下内容的详细信息： BC40029： " <classname> " 不符合 cls，因为它所实现的接口 " <interfacename> " 不符合 cls
title: “<classname>”不符合 CLS，因为它所实现的接口“<interfacename>”不符合 CLS
ms.date: 07/20/2015
f1_keywords:
- bc40029
- vbc40029
helpviewer_keywords:
- BC40029
ms.assetid: 178452f3-5575-4da0-9d6c-53bcddb6a338
ms.openlocfilehash: 28264dd602bd20a6b33bebd965982ca12d402d01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796764"
---
# <a name="bc40029-classname-is-not-cls-compliant-because-the-interface-interfacename-it-implements-is-not-cls-compliant"></a>BC40029： " \<classname> " 不符合 cls，因为它所实现的接口 " \<interfacename> " 不符合 cls

当某一类或接口派生自或实现标记为 `<CLSCompliant(True)>` 的类型时，该类或接口将被标记为 `<CLSCompliant(False)>` 。

 为了使某个类或接口符合 [语言独立性并 Language-Independent 组件](../../../standard/language-independence-and-language-independent-components.md) (CLS) ，其整个继承层次结构必须是兼容的。 这意味着从它继承的每一个类型，不管是直接还是间接继承，都必须符合。 同样，如果一个类实现一个或多个接口，则其整个继承层次结构都必须符合。

 当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。 此参数没有默认值，必须为其提供一个值。

 如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。

 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。

 **错误 ID：** BC40029

## <a name="to-correct-this-error"></a>更正此错误

- 如果你需要 CLS 符合性，请在不同的继承层次结构或实现方案中定义此类型。

- 如果你要求此类型保留在其当前的继承层次结构或实现方案中，请从其定义中删除 <xref:System.CLSCompliantAttribute> ，或将其标记为 `<CLSCompliant(False)>`。
