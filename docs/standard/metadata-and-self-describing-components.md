---
description: 详细了解：元数据和自描述组件
title: 元数据和自描述组件
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- runtime, metadata
- languages, interoperability
- portable executable files, metadata
- self-describing files
- metadata, about metadata
- common language runtime, metadata
- PE files, metadata
- components [.NET], metadata
ms.assetid: 3dd13c5d-a508-455b-8dce-0a852882a5a7
ms.openlocfilehash: 5f043a1e204c019f83fb15705ca44562a82ad6a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99702205"
---
# <a name="metadata-and-self-describing-components"></a><span data-ttu-id="d1ee7-103">元数据和自描述组件</span><span class="sxs-lookup"><span data-stu-id="d1ee7-103">Metadata and Self-Describing Components</span></span>

<span data-ttu-id="d1ee7-104">在过去，以一种语言编写的软件组件（.exe 或 .dll）不能方便地使用以另一种语言编写的软件组件。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-104">In the past, a software component (.exe or .dll) that was written in one language could not easily use a software component that was written in another language.</span></span> <span data-ttu-id="d1ee7-105">在这个问题的解决上，COM 向前迈进了一步。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-105">COM provided a step towards solving this problem.</span></span> <span data-ttu-id="d1ee7-106">.NET 允许编译器向所有的模块和程序集发出附加的说明性信息，从而使组件互用更加简单。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-106">.NET makes component interoperation even easier by allowing compilers to emit additional declarative information into all modules and assemblies.</span></span> <span data-ttu-id="d1ee7-107">这种叫做“元数据”的信息有助于组件无缝交互。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-107">This information, called metadata, helps components to interact seamlessly.</span></span>

 <span data-ttu-id="d1ee7-108">元数据是一种二进制信息，用以对存储在公共语言运行时可迁移可执行文件 (PE) 文件或存储在内存中的程序进行描述。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-108">Metadata is binary information describing your program that is stored either in a common language runtime portable executable (PE) file or in memory.</span></span> <span data-ttu-id="d1ee7-109">将您的代码编译为 PE 文件时，便会将元数据插入到该文件的一部分中，而将代码转换为 Microsoft 中间语言 (MSIL) 并将其插入到该文件的另一部分中。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-109">When you compile your code into a PE file, metadata is inserted into one portion of the file, and your code is converted to Microsoft intermediate language (MSIL) and inserted into another portion of the file.</span></span> <span data-ttu-id="d1ee7-110">在模块或程序集中定义和引用的每个类型和成员都将在元数据中进行说明。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-110">Every type and member that is defined and referenced in a module or assembly is described within metadata.</span></span> <span data-ttu-id="d1ee7-111">当执行代码时，运行时将元数据加载到内存中，并引用它来发现有关代码的类、成员、继承等信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-111">When code is executed, the runtime loads metadata into memory and references it to discover information about your code's classes, members, inheritance, and so on.</span></span>

 <span data-ttu-id="d1ee7-112">元数据以非特定语言的方式描述在代码中定义的每一类型和成员。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-112">Metadata describes every type and member defined in your code in a language-neutral manner.</span></span> <span data-ttu-id="d1ee7-113">元数据存储以下信息：</span><span class="sxs-lookup"><span data-stu-id="d1ee7-113">Metadata stores the following information:</span></span>

- <span data-ttu-id="d1ee7-114">程序集的说明。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-114">Description of the assembly.</span></span>

  - <span data-ttu-id="d1ee7-115">标识（名称、版本、区域性、公钥）。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-115">Identity (name, version, culture, public key).</span></span>

  - <span data-ttu-id="d1ee7-116">导出的类型。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-116">The types that are exported.</span></span>

  - <span data-ttu-id="d1ee7-117">该程序集所依赖的其他程序集。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-117">Other assemblies that this assembly depends on.</span></span>

  - <span data-ttu-id="d1ee7-118">运行所需的安全权限。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-118">Security permissions needed to run.</span></span>

