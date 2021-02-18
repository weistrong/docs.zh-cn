---
description: 详细了解：-libpath
title: -libpath
ms.date: 03/10/2018
helpviewer_keywords:
- libpath compiler option [Visual Basic]
- /libpath compiler option [Visual Basic]
- -libpath compiler option [Visual Basic]
ms.assetid: 5f1c26c9-3455-4e89-bdf3-b12d6c2e655b
ms.openlocfilehash: cdc3f557e0d069930032ac3b0af7a0e88762189d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100455673"
---
# <a name="-libpath"></a><span data-ttu-id="30a56-103">-libpath</span><span class="sxs-lookup"><span data-stu-id="30a56-103">-libpath</span></span>

<span data-ttu-id="30a56-104">指定引用的程序集的位置。</span><span class="sxs-lookup"><span data-stu-id="30a56-104">Specifies the location of referenced assemblies.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30a56-105">语法</span><span class="sxs-lookup"><span data-stu-id="30a56-105">Syntax</span></span>  
  
```console  
-libpath:dirList  
```  
  
## <a name="arguments"></a><span data-ttu-id="30a56-106">自变量</span><span class="sxs-lookup"><span data-stu-id="30a56-106">Arguments</span></span>  
  
|<span data-ttu-id="30a56-107">术语</span><span class="sxs-lookup"><span data-stu-id="30a56-107">Term</span></span>|<span data-ttu-id="30a56-108">定义</span><span class="sxs-lookup"><span data-stu-id="30a56-108">Definition</span></span>|  
|---|---|  
|`dirList`|<span data-ttu-id="30a56-109">必需。</span><span class="sxs-lookup"><span data-stu-id="30a56-109">Required.</span></span> <span data-ttu-id="30a56-110">在当前工作目录（调用编译器的目录）或公共语言运行时的系统目录中未找到引用的程序集时，编译器将在其中进行查找的由分号分隔的目录列表。</span><span class="sxs-lookup"><span data-stu-id="30a56-110">Semicolon-delimited list of directories for the compiler to look in if a referenced assembly is not found in either the current working directory (the directory from which you are invoking the compiler) or the common language runtime's system directory.</span></span> <span data-ttu-id="30a56-111">如果目录名包含空格，则将名称括在引号 (" ") 内。</span><span class="sxs-lookup"><span data-stu-id="30a56-111">If the directory name contains a space, enclose the name in quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="30a56-112">备注</span><span class="sxs-lookup"><span data-stu-id="30a56-112">Remarks</span></span>  

 <span data-ttu-id="30a56-113">`-libpath` 选项指定通过 [-reference](reference.md) 选项引用的程序集的位置。</span><span class="sxs-lookup"><span data-stu-id="30a56-113">The `-libpath` option specifies the location of assemblies referenced by the [-reference](reference.md) option.</span></span>  
  
 <span data-ttu-id="30a56-114">编译器按以下顺序搜索未完全限定的程序集引用：</span><span class="sxs-lookup"><span data-stu-id="30a56-114">The compiler searches for assembly references that are not fully qualified in the following order:</span></span>  
  
1. <span data-ttu-id="30a56-115">当前工作目录。</span><span class="sxs-lookup"><span data-stu-id="30a56-115">Current working directory.</span></span> <span data-ttu-id="30a56-116">该目录为从其调用编译器的目录。</span><span class="sxs-lookup"><span data-stu-id="30a56-116">This is the directory from which the compiler is invoked.</span></span>  
  
2. <span data-ttu-id="30a56-117">公共语言运行时系统目录。</span><span class="sxs-lookup"><span data-stu-id="30a56-117">The common language runtime system directory.</span></span>  
  
3. <span data-ttu-id="30a56-118">由 `-libpath` 指定的目录。</span><span class="sxs-lookup"><span data-stu-id="30a56-118">Directories specified by `-libpath`.</span></span>  
  
4. <span data-ttu-id="30a56-119">由 LIB 环境变量指定的目录。</span><span class="sxs-lookup"><span data-stu-id="30a56-119">Directories specified by the LIB environment variable.</span></span>  
  
 <span data-ttu-id="30a56-120">`-libpath` 选项是累加的；每一次指定的值都追加到以前的值中。</span><span class="sxs-lookup"><span data-stu-id="30a56-120">The `-libpath` option is additive; specifying it more than once appends to any prior values.</span></span>  
  
 <span data-ttu-id="30a56-121">使用 `-reference` 指定程序集引用。</span><span class="sxs-lookup"><span data-stu-id="30a56-121">Use `-reference` to specify an assembly reference.</span></span>  
  
|<span data-ttu-id="30a56-122">在 Visual Studio 集成开发环境中设置 -libpath</span><span class="sxs-lookup"><span data-stu-id="30a56-122">To set -libpath in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="30a56-123">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="30a56-123">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="30a56-124">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="30a56-124">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="30a56-125">2.单击“引用”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="30a56-125">2.  Click the **References** tab.</span></span><br /><span data-ttu-id="30a56-126">3.单击“引用路径...”按钮。 </span><span class="sxs-lookup"><span data-stu-id="30a56-126">3.  Click the **Reference Paths...** button.</span></span><br /><span data-ttu-id="30a56-127">4.在“引用路径”对话框的“文件夹:”框中，输入目录名称。  </span><span class="sxs-lookup"><span data-stu-id="30a56-127">4.  In the **Reference Paths** dialog box, enter the directory name in the **Folder:** box.</span></span><br /><span data-ttu-id="30a56-128">5.单击“添加文件夹”。 </span><span class="sxs-lookup"><span data-stu-id="30a56-128">5.  Click **Add Folder**.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="30a56-129">示例</span><span class="sxs-lookup"><span data-stu-id="30a56-129">Example</span></span>  

 <span data-ttu-id="30a56-130">下面的代码编译 `T2.vb`，用于生成 .exe 文件。</span><span class="sxs-lookup"><span data-stu-id="30a56-130">The following code compiles `T2.vb` to create an .exe file.</span></span> <span data-ttu-id="30a56-131">编译器将在工作目录、C: 驱动器的根目录和 C: 驱动器的“新程序集”目录中查找程序集引用。</span><span class="sxs-lookup"><span data-stu-id="30a56-131">The compiler looks in the working directory, in the root directory of the C: drive, and in the New Assemblies directory of the C: drive for assembly references.</span></span>  
  
```console  
vbc -libpath:c:\;"c:\New Assemblies" -reference:t2.dll t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="30a56-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="30a56-132">See also</span></span>

- [<span data-ttu-id="30a56-133">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="30a56-133">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="30a56-134">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="30a56-134">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="30a56-135">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="30a56-135">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
