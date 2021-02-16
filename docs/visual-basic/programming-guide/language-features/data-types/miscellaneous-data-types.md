---
description: '了解详细信息：杂项数据类型 (Visual Basic) '
title: 杂项数据类型
ms.date: 07/20/2015
helpviewer_keywords:
- Object data type [Visual Basic], data types
- data types [Visual Basic], choosing
ms.assetid: 64c71a12-9057-4dbf-baca-7379c4aada69
ms.openlocfilehash: 3875a3fc3027d573013470cb96c9482a0be6cbbf
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100461991"
---
# <a name="miscellaneous-data-types-visual-basic"></a><span data-ttu-id="ffbdd-103">其他数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ffbdd-103">Miscellaneous Data Types (Visual Basic)</span></span>

<span data-ttu-id="ffbdd-104">Visual Basic 提供了多种数据类型，这些数据类型不是面向数字或字符。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-104">Visual Basic supplies several data types that are not oriented toward numbers or characters.</span></span> <span data-ttu-id="ffbdd-105">而是处理专用数据，如 "是/否" 值、日期/时间值和对象地址。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-105">Instead, they deal with specialized data such as yes/no values, date/time values, and object addresses.</span></span>  
  
 <span data-ttu-id="ffbdd-106">有关显示 Visual Basic 数据类型的并行比较的表，请参阅 [数据类型](../../../language-reference/data-types/index.md)。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-106">For a table showing a side-by-side comparison of the Visual Basic data types, see [Data Types](../../../language-reference/data-types/index.md).</span></span>  
  
## <a name="boolean-type"></a><span data-ttu-id="ffbdd-107">布尔类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-107">Boolean Type</span></span>  

 <span data-ttu-id="ffbdd-108">[布尔数据类型](../../../language-reference/data-types/boolean-data-type.md)是解释为或的无符号值 `True` `False` 。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-108">The [Boolean Data Type](../../../language-reference/data-types/boolean-data-type.md) is an unsigned value that is interpreted as either `True` or `False`.</span></span> <span data-ttu-id="ffbdd-109">其数据宽度取决于实现平台。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-109">Its data width depends on the implementing platform.</span></span> <span data-ttu-id="ffbdd-110">如果变量只能包含两个状态值，如 true/false、yes/no 或 on/off，则将其声明为 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-110">If a variable can contain only two-state values such as true/false, yes/no, or on/off, declare it as `Boolean`.</span></span>  
  
## <a name="date-type"></a><span data-ttu-id="ffbdd-111">日期类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-111">Date Type</span></span>  

 <span data-ttu-id="ffbdd-112">[日期数据类型](../../../language-reference/data-types/date-data-type.md)是包含日期和时间信息的64位值。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-112">The [Date Data Type](../../../language-reference/data-types/date-data-type.md) is a 64-bit value that holds both date and time information.</span></span> <span data-ttu-id="ffbdd-113">每个增量都表示100毫微秒，自开始 (12:00 AM) ，截止时间为公历第1年1月1日。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-113">Each increment represents 100 nanoseconds of elapsed time since the beginning (12:00 AM) of January 1 of the year 1 in the Gregorian calendar.</span></span> <span data-ttu-id="ffbdd-114">如果变量可以包含日期值和/或时间值，则将其声明为 `Date` 。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-114">If a variable can contain a date value, a time value, or both, declare it as `Date`.</span></span>  
  
## <a name="object-type"></a><span data-ttu-id="ffbdd-115">对象类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-115">Object Type</span></span>  

 <span data-ttu-id="ffbdd-116">[Object 数据类型](../../../language-reference/data-types/object-data-type.md)是一个32位地址，它指向应用程序或其他应用程序中的对象实例。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-116">The [Object Data Type](../../../language-reference/data-types/object-data-type.md) is a 32-bit address that points to an object instance within your application or in some other application.</span></span> <span data-ttu-id="ffbdd-117">`Object`变量可以引用应用程序识别的任何对象，或引用任何数据类型的数据。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-117">An `Object` variable can refer to any object your application recognizes, or to data of any data type.</span></span> <span data-ttu-id="ffbdd-118">这包括 *值类型*（如 `Integer` 、 `Boolean` 和结构实例）和 *引用类型*（即从和等类创建的对象的实例 `String` <xref:System.Windows.Forms.Form> ）和数组实例。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-118">This includes both *value types*, such as `Integer`, `Boolean`, and structure instances, and *reference types*, which are instances of objects created from classes such as `String` and <xref:System.Windows.Forms.Form>, and array instances.</span></span>  
  
 <span data-ttu-id="ffbdd-119">如果变量存储指向在编译时不知道的类的实例的指针，或者如果该变量可以指向各种数据类型的数据，则将其声明为 `Object` 。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-119">If a variable stores a pointer to an instance of a class that you do not know at compile time, or if it can point to data of various data types, declare it as `Object`.</span></span>  
  
 <span data-ttu-id="ffbdd-120">数据类型的优点在于， `Object` 您可以使用数据类型来存储任何数据类型的数据。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-120">The advantage of the `Object` data type is that you can use it to store data of any data type.</span></span> <span data-ttu-id="ffbdd-121">缺点是您会产生额外的操作，这些操作需要更长的执行时间，并使应用程序的运行速度更慢。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-121">The disadvantage is that you incur extra operations that take more execution time and make your application perform slower.</span></span> <span data-ttu-id="ffbdd-122">如果 `Object` 对值类型使用变量，则会产生 *装箱* 和 *取消装箱*。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-122">If you use an `Object` variable for value types, you incur *boxing* and *unboxing*.</span></span> <span data-ttu-id="ffbdd-123">如果将其用于引用类型，则会产生 *后期绑定*。</span><span class="sxs-lookup"><span data-stu-id="ffbdd-123">If you use it for reference types, you incur *late binding*.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffbdd-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="ffbdd-124">See also</span></span>

- [<span data-ttu-id="ffbdd-125">类型字符</span><span class="sxs-lookup"><span data-stu-id="ffbdd-125">Type Characters</span></span>](type-characters.md)
- [<span data-ttu-id="ffbdd-126">基本数据类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-126">Elementary Data Types</span></span>](elementary-data-types.md)
- [<span data-ttu-id="ffbdd-127">数值数据类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-127">Numeric Data Types</span></span>](numeric-data-types.md)
- [<span data-ttu-id="ffbdd-128">字符数据类型</span><span class="sxs-lookup"><span data-stu-id="ffbdd-128">Character Data Types</span></span>](character-data-types.md)
- [<span data-ttu-id="ffbdd-129">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="ffbdd-129">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)
- [<span data-ttu-id="ffbdd-130">早期绑定和后期绑定</span><span class="sxs-lookup"><span data-stu-id="ffbdd-130">Early and Late Binding</span></span>](../early-late-binding/index.md)
