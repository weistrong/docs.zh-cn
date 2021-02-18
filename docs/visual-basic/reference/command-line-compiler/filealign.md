---
description: 详细了解：-filealign
title: -filealign
ms.date: 03/10/2018
helpviewer_keywords:
- sections compiler option [Visual Basic]
- alignment compiler option [Visual Basic]
- -filealign compiler option [Visual Basic]
- section alignment
- /filealign compiler option [Visual Basic]
- filealign compiler option [Visual Basic]
ms.assetid: cc61ec3d-ad38-4b28-9659-099d73cad099
ms.openlocfilehash: f32ae370c0ef832b501f085351eadb9b6156c730
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100470286"
---
# <a name="-filealign"></a><span data-ttu-id="81cc1-103">-filealign</span><span class="sxs-lookup"><span data-stu-id="81cc1-103">-filealign</span></span>

<span data-ttu-id="81cc1-104">指定输出文件各节的对齐位置。</span><span class="sxs-lookup"><span data-stu-id="81cc1-104">Specifies where to align the sections of the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81cc1-105">语法</span><span class="sxs-lookup"><span data-stu-id="81cc1-105">Syntax</span></span>  
  
```console  
-filealign:number  
```  
  
## <a name="arguments"></a><span data-ttu-id="81cc1-106">自变量</span><span class="sxs-lookup"><span data-stu-id="81cc1-106">Arguments</span></span>  

 `number`  
 <span data-ttu-id="81cc1-107">必需。</span><span class="sxs-lookup"><span data-stu-id="81cc1-107">Required.</span></span> <span data-ttu-id="81cc1-108">一个值，用于指定输出文件中各节的对齐方式。</span><span class="sxs-lookup"><span data-stu-id="81cc1-108">A value that specifies the alignment of sections in the output file.</span></span> <span data-ttu-id="81cc1-109">有效值为 512、1024、2048、4096 和 8192。</span><span class="sxs-lookup"><span data-stu-id="81cc1-109">Valid values are 512, 1024, 2048, 4096, and 8192.</span></span> <span data-ttu-id="81cc1-110">这些值以字节为单位。</span><span class="sxs-lookup"><span data-stu-id="81cc1-110">These values are in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="81cc1-111">备注</span><span class="sxs-lookup"><span data-stu-id="81cc1-111">Remarks</span></span>  

 <span data-ttu-id="81cc1-112">可以使用 `-filealign` 选项来指定输出文件中各节的对齐方式。</span><span class="sxs-lookup"><span data-stu-id="81cc1-112">You can use the `-filealign` option to specify the alignment of sections in your output file.</span></span> <span data-ttu-id="81cc1-113">节是可移植可执行 (PE) 文件中包含代码或数据的连续内存块。</span><span class="sxs-lookup"><span data-stu-id="81cc1-113">Sections are blocks of contiguous memory in a Portable Executable (PE) file that contains either code or data.</span></span> <span data-ttu-id="81cc1-114">`-filealign` 选项允许你使用非标准对齐方式编译应用程序；大多数开发人员不需要使用此选项。</span><span class="sxs-lookup"><span data-stu-id="81cc1-114">The `-filealign` option lets you compile your application with a nonstandard alignment; most developers do not need to use this option.</span></span>  
  
 <span data-ttu-id="81cc1-115">每一节都与边界一致，该边界是 `-filealign` 值的倍数。</span><span class="sxs-lookup"><span data-stu-id="81cc1-115">Each section is aligned on a boundary that is a multiple of the `-filealign` value.</span></span> <span data-ttu-id="81cc1-116">没有固定的默认值。</span><span class="sxs-lookup"><span data-stu-id="81cc1-116">There is no fixed default.</span></span> <span data-ttu-id="81cc1-117">如果未指定 `-filealign`，编译器将在编译时选取默认值。</span><span class="sxs-lookup"><span data-stu-id="81cc1-117">If `-filealign` is not specified, the compiler picks a default at compile time.</span></span>  
  
 <span data-ttu-id="81cc1-118">通过指定节的大小，可以更改输出文件的大小。</span><span class="sxs-lookup"><span data-stu-id="81cc1-118">By specifying the section size, you can change the size of the output file.</span></span> <span data-ttu-id="81cc1-119">修改节的大小可能对将在较小设备上运行的程序有用。</span><span class="sxs-lookup"><span data-stu-id="81cc1-119">Modifying section size may be useful for programs that will run on smaller devices.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="81cc1-120">`-filealign` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="81cc1-120">The `-filealign` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81cc1-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="81cc1-121">See also</span></span>

- [<span data-ttu-id="81cc1-122">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="81cc1-122">Visual Basic Command-Line Compiler</span></span>](index.md)
