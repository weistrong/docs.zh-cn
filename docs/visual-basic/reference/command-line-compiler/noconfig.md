---
description: 详细了解：-noconfig
title: -noconfig
ms.date: 03/13/2018
helpviewer_keywords:
- noconfig compiler option [Visual Basic]
- -noconfig compiler option [Visual Basic]
- /noconfig compiler option [Visual Basic]
ms.assetid: a7405067-bd21-4171-adf4-a126fa3ad6c3
ms.openlocfilehash: e97d44427b537e73a404a47d30db202e2c3b1f41
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481683"
---
# <a name="-noconfig"></a><span data-ttu-id="82e73-103">-noconfig</span><span class="sxs-lookup"><span data-stu-id="82e73-103">-noconfig</span></span>

<span data-ttu-id="82e73-104">指定编译器不应自动引用常用 .NET Framework 程序集，也不应导入 `System` 和 `Microsoft.VisualBasic` 命名空间。</span><span class="sxs-lookup"><span data-stu-id="82e73-104">Specifies that the compiler should not automatically reference the commonly used .NET Framework assemblies or import the `System` and `Microsoft.VisualBasic` namespaces.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82e73-105">语法</span><span class="sxs-lookup"><span data-stu-id="82e73-105">Syntax</span></span>  
  
```console  
-noconfig  
```  
  
## <a name="remarks"></a><span data-ttu-id="82e73-106">备注</span><span class="sxs-lookup"><span data-stu-id="82e73-106">Remarks</span></span>  

 <span data-ttu-id="82e73-107">`-noconfig` 选项告知编译器不要在 Vbc.rsp 文件中编译，该文件与 Vbc.exe 文件位于同一目录。</span><span class="sxs-lookup"><span data-stu-id="82e73-107">The `-noconfig` option tells the compiler not to compile with the Vbc.rsp file, which is located in the same directory as the Vbc.exe file.</span></span> <span data-ttu-id="82e73-108">Vbc.rsp 文件引用常用的 .NET Framework 程序集，并导入 `System` 和 `Microsoft.VisualBasic` 命名空间。</span><span class="sxs-lookup"><span data-stu-id="82e73-108">The Vbc.rsp file references the commonly used .NET Framework assemblies and imports the `System` and `Microsoft.VisualBasic` namespaces.</span></span> <span data-ttu-id="82e73-109">除非指定 `-nostdlib` 选项，否则编译器将隐式引用 System.dll 程序集。</span><span class="sxs-lookup"><span data-stu-id="82e73-109">The compiler implicitly references the System.dll assembly unless the `-nostdlib` option is specified.</span></span> <span data-ttu-id="82e73-110">`-nostdlib` 选项指示编译器不要在 Vbc.rsp 中编译或自动引用 System.dll 程序集。</span><span class="sxs-lookup"><span data-stu-id="82e73-110">The `-nostdlib` option tells the compiler not to compile with Vbc.rsp or automatically reference the System.dll assembly.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="82e73-111">始终引用 Mscorlib.dll 和 Microsoft.VisualBasic.dll 程序集。</span><span class="sxs-lookup"><span data-stu-id="82e73-111">The Mscorlib.dll and Microsoft.VisualBasic.dll assemblies are always referenced.</span></span>  
  
 <span data-ttu-id="82e73-112">你可以修改 Vbc.rsp 文件以指定应包括在每个 Vbc.exe 编译中的其他编译器选项（指定 `-noconfig` 选项时除外）。</span><span class="sxs-lookup"><span data-stu-id="82e73-112">You can modify the Vbc.rsp file to specify additional compiler options that should be included in every Vbc.exe compilation (except when specifying the `-noconfig` option).</span></span> <span data-ttu-id="82e73-113">有关详细信息，请参阅 [@（指定响应文件）](specify-response-file.md)。</span><span class="sxs-lookup"><span data-stu-id="82e73-113">For more information, see [@ (Specify Response File)](specify-response-file.md).</span></span>  
  
 <span data-ttu-id="82e73-114">编译器最后处理传递给 `vbc` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="82e73-114">The compiler processes the options passed to the `vbc` command last.</span></span> <span data-ttu-id="82e73-115">因此，命令行中的任何选项都将替代 Vbc.rsp 文件中相同选项的设置。</span><span class="sxs-lookup"><span data-stu-id="82e73-115">Therefore, any option on the command line overrides the setting of the same option in the Vbc.rsp file.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="82e73-116">`-noconfig` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="82e73-116">The `-noconfig` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82e73-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="82e73-117">See also</span></span>

- [<span data-ttu-id="82e73-118">-nostdlib (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="82e73-118">-nostdlib (Visual Basic)</span></span>](nostdlib.md)
- [<span data-ttu-id="82e73-119">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="82e73-119">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="82e73-120">@（指定响应文件）</span><span class="sxs-lookup"><span data-stu-id="82e73-120">@ (Specify Response File)</span></span>](specify-response-file.md)
- [<span data-ttu-id="82e73-121">-reference (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="82e73-121">-reference (Visual Basic)</span></span>](reference.md)
