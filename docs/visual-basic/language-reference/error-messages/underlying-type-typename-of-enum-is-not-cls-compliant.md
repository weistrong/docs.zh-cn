---
description: 了解详细信息： BC40032： <typename> 枚举的基础类型不符合 CLS
title: 枚举的基础类型 <typename> 不符合 CLS
ms.date: 07/20/2015
f1_keywords:
- vbc40032
- bc40032
helpviewer_keywords:
- BC40032
ms.assetid: 32bf1949-fd73-456c-a323-bf1ffe1320ed
ms.openlocfilehash: aebee5a9e0cd7f2e780d0171ad59dcfd4fd1d940
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674787"
---
# <a name="bc40032-underlying-type-typename-of-enum-is-not-cls-compliant"></a><span data-ttu-id="dedd9-103">BC40032： \<typename> 枚举的基础类型不符合 CLS</span><span class="sxs-lookup"><span data-stu-id="dedd9-103">BC40032: Underlying type \<typename> of Enum is not CLS-compliant</span></span>

<span data-ttu-id="dedd9-104">为此枚举指定的数据类型不是 [语言独立性的一部分，并且 Language-Independent 组件](../../../standard/language-independence-and-language-independent-components.md) (CLS) 。</span><span class="sxs-lookup"><span data-stu-id="dedd9-104">The data type specified for this enumeration is not part of the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span></span> <span data-ttu-id="dedd9-105">这不是你的组件中的错误，因为 .NET Framework 和 Visual Basic 支持此数据类型。</span><span class="sxs-lookup"><span data-stu-id="dedd9-105">This is not an error within your component, because the .NET Framework and Visual Basic support this data type.</span></span> <span data-ttu-id="dedd9-106">但是，以严格符合 CLS 的代码编写的另一个组件可能不支持此数据类型。</span><span class="sxs-lookup"><span data-stu-id="dedd9-106">However, another component written in strictly CLS-compliant code might not support this data type.</span></span> <span data-ttu-id="dedd9-107">此类组件可能无法与组件成功交互。</span><span class="sxs-lookup"><span data-stu-id="dedd9-107">Such a component might not be able to interact successfully with your component.</span></span>

 <span data-ttu-id="dedd9-108">以下 Visual Basic 数据类型不符合 CLS：</span><span class="sxs-lookup"><span data-stu-id="dedd9-108">The following Visual Basic data types are not CLS-compliant:</span></span>

- [<span data-ttu-id="dedd9-109">SByte 数据类型</span><span class="sxs-lookup"><span data-stu-id="dedd9-109">SByte Data Type</span></span>](../data-types/sbyte-data-type.md)

- [<span data-ttu-id="dedd9-110">UInteger 数据类型</span><span class="sxs-lookup"><span data-stu-id="dedd9-110">UInteger Data Type</span></span>](../data-types/uinteger-data-type.md)

- [<span data-ttu-id="dedd9-111">ULong 数据类型</span><span class="sxs-lookup"><span data-stu-id="dedd9-111">ULong Data Type</span></span>](../data-types/ulong-data-type.md)

- [<span data-ttu-id="dedd9-112">UShort 数据类型</span><span class="sxs-lookup"><span data-stu-id="dedd9-112">UShort Data Type</span></span>](../data-types/ushort-data-type.md)

 <span data-ttu-id="dedd9-113">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="dedd9-113">By default, this message is a warning.</span></span> <span data-ttu-id="dedd9-114">有关隐藏警告或将警告视为错误的详细信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="dedd9-114">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="dedd9-115">**错误 ID：** BC40032</span><span class="sxs-lookup"><span data-stu-id="dedd9-115">**Error ID:** BC40032</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="dedd9-116">更正此错误</span><span class="sxs-lookup"><span data-stu-id="dedd9-116">To correct this error</span></span>

- <span data-ttu-id="dedd9-117">如果你的组件只与其他 .NET Framework 组件交互，或者不与任何其他组件进行交互，则无需更改任何内容。</span><span class="sxs-lookup"><span data-stu-id="dedd9-117">If your component interfaces only with other .NET Framework components, or does not interface with any other components, you do not need to change anything.</span></span>

- <span data-ttu-id="dedd9-118">如果与不是为 .NET Framework 编写的组件进行交互，则可以通过反射或文档来确定它是否支持此数据类型。</span><span class="sxs-lookup"><span data-stu-id="dedd9-118">If you are interfacing with a component not written for the .NET Framework, you might be able to determine, either through reflection or from documentation, whether it supports this data type.</span></span> <span data-ttu-id="dedd9-119">如果是这样，则无需更改任何内容。</span><span class="sxs-lookup"><span data-stu-id="dedd9-119">If it does, you do not need to change anything.</span></span>

- <span data-ttu-id="dedd9-120">如果与不支持此数据类型的组件进行交互，则必须将其替换为最接近的符合 CLS 的类型。</span><span class="sxs-lookup"><span data-stu-id="dedd9-120">If you are interfacing with a component that does not support this data type, you must replace it with the closest CLS-compliant type.</span></span> <span data-ttu-id="dedd9-121">例如，如果不需要 2147483647 以上的数值范围，可以使用 `UInteger` 取代 `Integer` 。</span><span class="sxs-lookup"><span data-stu-id="dedd9-121">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="dedd9-122">如果确实需要更大范围，可以用 `UInteger` 代替 `Long`。</span><span class="sxs-lookup"><span data-stu-id="dedd9-122">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>

- <span data-ttu-id="dedd9-123">如果要与自动化或 COM 对象进行交互，请记住，某些类型的数据宽度与 .NET Framework 中的不同。</span><span class="sxs-lookup"><span data-stu-id="dedd9-123">If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the .NET Framework.</span></span> <span data-ttu-id="dedd9-124">例如，`uint` 在其他环境中通常为 16 位。</span><span class="sxs-lookup"><span data-stu-id="dedd9-124">For example, `uint` is often 16 bits in other environments.</span></span> <span data-ttu-id="dedd9-125">如果要将16位参数传递给此类组件，请 `UShort` `UInteger` 在托管的 Visual Basic 代码中将其声明为而不是。</span><span class="sxs-lookup"><span data-stu-id="dedd9-125">If you are passing a 16-bit argument to such a component, declare it as `UShort` instead of `UInteger` in your managed Visual Basic code.</span></span>

## <a name="see-also"></a><span data-ttu-id="dedd9-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="dedd9-126">See also</span></span>

- [<span data-ttu-id="dedd9-127">反射 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dedd9-127">Reflection (Visual Basic)</span></span>](../../programming-guide/concepts/reflection.md)
- [<span data-ttu-id="dedd9-128">反射</span><span class="sxs-lookup"><span data-stu-id="dedd9-128">Reflection</span></span>](../../../framework/reflection-and-codedom/reflection.md)
