---
title: 代码样式命名规则
description: 了解用于命名代码元素的 .NET 代码样式规则。
ms.date: 09/25/2020
ms.topic: reference
author: gewarren
ms.author: gewarren
dev_langs:
- CSharp
- VB
f1_keywords:
- IDE1006
- naming rules
helpviewer_keywords:
- IDE1006
- naming code style rules [EditorConfig]
- naming rules
- EditorConfig naming conventions
ms.openlocfilehash: 0eea5e89ac5055a45d9ead14363cc2f2fc574401
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98191074"
---
# <a name="naming-rules"></a><span data-ttu-id="fe076-103">命名规则</span><span class="sxs-lookup"><span data-stu-id="fe076-103">Naming rules</span></span>

<span data-ttu-id="fe076-104">命名规则涉及 .NET 编程语言代码元素的命名，如类、属性和方法。</span><span class="sxs-lookup"><span data-stu-id="fe076-104">Naming rules concern the naming of .NET programming language code elements, such as classes, properties, and methods.</span></span> <span data-ttu-id="fe076-105">例如，可以指定公共成员必须采用大写形式，或者私有字段必须以 `_` 开头。</span><span class="sxs-lookup"><span data-stu-id="fe076-105">For example, you can specify that public members must be capitalized or that private fields must begin with `_`.</span></span>

<span data-ttu-id="fe076-106">命名规则有三个部分：</span><span class="sxs-lookup"><span data-stu-id="fe076-106">A naming rule has three parts:</span></span>

* <span data-ttu-id="fe076-107">它应用于的符号组。</span><span class="sxs-lookup"><span data-stu-id="fe076-107">The group of symbols it applies to.</span></span>
* <span data-ttu-id="fe076-108">要与规则关联的命名样式。</span><span class="sxs-lookup"><span data-stu-id="fe076-108">The naming style to associate with the rule.</span></span>
* <span data-ttu-id="fe076-109">强制实施约定的严重性。</span><span class="sxs-lookup"><span data-stu-id="fe076-109">The severity for enforcing the convention.</span></span>

<span data-ttu-id="fe076-110">在 EditorConfig 文件中定义命名规则。</span><span class="sxs-lookup"><span data-stu-id="fe076-110">You define naming rules in an EditorConfig file.</span></span>

## <a name="general-syntax"></a><span data-ttu-id="fe076-111">常规语法</span><span class="sxs-lookup"><span data-stu-id="fe076-111">General syntax</span></span>

<span data-ttu-id="fe076-112">若要定义命名规则、符号组或命名样式，请使用以下语法设置一个或多个属性：</span><span class="sxs-lookup"><span data-stu-id="fe076-112">To define a naming rule, symbol group, or naming style, set one or more properties using the following syntax:</span></span>

```ini
<prefix>.<title>.<propertyName> = <propertyValue>
```

<span data-ttu-id="fe076-113">每个属性只能设置一次，但某些设置允许以逗号分隔的多个值。</span><span class="sxs-lookup"><span data-stu-id="fe076-113">Each property should only be set once, but some settings allow multiple, comma-separated values.</span></span>

<span data-ttu-id="fe076-114">属性的顺序并不重要。</span><span class="sxs-lookup"><span data-stu-id="fe076-114">The order of the properties is not important.</span></span>

### \<prefix>

<span data-ttu-id="fe076-115">**\<prefix>** 指定正在定义的元素类型（ &mdash; 命名规则、符号组或命名样式）， &mdash; 必须为下列类型之一：</span><span class="sxs-lookup"><span data-stu-id="fe076-115">**\<prefix>** specifies which kind of element is being defined&mdash;naming rule, symbol group, or naming style&mdash;and must be one of the following:</span></span>

