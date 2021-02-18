---
description: 详细了解：-main
title: -main
ms.date: 03/13/2018
helpviewer_keywords:
- main compiler option [Visual Basic]
- /main compiler option [Visual Basic]
- -main compiler option [Visual Basic]
ms.assetid: 83fc339d-6652-415d-b205-b5133319b5b0
ms.openlocfilehash: 4c225c5a0030de6de0aaa510080a586272aa920b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100455660"
---
# <a name="-main"></a><span data-ttu-id="b82ea-103">-main</span><span class="sxs-lookup"><span data-stu-id="b82ea-103">-main</span></span>

<span data-ttu-id="b82ea-104">指定包含 `Sub Main` 过程的类或模块。</span><span class="sxs-lookup"><span data-stu-id="b82ea-104">Specifies the class or module that contains the `Sub Main` procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b82ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="b82ea-105">Syntax</span></span>  
  
```console  
-main:location  
```  
  
## <a name="arguments"></a><span data-ttu-id="b82ea-106">自变量</span><span class="sxs-lookup"><span data-stu-id="b82ea-106">Arguments</span></span>  

 `location`  
 <span data-ttu-id="b82ea-107">必需。</span><span class="sxs-lookup"><span data-stu-id="b82ea-107">Required.</span></span> <span data-ttu-id="b82ea-108">类或模块的名称，其中包含在程序启动时要调用的 `Sub Main` 过程。</span><span class="sxs-lookup"><span data-stu-id="b82ea-108">The name of the class or module that contains the `Sub Main` procedure to be called when the program starts.</span></span> <span data-ttu-id="b82ea-109">此格式可以是 -main:module  或 -main:namespace.module  。</span><span class="sxs-lookup"><span data-stu-id="b82ea-109">This may be in the form **-main:module** or **-main:namespace.module**.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b82ea-110">备注</span><span class="sxs-lookup"><span data-stu-id="b82ea-110">Remarks</span></span>  

 <span data-ttu-id="b82ea-111">创建可执行文件或 Windows 可执行程序时，请使用此选项。</span><span class="sxs-lookup"><span data-stu-id="b82ea-111">Use this option when you create an executable file or Windows executable program.</span></span> <span data-ttu-id="b82ea-112">如果省略“-main”  选项，编译器将在所有公共类和模块中搜索有效的共享 `Sub Main`。</span><span class="sxs-lookup"><span data-stu-id="b82ea-112">If the **-main** option is omitted, the compiler searches for a valid shared `Sub Main` in all public classes and modules.</span></span>  
  
 <span data-ttu-id="b82ea-113">有关 `Main` 过程的各种形式的讨论，请参阅 [Visual Basic 中的 Main 过程](../../programming-guide/program-structure/main-procedure.md)。</span><span class="sxs-lookup"><span data-stu-id="b82ea-113">See [Main Procedure in Visual Basic](../../programming-guide/program-structure/main-procedure.md) for a discussion of the various forms of the `Main` procedure.</span></span>  
  
 <span data-ttu-id="b82ea-114">如果 `location` 是从 <xref:System.Windows.Forms.Form> 继承的类，则编译器将提供一个默认的 `Main` 过程，该过程在类没有 `Main` 过程的情况下启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="b82ea-114">When `location` is a class that inherits from <xref:System.Windows.Forms.Form>, the compiler provides a default `Main` procedure that starts the application if the class has no `Main` procedure.</span></span> <span data-ttu-id="b82ea-115">这使你可以在开发环境中创建的命令行上编译代码。</span><span class="sxs-lookup"><span data-stu-id="b82ea-115">This lets you compile code at the command line that was created in the development environment.</span></span>  
  
 [!code-vb[VbVbalrCompiler#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/Class1.vb#16)]  
  
### <a name="to-set--main-in-the-visual-studio-integrated-development-environment"></a><span data-ttu-id="b82ea-116">在 Visual Studio 集成开发环境中设置 -main</span><span class="sxs-lookup"><span data-stu-id="b82ea-116">To set -main in the Visual Studio integrated development environment</span></span>  
  
1. <span data-ttu-id="b82ea-117">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="b82ea-117">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="b82ea-118">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="b82ea-118">On the **Project** menu, click **Properties**.</span></span>  
  
2. <span data-ttu-id="b82ea-119">单击“应用程序”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="b82ea-119">Click the **Application** tab.</span></span>  
  
3. <span data-ttu-id="b82ea-120">请确保未选中“启用应用程序框架”  复选框。</span><span class="sxs-lookup"><span data-stu-id="b82ea-120">Make sure the **Enable application framework** check box is not checked.</span></span>  
  
4. <span data-ttu-id="b82ea-121">修改“启动对象”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="b82ea-121">Modify the value in the **Startup object** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b82ea-122">示例</span><span class="sxs-lookup"><span data-stu-id="b82ea-122">Example</span></span>  

 <span data-ttu-id="b82ea-123">下面的代码编译 `T2.vb` 和 `T3.vb`，指定将在 `Test2` 类中找到 `Sub Main` 过程。</span><span class="sxs-lookup"><span data-stu-id="b82ea-123">The following code compiles `T2.vb` and `T3.vb`, specifying that the `Sub Main` procedure will be found in the `Test2` class.</span></span>  
  
```console
vbc t2.vb t3.vb -main:Test2  
```  
  
## <a name="see-also"></a><span data-ttu-id="b82ea-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="b82ea-124">See also</span></span>

- [<span data-ttu-id="b82ea-125">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="b82ea-125">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="b82ea-126">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b82ea-126">-target (Visual Basic)</span></span>](target.md)
- [<span data-ttu-id="b82ea-127">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="b82ea-127">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="b82ea-128">Visual Basic 中的 Main 过程</span><span class="sxs-lookup"><span data-stu-id="b82ea-128">Main Procedure in Visual Basic</span></span>](../../programming-guide/program-structure/main-procedure.md)
