---
ms.openlocfilehash: 53840ddd59ae3463bae2930fd0151ab2cd2d65cb
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97593315"
---
### <a name="design-time-builds-only-return-top-level-package-references"></a>设计时生成仅返回最上层包引用

从 .NET Core SDK 3.1.400 开始，`RunResolvePackageDependencies` 目标仅返回最上层包引用。

#### <a name="version-introduced"></a>引入的版本

.NET Core SDK 3.1.400

#### <a name="change-description"></a>更改描述

在早期版本的 .NET Core SDK 中，`RunResolvePackageDependencies` 目标创建了以下 MSBuild 项，其中包含 NuGet 资产文件中的信息：

- `PackageDefinitions`
- `PackageDependencies`
- `TargetDefinitions`
- `FileDefinitions`
- `FileDependencies`

Visual Studio 使用这些数据来填充解决方案资源管理器中的依赖项节点。 但这些数据可能很大，除非对依赖项节点进行了扩展，否则不需要这些数据。

从 .NET Core SDK 3.1.400 版开始，默认不会生成这些项中的大多数。 仅返回 `Package` 类型的项。 如果 Visual Studio 需要这些项来填充依赖项节点，它会直接从资产文件中读取信息。

#### <a name="reason-for-change"></a>更改原因

引入此更改是为了改进 Visual Studio 内的解决方案加载性能。 之前系统会加载所有的包引用，包括加载多数用户永远不会查看的许多引用。

#### <a name="recommended-action"></a>建议的操作

如果你有依赖于所创建项的 MSBuild 逻辑，请在项目文件中将 `EmitLegacyAssetsFileItems` 属性设置为 `true`。 此设置会启用以前的行为（这种行为将创建所有项）。

#### <a name="category"></a>类别

MSBuild

#### <a name="affected-apis"></a>受影响的 API

不可用
