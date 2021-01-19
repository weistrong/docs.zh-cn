---
title: NETSDK1059：项目包含已过时的 .NET CLI 工具
description: 如何解决项目包含已过时的 .NET CLI 工具的问题。
author: sfoslund
ms.topic: error-reference
ms.date: 10/09/2020
f1_keywords:
- NETSDK1059
ms.openlocfilehash: bba5f4dafa346d81274541f3c40ecc5ed6fff8ab
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98190320"
---
# <a name="netsdk1059-project-contains-obsolete-net-cli-tool"></a>NETSDK1059：项目包含已过时的 .NET CLI 工具

本文适用于：✔️ .NET Core 2.1.100 SDK 及更高版本

当 .NET SDK 发出警告 NETSDK1059 时，表示项目包含已过时的 .NET CLI 工具。 自 .NET Core 2.1 起，这些工具包含在 .NET SDK 中，无需由项目显式引用。 要详细了解如何迁移到 .NET Core 2.1，请参阅[此处](../../migration/20-21.md)。
