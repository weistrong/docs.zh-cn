---
description: 了解详细信息： BC30202：应为 "Optional"
title: 需要“Optional”
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 543dbf6226d4d298d46764ee506b55e770c91604
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795542"
---
# <a name="bc30202-optional-expected"></a>BC30202：应为 "Optional"

过程声明中的可选参数后跟必需的参数。 可选参数后面的每个参数都必须是可选的。

 **错误 ID：** BC30202

## <a name="to-correct-this-error"></a>更正此错误

- 如果需要参数，请将其移动到自变量列表中的第一个可选参数之前。

- 如果参数旨在作为可选参数，请使用 `Optional` 关键字。

## <a name="see-also"></a>请参阅

- [可选参数](../../programming-guide/language-features/procedures/optional-parameters.md)