- <span data-ttu-id="d1ee7-119">类型的说明。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-119">Description of types.</span></span>

  - <span data-ttu-id="d1ee7-120">名称、可见性、基类和实现的接口。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-120">Name, visibility, base class, and interfaces implemented.</span></span>

  - <span data-ttu-id="d1ee7-121">成员（方法、字段、属性、事件、嵌套的类型）。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-121">Members (methods, fields, properties, events, nested types).</span></span>

- <span data-ttu-id="d1ee7-122">特性。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-122">Attributes.</span></span>

  - <span data-ttu-id="d1ee7-123">修饰类型和成员的其他说明性元素。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-123">Additional descriptive elements that modify types and members.</span></span>

## <a name="benefits-of-metadata"></a><span data-ttu-id="d1ee7-124">元数据的优点</span><span class="sxs-lookup"><span data-stu-id="d1ee7-124">Benefits of Metadata</span></span>

<span data-ttu-id="d1ee7-125">对于一种更简单的编程模型来说，元数据是关键，该模型不再需要接口定义语言 (IDL) 文件、头文件或任何外部组件引用方法。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-125">Metadata is the key to a simpler programming model, and eliminates the need for Interface Definition Language (IDL) files, header files, or any external method of component reference.</span></span> <span data-ttu-id="d1ee7-126">元数据使 .NET 语言能够自动以非特定语言的方式对其自身进行描述，而这是开发人员和用户都无法看见的。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-126">Metadata enables .NET languages to describe themselves automatically in a language-neutral manner, unseen by both the developer and the user.</span></span> <span data-ttu-id="d1ee7-127">另外，通过使用特性，可以对元数据进行扩展。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-127">Additionally, metadata is extensible through the use of attributes.</span></span> <span data-ttu-id="d1ee7-128">元数据具有以下主要优点：</span><span class="sxs-lookup"><span data-stu-id="d1ee7-128">Metadata provides the following major benefits:</span></span>

- <span data-ttu-id="d1ee7-129">自描述文件。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-129">Self-describing files.</span></span>

  <span data-ttu-id="d1ee7-130">公共语言运行时模块和程序集是自描述的。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-130">Common language runtime modules and assemblies are self-describing.</span></span> <span data-ttu-id="d1ee7-131">模块的元数据包含与另一个模块进行交互所需的全部信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-131">A module's metadata contains everything needed to interact with another module.</span></span> <span data-ttu-id="d1ee7-132">元数据自动提供 COM 中 IDL 的功能，因此可以将一个文件同时用于定义和实现。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-132">Metadata automatically provides the functionality of IDL in COM, so you can use one file for both definition and implementation.</span></span> <span data-ttu-id="d1ee7-133">运行时模块和程序集甚至不需要向操作系统注册。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-133">Runtime modules and assemblies do not even require registration with the operating system.</span></span> <span data-ttu-id="d1ee7-134">结果，运行时使用的说明始终反映编译文件中的实际代码，从而提高应用程序的可靠性。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-134">As a result, the descriptions used by the runtime always reflect the actual code in your compiled file, which increases application reliability.</span></span>

- <span data-ttu-id="d1ee7-135">语言互用性和更简单的基于组件的设计。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-135">Language interoperability and easier component-based design.</span></span>

  <span data-ttu-id="d1ee7-136">元数据提供所有必需的有关已编译代码的信息，以供你从用不同语言编写的 PE 文件中继承类。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-136">Metadata provides all the information required about compiled code for you to inherit a class from a PE file written in a different language.</span></span> <span data-ttu-id="d1ee7-137">你可以创建用任何托管语言（任何面向公共语言运行时的语言）编写的任何类的实例，而不用担心显式封送处理或使用自定义的互用代码。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-137">You can create an instance of any class written in any managed language (any language that targets the common language runtime) without worrying about explicit marshaling or using custom interoperability code.</span></span>

