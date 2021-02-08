---
description: '了解详细信息：数据类型摘要 (Visual Basic) '
title: 数据类型摘要
ms.date: 07/20/2015
helpviewer_keywords:
- Boolean data type [Visual Basic], supported types in Visual Basic
- storage [Visual Basic], order of storage
- data types [Visual Basic], Visual Basic
- Single data type [Visual Basic], supported types in Visual Basic
- notation [Visual Basic], scientific
- memory requirements, data types
- user-defined data types [Visual Basic], Visual Basic
- Date data type [Visual Basic], Visual Basic
- Visual Basic, data types
- storage [Visual Basic], allocation
- Integer data type [Visual Basic], Visual Basic data types
- storage [Visual Basic], space
- Variant data types [Visual Basic], supported types in Visual Basic
- Char data type [Visual Basic], Visual Basic data types
- intrinsic data types [Visual Basic]
- memory consumption [Visual Basic], data types
- single-precision numbers
- data types [Visual Basic], order of storage
- Long data type [Visual Basic], supported types in Visual Basic
- String data type [Visual Basic], Visual Basic data types
- storage order, data types
- StructLayoutAttribute class, Visual Basic data type storage
- scientific notation
- Double data type [Visual Basic], Visual Basic data types
- Byte data type [Visual Basic], Visual Basic data types
- Object data type [Visual Basic], supported types in Visual Basic
- data types [Visual Basic], storage allocation
- double-precision numbers
- data types [Visual Basic], summary
- dates [Visual Basic], data types
- strings [Visual Basic], data types
- memory consumption
- storage order, controlling in Visual Basic
- data types [Visual Basic], memory requirements
ms.assetid: e975cdb6-64d8-4a4a-ae27-f3b3ed198ae0
ms.openlocfilehash: ac5b8e438210c2d1407e0d6a12d560f29523620c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792188"
---
# <a name="data-type-summary-visual-basic"></a><span data-ttu-id="9f32e-103">数据类型摘要 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9f32e-103">Data Type Summary (Visual Basic)</span></span>

<span data-ttu-id="9f32e-104">下表显示了 Visual Basic 的数据类型、其支持的公共语言运行时类型、其名义存储分配及其值范围。</span><span class="sxs-lookup"><span data-stu-id="9f32e-104">The following table shows the Visual Basic data types, their supporting common language runtime types, their nominal storage allocation, and their value ranges.</span></span>  
  
