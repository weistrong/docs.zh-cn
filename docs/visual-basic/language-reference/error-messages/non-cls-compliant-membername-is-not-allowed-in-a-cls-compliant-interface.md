---
description: 了解有关以下内容的详细信息： BC40033： <membername> 在符合 cls 的接口中不允许出现不符合 cls 的
title: 在符合 CLS 的接口中不允许出现不符合 CLS 的 <membername>
ms.date: 07/20/2015
f1_keywords:
- bc40033
- vbc40033
helpviewer_keywords:
- BC40033
ms.assetid: 060c4b08-798e-40f1-94cf-c05c524f1b8a
ms.openlocfilehash: 070b56a8bf9df930de5bb5e363a9b157fcdc7ad7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795633"
---
# <a name="bc40033-non-cls-compliant-membername-is-not-allowed-in-a-cls-compliant-interface"></a><span data-ttu-id="a99ac-103">BC40033： \<membername> 在符合 cls 的接口中不允许出现不符合 cls 的</span><span class="sxs-lookup"><span data-stu-id="a99ac-103">BC40033: Non-CLS-compliant \<membername> is not allowed in a CLS-compliant interface</span></span>

<span data-ttu-id="a99ac-104">接口中的属性、过程或事件被标记为 `<CLSCompliant(True)>` 当接口本身标记为 `<CLSCompliant(False)>` 或未标记时。</span><span class="sxs-lookup"><span data-stu-id="a99ac-104">A property, procedure, or event in an interface is marked as `<CLSCompliant(True)>` when the interface itself is marked as `<CLSCompliant(False)>` or is not marked.</span></span>

 <span data-ttu-id="a99ac-105">为了使接口符合 [语言独立性并 Language-Independent 组件](../../../standard/language-independence-and-language-independent-components.md) (CLS) ，其所有成员都必须符合。</span><span class="sxs-lookup"><span data-stu-id="a99ac-105">For an interface to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), all its members must be compliant.</span></span>

 <span data-ttu-id="a99ac-106">当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。</span><span class="sxs-lookup"><span data-stu-id="a99ac-106">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="a99ac-107">此参数没有默认值，必须为其提供一个值。</span><span class="sxs-lookup"><span data-stu-id="a99ac-107">There is no default for this parameter, and you must supply a value.</span></span>

 <span data-ttu-id="a99ac-108">如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。</span><span class="sxs-lookup"><span data-stu-id="a99ac-108">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>

 <span data-ttu-id="a99ac-109">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="a99ac-109">By default, this message is a warning.</span></span> <span data-ttu-id="a99ac-110">有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="a99ac-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="a99ac-111">**错误 ID：** BC40033</span><span class="sxs-lookup"><span data-stu-id="a99ac-111">**Error ID:** BC40033</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="a99ac-112">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a99ac-112">To correct this error</span></span>

- <span data-ttu-id="a99ac-113">如果你需要 CLS 符合性并且可以控制接口源代码，请将接口标记为 `<CLSCompliant(True)>` 符合其所有成员的条件。</span><span class="sxs-lookup"><span data-stu-id="a99ac-113">If you require CLS compliance and have control over the interface source code, mark the interface as `<CLSCompliant(True)>` if all its members are compliant.</span></span>

- <span data-ttu-id="a99ac-114">如果你需要 CLS 符合性并且无法控制接口源代码，或者不符合要求，请在不同的接口中定义此成员。</span><span class="sxs-lookup"><span data-stu-id="a99ac-114">If you require CLS compliance and do not have control over the interface source code, or if it does not qualify to be compliant, define this member within a different interface.</span></span>

- <span data-ttu-id="a99ac-115">如果要求此成员保留在其当前接口内，请 <xref:System.CLSCompliantAttribute> 从其定义中删除或将其标记为 `<CLSCompliant(False)>` 。</span><span class="sxs-lookup"><span data-stu-id="a99ac-115">If you require that this member remain within its current interface, remove the <xref:System.CLSCompliantAttribute> from its definition or mark it as `<CLSCompliant(False)>`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a99ac-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a99ac-116">See also</span></span>

- [<span data-ttu-id="a99ac-117">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="a99ac-117">Interface Statement</span></span>](../statements/interface-statement.md)
