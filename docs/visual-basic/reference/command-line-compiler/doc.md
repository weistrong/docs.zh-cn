---
description: 详细了解：-doc
title: -doc
ms.date: 03/10/2018
helpviewer_keywords:
- doc compiler option [Visual Basic]
- -doc compiler option [Visual Basic]
- /doc compiler option [Visual Basic]
ms.assetid: 5fc32ec9-a149-4648-994c-a8d0cccd0a65
ms.openlocfilehash: da1ff6ad133dd2f46484b61ff73e1c6159eae557
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100461419"
---
# <a name="-doc"></a><span data-ttu-id="fe35b-103">-doc</span><span class="sxs-lookup"><span data-stu-id="fe35b-103">-doc</span></span>

<span data-ttu-id="fe35b-104">将文档注释处理到一个 XML 文件中。</span><span class="sxs-lookup"><span data-stu-id="fe35b-104">Processes documentation comments to an XML file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe35b-105">语法</span><span class="sxs-lookup"><span data-stu-id="fe35b-105">Syntax</span></span>  
  
```console  
-doc[+ | -]  
```

<span data-ttu-id="fe35b-106">or</span><span class="sxs-lookup"><span data-stu-id="fe35b-106">or</span></span>  

```console
-doc:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="fe35b-107">自变量</span><span class="sxs-lookup"><span data-stu-id="fe35b-107">Arguments</span></span>  
  
|<span data-ttu-id="fe35b-108">术语</span><span class="sxs-lookup"><span data-stu-id="fe35b-108">Term</span></span>|<span data-ttu-id="fe35b-109">定义</span><span class="sxs-lookup"><span data-stu-id="fe35b-109">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="fe35b-110">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="fe35b-110">`+` &#124; `-`</span></span>|<span data-ttu-id="fe35b-111">可选。</span><span class="sxs-lookup"><span data-stu-id="fe35b-111">Optional.</span></span> <span data-ttu-id="fe35b-112">指定 + 或仅 `-doc` 会导致编译器生成文档信息并将其置于 XML 文件中。</span><span class="sxs-lookup"><span data-stu-id="fe35b-112">Specifying +, or just `-doc`, causes the compiler to generate documentation information and place it in an XML file.</span></span> <span data-ttu-id="fe35b-113">指定 `-` 相当于未指定 `-doc`，因此不会创建任何文档信息。</span><span class="sxs-lookup"><span data-stu-id="fe35b-113">Specifying `-` is the equivalent of not specifying `-doc`, causing no documentation information to be created.</span></span>|  
|`file`|<span data-ttu-id="fe35b-114">如果使用 `-doc:`，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="fe35b-114">Required if `-doc:` is used.</span></span> <span data-ttu-id="fe35b-115">指定输出 XML 文件（由编译的源代码文件中的注释填充）。</span><span class="sxs-lookup"><span data-stu-id="fe35b-115">Specifies the output XML file, which is populated with the comments from the source-code files of the compilation.</span></span> <span data-ttu-id="fe35b-116">如果文件名包含空格，请用引号 (" ") 括住该名称。</span><span class="sxs-lookup"><span data-stu-id="fe35b-116">If the file name contains a space, surround the name with quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe35b-117">备注</span><span class="sxs-lookup"><span data-stu-id="fe35b-117">Remarks</span></span>  

 <span data-ttu-id="fe35b-118">`-doc` 选项控制编译器是否生成包含文档注释的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="fe35b-118">The `-doc` option controls whether the compiler generates an XML file containing the documentation comments.</span></span> <span data-ttu-id="fe35b-119">如果使用 `-doc:file` 语法，`file` 参数会指定 XML 文件的名称。</span><span class="sxs-lookup"><span data-stu-id="fe35b-119">If you use the `-doc:file` syntax, the `file` parameter specifies the name of the XML file.</span></span> <span data-ttu-id="fe35b-120">如果使用 `-doc` 或 `-doc+`，编译器会从其正在创建的可执行文件或库中获取 XML 文件名。</span><span class="sxs-lookup"><span data-stu-id="fe35b-120">If you use `-doc` or `-doc+`, the compiler takes the XML file name from the executable file or library that the compiler is creating.</span></span> <span data-ttu-id="fe35b-121">如果使用 `-doc-` 或未指定 `-doc` 选项，则编译器不会创建 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="fe35b-121">If you use `-doc-` or do not specify the `-doc` option, the compiler does not create an XML file.</span></span>  
  
 <span data-ttu-id="fe35b-122">在源代码文件中，文档注释可先于以下定义：</span><span class="sxs-lookup"><span data-stu-id="fe35b-122">In source-code files, documentation comments can precede the following definitions:</span></span>  
  
- <span data-ttu-id="fe35b-123">用户定义类型，例如[类](../../language-reference/statements/class-statement.md)或[接口](../../language-reference/statements/interface-statement.md)</span><span class="sxs-lookup"><span data-stu-id="fe35b-123">User-defined types, such as a [class](../../language-reference/statements/class-statement.md) or [interface](../../language-reference/statements/interface-statement.md)</span></span>  
  
- <span data-ttu-id="fe35b-124">成员，例如字段、[事件](../../language-reference/statements/event-statement.md)、[属性](../../language-reference/statements/property-statement.md)、[函数](../../language-reference/statements/function-statement.md)或[子例程](../../language-reference/statements/sub-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="fe35b-124">Members, such as a field, [event](../../language-reference/statements/event-statement.md), [property](../../language-reference/statements/property-statement.md), [function](../../language-reference/statements/function-statement.md), or [subroutine](../../language-reference/statements/sub-statement.md).</span></span>  
  
 <span data-ttu-id="fe35b-125">若要将生成的 XML 文件与 Visual Studio [IntelliSense](/visualstudio/ide/using-intellisense) 功能配合使用，请将 XML 文件的文件名设为与要支持的程序集相同的名称。</span><span class="sxs-lookup"><span data-stu-id="fe35b-125">To use the generated XML file with the Visual Studio [IntelliSense](/visualstudio/ide/using-intellisense) feature, let the file name of the XML file be the same as the assembly you want to support.</span></span> <span data-ttu-id="fe35b-126">确保 XML 文件与程序集位于同一目录中，以便在 Visual Studio 项目中引用此程序集时，也可以找到 .xml 文件。</span><span class="sxs-lookup"><span data-stu-id="fe35b-126">Make sure the XML file is in the same directory as the assembly so that when the assembly is referenced in the Visual Studio project, the .xml file is found as well.</span></span> <span data-ttu-id="fe35b-127">IntelliSense 不需要 XML 文档文件来处理项目内或项目引用的项目中的代码。</span><span class="sxs-lookup"><span data-stu-id="fe35b-127">XML documentation files are not required for IntelliSense to work for code within a project or within projects referenced by a project.</span></span>  
  
 <span data-ttu-id="fe35b-128">除非使用 `-target:module` 进行编译，否则 XML 文件包含标记 `<assembly></assembly>`。</span><span class="sxs-lookup"><span data-stu-id="fe35b-128">Unless you compile with `-target:module`, the XML file contains the tags `<assembly></assembly>`.</span></span> <span data-ttu-id="fe35b-129">这些标记指定包含编译输出文件的程序集清单的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="fe35b-129">These tags specify the name of the file containing the assembly manifest for the output file of the compilation.</span></span>  
  
 <span data-ttu-id="fe35b-130">有关从代码中的注释生成文档的方法，请参阅 [XML 注释标记](../../language-reference/xmldoc/index.md)。</span><span class="sxs-lookup"><span data-stu-id="fe35b-130">See [XML Comment Tags](../../language-reference/xmldoc/index.md) for ways to generate documentation from comments in your code.</span></span>  
  
|<span data-ttu-id="fe35b-131">在 Visual Studio 集成开发环境中设置 -doc</span><span class="sxs-lookup"><span data-stu-id="fe35b-131">To set -doc in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="fe35b-132">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="fe35b-132">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="fe35b-133">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="fe35b-133">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="fe35b-134">2.单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="fe35b-134">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="fe35b-135">3.在“生成 XML 文档文件”  框中设置值。</span><span class="sxs-lookup"><span data-stu-id="fe35b-135">3.  Set the value in the **Generate XML documentation file** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fe35b-136">示例</span><span class="sxs-lookup"><span data-stu-id="fe35b-136">Example</span></span>  

 <span data-ttu-id="fe35b-137">有关示例，请参阅[使用 XML 来记录代码](../../programming-guide/program-structure/documenting-your-code-with-xml.md)。</span><span class="sxs-lookup"><span data-stu-id="fe35b-137">See [Documenting Your Code with XML](../../programming-guide/program-structure/documenting-your-code-with-xml.md) for a sample.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe35b-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="fe35b-138">See also</span></span>

- [<span data-ttu-id="fe35b-139">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="fe35b-139">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="fe35b-140">使用 XML 记录代码</span><span class="sxs-lookup"><span data-stu-id="fe35b-140">Documenting Your Code with XML</span></span>](../../programming-guide/program-structure/documenting-your-code-with-xml.md)
