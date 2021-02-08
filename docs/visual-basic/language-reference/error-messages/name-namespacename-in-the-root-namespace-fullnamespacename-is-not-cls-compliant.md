---
description: 了解详细信息： BC40039： <namespacename> 根命名空间中的名称 <fullnamespacename> 不符合 CLS
title: 根命名空间 <namespacename> 中的名称 <fullnamespacename> 不符合 CLS
ms.date: 07/20/2015
f1_keywords:
- vbc40039
- bc40039
helpviewer_keywords:
- BC40039
ms.assetid: c5bd5914-ae71-416a-8bed-f76f644f78be
ms.openlocfilehash: 2560c5c056c70909a08a48a0ff8b2859b178cc8a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795724"
---
# <a name="bc40039-name-namespacename-in-the-root-namespace-fullnamespacename-is-not-cls-compliant"></a><span data-ttu-id="62ffb-103">BC40039： \<namespacename> 根命名空间中的名称 \<fullnamespacename> 不符合 CLS</span><span class="sxs-lookup"><span data-stu-id="62ffb-103">BC40039: Name \<namespacename> in the root namespace \<fullnamespacename> is not CLS-compliant</span></span>

<span data-ttu-id="62ffb-104">程序集标记为 `<CLSCompliant(True)>` ，但根命名空间名称的元素以下划线 (`_`) 开头。</span><span class="sxs-lookup"><span data-stu-id="62ffb-104">An assembly is marked as `<CLSCompliant(True)>`, but an element of the root namespace name begins with an underscore (`_`).</span></span>

 <span data-ttu-id="62ffb-105">编程元素可以包含一个或多个下划线，但要符合 [语言独立性和 Language-Independent 组件](../../../standard/language-independence-and-language-independent-components.md) (CLS) ，它不能以下划线开头。</span><span class="sxs-lookup"><span data-stu-id="62ffb-105">A programming element can contain one or more underscores, but to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must not begin with an underscore.</span></span> <span data-ttu-id="62ffb-106">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="62ffb-106">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

 <span data-ttu-id="62ffb-107">当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。</span><span class="sxs-lookup"><span data-stu-id="62ffb-107">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="62ffb-108">此参数没有默认值，必须为其提供一个值。</span><span class="sxs-lookup"><span data-stu-id="62ffb-108">There is no default for this parameter, and you must supply a value.</span></span>

 <span data-ttu-id="62ffb-109">如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。</span><span class="sxs-lookup"><span data-stu-id="62ffb-109">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>

 <span data-ttu-id="62ffb-110">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="62ffb-110">By default, this message is a warning.</span></span> <span data-ttu-id="62ffb-111">有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="62ffb-111">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="62ffb-112">**错误 ID：** BC40039</span><span class="sxs-lookup"><span data-stu-id="62ffb-112">**Error ID:** BC40039</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="62ffb-113">更正此错误</span><span class="sxs-lookup"><span data-stu-id="62ffb-113">To correct this error</span></span>

- <span data-ttu-id="62ffb-114">如果需要符合 CLS，请更改根命名空间名称，使其所有元素都不以下划线开头。</span><span class="sxs-lookup"><span data-stu-id="62ffb-114">If you require CLS compliance, change the root namespace name so that none of its elements begins with an underscore.</span></span>

- <span data-ttu-id="62ffb-115">如果要求命名空间名称保持不变，则 <xref:System.CLSCompliantAttribute> 从程序集删除或将其标记为 `<CLSCompliant(False)>` 。</span><span class="sxs-lookup"><span data-stu-id="62ffb-115">If you require that the namespace name remain unchanged, then remove the <xref:System.CLSCompliantAttribute> from the assembly or mark it as `<CLSCompliant(False)>`.</span></span>

## <a name="see-also"></a><span data-ttu-id="62ffb-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="62ffb-116">See also</span></span>

- [<span data-ttu-id="62ffb-117">Namespace 语句</span><span class="sxs-lookup"><span data-stu-id="62ffb-117">Namespace Statement</span></span>](../statements/namespace-statement.md)
- [<span data-ttu-id="62ffb-118">Visual Basic 中的命名空间</span><span class="sxs-lookup"><span data-stu-id="62ffb-118">Namespaces in Visual Basic</span></span>](../../programming-guide/program-structure/namespaces.md)
- [<span data-ttu-id="62ffb-119">-rootnamespace</span><span class="sxs-lookup"><span data-stu-id="62ffb-119">-rootnamespace</span></span>](../../reference/command-line-compiler/rootnamespace.md)
- [<span data-ttu-id="62ffb-120">“项目设计器”->“应用程序”页 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="62ffb-120">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [<span data-ttu-id="62ffb-121">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="62ffb-121">Declared Element Names</span></span>](../../programming-guide/language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="62ffb-122">Visual Basic 命名约定</span><span class="sxs-lookup"><span data-stu-id="62ffb-122">Visual Basic Naming Conventions</span></span>](../../programming-guide/program-structure/naming-conventions.md)
