---
description: 了解更多相关信息：进行和提交数据更改
title: 进行和提交数据更改
ms.date: 03/30/2017
ms.assetid: d68c2dc3-99b3-49ab-b547-2ca5b386429a
ms.openlocfilehash: 260dab911057b45250d44ded7c254dd903e2aed7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695551"
---
# <a name="making-and-submitting-data-changes"></a>进行和提交数据更改

本节中的主题介绍如何做出更改并将更改传输至数据库，以及如何处理开放式并发冲突。

> [!NOTE]
> 您可以重写 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]、`Insert` 和 `Update` 数据库操作的 `Delete` 默认方法。 有关详细信息，请参阅 [自定义插入、更新和删除操作](customizing-insert-update-and-delete-operations.md)。
>
> 使用 Visual Studio 的开发人员可以使用对象关系设计器来开发用于实现相同目的的存储过程。

## <a name="in-this-section"></a>本节内容

[如何：在数据库中插入行](how-to-insert-rows-into-the-database.md) \
介绍如何通过向对象模型添加对象将行插入到数据库中。

[如何：更新数据库中的行](how-to-update-rows-in-the-database.md) \
介绍如何通过更新对象模型中的对象来更新数据库中的行。

[如何：从数据库中删除行](how-to-delete-rows-from-the-database.md) \
介绍如何通过删除对象模型中的对象来删除数据库中的行。

[如何：将更改提交到数据库](how-to-submit-changes-to-the-database.md) \
介绍如何将对象模型更改发送到数据库。

[如何：通过使用事务对数据提交进行方括号](how-to-bracket-data-submissions-by-using-transactions.md) \
介绍如何将操作包含在事务中。

[如何：动态创建数据库](how-to-dynamically-create-a-database.md) \
介绍如何动态生成数据库，以及此方法的一些典型方案。

[如何：管理更改冲突](how-to-manage-change-conflicts.md) \
介绍用于处理开放式并发问题的技术。
