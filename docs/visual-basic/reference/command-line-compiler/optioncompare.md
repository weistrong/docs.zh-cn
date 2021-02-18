---
description: 详细了解：-optioncompare
title: -optioncompare
ms.date: 07/20/2015
f1_keywords:
- /optioncompare
- -optioncompare
helpviewer_keywords:
- optioncompare compiler option [Visual Basic]
- -optioncompare compiler option [Visual Basic]
- /optioncompare compiler option [Visual Basic]
ms.assetid: 7237b766-b44d-4cc5-9a3c-885348a7d9e4
ms.openlocfilehash: 9be4867c75cc16a8f699cf492dc41e9d08b96495
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475924"
---
# <a name="-optioncompare"></a><span data-ttu-id="83ffc-103">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="83ffc-103">-optioncompare</span></span>

<span data-ttu-id="83ffc-104">指定如何进行字符串比较。</span><span class="sxs-lookup"><span data-stu-id="83ffc-104">Specifies how string comparisons are made.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ffc-105">语法</span><span class="sxs-lookup"><span data-stu-id="83ffc-105">Syntax</span></span>

```console
-optioncompare:{binary | text}
```

## <a name="remarks"></a><span data-ttu-id="83ffc-106">备注</span><span class="sxs-lookup"><span data-stu-id="83ffc-106">Remarks</span></span>

<span data-ttu-id="83ffc-107">可以使用以下两种形式之一指定 `-optioncompare`：使用二进制字符串比较的 `-optioncompare:binary`，和使用文本字符串比较的 `-optioncompare:text`。</span><span class="sxs-lookup"><span data-stu-id="83ffc-107">You can specify `-optioncompare` in one of two forms: `-optioncompare:binary` to use binary string comparisons, and `-optioncompare:text` to use text string comparisons.</span></span> <span data-ttu-id="83ffc-108">默认情况下，编译器使用 `-optioncompare:binary`。</span><span class="sxs-lookup"><span data-stu-id="83ffc-108">By default, the compiler uses `-optioncompare:binary`.</span></span>

<span data-ttu-id="83ffc-109">在 Microsoft Windows 中，当前代码页确定二进制排序顺序。</span><span class="sxs-lookup"><span data-stu-id="83ffc-109">In Microsoft Windows, the current code page determines the binary sort order.</span></span> <span data-ttu-id="83ffc-110">典型的二进制排序顺序如下所示：</span><span class="sxs-lookup"><span data-stu-id="83ffc-110">A typical binary sort order is as follows:</span></span>

`A < B < E < Z < a < b < e < z < À < Ê < Ø < à < ê < ø`

<span data-ttu-id="83ffc-111">基于由系统的区域设置确定的不区分大小写的文本排序顺序对基于文本的字符串进行比较。</span><span class="sxs-lookup"><span data-stu-id="83ffc-111">Text-based string comparisons are based on a case-insensitive text sort order determined by your system's locale.</span></span> <span data-ttu-id="83ffc-112">典型的文本排序顺序如下所示：</span><span class="sxs-lookup"><span data-stu-id="83ffc-112">A typical text sort order is as follows:</span></span>

`(A = a) < (À = à) < (B=b) < (E=e) < (Ê = ê) < (Z=z) < (Ø = ø)`

### <a name="to-set--optioncompare-in-the-visual-studio-ide"></a><span data-ttu-id="83ffc-113">若要在 Visual Studio IDE 中设置 -optioncompare</span><span class="sxs-lookup"><span data-stu-id="83ffc-113">To set -optioncompare in the Visual Studio IDE</span></span>

1. <span data-ttu-id="83ffc-114">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="83ffc-114">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="83ffc-115">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="83ffc-115">On the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="83ffc-116">单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="83ffc-116">Click the **Compile** tab.</span></span>

3. <span data-ttu-id="83ffc-117">修改“Option Compare”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="83ffc-117">Modify the value in the **Option Compare** box.</span></span>

### <a name="to-set--optioncompare-programmatically"></a><span data-ttu-id="83ffc-118">以编程方式设置 -optioncompare</span><span class="sxs-lookup"><span data-stu-id="83ffc-118">To set -optioncompare programmatically</span></span>

<span data-ttu-id="83ffc-119">请参阅 [Option Compare 语句](../../language-reference/statements/option-compare-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="83ffc-119">See [Option Compare Statement](../../language-reference/statements/option-compare-statement.md).</span></span>

## <a name="example"></a><span data-ttu-id="83ffc-120">示例</span><span class="sxs-lookup"><span data-stu-id="83ffc-120">Example</span></span>

<span data-ttu-id="83ffc-121">下面的代码编译 `ProjFile.vb`，并使用二进制字符串比较。</span><span class="sxs-lookup"><span data-stu-id="83ffc-121">The following code compiles `ProjFile.vb` and uses binary string comparisons.</span></span>

```console
vbc -optioncompare:binary projFile.vb
```

## <a name="see-also"></a><span data-ttu-id="83ffc-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="83ffc-122">See also</span></span>

- [<span data-ttu-id="83ffc-123">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="83ffc-123">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="83ffc-124">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="83ffc-124">-optionexplicit</span></span>](optionexplicit.md)
- [<span data-ttu-id="83ffc-125">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="83ffc-125">-optionstrict</span></span>](optionstrict.md)
- [<span data-ttu-id="83ffc-126">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="83ffc-126">-optioninfer</span></span>](optioninfer.md)
- [<span data-ttu-id="83ffc-127">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="83ffc-127">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="83ffc-128">Option Compare 语句</span><span class="sxs-lookup"><span data-stu-id="83ffc-128">Option Compare Statement</span></span>](../../language-reference/statements/option-compare-statement.md)
- [<span data-ttu-id="83ffc-129">“选项”对话框 ->“项目”->“Visual Basic 默认值”</span><span class="sxs-lookup"><span data-stu-id="83ffc-129">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
