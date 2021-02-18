---
title: 中断性变更：Blazor：RequestImageFileAsync 方法中的参数名称已更改
description: 了解 ASP.NET Core 6.0 中的中断性变更，其标题为：Blazor：RequestImageFileAsync 方法中的参数名称已更改
author: scottaddie
ms.author: scaddie
ms.date: 02/09/2021
ms.openlocfilehash: bfaaa6bfe94c32fbc1a5b5b70db863d105d389b5
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488199"
---
# <a name="blazor-parameter-name-changed-in-requestimagefileasync-method"></a>Blazor：RequestImageFileAsync 方法中的参数名称已更改

`RequestImageFileAsync` 方法的 `maxWith` 参数已从 `maxWith` 重命名为 `maxWidth`。

## <a name="version-introduced"></a>引入的版本

6.0 预览版 1

## <a name="old-behavior"></a>旧行为

参数名称的拼写为 `maxWith`。

## <a name="new-behavior"></a>新行为

参数名称的拼写为 `maxWidth`。

## <a name="reason-for-change"></a>更改原因

原始参数名称存在录入错误。

## <a name="recommended-action"></a>建议的操作

如果使用的是 `RequestImageFile` API 中的命名参数，请将 `maxWith` 参数名称更新为 `maxWidth`。 否则，不需要进行任何更改。

## <a name="affected-apis"></a>受影响的 API

<xref:Microsoft.AspNetCore.Components.Forms.BrowserFileExtensions.RequestImageFileAsync%2A?displayProperty=nameWithType>

<!--

## Category

ASP.NET Core

## Affected APIs

`Overload:Microsoft.AspNetCore.Components.Forms.BrowserFileExtensions.RequestImageFileAsync`

-->