- <span data-ttu-id="d1ee7-138">特性。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-138">Attributes.</span></span>

  <span data-ttu-id="d1ee7-139">.NET 允许在编译文件中声明特定种类的元数据（称为特性）。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-139">.NET lets you declare specific kinds of metadata, called attributes, in your compiled file.</span></span> <span data-ttu-id="d1ee7-140">特性在 .NET 中处处可见，用于更精确地控制程序在运行时的行为。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-140">Attributes can be found throughout .NET and are used to control in more detail how your program behaves at run time.</span></span> <span data-ttu-id="d1ee7-141">另外，还可以通过用户定义的自定义特性，向 .NET 文件发出自己的自定义元数据。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-141">Additionally, you can emit your own custom metadata into .NET files through user-defined custom attributes.</span></span> <span data-ttu-id="d1ee7-142">有关更多信息，请参阅[特性](attributes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-142">For more information, see [Attributes](attributes/index.md).</span></span>

## <a name="metadata-and-the-pe-file-structure"></a><span data-ttu-id="d1ee7-143">元数据和 PE 文件结构</span><span class="sxs-lookup"><span data-stu-id="d1ee7-143">Metadata and the PE File Structure</span></span>

<span data-ttu-id="d1ee7-144">元数据存储在 .NET 可迁移可执行文件 (PE) 文件的一个部分中，而 Microsoft 中间语言 (MSIL) 则存储在 PE 文件的另一部分中。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-144">Metadata is stored in one section of a .NET portable executable (PE) file, while Microsoft intermediate language (MSIL) is stored in another section of the PE file.</span></span> <span data-ttu-id="d1ee7-145">文件的元数据部分包含一系列的表和堆数据结构。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-145">The metadata portion of the file contains a series of table and heap data structures.</span></span> <span data-ttu-id="d1ee7-146">MSIL 部分包含 MSIL 和引用 PE 文件元数据部分的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-146">The MSIL portion contains MSIL and metadata tokens that reference the metadata portion of the PE file.</span></span> <span data-ttu-id="d1ee7-147">例如，使用 [MSIL 反汇编程序 (Ildasm.exe)](../framework/tools/ildasm-exe-il-disassembler.md) 等工具查看代码的 MSIL 时，可能会遇到元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-147">You might encounter metadata tokens when you use tools such as the [MSIL Disassembler (Ildasm.exe)](../framework/tools/ildasm-exe-il-disassembler.md) to view your code's MSIL, for example.</span></span>

### <a name="metadata-tables-and-heaps"></a><span data-ttu-id="d1ee7-148">元数据表和堆</span><span class="sxs-lookup"><span data-stu-id="d1ee7-148">Metadata Tables and Heaps</span></span>

<span data-ttu-id="d1ee7-149">每个元数据表都保留有关程序元素的信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-149">Each metadata table holds information about the elements of your program.</span></span> <span data-ttu-id="d1ee7-150">例如，一个元数据表说明代码中的类，另一个元数据表说明字段等。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-150">For example, one metadata table describes the classes in your code, another table describes the fields, and so on.</span></span> <span data-ttu-id="d1ee7-151">如果你的代码中有 10 个类，类表将有 10 行，每行一类。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-151">If you have ten classes in your code, the class table will have tens rows, one for each class.</span></span> <span data-ttu-id="d1ee7-152">元数据表引用其他的表和堆。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-152">Metadata tables reference other tables and heaps.</span></span> <span data-ttu-id="d1ee7-153">例如，类的元数据表引用方法表。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-153">For example, the metadata table for classes references the table for methods.</span></span>

