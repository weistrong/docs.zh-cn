---
description: 了解详细信息： BC40042：可选参数的可选值类型 <parametername> 不符合 CLS
title: 可选参数 <parametername> 的可选值的类型不符合 CLS
ms.date: 07/20/2015
f1_keywords:
- BC40042
- vbc40042
helpviewer_keywords:
- BC40042
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
ms.openlocfilehash: 44dee07120ebcd99be69257aef6a334f9067cdb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774858"
---
# <a name="bc40042-type-of-optional-value-for-optional-parameter-parametername-is-not-cls-compliant"></a><span data-ttu-id="e0a71-103">BC40042：可选参数的可选值的类型 \<parametername> 不符合 CLS</span><span class="sxs-lookup"><span data-stu-id="e0a71-103">BC40042: Type of optional value for optional parameter \<parametername> is not CLS-compliant</span></span>

<span data-ttu-id="e0a71-104">一个过程标记为 `<CLSCompliant(True)>`，但声明一个[可选](../modifiers/optional.md)参数，该参数具有不符合的类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="e0a71-104">A procedure is marked as `<CLSCompliant(True)>` but declares an [Optional](../modifiers/optional.md) parameter with default value of a noncompliant type.</span></span>

 <span data-ttu-id="e0a71-105">一个过程要符合[语言独立性和与语言无关的组件](../../../standard/language-independence-and-language-independent-components.md) (CLS)，必须只使用符合 CLS 的类型。</span><span class="sxs-lookup"><span data-stu-id="e0a71-105">For a procedure to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must use only CLS-compliant types.</span></span> <span data-ttu-id="e0a71-106">这适用于参数的类型、返回类型及其所有本地变量的类型。</span><span class="sxs-lookup"><span data-stu-id="e0a71-106">This applies to the types of the parameters, the return type, and the types of all its local variables.</span></span> <span data-ttu-id="e0a71-107">也适用于可选参数的默认值。</span><span class="sxs-lookup"><span data-stu-id="e0a71-107">It also applies to the default values of optional parameters.</span></span>

 <span data-ttu-id="e0a71-108">以下 Visual Basic 数据类型不符合 CLS：</span><span class="sxs-lookup"><span data-stu-id="e0a71-108">The following Visual Basic data types are not CLS-compliant:</span></span>

- [<span data-ttu-id="e0a71-109">SByte 数据类型</span><span class="sxs-lookup"><span data-stu-id="e0a71-109">SByte Data Type</span></span>](../data-types/sbyte-data-type.md)

- [<span data-ttu-id="e0a71-110">UInteger 数据类型</span><span class="sxs-lookup"><span data-stu-id="e0a71-110">UInteger Data Type</span></span>](../data-types/uinteger-data-type.md)

- [<span data-ttu-id="e0a71-111">ULong 数据类型</span><span class="sxs-lookup"><span data-stu-id="e0a71-111">ULong Data Type</span></span>](../data-types/ulong-data-type.md)

- [<span data-ttu-id="e0a71-112">UShort 数据类型</span><span class="sxs-lookup"><span data-stu-id="e0a71-112">UShort Data Type</span></span>](../data-types/ushort-data-type.md)

 <span data-ttu-id="e0a71-113">当将 <xref:System.CLSCompliantAttribute> 特性应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。</span><span class="sxs-lookup"><span data-stu-id="e0a71-113">When you apply the <xref:System.CLSCompliantAttribute> attribute to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="e0a71-114">此参数没有默认值，必须为其提供一个值。</span><span class="sxs-lookup"><span data-stu-id="e0a71-114">There is no default for this parameter, and you must supply a value.</span></span>

 <span data-ttu-id="e0a71-115">如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。</span><span class="sxs-lookup"><span data-stu-id="e0a71-115">If you do not apply <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>

 <span data-ttu-id="e0a71-116">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="e0a71-116">By default, this message is a warning.</span></span> <span data-ttu-id="e0a71-117">有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="e0a71-117">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="e0a71-118">**错误 ID:** BC40042</span><span class="sxs-lookup"><span data-stu-id="e0a71-118">**Error ID:** BC40042</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="e0a71-119">更正此错误</span><span class="sxs-lookup"><span data-stu-id="e0a71-119">To correct this error</span></span>

- <span data-ttu-id="e0a71-120">如果可选参数必须具有此特定类型的默认值，请删除 <xref:System.CLSCompliantAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="e0a71-120">If the optional parameter must have a default value of this particular type, remove <xref:System.CLSCompliantAttribute>.</span></span> <span data-ttu-id="e0a71-121">该过程不符合 CLS。</span><span class="sxs-lookup"><span data-stu-id="e0a71-121">The procedure cannot be CLS-compliant.</span></span>

- <span data-ttu-id="e0a71-122">如果过程必须符合 CLS，则将此默认值的类型改为最接近的符合 CLS 的类型。</span><span class="sxs-lookup"><span data-stu-id="e0a71-122">If the procedure must be CLS-compliant, change the type of this default value to the closest CLS-compliant type.</span></span> <span data-ttu-id="e0a71-123">例如，如果不需要 2147483647 以上的数值范围，可以使用 `UInteger` 取代 `Integer` 。</span><span class="sxs-lookup"><span data-stu-id="e0a71-123">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="e0a71-124">如果确实需要更大范围，可以用 `UInteger` 代替 `Long`。</span><span class="sxs-lookup"><span data-stu-id="e0a71-124">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>

- <span data-ttu-id="e0a71-125">如果要与自动化或 COM 对象进行交互，请记住，某些类型的数据宽度与 .NET Framework 中的不同。</span><span class="sxs-lookup"><span data-stu-id="e0a71-125">If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the .NET Framework.</span></span> <span data-ttu-id="e0a71-126">例如，`int` 在其他环境中通常为 16 位。</span><span class="sxs-lookup"><span data-stu-id="e0a71-126">For example, `int` is often 16 bits in other environments.</span></span> <span data-ttu-id="e0a71-127">如果接受此类组件的16位整数，请 `Short` `Integer` 在托管的 Visual Basic 代码中将其声明为而不是。</span><span class="sxs-lookup"><span data-stu-id="e0a71-127">If you are accepting a 16-bit integer from such a component, declare it as `Short` instead of `Integer` in your managed Visual Basic code.</span></span>