| <span data-ttu-id="fe076-116">设置属性</span><span class="sxs-lookup"><span data-stu-id="fe076-116">To set a property for</span></span> | <span data-ttu-id="fe076-117">使用前缀</span><span class="sxs-lookup"><span data-stu-id="fe076-117">Use the prefix</span></span> | <span data-ttu-id="fe076-118">示例</span><span class="sxs-lookup"><span data-stu-id="fe076-118">Example</span></span> |
| --- | --- | -- |
| <span data-ttu-id="fe076-119">命名规则</span><span class="sxs-lookup"><span data-stu-id="fe076-119">Naming rule</span></span> | `dotnet_naming_rule` | `dotnet_naming_rule.types_should_be_pascal_case.severity = suggestion` |
| <span data-ttu-id="fe076-120">符号组</span><span class="sxs-lookup"><span data-stu-id="fe076-120">Symbol group</span></span> | `dotnet_naming_symbols` | `dotnet_naming_symbols.interface.applicable_kinds = interface` |
| <span data-ttu-id="fe076-121">命名样式</span><span class="sxs-lookup"><span data-stu-id="fe076-121">Naming style</span></span> | `dotnet_naming_style` | `dotnet_naming_style.pascal_case.capitalization = pascal_case` |

<span data-ttu-id="fe076-122">每种类型的定义 &mdash; [命名规则](#naming-rule-properties)、[符号组](#symbol-group-properties)或[命名样式](#naming-style-properties) &mdash; 都具有其自己支持的属性，如以下各节所述。</span><span class="sxs-lookup"><span data-stu-id="fe076-122">Each type of definition&mdash;[naming rule](#naming-rule-properties), [symbol group](#symbol-group-properties), or [naming style](#naming-style-properties)&mdash;has its own supported properties, as described in the following sections.</span></span>

### \<title>

<span data-ttu-id="fe076-123">**\<title>** 您选择的描述性名称，它将多个属性设置关联到单个定义。</span><span class="sxs-lookup"><span data-stu-id="fe076-123">**\<title>** is a descriptive name you choose that associates multiple property settings into a single definition.</span></span> <span data-ttu-id="fe076-124">例如，以下属性将生成两个符号组定义， `interface` `types` 其中每个定义都设置了两个属性。</span><span class="sxs-lookup"><span data-stu-id="fe076-124">For example, the following properties produce two symbol group definitions, `interface` and `types`, each of which has two properties set on it.</span></span>

```ini
dotnet_naming_symbols.interface.applicable_kinds = interface
dotnet_naming_symbols.interface.applicable_accessibilities = public, internal, private, protected, protected_internal, private_protected

dotnet_naming_symbols.types.applicable_kinds = class, struct, interface, enum, delegate
dotnet_naming_symbols.types.applicable_accessibilities = public, internal, private, protected, protected_internal, private_protected
```

## <a name="naming-rule-properties"></a><span data-ttu-id="fe076-125">命名规则属性</span><span class="sxs-lookup"><span data-stu-id="fe076-125">Naming rule properties</span></span>

<span data-ttu-id="fe076-126">所有命名规则属性都是规则生效的必需属性。</span><span class="sxs-lookup"><span data-stu-id="fe076-126">All naming rule properties are required for a rule to take effect.</span></span>

| <span data-ttu-id="fe076-127">properties</span><span class="sxs-lookup"><span data-stu-id="fe076-127">Property</span></span> | <span data-ttu-id="fe076-128">说明</span><span class="sxs-lookup"><span data-stu-id="fe076-128">Description</span></span> |
| -- | -- |
| `symbols` | <span data-ttu-id="fe076-129">符号组的标题，定义应应用此规则的符号</span><span class="sxs-lookup"><span data-stu-id="fe076-129">The title of the symbol group, defining the symbols to which this rule should be applied</span></span> |
| `style` | <span data-ttu-id="fe076-130">应与此规则关联的命名样式的标题</span><span class="sxs-lookup"><span data-stu-id="fe076-130">The title of the naming style which should be associated with this rule</span></span> |
| `severity` |  <span data-ttu-id="fe076-131">设置用于强制执行命名规则的严重性。</span><span class="sxs-lookup"><span data-stu-id="fe076-131">Sets the severity with which to enforce the naming rule.</span></span> <span data-ttu-id="fe076-132">将关联的值设置为一个可用的 [严重性级别](../configuration-options.md#severity-level)。<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="fe076-132">Set the associated value to one of the available [severity levels](../configuration-options.md#severity-level).<sup>1</sup></span></span> |

<span data-ttu-id="fe076-133">**注意：**</span><span class="sxs-lookup"><span data-stu-id="fe076-133">**Notes:**</span></span>

1. <span data-ttu-id="fe076-134">命名规则内的严重性规范仅适用于开发 Ide （如 Visual Studio）。</span><span class="sxs-lookup"><span data-stu-id="fe076-134">Severity specification within a naming rule is only respected inside development IDEs, such as Visual Studio.</span></span> <span data-ttu-id="fe076-135">C # 或 VB 编译器不理解此设置，因此在生成过程中不会考虑此设置。</span><span class="sxs-lookup"><span data-stu-id="fe076-135">This setting is not understood by the C# or VB compilers, hence not respected during build.</span></span> <span data-ttu-id="fe076-136">相反，若要在生成时强制命名样式规则，应使用 [本部分](#rule-id-ide1006-naming-rule-violation)中所述的基于规则 ID 的严重性配置来设置严重性。</span><span class="sxs-lookup"><span data-stu-id="fe076-136">Instead, to enforce naming style rules on build, you should set the severity by using the rule ID-based severity configuration as explained in [this section](#rule-id-ide1006-naming-rule-violation).</span></span> <span data-ttu-id="fe076-137">有关详细信息，请参阅此 [GitHub 问题](https://github.com/dotnet/roslyn/issues/44201)。</span><span class="sxs-lookup"><span data-stu-id="fe076-137">For more information, see this [GitHub issue](https://github.com/dotnet/roslyn/issues/44201).</span></span>

## <a name="rule-order"></a><span data-ttu-id="fe076-138">规则顺序</span><span class="sxs-lookup"><span data-stu-id="fe076-138">Rule order</span></span>

<span data-ttu-id="fe076-139">命名规则在 EditorConfig 文件中的定义顺序并不重要。</span><span class="sxs-lookup"><span data-stu-id="fe076-139">The order in which naming rules are defined in an EditorConfig file doesn't matter.</span></span> <span data-ttu-id="fe076-140">命名规则根据规则本身的定义自动排序。</span><span class="sxs-lookup"><span data-stu-id="fe076-140">The naming rules are automatically ordered according to the definition of the rules themselves.</span></span> <span data-ttu-id="fe076-141">[EditorConfig 语言服务扩展](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.EditorConfig)可以分析 EditorConfig 文件，如果文件中的规则顺序与编译器在运行时使用的规则不同，该扩展还会进行报告。</span><span class="sxs-lookup"><span data-stu-id="fe076-141">The [EditorConfig Language Service extension](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.EditorConfig) can analyze an EditorConfig file and report cases where the rule ordering in the file is different to what the compiler will use at run time.</span></span>

> [!NOTE]
>
> <span data-ttu-id="fe076-142">如果使用早于 Visual Studio 2019 版本16.2 的 Visual Studio 版本，则应在 EditorConfig 文件中按从最特定到最小的顺序对命名规则进行排序。</span><span class="sxs-lookup"><span data-stu-id="fe076-142">If you're using a version of Visual Studio earlier than Visual Studio 2019 version 16.2, naming rules should be ordered from most-specific to least-specific in the EditorConfig file.</span></span> <span data-ttu-id="fe076-143">遇到的第一个可应用规则是唯一应用的规则。</span><span class="sxs-lookup"><span data-stu-id="fe076-143">The first rule encountered that can be applied is the only rule that is applied.</span></span> <span data-ttu-id="fe076-144">但是，如果有多个具有相同名称的规则属性  ，则最近找到的具有该名称的属性具有优先权。</span><span class="sxs-lookup"><span data-stu-id="fe076-144">However, if there are multiple rule *properties* with the same name, the most recently found property with that name takes precedence.</span></span> <span data-ttu-id="fe076-145">有关详细信息，请参阅[文件层次结构和优先级](/visualstudio/ide/create-portable-custom-editor-options#file-hierarchy-and-precedence)。</span><span class="sxs-lookup"><span data-stu-id="fe076-145">For more information, see [File hierarchy and precedence](/visualstudio/ide/create-portable-custom-editor-options#file-hierarchy-and-precedence).</span></span>

## <a name="symbol-group-properties"></a><span data-ttu-id="fe076-146">符号组属性</span><span class="sxs-lookup"><span data-stu-id="fe076-146">Symbol group properties</span></span>

<span data-ttu-id="fe076-147">可以为符号组设置以下属性，以限制组中包含的符号。</span><span class="sxs-lookup"><span data-stu-id="fe076-147">You can set the following properties for symbol groups, to limit which symbols are included in the group.</span></span> <span data-ttu-id="fe076-148">若要在单个属性设置中指定多个值，请用逗号分隔它们。</span><span class="sxs-lookup"><span data-stu-id="fe076-148">To specify multiple values in a single property setting, separate them with a comma.</span></span>

| <span data-ttu-id="fe076-149">properties</span><span class="sxs-lookup"><span data-stu-id="fe076-149">Property</span></span> | <span data-ttu-id="fe076-150">说明</span><span class="sxs-lookup"><span data-stu-id="fe076-150">Description</span></span> | <span data-ttu-id="fe076-151">允许的值</span><span class="sxs-lookup"><span data-stu-id="fe076-151">Allowed values</span></span> | <span data-ttu-id="fe076-152">必须</span><span class="sxs-lookup"><span data-stu-id="fe076-152">Required</span></span> |
| -- | -- | -- | -- |
| `applicable_kinds` | <span data-ttu-id="fe076-153">组<sup>1</sup>中的符号类型</span><span class="sxs-lookup"><span data-stu-id="fe076-153">Kinds of symbols in the group <sup>1</sup></span></span> | <span data-ttu-id="fe076-154">`*`（使用此值可指定所有符号）</span><span class="sxs-lookup"><span data-stu-id="fe076-154">`*` (use this value to specify all symbols)</span></span><br/>`namespace`<br/>`class`<br/>`struct`<br/>`interface`<br/>`enum`<br/>`property`<br/>`method`<br/>`field`<br/>`event`<br/>`delegate`<br/>`parameter`<br/>`type_parameter`<br/>`local`<br/>`local_function` | <span data-ttu-id="fe076-155">是</span><span class="sxs-lookup"><span data-stu-id="fe076-155">Yes</span></span> |
| `applicable_accessibilities` | <span data-ttu-id="fe076-156">组中符号的可访问性级别</span><span class="sxs-lookup"><span data-stu-id="fe076-156">Accessibility levels of the symbols in the group</span></span> | <span data-ttu-id="fe076-157">`*`（使用此值可指定所有可访问性级别）</span><span class="sxs-lookup"><span data-stu-id="fe076-157">`*` (use this value to specify all accessibility levels)</span></span><br/>`public`<br/><span data-ttu-id="fe076-158">`internal` 或 `friend`</span><span class="sxs-lookup"><span data-stu-id="fe076-158">`internal` or `friend`</span></span><br/>`private`<br/>`protected`<br/><span data-ttu-id="fe076-159">`protected_internal` 或 `protected_friend`</span><span class="sxs-lookup"><span data-stu-id="fe076-159">`protected_internal` or `protected_friend`</span></span><br/>`private_protected`<br/><span data-ttu-id="fe076-160">`local` 方法中定义的符号 () </span><span class="sxs-lookup"><span data-stu-id="fe076-160">`local` (for symbols defined within a method)</span></span> | <span data-ttu-id="fe076-161">是</span><span class="sxs-lookup"><span data-stu-id="fe076-161">Yes</span></span> |
| `required_modifiers` | <span data-ttu-id="fe076-162">仅匹配具有 _所有_ 指定修饰符 <sup>2</sup>的符号</span><span class="sxs-lookup"><span data-stu-id="fe076-162">Only match symbols with _all_ the specified modifiers <sup>2</sup></span></span> | <span data-ttu-id="fe076-163">`abstract` 或 `must_inherit`</span><span class="sxs-lookup"><span data-stu-id="fe076-163">`abstract` or `must_inherit`</span></span><br/>`async`<br/>`const`<br/>`readonly`<br/><span data-ttu-id="fe076-164">`static` 或 `shared` <sup>3</sup></span><span class="sxs-lookup"><span data-stu-id="fe076-164">`static` or `shared` <sup>3</sup></span></span> | <span data-ttu-id="fe076-165">否</span><span class="sxs-lookup"><span data-stu-id="fe076-165">No</span></span> |

<span data-ttu-id="fe076-166">**注意：**</span><span class="sxs-lookup"><span data-stu-id="fe076-166">**Notes:**</span></span>

1. <span data-ttu-id="fe076-167">当前不支持元组成员 `applicable_kinds` 。</span><span class="sxs-lookup"><span data-stu-id="fe076-167">Tuple members aren't currently supported in `applicable_kinds`.</span></span>
2. <span data-ttu-id="fe076-168">符号组与属性中的 _所有_ 修饰符匹配 `required_modifiers` 。</span><span class="sxs-lookup"><span data-stu-id="fe076-168">The symbol group matches _all_ the modifiers in the `required_modifiers` property.</span></span>  <span data-ttu-id="fe076-169">如果省略此属性，则匹配不需要任何特定的修饰符。</span><span class="sxs-lookup"><span data-stu-id="fe076-169">If you omit this property, no specific modifiers are required for a match.</span></span> <span data-ttu-id="fe076-170">这意味着符号的修饰符不会影响是否应用此规则。</span><span class="sxs-lookup"><span data-stu-id="fe076-170">This means a symbol's modifiers have no effect on whether or not this rule is applied.</span></span>
3. <span data-ttu-id="fe076-171">如果组具有 `static` 或 `shared` 属性中的 `required_modifiers` ，则组还将包含 `const` 符号，因为它们是隐式的 `static` / `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="fe076-171">If your group has `static` or `shared` in the `required_modifiers` property, the group will also include `const` symbols because they are implicitly `static`/`Shared`.</span></span> <span data-ttu-id="fe076-172">但是，如果不希望 `static` 将命名规则应用于 `const` 符号，则可以使用符号组创建新的命名规则 `const` 。</span><span class="sxs-lookup"><span data-stu-id="fe076-172">However, if you don't want the `static` naming rule to apply to `const` symbols, you can create a new naming rule with a symbol group of `const`.</span></span>

## <a name="naming-style-properties"></a><span data-ttu-id="fe076-173">命名样式属性</span><span class="sxs-lookup"><span data-stu-id="fe076-173">Naming style properties</span></span>

<span data-ttu-id="fe076-174">命名样式定义要通过规则强制执行的约定。</span><span class="sxs-lookup"><span data-stu-id="fe076-174">A naming style defines the conventions you want to enforce with the rule.</span></span> <span data-ttu-id="fe076-175">例如：</span><span class="sxs-lookup"><span data-stu-id="fe076-175">For example:</span></span>

* <span data-ttu-id="fe076-176">大写 `PascalCase`</span><span class="sxs-lookup"><span data-stu-id="fe076-176">Capitalize with `PascalCase`</span></span>
* <span data-ttu-id="fe076-177">开头为 `m_`</span><span class="sxs-lookup"><span data-stu-id="fe076-177">Starts with `m_`</span></span>
* <span data-ttu-id="fe076-178">结尾为 `_g`</span><span class="sxs-lookup"><span data-stu-id="fe076-178">Ends with `_g`</span></span>
* <span data-ttu-id="fe076-179">用词分隔 `__`</span><span class="sxs-lookup"><span data-stu-id="fe076-179">Separate words with `__`</span></span>

<span data-ttu-id="fe076-180">您可以为命名样式设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="fe076-180">You can set the following properties for a naming style:</span></span>

| <span data-ttu-id="fe076-181">properties</span><span class="sxs-lookup"><span data-stu-id="fe076-181">Property</span></span> | <span data-ttu-id="fe076-182">说明</span><span class="sxs-lookup"><span data-stu-id="fe076-182">Description</span></span> | <span data-ttu-id="fe076-183">允许的值</span><span class="sxs-lookup"><span data-stu-id="fe076-183">Allowed values</span></span> | <span data-ttu-id="fe076-184">必须</span><span class="sxs-lookup"><span data-stu-id="fe076-184">Required</span></span> |
| -- | -- | -- | -- |
| `capitalization` | <span data-ttu-id="fe076-185">符号内的单词的大小写样式</span><span class="sxs-lookup"><span data-stu-id="fe076-185">Capitalization style for words within the symbol</span></span> | `pascal_case`<br/>`camel_case`<br/>`first_word_upper`<br/>`all_upper`<br/>`all_lower` | <span data-ttu-id="fe076-186">是<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="fe076-186">Yes<sup>1</sup></span></span> |
| `required_prefix` | <span data-ttu-id="fe076-187">必须以这些字符开头</span><span class="sxs-lookup"><span data-stu-id="fe076-187">Must begin with these characters</span></span> | | <span data-ttu-id="fe076-188">否</span><span class="sxs-lookup"><span data-stu-id="fe076-188">No</span></span> |
| `required_suffix` | <span data-ttu-id="fe076-189">必须以这些字符结尾</span><span class="sxs-lookup"><span data-stu-id="fe076-189">Must end with these characters</span></span> | | <span data-ttu-id="fe076-190">否</span><span class="sxs-lookup"><span data-stu-id="fe076-190">No</span></span> |
| `word_separator` | <span data-ttu-id="fe076-191">符号内的单词需要用此字符分隔</span><span class="sxs-lookup"><span data-stu-id="fe076-191">Words within the symbol need to be separated with this character</span></span> | | <span data-ttu-id="fe076-192">否</span><span class="sxs-lookup"><span data-stu-id="fe076-192">No</span></span> |

<span data-ttu-id="fe076-193">**注意：**</span><span class="sxs-lookup"><span data-stu-id="fe076-193">**Notes:**</span></span>

1. <span data-ttu-id="fe076-194">必须在命名样式中指定大写样式，否则会忽略命名样式。</span><span class="sxs-lookup"><span data-stu-id="fe076-194">You must specify a capitalization style as part of your naming style, otherwise your naming style might be ignored.</span></span>

## <a name="default-naming-styles"></a><span data-ttu-id="fe076-195">默认命名样式</span><span class="sxs-lookup"><span data-stu-id="fe076-195">Default naming styles</span></span>

<span data-ttu-id="fe076-196">如果未指定任何自定义命名规则，则使用以下默认样式：</span><span class="sxs-lookup"><span data-stu-id="fe076-196">If you don't specify any custom naming rules, the following default styles are used:</span></span>

- <span data-ttu-id="fe076-197">对于可访问性为 `public`、`private`、`internal`、`protected` 或 `protected_internal` 的类、结构、枚举、属性以及事件，默认的命名样式为帕斯卡拼写法。</span><span class="sxs-lookup"><span data-stu-id="fe076-197">For classes, structs, enumerations, properties, and events with `public`, `private`, `internal`, `protected`, or `protected_internal` accessibility, the default naming style is Pascal case.</span></span>

- <span data-ttu-id="fe076-198">对于可访问性为 `public`、`private`、`internal`、`protected` 或 `protected_internal` 的接口，默认的命名样式为帕斯卡拼写法并必须附加 l 前缀。 </span><span class="sxs-lookup"><span data-stu-id="fe076-198">For interfaces with `public`, `private`, `internal`, `protected`, or `protected_internal` accessibility, the default naming style is Pascal case with a required prefix of **I**.</span></span>

## <a name="example"></a><span data-ttu-id="fe076-199">示例</span><span class="sxs-lookup"><span data-stu-id="fe076-199">Example</span></span>

<span data-ttu-id="fe076-200">以下 .editorconfig 文件包含命名约定，该约定指定公共属性、方法、字段、事件和委托必须采用大写形式  。</span><span class="sxs-lookup"><span data-stu-id="fe076-200">The following *.editorconfig* file contains a naming convention that specifies that public properties, methods, fields, events, and delegates must be capitalized.</span></span> <span data-ttu-id="fe076-201">请注意，此命名约定指定了多种应用规则的符号，以逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="fe076-201">Notice that this naming convention specifies multiple kinds of symbol to apply the rule to, using a comma to separate the values.</span></span>

```ini
[*.{cs,vb}]

# Defining the 'public_symbols' symbol group
dotnet_naming_symbols.public_symbols.applicable_kinds           = property,method,field,event,delegate
dotnet_naming_symbols.public_symbols.applicable_accessibilities = public
dotnet_naming_symbols.public_symbols.required_modifiers         = readonly

# Defining the `first_word_upper_case_style` naming style
dotnet_naming_style.first_word_upper_case_style.capitalization = first_word_upper

# Defining the `public_members_must_be_capitalized` naming rule, by setting the symbol group to the 'public symbols' symbol group,
dotnet_naming_rule.public_members_must_be_capitalized.symbols   = public_symbols
# setting the naming style to the `first_word_upper_case_style` naming style,
dotnet_naming_rule.public_members_must_be_capitalized.style    = first_word_upper_case_style
# and setting the severity.
dotnet_naming_rule.public_members_must_be_capitalized.severity = suggestion
```

## <a name="rule-id-ide1006-naming-rule-violation"></a><a name="rule-id-ide1006-naming-rule-violation"></a><span data-ttu-id="fe076-202">规则 ID： "IDE1006" (命名规则冲突) </span><span class="sxs-lookup"><span data-stu-id="fe076-202">Rule ID: "IDE1006" (Naming rule violation)</span></span>

<span data-ttu-id="fe076-203">所有命名选项都有规则 ID `IDE1006` 和标题 `Naming rule violation` 。</span><span class="sxs-lookup"><span data-stu-id="fe076-203">All naming options have rule ID `IDE1006` and title `Naming rule violation`.</span></span> <span data-ttu-id="fe076-204">你可以使用以下语法在 EditorConfig 文件中全局配置命名冲突的严重性：</span><span class="sxs-lookup"><span data-stu-id="fe076-204">You can configure the severity of naming violations globally in an EditorConfig file with the following syntax:</span></span>

```ini
dotnet_diagnostic.IDE1006.severity = <severity value>
```

<span data-ttu-id="fe076-205">严重性值必须是 `warning` 或 `error` 才能 [在生成时强制执行](../overview.md#code-style-analysis)。</span><span class="sxs-lookup"><span data-stu-id="fe076-205">The severity value must be `warning` or `error` to be [enforced on build](../overview.md#code-style-analysis).</span></span> <span data-ttu-id="fe076-206">对于所有可能的严重性值，请参阅 [严重性级别](../configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="fe076-206">For all possible severity values, see [severity level](../configuration-options.md#severity-level).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe076-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe076-207">See also</span></span>

- [<span data-ttu-id="fe076-208">语言规则</span><span class="sxs-lookup"><span data-stu-id="fe076-208">Language rules</span></span>](language-rules.md)
- [<span data-ttu-id="fe076-209">格式设置规则</span><span class="sxs-lookup"><span data-stu-id="fe076-209">Formatting rules</span></span>](formatting-rules.md)
- [<span data-ttu-id="fe076-210">Roslyn 命名规则</span><span class="sxs-lookup"><span data-stu-id="fe076-210">Roslyn naming rules</span></span>](https://github.com/dotnet/roslyn/blob/master/.editorconfig#L63)
- [<span data-ttu-id="fe076-211">.NET 代码样式规则参考</span><span class="sxs-lookup"><span data-stu-id="fe076-211">.NET code style rules reference</span></span>](index.md)
