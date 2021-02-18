---
description: 详细了解：-verbose
title: -verbose
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
ms.openlocfilehash: ea222d4f284bcaf163b142269fe250a081b0ee4f
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100470131"
---
# <a name="-verbose"></a><span data-ttu-id="da058-103">-verbose</span><span class="sxs-lookup"><span data-stu-id="da058-103">-verbose</span></span>

<span data-ttu-id="da058-104">导致编译器生成详细状态和错误消息。</span><span class="sxs-lookup"><span data-stu-id="da058-104">Causes the compiler to produce verbose status and error messages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da058-105">语法</span><span class="sxs-lookup"><span data-stu-id="da058-105">Syntax</span></span>  
  
```console  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="da058-106">自变量</span><span class="sxs-lookup"><span data-stu-id="da058-106">Arguments</span></span>  

 <span data-ttu-id="da058-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="da058-107">`+` &#124; `-`</span></span>  
 <span data-ttu-id="da058-108">可选。</span><span class="sxs-lookup"><span data-stu-id="da058-108">Optional.</span></span> <span data-ttu-id="da058-109">指定 `-verbose` 与指定 `-verbose+` 相同，这将导致编译器发出详细消息。</span><span class="sxs-lookup"><span data-stu-id="da058-109">Specifying `-verbose` is the same as specifying `-verbose+`, which causes the compiler to emit verbose messages.</span></span> <span data-ttu-id="da058-110">此选项的默认值为 `-verbose-`。</span><span class="sxs-lookup"><span data-stu-id="da058-110">The default for this option is `-verbose-`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="da058-111">备注</span><span class="sxs-lookup"><span data-stu-id="da058-111">Remarks</span></span>  

 <span data-ttu-id="da058-112">`-verbose` 选项显示编译器发出的错误总数的相关信息，报告模块正在加载的程序集，并显示当前正在编译的文件。</span><span class="sxs-lookup"><span data-stu-id="da058-112">The `-verbose` option displays information about the total number of errors issued by the compiler, reports which assemblies are being loaded by a module, and displays which files are currently being compiled.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="da058-113">`-verbose` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="da058-113">The `-verbose` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da058-114">示例</span><span class="sxs-lookup"><span data-stu-id="da058-114">Example</span></span>  

 <span data-ttu-id="da058-115">下面的代码编译 `In.vb`，并指示编译器显示详细状态信息。</span><span class="sxs-lookup"><span data-stu-id="da058-115">The following code compiles `In.vb` and directs the compiler to display verbose status information.</span></span>  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="da058-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="da058-116">See also</span></span>

- [<span data-ttu-id="da058-117">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="da058-117">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="da058-118">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="da058-118">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
