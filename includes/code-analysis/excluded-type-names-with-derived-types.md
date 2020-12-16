---
ms.openlocfilehash: 4125df1d64fe7f3f2eb1eb4a821ed46c8270c95f
ms.sourcegitcommit: d0990c1c1ab2f81908360f47eafa8db9aa165137
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "97531897"
---
### <a name="exclude-specific-types-and-their-derived-types"></a><span data-ttu-id="964cf-101">排除特定类型及其派生类型</span><span class="sxs-lookup"><span data-stu-id="964cf-101">Exclude specific types and their derived types</span></span>

<span data-ttu-id="964cf-102">可以从分析中排除特定类型及其派生类型。</span><span class="sxs-lookup"><span data-stu-id="964cf-102">You can exclude specific types and their derived types from analysis.</span></span> <span data-ttu-id="964cf-103">例如，若要指定规则不应在名为的类型中的任何方法 `MyType` 及其派生类型上运行，请将以下键-值对添加到项目中的 *editorconfig* 文件中：</span><span class="sxs-lookup"><span data-stu-id="964cf-103">For example, to specify that the rule should not run on any methods within types named `MyType` and their derived types, add the following key-value pair to an *.editorconfig* file in your project:</span></span>

```ini
dotnet_code_quality.CAXXXX.excluded_type_names_with_derived_types = MyType
```

<span data-ttu-id="964cf-104">选项值中允许的符号名称格式 (用 `|`) 分隔：</span><span class="sxs-lookup"><span data-stu-id="964cf-104">Allowed symbol name formats in the option value (separated by `|`):</span></span>

- <span data-ttu-id="964cf-105">仅限类型名称 (包含名称的所有类型，而不管包含类型或命名空间) 。</span><span class="sxs-lookup"><span data-stu-id="964cf-105">Type name only (includes all types with the name, regardless of the containing type or namespace).</span></span>
- <span data-ttu-id="964cf-106">符号 [文档 ID 格式](../../docs/csharp/programming-guide/xmldoc/processing-the-xml-file.md#id-strings)的完全限定名称，带有可选 `T:` 前缀。</span><span class="sxs-lookup"><span data-stu-id="964cf-106">Fully qualified names in the symbol's [documentation ID format](../../docs/csharp/programming-guide/xmldoc/processing-the-xml-file.md#id-strings), with an optional `T:` prefix.</span></span>

<span data-ttu-id="964cf-107">示例:</span><span class="sxs-lookup"><span data-stu-id="964cf-107">Examples:</span></span>

| <span data-ttu-id="964cf-108">选项值</span><span class="sxs-lookup"><span data-stu-id="964cf-108">Option Value</span></span> | <span data-ttu-id="964cf-109">总结</span><span class="sxs-lookup"><span data-stu-id="964cf-109">Summary</span></span> |
| --- | --- |
|`dotnet_code_quality.CAXXXX.excluded_type_names_with_derived_types = MyType` | <span data-ttu-id="964cf-110">匹配名为的所有类型 `MyType` 及其所有派生类型。</span><span class="sxs-lookup"><span data-stu-id="964cf-110">Matches all types named `MyType` and all of their derived types.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_type_names_with_derived_types = MyType1|MyType2` | <span data-ttu-id="964cf-111">匹配名为或及其 `MyType1` `MyType2` 所有派生类型的所有类型。</span><span class="sxs-lookup"><span data-stu-id="964cf-111">Matches all types named either `MyType1` or `MyType2` and all of their derived types.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_type_names_with_derived_types = M:NS.MyType` | <span data-ttu-id="964cf-112">匹配 `MyType` 具有给定完全限定名称及其所有派生类型的特定类型。</span><span class="sxs-lookup"><span data-stu-id="964cf-112">Matches specific type `MyType` with given fully qualified name and all of its derived types.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_type_names_with_derived_types = M:NS1.MyType1|M:NS2.MyType2` | <span data-ttu-id="964cf-113">匹配特定的类型， `MyType1` 以及 `MyType2` 相应的完全限定名称及其所有派生类型。</span><span class="sxs-lookup"><span data-stu-id="964cf-113">Matches specific types `MyType1` and `MyType2` with the respective fully qualified names, and all of their derived types.</span></span> |