|<span data-ttu-id="9f32e-105">Visual Basic 类型</span><span class="sxs-lookup"><span data-stu-id="9f32e-105">Visual Basic type</span></span>|<span data-ttu-id="9f32e-106">公共语言运行时类型结构</span><span class="sxs-lookup"><span data-stu-id="9f32e-106">Common language runtime type structure</span></span>|<span data-ttu-id="9f32e-107">标称存储分配</span><span class="sxs-lookup"><span data-stu-id="9f32e-107">Nominal storage allocation</span></span>|<span data-ttu-id="9f32e-108">取值范围</span><span class="sxs-lookup"><span data-stu-id="9f32e-108">Value range</span></span>|  
|-----------------------|--------------------------------------------|--------------------------------|-----------------|  
|<span data-ttu-id="9f32e-109">布尔 </span><span class="sxs-lookup"><span data-stu-id="9f32e-109">[Boolean](boolean-data-type.md)</span></span>|<xref:System.Boolean>|<span data-ttu-id="9f32e-110">依赖于实现平台</span><span class="sxs-lookup"><span data-stu-id="9f32e-110">Depends on implementing platform</span></span>|<span data-ttu-id="9f32e-111">`True` 或 `False`</span><span class="sxs-lookup"><span data-stu-id="9f32e-111">`True` or `False`</span></span>|  
|[<span data-ttu-id="9f32e-112">Byte</span><span class="sxs-lookup"><span data-stu-id="9f32e-112">Byte</span></span>](byte-data-type.md)|<xref:System.Byte>|<span data-ttu-id="9f32e-113">1 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-113">1 byte</span></span>|<span data-ttu-id="9f32e-114">0到 255 (无符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-114">0 through 255 (unsigned)</span></span>|  
|<span data-ttu-id="9f32e-115">[Char](char-data-type.md) (单个字符) </span><span class="sxs-lookup"><span data-stu-id="9f32e-115">[Char](char-data-type.md) (single character)</span></span>|<xref:System.Char>|<span data-ttu-id="9f32e-116">2 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-116">2 bytes</span></span>|<span data-ttu-id="9f32e-117">0到 65535 (无符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-117">0 through 65535 (unsigned)</span></span>|  
|[<span data-ttu-id="9f32e-118">日期</span><span class="sxs-lookup"><span data-stu-id="9f32e-118">Date</span></span>](date-data-type.md)|<xref:System.DateTime>|<span data-ttu-id="9f32e-119">8 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-119">8 bytes</span></span>|<span data-ttu-id="9f32e-120">0:00:00 (0001 年1月1日午夜) 9999，年12月1日到 11:59:59 PM</span><span class="sxs-lookup"><span data-stu-id="9f32e-120">0:00:00 (midnight) on January 1, 0001 through 11:59:59 PM on December 31, 9999</span></span>|  
|<span data-ttu-id="9f32e-121">十进制 </span><span class="sxs-lookup"><span data-stu-id="9f32e-121">[Decimal](decimal-data-type.md)</span></span>|<xref:System.Decimal>|<span data-ttu-id="9f32e-122">16 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-122">16 bytes</span></span>|<span data-ttu-id="9f32e-123">0到 +/-79228162514264337593543950335 (+/-7.9...E + 28) <sup>†</sup> ，无小数点;0到 +/-7.9228162514264337593543950335，小数点右侧有28个位置;</span><span class="sxs-lookup"><span data-stu-id="9f32e-123">0 through +/-79,228,162,514,264,337,593,543,950,335 (+/-7.9...E+28) <sup>†</sup> with no decimal point; 0 through +/-7.9228162514264337593543950335 with 28 places to the right of the decimal;</span></span><br /><br /> <span data-ttu-id="9f32e-124">最小非零数字为 +/-0.0000000000000000000000000001 (+/-1E-28) <sup>†</sup></span><span class="sxs-lookup"><span data-stu-id="9f32e-124">smallest nonzero number is +/-0.0000000000000000000000000001 (+/-1E-28) <sup>†</sup></span></span>|  
|<span data-ttu-id="9f32e-125">[双](double-data-type.md) 精度 (双精度浮点) </span><span class="sxs-lookup"><span data-stu-id="9f32e-125">[Double](double-data-type.md) (double-precision floating-point)</span></span>|<xref:System.Double>|<span data-ttu-id="9f32e-126">8 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-126">8 bytes</span></span>|<span data-ttu-id="9f32e-127">-1.79769313486231570 e + 308 到-4.94065645841246544 E-324 <sup>†</sup> 表示负值;</span><span class="sxs-lookup"><span data-stu-id="9f32e-127">-1.79769313486231570E+308 through -4.94065645841246544E-324 <sup>†</sup> for negative values;</span></span><br /><br /> <span data-ttu-id="9f32e-128">4.94065645841246544 e-324 到 1.79769313486231570 E + 308 <sup>†</sup> 用于正值</span><span class="sxs-lookup"><span data-stu-id="9f32e-128">4.94065645841246544E-324 through 1.79769313486231570E+308 <sup>†</sup> for positive values</span></span>|  
|[<span data-ttu-id="9f32e-129">Integer</span><span class="sxs-lookup"><span data-stu-id="9f32e-129">Integer</span></span>](integer-data-type.md)|<xref:System.Int32>|<span data-ttu-id="9f32e-130">4 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-130">4 bytes</span></span>|<span data-ttu-id="9f32e-131">-2147483648 到 2147483647 (有符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-131">-2,147,483,648 through 2,147,483,647 (signed)</span></span>|  
|<span data-ttu-id="9f32e-132">[长](long-data-type.md) (长整型) </span><span class="sxs-lookup"><span data-stu-id="9f32e-132">[Long](long-data-type.md) (long integer)</span></span>|<xref:System.Int64>|<span data-ttu-id="9f32e-133">8 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-133">8 bytes</span></span>|<span data-ttu-id="9f32e-134">-9223372036854775808 到 9223372036854775807 (9.2. E + 18 <sup>†</sup>)  (签名) </span><span class="sxs-lookup"><span data-stu-id="9f32e-134">-9,223,372,036,854,775,808 through 9,223,372,036,854,775,807 (9.2...E+18 <sup>†</sup>) (signed)</span></span>|  
|[<span data-ttu-id="9f32e-135">对象</span><span class="sxs-lookup"><span data-stu-id="9f32e-135">Object</span></span>](object-data-type.md)|<span data-ttu-id="9f32e-136"><xref:System.Object> (类) </span><span class="sxs-lookup"><span data-stu-id="9f32e-136"><xref:System.Object> (class)</span></span>|<span data-ttu-id="9f32e-137">32位平台上的4个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-137">4 bytes on 32-bit platform</span></span><br /><br /> <span data-ttu-id="9f32e-138">64位平台上的8个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-138">8 bytes on 64-bit platform</span></span>|<span data-ttu-id="9f32e-139">任何类型都可以存储在类型的变量中 `Object`</span><span class="sxs-lookup"><span data-stu-id="9f32e-139">Any type can be stored in a variable of type `Object`</span></span>|  
|[<span data-ttu-id="9f32e-140">SByte</span><span class="sxs-lookup"><span data-stu-id="9f32e-140">SByte</span></span>](sbyte-data-type.md)|<xref:System.SByte>|<span data-ttu-id="9f32e-141">1 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-141">1 byte</span></span>|<span data-ttu-id="9f32e-142">-128 到 127 (有符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-142">-128 through 127 (signed)</span></span>|  
|<span data-ttu-id="9f32e-143">[Short](short-data-type.md) (短整型) </span><span class="sxs-lookup"><span data-stu-id="9f32e-143">[Short](short-data-type.md) (short integer)</span></span>|<xref:System.Int16>|<span data-ttu-id="9f32e-144">2 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-144">2 bytes</span></span>|<span data-ttu-id="9f32e-145">-32768 到 32767 (有符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-145">-32,768 through 32,767 (signed)</span></span>|  
|<span data-ttu-id="9f32e-146">[单个](single-data-type.md) (单精度浮点) </span><span class="sxs-lookup"><span data-stu-id="9f32e-146">[Single](single-data-type.md) (single-precision floating-point)</span></span>|<xref:System.Single>|<span data-ttu-id="9f32e-147">4 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-147">4 bytes</span></span>|<span data-ttu-id="9f32e-148">-3.4028235 e + 38 到-1.401298 E-45 <sup>†</sup> 表示负值;</span><span class="sxs-lookup"><span data-stu-id="9f32e-148">-3.4028235E+38 through -1.401298E-45 <sup>†</sup> for negative values;</span></span><br /><br /> <span data-ttu-id="9f32e-149">1.401298 e-45 到 3.4028235 E + 38 <sup>†</sup> 用于正值</span><span class="sxs-lookup"><span data-stu-id="9f32e-149">1.401298E-45 through 3.4028235E+38 <sup>†</sup> for positive values</span></span>|  
|<span data-ttu-id="9f32e-150">[字符串](string-data-type.md) (长度可变的) </span><span class="sxs-lookup"><span data-stu-id="9f32e-150">[String](string-data-type.md) (variable-length)</span></span>|<span data-ttu-id="9f32e-151"><xref:System.String> (类) </span><span class="sxs-lookup"><span data-stu-id="9f32e-151"><xref:System.String> (class)</span></span>|<span data-ttu-id="9f32e-152">依赖于实现平台</span><span class="sxs-lookup"><span data-stu-id="9f32e-152">Depends on implementing platform</span></span>|<span data-ttu-id="9f32e-153">0到约 2000000000 Unicode 字符</span><span class="sxs-lookup"><span data-stu-id="9f32e-153">0 to approximately 2 billion Unicode characters</span></span>|  
|[<span data-ttu-id="9f32e-154">UInteger</span><span class="sxs-lookup"><span data-stu-id="9f32e-154">UInteger</span></span>](uinteger-data-type.md)|<xref:System.UInt32>|<span data-ttu-id="9f32e-155">4 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-155">4 bytes</span></span>|<span data-ttu-id="9f32e-156">0到 4294967295 (无符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-156">0 through 4,294,967,295 (unsigned)</span></span>|  
|[<span data-ttu-id="9f32e-157">ULong</span><span class="sxs-lookup"><span data-stu-id="9f32e-157">ULong</span></span>](ulong-data-type.md)|<xref:System.UInt64>|<span data-ttu-id="9f32e-158">8 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-158">8 bytes</span></span>|<span data-ttu-id="9f32e-159">0到 18446744073709551615 (1.8 ... E + 19 <sup>†</sup>)  (无符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-159">0 through 18,446,744,073,709,551,615 (1.8...E+19 <sup>†</sup>) (unsigned)</span></span>|  
|<span data-ttu-id="9f32e-160">[用户定义的](user-defined-data-type.md) (结构) </span><span class="sxs-lookup"><span data-stu-id="9f32e-160">[User-Defined](user-defined-data-type.md) (structure)</span></span>|<span data-ttu-id="9f32e-161"> (继承自 <xref:System.ValueType>) </span><span class="sxs-lookup"><span data-stu-id="9f32e-161">(inherits from <xref:System.ValueType>)</span></span>|<span data-ttu-id="9f32e-162">依赖于实现平台</span><span class="sxs-lookup"><span data-stu-id="9f32e-162">Depends on implementing platform</span></span>|<span data-ttu-id="9f32e-163">结构的每个成员都有一个由其数据类型确定的范围，并与其他成员的范围无关</span><span class="sxs-lookup"><span data-stu-id="9f32e-163">Each member of the structure has a range determined by its data type and independent of the ranges of the other members</span></span>|  
|[<span data-ttu-id="9f32e-164">UShort</span><span class="sxs-lookup"><span data-stu-id="9f32e-164">UShort</span></span>](ushort-data-type.md)|<xref:System.UInt16>|<span data-ttu-id="9f32e-165">2 个字节</span><span class="sxs-lookup"><span data-stu-id="9f32e-165">2 bytes</span></span>|<span data-ttu-id="9f32e-166">0到 65535 (无符号) </span><span class="sxs-lookup"><span data-stu-id="9f32e-166">0 through 65,535 (unsigned)</span></span>|  
  
 <span data-ttu-id="9f32e-167"><sup>†</sup> 使用 *科学记数法* 时，"E" 指的是10的幂。</span><span class="sxs-lookup"><span data-stu-id="9f32e-167"><sup>†</sup> In *scientific notation*, "E" refers to a power of 10.</span></span> <span data-ttu-id="9f32e-168">因此，3.56 E + 2 表示 3.56 x 10<sup>2</sup> 或356，3.56 e-2 表示 3.56/10<sup>2</sup> 或0.0356。</span><span class="sxs-lookup"><span data-stu-id="9f32e-168">So 3.56E+2 signifies 3.56 x 10<sup>2</sup> or 356, and 3.56E-2 signifies 3.56 / 10<sup>2</sup> or 0.0356.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9f32e-169">对于包含文本的字符串，请使用 <xref:Microsoft.VisualBasic.Strings.StrConv%2A> 函数从一种文本格式转换为另一种文本格式。</span><span class="sxs-lookup"><span data-stu-id="9f32e-169">For strings containing text, use the <xref:Microsoft.VisualBasic.Strings.StrConv%2A> function to convert from one text format to another.</span></span>  
  
 <span data-ttu-id="9f32e-170">除了在声明语句中指定数据类型之外，还可以使用类型字符强制某些编程元素的数据类型。</span><span class="sxs-lookup"><span data-stu-id="9f32e-170">In addition to specifying a data type in a declaration statement, you can force the data type of some programming elements by using a type character.</span></span> <span data-ttu-id="9f32e-171">请参阅 [类型字符](../../programming-guide/language-features/data-types/type-characters.md)。</span><span class="sxs-lookup"><span data-stu-id="9f32e-171">See [Type Characters](../../programming-guide/language-features/data-types/type-characters.md).</span></span>  
  
