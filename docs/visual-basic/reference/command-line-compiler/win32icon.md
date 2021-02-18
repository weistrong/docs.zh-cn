---
description: 详细了解：-win32icon
title: -win32icon
ms.date: 03/13/2018
helpviewer_keywords:
- win32icon compiler option [Visual Basic]
- -win32icon compiler option [Visual Basic]
- /win32icon compiler option [Visual Basic]
ms.assetid: aecaab01-9353-46c5-941c-6edabd4eff92
ms.openlocfilehash: 32a46771012708a42beb5450d28daf2fbab3f1c0
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433544"
---
# <a name="-win32icon"></a><span data-ttu-id="c1bc1-103">-win32icon</span><span class="sxs-lookup"><span data-stu-id="c1bc1-103">-win32icon</span></span>

<span data-ttu-id="c1bc1-104">将 .ico 文件插入到输出文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-104">Inserts an .ico file in the output file.</span></span> <span data-ttu-id="c1bc1-105">此 .ico 文件表示文件资源管理器  中的输出文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-105">This .ico file represents the output file in **File Explorer**.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1bc1-106">语法</span><span class="sxs-lookup"><span data-stu-id="c1bc1-106">Syntax</span></span>  
  
```console  
-win32icon:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="c1bc1-107">自变量</span><span class="sxs-lookup"><span data-stu-id="c1bc1-107">Arguments</span></span>  
  
|<span data-ttu-id="c1bc1-108">术语</span><span class="sxs-lookup"><span data-stu-id="c1bc1-108">Term</span></span>|<span data-ttu-id="c1bc1-109">定义</span><span class="sxs-lookup"><span data-stu-id="c1bc1-109">Definition</span></span>|  
|---|---|  
|`filename`|<span data-ttu-id="c1bc1-110">要向输出文件添加的 .ico 文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-110">The .ico file to add to your output file.</span></span> <span data-ttu-id="c1bc1-111">如果文件名包含空格，则将名称括在引号 (" ") 内。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-111">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c1bc1-112">备注</span><span class="sxs-lookup"><span data-stu-id="c1bc1-112">Remarks</span></span>  

 <span data-ttu-id="c1bc1-113">可以使用 Microsoft Windows 资源编译器 (RC) 创建 .ico 文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-113">You can create an .ico file with the Microsoft Windows Resource Compiler (RC).</span></span> <span data-ttu-id="c1bc1-114">在编译 Visual C++ 程序时会调用资源编译器；.ico 文件是从 .rc 文件创建的。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-114">The resource compiler is invoked when you compile a Visual C++ program; an .ico file is created from the .rc file.</span></span> <span data-ttu-id="c1bc1-115">`-win32icon` 和 `-win32resource` 选项互斥。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-115">The `-win32icon` and `-win32resource` options are mutually exclusive.</span></span>  
  
 <span data-ttu-id="c1bc1-116">请参阅 [-linkresource (Visual Basic)](linkresource.md) 以引用 .NET Framework 资源文件，或参阅 [-resource (Visual Basic)](resource.md) 以附加 .NET Framework 资源文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-116">See [-linkresource (Visual Basic)](linkresource.md) to reference a .NET Framework resource file, or [-resource (Visual Basic)](resource.md) to attach a .NET Framework resource file.</span></span> <span data-ttu-id="c1bc1-117">请参阅 [-win32resource](win32resource.md) 以导入 .res 文件。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-117">See [-win32resource](win32resource.md) to import a .res file.</span></span>  
  
|<span data-ttu-id="c1bc1-118">若要在 Visual Studio IDE 中设置 -win32icon</span><span class="sxs-lookup"><span data-stu-id="c1bc1-118">To set -win32icon in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="c1bc1-119">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-119">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="c1bc1-120">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-120">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="c1bc1-121">2.单击“应用程序”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-121">2.  Click the **Application** tab.</span></span><br /><span data-ttu-id="c1bc1-122">3.修改“图标”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-122">3.  Modify the value in the **Icon** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c1bc1-123">示例</span><span class="sxs-lookup"><span data-stu-id="c1bc1-123">Example</span></span>  

 <span data-ttu-id="c1bc1-124">下面的代码编译 `In.vb` 并附加 .ico 文件 `Rf.ico`。</span><span class="sxs-lookup"><span data-stu-id="c1bc1-124">The following code compiles `In.vb` and attaches an .ico file, `Rf.ico`.</span></span>  
  
```console
vbc -win32icon:rf.ico in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="c1bc1-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1bc1-125">See also</span></span>

- [<span data-ttu-id="c1bc1-126">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="c1bc1-126">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="c1bc1-127">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="c1bc1-127">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
