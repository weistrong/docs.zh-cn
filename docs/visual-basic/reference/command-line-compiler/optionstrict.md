---
description: 详细了解：-optionstrict
title: -optionstrict
ms.date: 07/20/2015
f1_keywords:
- -optionstrict
helpviewer_keywords:
- -optionstrict compiler option [Visual Basic]
- optionstrict compiler option [Visual Basic]
- /optionstrict compiler option [Visual Basic]
ms.assetid: c7b10086-0fa4-49db-b3c8-4ae0db5957da
ms.openlocfilehash: ad58c7775eaa77c1bf693629cf12cc70e4222920
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475898"
---
# <a name="-optionstrict"></a><span data-ttu-id="11534-103">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="11534-103">-optionstrict</span></span>

<span data-ttu-id="11534-104">强制执行严格类型语义，限制隐式类型转换。</span><span class="sxs-lookup"><span data-stu-id="11534-104">Enforces strict type semantics to restrict implicit type conversions.</span></span>

## <a name="syntax"></a><span data-ttu-id="11534-105">语法</span><span class="sxs-lookup"><span data-stu-id="11534-105">Syntax</span></span>

```console
-optionstrict[+ | -]
-optionstrict[:custom]
```

## <a name="arguments"></a><span data-ttu-id="11534-106">自变量</span><span class="sxs-lookup"><span data-stu-id="11534-106">Arguments</span></span>

<span data-ttu-id="11534-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="11534-107">`+` &#124; `-`</span></span>  
<span data-ttu-id="11534-108">可选。</span><span class="sxs-lookup"><span data-stu-id="11534-108">Optional.</span></span> <span data-ttu-id="11534-109">`-optionstrict+` 选项限制隐式类型转换。</span><span class="sxs-lookup"><span data-stu-id="11534-109">The `-optionstrict+` option restricts implicit type conversion.</span></span> <span data-ttu-id="11534-110">此选项的默认值为 `-optionstrict-`。</span><span class="sxs-lookup"><span data-stu-id="11534-110">The default for this option is `-optionstrict-`.</span></span> <span data-ttu-id="11534-111">`-optionstrict+` 选项与 `-optionstrict` 相同。</span><span class="sxs-lookup"><span data-stu-id="11534-111">The `-optionstrict+` option is the same as `-optionstrict`.</span></span> <span data-ttu-id="11534-112">两者均可用于宽松类型语义。</span><span class="sxs-lookup"><span data-stu-id="11534-112">You can use both for permissive type semantics.</span></span>

`custom`  
<span data-ttu-id="11534-113">必需。</span><span class="sxs-lookup"><span data-stu-id="11534-113">Required.</span></span> <span data-ttu-id="11534-114">不遵从严格语言语义时发出警告。</span><span class="sxs-lookup"><span data-stu-id="11534-114">Warn when strict language semantics are not respected.</span></span>

## <a name="remarks"></a><span data-ttu-id="11534-115">备注</span><span class="sxs-lookup"><span data-stu-id="11534-115">Remarks</span></span>

<span data-ttu-id="11534-116">`-optionstrict+` 生效时，仅可隐式生成扩大类型转换。</span><span class="sxs-lookup"><span data-stu-id="11534-116">When `-optionstrict+` is in effect, only widening type conversions can be made implicitly.</span></span> <span data-ttu-id="11534-117">隐式收缩类型转换将被报告为错误，例如将 `Decimal` 类型对象分配给整数类型对象。</span><span class="sxs-lookup"><span data-stu-id="11534-117">Implicit narrowing type conversions, such as assigning a `Decimal` type object to an integer type object, are reported as errors.</span></span>

<span data-ttu-id="11534-118">若要针对隐式收缩类型转换生成警告，请使用 `-optionstrict:custom`。</span><span class="sxs-lookup"><span data-stu-id="11534-118">To generate warnings for implicit narrowing type conversions, use `-optionstrict:custom`.</span></span> <span data-ttu-id="11534-119">使用 `-nowarn:numberlist` 可忽略特定警告，使用 `-warnaserror:numberlist` 可将特定警告视为错误。</span><span class="sxs-lookup"><span data-stu-id="11534-119">Use `-nowarn:numberlist` to ignore particular warnings and `-warnaserror:numberlist` to treat particular warnings as errors.</span></span>

### <a name="to-set--optionstrict-in-the-visual-studio-ide"></a><span data-ttu-id="11534-120">在 Visual Studio IDE 中设置 -optionstrict</span><span class="sxs-lookup"><span data-stu-id="11534-120">To set -optionstrict in the Visual Studio IDE</span></span>

1. <span data-ttu-id="11534-121">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="11534-121">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="11534-122">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="11534-122">On the **Project** menu, click **Properties.**</span></span>

2. <span data-ttu-id="11534-123">单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="11534-123">Click the **Compile** tab.</span></span>

3. <span data-ttu-id="11534-124">修改“Option Strict”框中的值。 </span><span class="sxs-lookup"><span data-stu-id="11534-124">Modify the value in the **Option Strict** box.</span></span>

### <a name="to-set--optionstrict-programmatically"></a><span data-ttu-id="11534-125">以编程方式设置 -optionstrict</span><span class="sxs-lookup"><span data-stu-id="11534-125">To set -optionstrict programmatically</span></span>

<span data-ttu-id="11534-126">请参阅 [Option Strict 语句](../../language-reference/statements/option-strict-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="11534-126">See [Option Strict Statement](../../language-reference/statements/option-strict-statement.md).</span></span>

## <a name="example"></a><span data-ttu-id="11534-127">示例</span><span class="sxs-lookup"><span data-stu-id="11534-127">Example</span></span>

<span data-ttu-id="11534-128">下面的代码使用严格类型语义编译 `Test.vb`。</span><span class="sxs-lookup"><span data-stu-id="11534-128">The following code compiles `Test.vb` using strict type semantics.</span></span>

```console
vbc -optionstrict+ test.vb
```

## <a name="see-also"></a><span data-ttu-id="11534-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="11534-129">See also</span></span>

- [<span data-ttu-id="11534-130">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="11534-130">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="11534-131">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="11534-131">-optioncompare</span></span>](optioncompare.md)
- [<span data-ttu-id="11534-132">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="11534-132">-optionexplicit</span></span>](optionexplicit.md)
- [<span data-ttu-id="11534-133">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="11534-133">-optioninfer</span></span>](optioninfer.md)
- [<span data-ttu-id="11534-134">-nowarn</span><span class="sxs-lookup"><span data-stu-id="11534-134">-nowarn</span></span>](nowarn.md)
- [<span data-ttu-id="11534-135">-warnaserror (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="11534-135">-warnaserror (Visual Basic)</span></span>](warnaserror.md)
- [<span data-ttu-id="11534-136">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="11534-136">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="11534-137">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="11534-137">Option Strict Statement</span></span>](../../language-reference/statements/option-strict-statement.md)
- [<span data-ttu-id="11534-138">“选项”对话框 ->“项目”->“Visual Basic 默认值”</span><span class="sxs-lookup"><span data-stu-id="11534-138">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