<span data-ttu-id="d1ee7-154">元数据还以四种堆结构存储信息：字符串、Blob、用户字符串和 GUID。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-154">Metadata also stores information in four heap structures: string, blob, user string, and GUID.</span></span> <span data-ttu-id="d1ee7-155">所有用于对类型和成员进行命名的字符串都存储在字符串堆中。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-155">All the strings used to name types and members are stored in the string heap.</span></span> <span data-ttu-id="d1ee7-156">例如，方法表不直接存储特定方法的名称，而是指向存储在字符串堆中的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-156">For example, a method table does not directly store the name of a particular method, but points to the method's name stored in the string heap.</span></span>

### <a name="metadata-tokens"></a><span data-ttu-id="d1ee7-157">元数据标记</span><span class="sxs-lookup"><span data-stu-id="d1ee7-157">Metadata Tokens</span></span>

<span data-ttu-id="d1ee7-158">元数据标记在 PE 文件的 MSIL 部分中唯一确定每个元数据表的每一行。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-158">Each row of each metadata table is uniquely identified in the MSIL portion of the PE file by a metadata token.</span></span> <span data-ttu-id="d1ee7-159">元数据标记在概念上和指针相似，永久驻留在 MSIL 中，引用特定的元数据表。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-159">Metadata tokens are conceptually similar to pointers, persisted in MSIL, that reference a particular metadata table.</span></span>

<span data-ttu-id="d1ee7-160">元数据标记是一个四个字节的数字。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-160">A metadata token is a four-byte number.</span></span> <span data-ttu-id="d1ee7-161">最高位字节表示特定标记（方法、类型等）引用的元数据表。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-161">The top byte denotes the metadata table to which a particular token refers (method, type, and so on).</span></span> <span data-ttu-id="d1ee7-162">剩下的三个字节指定与所说明的编程元素对应的元数据表中的行。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-162">The remaining three bytes specify the row in the metadata table that corresponds to the programming element being described.</span></span> <span data-ttu-id="d1ee7-163">如果您用 C# 定义一个方法并将其编译到 PE 文件，下面的元数据标记可能存在于 PE 文件的 MSIL 部分：</span><span class="sxs-lookup"><span data-stu-id="d1ee7-163">If you define a method in C# and compile it into a PE file, the following metadata token might exist in the MSIL portion of the PE file:</span></span>

`0x06000004`

<span data-ttu-id="d1ee7-164">最高位字节 (`0x06`) 表示这是一个 MethodDef  标记。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-164">The top byte (`0x06`) indicates that this is a **MethodDef** token.</span></span> <span data-ttu-id="d1ee7-165">低位的三个字节 (`000004`) 指示公共语言运行时在 MethodDef  表的第四行查找对该方法定义进行描述的信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-165">The lower three bytes (`000004`) tells the common language runtime to look in the fourth row of the **MethodDef** table for the information that describes this method definition.</span></span>

### <a name="metadata-within-a-pe-file"></a><span data-ttu-id="d1ee7-166">PE 文件中的元数据</span><span class="sxs-lookup"><span data-stu-id="d1ee7-166">Metadata within a PE File</span></span>

<span data-ttu-id="d1ee7-167">当为公共语言运行时编译程序时，该程序转换为由三部分组成的 PE 文件。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-167">When a program is compiled for the common language runtime, it is converted to a PE file that consists of three parts.</span></span> <span data-ttu-id="d1ee7-168">下表说明了每部分的内容。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-168">The following table describes the contents of each part.</span></span>

