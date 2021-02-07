---
description: '了解更多详细信息： (Visual Basic 的 CStr 函数返回值) '
title: 返回 CStr 函数的值
ms.date: 07/20/2015
helpviewer_keywords:
- times [Visual Basic], CStr Function return values
- type conversion [Visual Basic]
- dates [Visual Basic], CStr Function return values
- CStr function
- strings [Visual Basic], return value
- Date data type [Visual Basic], converting
- dates [Visual Basic]
- String data type [Visual Basic], converting
ms.assetid: 3aa744e7-1419-45d5-85e3-e5abc2953673
ms.openlocfilehash: ce45059db8ff8e926954014a09379ee54f1caf30
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731103"
---
# <a name="return-values-for-the-cstr-function-visual-basic"></a><span data-ttu-id="fea94-103">返回 CStr 函数的值 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fea94-103">Return Values for the CStr Function (Visual Basic)</span></span>

<span data-ttu-id="fea94-104">下表描述了的 `CStr` 不同数据类型的返回值 `expression` 。</span><span class="sxs-lookup"><span data-stu-id="fea94-104">The following table describes the return values for `CStr` for different data types of `expression`.</span></span>  
  
|<span data-ttu-id="fea94-105">如果 `expression` 类型为</span><span class="sxs-lookup"><span data-stu-id="fea94-105">If `expression` type is</span></span>|<span data-ttu-id="fea94-106">`CStr` 返回</span><span class="sxs-lookup"><span data-stu-id="fea94-106">`CStr` returns</span></span>|  
|-----------------------------|--------------------|  
|[<span data-ttu-id="fea94-107">布尔数据类型</span><span class="sxs-lookup"><span data-stu-id="fea94-107">Boolean Data Type</span></span>](../data-types/boolean-data-type.md)|<span data-ttu-id="fea94-108">包含 "True" 或 "False" 的字符串。</span><span class="sxs-lookup"><span data-stu-id="fea94-108">A string containing "True" or "False".</span></span>|  
|[<span data-ttu-id="fea94-109">Date 数据类型</span><span class="sxs-lookup"><span data-stu-id="fea94-109">Date Data Type</span></span>](../data-types/date-data-type.md)|<span data-ttu-id="fea94-110">一个字符串，其中包含 `Date` 以您的系统的短日期格式 (日期和时间) 值。</span><span class="sxs-lookup"><span data-stu-id="fea94-110">A string containing a `Date` value (date and time) in the short date format of your system.</span></span>|  
|[<span data-ttu-id="fea94-111">数值数据类型</span><span class="sxs-lookup"><span data-stu-id="fea94-111">Numeric Data Types</span></span>](../../programming-guide/language-features/data-types/numeric-data-types.md)|<span data-ttu-id="fea94-112">表示数字的字符串。</span><span class="sxs-lookup"><span data-stu-id="fea94-112">A string representing the number.</span></span>|  
  
## <a name="cstr-and-date"></a><span data-ttu-id="fea94-113">CStr 和日期</span><span class="sxs-lookup"><span data-stu-id="fea94-113">CStr and Date</span></span>  

 <span data-ttu-id="fea94-114">`Date`类型始终包含日期和时间信息。</span><span class="sxs-lookup"><span data-stu-id="fea94-114">The `Date` type always contains both date and time information.</span></span> <span data-ttu-id="fea94-115">出于类型转换的目的，Visual Basic 会考虑 (1/1/0001 年1月1日) 为日期的 *非特定值* ，00:00:00 (午夜) 为时间的非特定值。</span><span class="sxs-lookup"><span data-stu-id="fea94-115">For purposes of type conversion, Visual Basic considers 1/1/0001 (January 1 of the year 1) to be a *neutral value* for the date, and 00:00:00 (midnight) to be a neutral value for the time.</span></span> <span data-ttu-id="fea94-116">`CStr` 不会在生成的字符串中包含非特定值。</span><span class="sxs-lookup"><span data-stu-id="fea94-116">`CStr` does not include neutral values in the resulting string.</span></span> <span data-ttu-id="fea94-117">例如，如果转换 `#January 1, 0001 9:30:00#` 为字符串，则结果为 "9:30:00 AM"; 日期信息将被取消。</span><span class="sxs-lookup"><span data-stu-id="fea94-117">For example, if you convert `#January 1, 0001 9:30:00#` to a string, the result is "9:30:00 AM"; the date information is suppressed.</span></span> <span data-ttu-id="fea94-118">但是，日期信息仍以原始值的形式存在 `Date` ，可以通过等函数进行恢复 <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A> 。</span><span class="sxs-lookup"><span data-stu-id="fea94-118">However, the date information is still present in the original `Date` value and can be recovered with functions such as <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="fea94-119">`CStr`函数根据应用程序的当前区域性设置来执行转换。</span><span class="sxs-lookup"><span data-stu-id="fea94-119">The `CStr` function performs its conversion based on the current culture settings for the application.</span></span> <span data-ttu-id="fea94-120">若要获取特定区域性中的数字的字符串表示形式，请使用数字的 `ToString(IFormatProvider)` 方法。</span><span class="sxs-lookup"><span data-stu-id="fea94-120">To get the string representation of a number in a particular culture, use the number's `ToString(IFormatProvider)` method.</span></span> <span data-ttu-id="fea94-121">例如，在将 <xref:System.Double.ToString%2A?displayProperty=nameWithType> 类型的值转换为时使用 `Double` `String` 。</span><span class="sxs-lookup"><span data-stu-id="fea94-121">For example, use <xref:System.Double.ToString%2A?displayProperty=nameWithType> when converting a value of type `Double` to a `String`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fea94-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="fea94-122">See also</span></span>

- <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A>
- [<span data-ttu-id="fea94-123">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="fea94-123">Type Conversion Functions</span></span>](type-conversion-functions.md)
- [<span data-ttu-id="fea94-124">布尔数据类型</span><span class="sxs-lookup"><span data-stu-id="fea94-124">Boolean Data Type</span></span>](../data-types/boolean-data-type.md)
- [<span data-ttu-id="fea94-125">Date 数据类型</span><span class="sxs-lookup"><span data-stu-id="fea94-125">Date Data Type</span></span>](../data-types/date-data-type.md)
