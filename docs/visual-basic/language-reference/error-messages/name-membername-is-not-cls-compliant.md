---
description: 了解详细信息： BC40031：名称 <membername> 不符合 CLS
title: 名称 <membername> 不符合 CLS
ms.date: 07/20/2015
f1_keywords:
- bc40031
- vbc40031
helpviewer_keywords:
- BC40031
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
ms.openlocfilehash: 7abc4aee8bb468b523e5bdd2ac13947d19c926bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795750"
---
# <a name="bc40031-name-membername-is-not-cls-compliant"></a><span data-ttu-id="4da5f-103">BC40031：名称 \<membername> 不符合 CLS</span><span class="sxs-lookup"><span data-stu-id="4da5f-103">BC40031: Name \<membername> is not CLS-compliant</span></span>

<span data-ttu-id="4da5f-104">程序集标记为， `<CLSCompliant(True)>` 但公开名称以下划线 () 开头的成员 `_` 。</span><span class="sxs-lookup"><span data-stu-id="4da5f-104">An assembly is marked as `<CLSCompliant(True)>` but exposes a member with a name that begins with an underscore (`_`).</span></span>

 <span data-ttu-id="4da5f-105">编程元素可以包含一个或多个下划线，但要符合 [语言独立性和 Language-Independent 组件](../../../standard/language-independence-and-language-independent-components.md) (CLS) ，它不能以下划线开头。</span><span class="sxs-lookup"><span data-stu-id="4da5f-105">A programming element can contain one or more underscores, but to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must not begin with an underscore.</span></span> <span data-ttu-id="4da5f-106">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="4da5f-106">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

 <span data-ttu-id="4da5f-107">当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。</span><span class="sxs-lookup"><span data-stu-id="4da5f-107">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="4da5f-108">此参数没有默认值，必须为其提供一个值。</span><span class="sxs-lookup"><span data-stu-id="4da5f-108">There is no default for this parameter, and you must supply a value.</span></span>

 <span data-ttu-id="4da5f-109">如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。</span><span class="sxs-lookup"><span data-stu-id="4da5f-109">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>

 <span data-ttu-id="4da5f-110">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="4da5f-110">By default, this message is a warning.</span></span> <span data-ttu-id="4da5f-111">有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="4da5f-111">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="4da5f-112">**错误 ID：** BC40031</span><span class="sxs-lookup"><span data-stu-id="4da5f-112">**Error ID:** BC40031</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4da5f-113">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4da5f-113">To correct this error</span></span>

- <span data-ttu-id="4da5f-114">如果你可以控制源代码，请更改成员名称，使其不以下划线开头。</span><span class="sxs-lookup"><span data-stu-id="4da5f-114">If you have control over the source code, change the member name so that it does not begin with an underscore.</span></span>

- <span data-ttu-id="4da5f-115">如果要求成员名称保持不变，请 <xref:System.CLSCompliantAttribute> 从其定义中删除或将其标记为 `<CLSCompliant(False)>` 。</span><span class="sxs-lookup"><span data-stu-id="4da5f-115">If you require that the member name remain unchanged, remove the <xref:System.CLSCompliantAttribute> from its definition or mark it as `<CLSCompliant(False)>`.</span></span> <span data-ttu-id="4da5f-116">你仍可以将程序集标记为 `<CLSCompliant(True)>` 。</span><span class="sxs-lookup"><span data-stu-id="4da5f-116">You can still mark the assembly as `<CLSCompliant(True)>`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4da5f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="4da5f-117">See also</span></span>

- [<span data-ttu-id="4da5f-118">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="4da5f-118">Declared Element Names</span></span>](../../programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="4da5f-119">Visual Basic 命名约定</span><span class="sxs-lookup"><span data-stu-id="4da5f-119">Visual Basic Naming Conventions</span></span>](../../programming-guide/program-structure/naming-conventions.md)