|<span data-ttu-id="d1ee7-169">PE 部分</span><span class="sxs-lookup"><span data-stu-id="d1ee7-169">PE section</span></span>|<span data-ttu-id="d1ee7-170">PE 部分的内容</span><span class="sxs-lookup"><span data-stu-id="d1ee7-170">Contents of PE section</span></span>|
|----------------|----------------------------|
|<span data-ttu-id="d1ee7-171">PE 头</span><span class="sxs-lookup"><span data-stu-id="d1ee7-171">PE header</span></span>|<span data-ttu-id="d1ee7-172">PE 文件主要部分的索引和入口点的地址。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-172">The index of the PE file's main sections and the address of the entry point.</span></span><br /><br /> <span data-ttu-id="d1ee7-173">运行时使用该信息确定该文件为 PE 文件并确定当将程序加载到内存时执行从何处开始。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-173">The runtime uses this information to identify the file as a PE file and to determine where execution starts when loading the program into memory.</span></span>|
|<span data-ttu-id="d1ee7-174">MSIL 指令</span><span class="sxs-lookup"><span data-stu-id="d1ee7-174">MSIL instructions</span></span>|<span data-ttu-id="d1ee7-175">组成代码的 Microsoft 中间语言指令 (MSIL)。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-175">The Microsoft intermediate language instructions (MSIL) that make up your code.</span></span> <span data-ttu-id="d1ee7-176">许多 MSIL 指令带有元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-176">Many MSIL instructions are accompanied by metadata tokens.</span></span>|
|<span data-ttu-id="d1ee7-177">元数据</span><span class="sxs-lookup"><span data-stu-id="d1ee7-177">Metadata</span></span>|<span data-ttu-id="d1ee7-178">元数据表和堆。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-178">Metadata tables and heaps.</span></span> <span data-ttu-id="d1ee7-179">运行时使用该部分记录您的代码中每个类型和成员的信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-179">The runtime uses this section to record information about every type and member in your code.</span></span> <span data-ttu-id="d1ee7-180">本部分还包括自定义特性和安全性信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-180">This section also includes custom attributes and security information.</span></span>|

## <a name="run-time-use-of-metadata"></a><span data-ttu-id="d1ee7-181">元数据在运行时的作用</span><span class="sxs-lookup"><span data-stu-id="d1ee7-181">Run-Time Use of Metadata</span></span>

<span data-ttu-id="d1ee7-182">要更好地理解元数据和它在公共语言运行时中的作用，构造一个简单的程序并说明元数据如何影响它的运行时情况可能很有帮助。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-182">To better understand metadata and its role in the common language runtime, it might be helpful to construct a simple program and illustrate how metadata affects its run-time life.</span></span> <span data-ttu-id="d1ee7-183">下面的代码示例显示名为 `MyApp` 的类中的两种方法。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-183">The following code example shows two methods inside a class called `MyApp`.</span></span> <span data-ttu-id="d1ee7-184">`Main` 方法是程序入口点，而 `Add` 方法只返回两个整数参数的和。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-184">The `Main` method is the program entry point, while the `Add` method simply returns the sum of two integer arguments.</span></span>

```vb
Public Class MyApp
   Public Shared Sub Main()
      Dim ValueOne As Integer = 10
      Dim ValueTwo As Integer = 20
      Console.WriteLine("The Value is: {0}", Add(ValueOne, ValueTwo))
   End Sub

   Public Shared Function Add(One As Integer, Two As Integer) As Integer
      Return (One + Two)
   End Function
End Class
```

```csharp
using System;
public class MyApp
{
   public static int Main()
   {
      int ValueOne = 10;
      int ValueTwo = 20;
      Console.WriteLine("The Value is: {0}", Add(ValueOne, ValueTwo));
      return 0;
   }
   public static int Add(int One, int Two)
   {
      return (One + Two);
   }
}
```

<span data-ttu-id="d1ee7-185">当代码运行时，运行时将模块加载到内存并向元数据咨询该类的信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-185">When the code runs, the runtime loads the module into memory and consults the metadata for this class.</span></span> <span data-ttu-id="d1ee7-186">加载后，运行时对方法的 Microsoft 中间语言 (MSIL) 流执行广泛的分析，将其转换为快速本机指令。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-186">Once loaded, the runtime performs extensive analysis of the method's Microsoft intermediate language (MSIL) stream to convert it to fast native machine instructions.</span></span> <span data-ttu-id="d1ee7-187">运行时根据需要使用实时 (JIT) 编译器将 MSIL 指令转换为本机代码，每次转换一个方法。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-187">The runtime uses a just-in-time (JIT) compiler to convert the MSIL instructions to native machine code one method at a time as needed.</span></span>

