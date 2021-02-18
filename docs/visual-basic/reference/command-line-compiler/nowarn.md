---
description: 详细了解：-nowarn
title: -nowarn
ms.date: 07/20/2015
helpviewer_keywords:
- nowarn compiler option [Visual Basic]
- /nowarn compiler option [Visual Basic]
- -nowarn compiler option [Visual Basic]
ms.assetid: 7ebf2106-0652-4fdc-bf60-70fc86465d83
ms.openlocfilehash: 4fb7d39aef48ff1443c342367f9e20bb37f9c5e0
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434857"
---
# <a name="-nowarn"></a><span data-ttu-id="c2c93-103">-nowarn</span><span class="sxs-lookup"><span data-stu-id="c2c93-103">-nowarn</span></span>

<span data-ttu-id="c2c93-104">禁止编译器生成警告的能力。</span><span class="sxs-lookup"><span data-stu-id="c2c93-104">Suppresses the compiler's ability to generate warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2c93-105">语法</span><span class="sxs-lookup"><span data-stu-id="c2c93-105">Syntax</span></span>  
  
```console  
-nowarn[:numberList]  
```  
  
## <a name="arguments"></a><span data-ttu-id="c2c93-106">自变量</span><span class="sxs-lookup"><span data-stu-id="c2c93-106">Arguments</span></span>  
  
|<span data-ttu-id="c2c93-107">术语</span><span class="sxs-lookup"><span data-stu-id="c2c93-107">Term</span></span>|<span data-ttu-id="c2c93-108">定义</span><span class="sxs-lookup"><span data-stu-id="c2c93-108">Definition</span></span>|  
|---|---|  
|`numberList`|<span data-ttu-id="c2c93-109">可选。</span><span class="sxs-lookup"><span data-stu-id="c2c93-109">Optional.</span></span> <span data-ttu-id="c2c93-110">编译器应禁止的以逗号分隔的警告 ID 编号列表。</span><span class="sxs-lookup"><span data-stu-id="c2c93-110">Comma-delimited list of the warning ID numbers that the compiler should suppress.</span></span> <span data-ttu-id="c2c93-111">如果未指定警告 ID，将禁止所有警告。</span><span class="sxs-lookup"><span data-stu-id="c2c93-111">If the warning IDs are not specified, all warnings are suppressed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2c93-112">备注</span><span class="sxs-lookup"><span data-stu-id="c2c93-112">Remarks</span></span>  

 <span data-ttu-id="c2c93-113">`-nowarn` 选项会导致编译器不生成警告。</span><span class="sxs-lookup"><span data-stu-id="c2c93-113">The `-nowarn` option causes the compiler to not generate warnings.</span></span> <span data-ttu-id="c2c93-114">若要禁止单个警告，请向后跟冒号的 `-nowarn` 选项提供警告 ID。</span><span class="sxs-lookup"><span data-stu-id="c2c93-114">To suppress an individual warning, supply the warning ID to the `-nowarn` option following the colon.</span></span> <span data-ttu-id="c2c93-115">使用逗号分隔多个警告编号。</span><span class="sxs-lookup"><span data-stu-id="c2c93-115">Separate multiple warning numbers with commas.</span></span>  
  
 <span data-ttu-id="c2c93-116">仅需指定警告标识符的数值部分。</span><span class="sxs-lookup"><span data-stu-id="c2c93-116">You need to specify only the numeric part of the warning identifier.</span></span> <span data-ttu-id="c2c93-117">例如，如果要禁止 BC42024（针对未使用本地变量的警告），请指定 `-nowarn:42024`。</span><span class="sxs-lookup"><span data-stu-id="c2c93-117">For example, if you want to suppress BC42024, the warning for unused local variables, specify `-nowarn:42024`.</span></span>  
  
 <span data-ttu-id="c2c93-118">有关警告 ID 编号的详细信息，请参阅[在 Visual Basic 中配置警告](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="c2c93-118">For more information on the warning ID numbers, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
|<span data-ttu-id="c2c93-119">在 Visual Studio 集成开发环境中设置 -nowarn</span><span class="sxs-lookup"><span data-stu-id="c2c93-119">To set -nowarn in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="c2c93-120">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="c2c93-120">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="c2c93-121">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="c2c93-121">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="c2c93-122">2.单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="c2c93-122">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="c2c93-123">3.选择“禁用所有警告”  复选框以禁用所有警告。</span><span class="sxs-lookup"><span data-stu-id="c2c93-123">3.  Select the **Disable all warnings** check box to disable all warnings.</span></span><br />     <span data-ttu-id="c2c93-124">- 或 -</span><span class="sxs-lookup"><span data-stu-id="c2c93-124">- or -</span></span><br />     <span data-ttu-id="c2c93-125">若要禁用特定警告，请单击警告旁边的下拉列表中的“无”  。</span><span class="sxs-lookup"><span data-stu-id="c2c93-125">To disable a particular warning, click **None** from the drop-down list adjacent to the warning.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c2c93-126">示例</span><span class="sxs-lookup"><span data-stu-id="c2c93-126">Example</span></span>  

 <span data-ttu-id="c2c93-127">以下代码编译 `T2.vb` 并且不显示任何警告。</span><span class="sxs-lookup"><span data-stu-id="c2c93-127">The following code compiles `T2.vb` and does not display any warnings.</span></span>  
  
```console
vbc -nowarn t2.vb  
```  
  
## <a name="example"></a><span data-ttu-id="c2c93-128">示例</span><span class="sxs-lookup"><span data-stu-id="c2c93-128">Example</span></span>  

 <span data-ttu-id="c2c93-129">以下代码编译 `T2.vb` 并且不显示未使用的本地变量 (42024) 的警告。</span><span class="sxs-lookup"><span data-stu-id="c2c93-129">The following code compiles `T2.vb` and does not display the warnings for unused local variables (42024).</span></span>  
  
```console
vbc -nowarn:42024 t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="c2c93-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2c93-130">See also</span></span>

- [<span data-ttu-id="c2c93-131">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="c2c93-131">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="c2c93-132">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="c2c93-132">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="c2c93-133">Configuring Warnings in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c2c93-133">Configuring Warnings in Visual Basic</span></span>](/visualstudio/ide/configuring-warnings-in-visual-basic)