## <a name="memory-consumption"></a><span data-ttu-id="9f32e-172">内存消耗</span><span class="sxs-lookup"><span data-stu-id="9f32e-172">Memory Consumption</span></span>  

 <span data-ttu-id="9f32e-173">在声明基本数据类型时，不安全地假定其内存消耗与其名义存储分配相同。</span><span class="sxs-lookup"><span data-stu-id="9f32e-173">When you declare an elementary data type, it is not safe to assume that its memory consumption is the same as its nominal storage allocation.</span></span> <span data-ttu-id="9f32e-174">这是由于下列注意事项：</span><span class="sxs-lookup"><span data-stu-id="9f32e-174">This is due to the following considerations:</span></span>  
  
- <span data-ttu-id="9f32e-175">**存储分配。**</span><span class="sxs-lookup"><span data-stu-id="9f32e-175">**Storage Assignment.**</span></span> <span data-ttu-id="9f32e-176">公共语言运行时可以基于执行应用程序的平台的当前特性来分配存储空间。</span><span class="sxs-lookup"><span data-stu-id="9f32e-176">The common language runtime can assign storage based on the current characteristics of the platform on which your application is executing.</span></span> <span data-ttu-id="9f32e-177">如果内存几乎已满，则可能会将声明的元素尽可能紧密地打包在一起。</span><span class="sxs-lookup"><span data-stu-id="9f32e-177">If memory is nearly full, it might pack your declared elements as closely together as possible.</span></span> <span data-ttu-id="9f32e-178">在其他情况下，它可能会将内存地址与自然硬件边界对齐，以优化性能。</span><span class="sxs-lookup"><span data-stu-id="9f32e-178">In other cases it might align their memory addresses to natural hardware boundaries to optimize performance.</span></span>  
  