<span data-ttu-id="d1ee7-188">下面的示例显示了从以前代码的 `Main` 功能生成的部分 MSIL。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-188">The following example shows part of the MSIL produced from the previous code's `Main` function.</span></span> <span data-ttu-id="d1ee7-189">可使用 [MSIL 反汇编程序 (Ildasm.exe)](../framework/tools/ildasm-exe-il-disassembler.md) 从任何 .NET 应用程序中查看 MSIL 和元数据。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-189">You can view the MSIL and metadata from any .NET application using the [MSIL Disassembler (Ildasm.exe)](../framework/tools/ildasm-exe-il-disassembler.md).</span></span>

```console
.entrypoint
.maxstack  3
.locals ([0] int32 ValueOne,
         [1] int32 ValueTwo,
         [2] int32 V_2,
         [3] int32 V_3)
IL_0000:  ldc.i4.s   10
IL_0002:  stloc.0
IL_0003:  ldc.i4.s   20
IL_0005:  stloc.1
IL_0006:  ldstr      "The Value is: {0}"
IL_000b:  ldloc.0
IL_000c:  ldloc.1
IL_000d:  call int32 ConsoleApplication.MyApp::Add(int32,int32) /* 06000003 */
```

<span data-ttu-id="d1ee7-190">JIT 编译器读取整个方法的 MSIL，对其进行彻底地分析，然后为该方法生成有效的本机指令。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-190">The JIT compiler reads the MSIL for the whole method, analyzes it thoroughly, and generates efficient native instructions for the method.</span></span> <span data-ttu-id="d1ee7-191">在 `IL_000d` 遇到 `Add` 方法 (`/*` `06000003 */`) 的元数据标记，运行时使用该标记参考 MethodDef 表的第三行  。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-191">At `IL_000d`, a metadata token for the `Add` method (`/*` `06000003 */`) is encountered and the runtime uses the token to consult the third row of the **MethodDef** table.</span></span>

<span data-ttu-id="d1ee7-192">下表显示了说明  **方法的元数据标记所引用的 MethodDef**`Add` 表的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-192">The following table shows part of the **MethodDef** table referenced by the metadata token that describes the `Add` method.</span></span> <span data-ttu-id="d1ee7-193">虽然程序集中存在其他元数据表并具有它们自己唯一的值，但这里只讨论该表。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-193">While other metadata tables exist in this assembly and have their own unique values, only this table is discussed.</span></span>

