---
description: 详细了解：-utf8output (Visual Basic)
title: -utf8output
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: 317c1be3f18150ae88bb8e95927d9f5faf0e4f3c
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100461887"
---
# <a name="-utf8output-visual-basic"></a><span data-ttu-id="03733-103">-utf8output (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="03733-103">-utf8output (Visual Basic)</span></span>

<span data-ttu-id="03733-104">显示使用 UTF-8 编码的编译器输出。</span><span class="sxs-lookup"><span data-stu-id="03733-104">Displays compiler output using UTF-8 encoding.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03733-105">语法</span><span class="sxs-lookup"><span data-stu-id="03733-105">Syntax</span></span>  
  
```console  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="03733-106">自变量</span><span class="sxs-lookup"><span data-stu-id="03733-106">Arguments</span></span>  

 <span data-ttu-id="03733-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="03733-107">`+` &#124; `-`</span></span>  
 <span data-ttu-id="03733-108">可选。</span><span class="sxs-lookup"><span data-stu-id="03733-108">Optional.</span></span> <span data-ttu-id="03733-109">此选项的默认值为 `-utf8output-`，这意味着编译器输出不使用 UTF-8 编码。</span><span class="sxs-lookup"><span data-stu-id="03733-109">The default for this option is `-utf8output-`, which means compiler output does not use UTF-8 encoding.</span></span> <span data-ttu-id="03733-110">指定 `-utf8output` 与指定 `-utf8output+` 相同。</span><span class="sxs-lookup"><span data-stu-id="03733-110">Specifying `-utf8output` is the same as specifying `-utf8output+`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="03733-111">备注</span><span class="sxs-lookup"><span data-stu-id="03733-111">Remarks</span></span>  

 <span data-ttu-id="03733-112">在某些国际配置中，编译器输出无法在控制台上正确显示。</span><span class="sxs-lookup"><span data-stu-id="03733-112">In some international configurations, compiler output cannot be displayed correctly in the console.</span></span> <span data-ttu-id="03733-113">在这种情况下，请使用 `-utf8output`，并将编译器输出重定向到文件。</span><span class="sxs-lookup"><span data-stu-id="03733-113">In such situations, use `-utf8output` and redirect compiler output to a file.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="03733-114">`-utf8output` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="03733-114">The `-utf8output` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="03733-115">示例</span><span class="sxs-lookup"><span data-stu-id="03733-115">Example</span></span>  

 <span data-ttu-id="03733-116">下面的代码编译 `In.vb`，并指示编译器使用 UTF-8 编码显示输出。</span><span class="sxs-lookup"><span data-stu-id="03733-116">The following code compiles `In.vb` and directs the compiler to display output using UTF-8 encoding.</span></span>  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="03733-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="03733-117">See also</span></span>

- [<span data-ttu-id="03733-118">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="03733-118">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="03733-119">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="03733-119">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