- <span data-ttu-id="9f32e-179">**平台宽度。**</span><span class="sxs-lookup"><span data-stu-id="9f32e-179">**Platform Width.**</span></span> <span data-ttu-id="9f32e-180">64位平台上的存储分配不同于32位平台上的分配。</span><span class="sxs-lookup"><span data-stu-id="9f32e-180">Storage assignment on a 64-bit platform is different from assignment on a 32-bit platform.</span></span>  
  
### <a name="composite-data-types"></a><span data-ttu-id="9f32e-181">复合数据类型</span><span class="sxs-lookup"><span data-stu-id="9f32e-181">Composite Data Types</span></span>  

 <span data-ttu-id="9f32e-182">相同的注意事项也适用于复合数据类型的每个成员，如结构或数组。</span><span class="sxs-lookup"><span data-stu-id="9f32e-182">The same considerations apply to each member of a composite data type, such as a structure or an array.</span></span> <span data-ttu-id="9f32e-183">你不能只是将类型成员的标称存储分配组合在一起。</span><span class="sxs-lookup"><span data-stu-id="9f32e-183">You cannot rely on simply adding together the nominal storage allocations of the type's members.</span></span> <span data-ttu-id="9f32e-184">此外，还有其他注意事项，如以下内容：</span><span class="sxs-lookup"><span data-stu-id="9f32e-184">Furthermore, there are other considerations, such as the following:</span></span>  
  