|<span data-ttu-id="d1ee7-194">行</span><span class="sxs-lookup"><span data-stu-id="d1ee7-194">Row</span></span>|<span data-ttu-id="d1ee7-195">相对虚拟地址 (RVA)</span><span class="sxs-lookup"><span data-stu-id="d1ee7-195">Relative Virtual Address (RVA)</span></span>|<span data-ttu-id="d1ee7-196">ImplFlags</span><span class="sxs-lookup"><span data-stu-id="d1ee7-196">ImplFlags</span></span>|<span data-ttu-id="d1ee7-197">Flags</span><span class="sxs-lookup"><span data-stu-id="d1ee7-197">Flags</span></span>|<span data-ttu-id="d1ee7-198">“属性”</span><span class="sxs-lookup"><span data-stu-id="d1ee7-198">Name</span></span><br /><br /> <span data-ttu-id="d1ee7-199">（指向字符串堆。）</span><span class="sxs-lookup"><span data-stu-id="d1ee7-199">(Points to string heap.)</span></span>|<span data-ttu-id="d1ee7-200">Signature（指向 Blob 堆）</span><span class="sxs-lookup"><span data-stu-id="d1ee7-200">Signature (Points to blob heap.)</span></span>|
|---------|--------------------------------------|---------------|-----------|-----------------------------------------|----------------------------------------|
|<span data-ttu-id="d1ee7-201">1</span><span class="sxs-lookup"><span data-stu-id="d1ee7-201">1</span></span>|<span data-ttu-id="d1ee7-202">0x00002050</span><span class="sxs-lookup"><span data-stu-id="d1ee7-202">0x00002050</span></span>|<span data-ttu-id="d1ee7-203">IL</span><span class="sxs-lookup"><span data-stu-id="d1ee7-203">IL</span></span><br /><br /> <span data-ttu-id="d1ee7-204">Managed</span><span class="sxs-lookup"><span data-stu-id="d1ee7-204">Managed</span></span>|<span data-ttu-id="d1ee7-205">Public</span><span class="sxs-lookup"><span data-stu-id="d1ee7-205">Public</span></span><br /><br /> <span data-ttu-id="d1ee7-206">ReuseSlot</span><span class="sxs-lookup"><span data-stu-id="d1ee7-206">ReuseSlot</span></span><br /><br /> <span data-ttu-id="d1ee7-207">SpecialName</span><span class="sxs-lookup"><span data-stu-id="d1ee7-207">SpecialName</span></span><br /><br /> <span data-ttu-id="d1ee7-208">RTSpecialName</span><span class="sxs-lookup"><span data-stu-id="d1ee7-208">RTSpecialName</span></span><br /><br /> <span data-ttu-id="d1ee7-209">.ctor</span><span class="sxs-lookup"><span data-stu-id="d1ee7-209">.ctor</span></span>|<span data-ttu-id="d1ee7-210">.ctor（构造函数）</span><span class="sxs-lookup"><span data-stu-id="d1ee7-210">.ctor (constructor)</span></span>||
|<span data-ttu-id="d1ee7-211">2</span><span class="sxs-lookup"><span data-stu-id="d1ee7-211">2</span></span>|<span data-ttu-id="d1ee7-212">0x00002058</span><span class="sxs-lookup"><span data-stu-id="d1ee7-212">0x00002058</span></span>|<span data-ttu-id="d1ee7-213">IL</span><span class="sxs-lookup"><span data-stu-id="d1ee7-213">IL</span></span><br /><br /> <span data-ttu-id="d1ee7-214">Managed</span><span class="sxs-lookup"><span data-stu-id="d1ee7-214">Managed</span></span>|<span data-ttu-id="d1ee7-215">Public</span><span class="sxs-lookup"><span data-stu-id="d1ee7-215">Public</span></span><br /><br /> <span data-ttu-id="d1ee7-216">Static</span><span class="sxs-lookup"><span data-stu-id="d1ee7-216">Static</span></span><br /><br /> <span data-ttu-id="d1ee7-217">ReuseSlot</span><span class="sxs-lookup"><span data-stu-id="d1ee7-217">ReuseSlot</span></span>|<span data-ttu-id="d1ee7-218">Main</span><span class="sxs-lookup"><span data-stu-id="d1ee7-218">Main</span></span>|<span data-ttu-id="d1ee7-219">String</span><span class="sxs-lookup"><span data-stu-id="d1ee7-219">String</span></span>|
|<span data-ttu-id="d1ee7-220">3</span><span class="sxs-lookup"><span data-stu-id="d1ee7-220">3</span></span>|<span data-ttu-id="d1ee7-221">0x0000208c</span><span class="sxs-lookup"><span data-stu-id="d1ee7-221">0x0000208c</span></span>|<span data-ttu-id="d1ee7-222">IL</span><span class="sxs-lookup"><span data-stu-id="d1ee7-222">IL</span></span><br /><br /> <span data-ttu-id="d1ee7-223">Managed</span><span class="sxs-lookup"><span data-stu-id="d1ee7-223">Managed</span></span>|<span data-ttu-id="d1ee7-224">Public</span><span class="sxs-lookup"><span data-stu-id="d1ee7-224">Public</span></span><br /><br /> <span data-ttu-id="d1ee7-225">Static</span><span class="sxs-lookup"><span data-stu-id="d1ee7-225">Static</span></span><br /><br /> <span data-ttu-id="d1ee7-226">ReuseSlot</span><span class="sxs-lookup"><span data-stu-id="d1ee7-226">ReuseSlot</span></span>|<span data-ttu-id="d1ee7-227">添加</span><span class="sxs-lookup"><span data-stu-id="d1ee7-227">Add</span></span>|<span data-ttu-id="d1ee7-228">int, int, int</span><span class="sxs-lookup"><span data-stu-id="d1ee7-228">int, int, int</span></span>|

<span data-ttu-id="d1ee7-229">该表的每一列都包含有关代码的重要信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-229">Each column of the table contains important information about your code.</span></span> <span data-ttu-id="d1ee7-230">RVA  列允许运行时计算定义此方法的 MSIL 的起始内存地址。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-230">The **RVA** column allows the runtime to calculate the starting memory address of the MSIL that defines this method.</span></span> <span data-ttu-id="d1ee7-231">ImplFlags  和 Flags  列包含说明该方法的位屏蔽（例如，该方法是公共的还是私有的）。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-231">The **ImplFlags** and **Flags** columns contain bitmasks that describe the method (for example, whether the method is public or private).</span></span> <span data-ttu-id="d1ee7-232">Name  列对来自字符串堆的方法的名称进行了索引。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-232">The **Name** column indexes the name of the method from the string heap.</span></span> <span data-ttu-id="d1ee7-233">Signature  列对在 Blob 堆中的方法签名的定义进行了索引。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-233">The **Signature** column indexes the definition of the method's signature in the blob heap.</span></span>

<span data-ttu-id="d1ee7-234">运行时在第三行的 RVA  列计算所需的偏移量地址并将该地址返回到 JIT 编译器，然后，JIT 编译器进入新地址。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-234">The runtime calculates the desired offset address from the **RVA** column in the third row and returns this address to the JIT compiler, which then proceeds to the new address.</span></span> <span data-ttu-id="d1ee7-235">JIT 编译器继续在新地址处理 MSIL，直到它遇到另一个元数据标记，之后，重复该过程。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-235">The JIT compiler continues to process MSIL at the new address until it encounters another metadata token and the process is repeated.</span></span>

<span data-ttu-id="d1ee7-236">使用元数据，运行时可以访问加载代码并将其处理为本机指令所需的所有信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-236">Using metadata, the runtime has access to all the information it needs to load your code and process it into native machine instructions.</span></span> <span data-ttu-id="d1ee7-237">以这种方式，元数据使自描述文件、常规类型系统和跨语言继承成为可能。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-237">In this manner, metadata enables self-describing files and, together with the common type system, cross-language inheritance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1ee7-238">相关主题</span><span class="sxs-lookup"><span data-stu-id="d1ee7-238">Related Topics</span></span>

|<span data-ttu-id="d1ee7-239">Title</span><span class="sxs-lookup"><span data-stu-id="d1ee7-239">Title</span></span>|<span data-ttu-id="d1ee7-240">描述</span><span class="sxs-lookup"><span data-stu-id="d1ee7-240">Description</span></span>|
|-----------|-----------------|
|[<span data-ttu-id="d1ee7-241">特性</span><span class="sxs-lookup"><span data-stu-id="d1ee7-241">Attributes</span></span>](attributes/index.md)|<span data-ttu-id="d1ee7-242">描述如何应用特性、编写自定义特性及检索存储在特性中的信息。</span><span class="sxs-lookup"><span data-stu-id="d1ee7-242">Describes how to apply attributes, write custom attributes, and retrieve information that is stored in attributes.</span></span>|