- <span data-ttu-id="9f32e-185">**费用.**</span><span class="sxs-lookup"><span data-stu-id="9f32e-185">**Overhead.**</span></span> <span data-ttu-id="9f32e-186">某些复合类型具有额外的内存需求。</span><span class="sxs-lookup"><span data-stu-id="9f32e-186">Some composite types have additional memory requirements.</span></span> <span data-ttu-id="9f32e-187">例如，数组对数组本身和每个维度使用额外的内存。</span><span class="sxs-lookup"><span data-stu-id="9f32e-187">For example, an array uses extra memory for the array itself and also for each dimension.</span></span> <span data-ttu-id="9f32e-188">在32位平台上，此开销目前为每个维度12个字节加上8个字节。</span><span class="sxs-lookup"><span data-stu-id="9f32e-188">On a 32-bit platform, this overhead is currently 12 bytes plus 8 bytes for each dimension.</span></span> <span data-ttu-id="9f32e-189">在64位平台上，此要求翻倍。</span><span class="sxs-lookup"><span data-stu-id="9f32e-189">On a 64-bit platform this requirement is doubled.</span></span>  
  
- <span data-ttu-id="9f32e-190">**存储布局。**</span><span class="sxs-lookup"><span data-stu-id="9f32e-190">**Storage Layout.**</span></span> <span data-ttu-id="9f32e-191">不能安全地假设内存中存储的顺序与声明顺序相同。</span><span class="sxs-lookup"><span data-stu-id="9f32e-191">You cannot safely assume that the order of storage in memory is the same as your order of declaration.</span></span> <span data-ttu-id="9f32e-192">甚至不能对字节对齐进行假设，如2字节或4字节边界。</span><span class="sxs-lookup"><span data-stu-id="9f32e-192">You cannot even make assumptions about byte alignment, such as a 2-byte or 4-byte boundary.</span></span> <span data-ttu-id="9f32e-193">如果要定义类或结构，并且需要控制其成员的存储布局，则可以将属性应用于 <xref:System.Runtime.InteropServices.StructLayoutAttribute> 类或结构。</span><span class="sxs-lookup"><span data-stu-id="9f32e-193">If you are defining a class or structure and you need to control the storage layout of its members, you can apply the <xref:System.Runtime.InteropServices.StructLayoutAttribute> attribute to the class or structure.</span></span>  
  
### <a name="object-overhead"></a><span data-ttu-id="9f32e-194">对象开销</span><span class="sxs-lookup"><span data-stu-id="9f32e-194">Object Overhead</span></span>  

 <span data-ttu-id="9f32e-195">`Object`除数据类型中包含的数据外，引用任何基本数据类型或复合数据类型的也使用4个字节。</span><span class="sxs-lookup"><span data-stu-id="9f32e-195">An `Object` referring to any elementary or composite data type uses 4 bytes in addition to the data contained in the data type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f32e-196">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f32e-196">See also</span></span>

- <xref:Microsoft.VisualBasic.Strings.StrConv%2A>
- <xref:System.Runtime.InteropServices.StructLayoutAttribute>
- [<span data-ttu-id="9f32e-197">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="9f32e-197">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="9f32e-198">转换摘要</span><span class="sxs-lookup"><span data-stu-id="9f32e-198">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="9f32e-199">类型字符</span><span class="sxs-lookup"><span data-stu-id="9f32e-199">Type Characters</span></span>](../../programming-guide/language-features/data-types/type-characters.md)
- [<span data-ttu-id="9f32e-200">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="9f32e-200">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
