---
description: 详细了解：-removeintchecks
title: -removeintchecks
ms.date: 03/13/2018
f1_keywords:
- removeintchecks
- -removeintchecks
helpviewer_keywords:
- removeintchecks compiler option [Visual Basic]
- /removeintchecks compiler option [Visual Basic]
- -removeintchecks compiler option [Visual Basic]
ms.assetid: c1835bd5-1e38-4fba-bd2f-6984774765d4
ms.openlocfilehash: 1dc484e1538718b68fe9f0cc450fa2480dc52412
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474091"
---
# <a name="-removeintchecks"></a><span data-ttu-id="f0193-103">-removeintchecks</span><span class="sxs-lookup"><span data-stu-id="f0193-103">-removeintchecks</span></span>

<span data-ttu-id="f0193-104">打开或关闭对整数运算的溢出错误检查。</span><span class="sxs-lookup"><span data-stu-id="f0193-104">Turns overflow-error checking for integer operations on or off.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0193-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0193-105">Syntax</span></span>  
  
```console  
-removeintchecks[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="f0193-106">自变量</span><span class="sxs-lookup"><span data-stu-id="f0193-106">Arguments</span></span>  
  
|<span data-ttu-id="f0193-107">术语</span><span class="sxs-lookup"><span data-stu-id="f0193-107">Term</span></span>|<span data-ttu-id="f0193-108">定义</span><span class="sxs-lookup"><span data-stu-id="f0193-108">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="f0193-109">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="f0193-109">`+` &#124; `-`</span></span>|<span data-ttu-id="f0193-110">可选。</span><span class="sxs-lookup"><span data-stu-id="f0193-110">Optional.</span></span> <span data-ttu-id="f0193-111">`-removeintchecks-` 选项会使编译器检查所有整数计算是否存在溢出错误。</span><span class="sxs-lookup"><span data-stu-id="f0193-111">The `-removeintchecks-` option causes the compiler to check all integer calculations for overflow errors.</span></span> <span data-ttu-id="f0193-112">默认值为 `-removeintchecks-`。</span><span class="sxs-lookup"><span data-stu-id="f0193-112">The default is `-removeintchecks-`.</span></span><br /><br /> <span data-ttu-id="f0193-113">指定 `-removeintchecks` 或 `-removeintchecks+` 可阻止错误检查并可以使整数计算更快。</span><span class="sxs-lookup"><span data-stu-id="f0193-113">Specifying `-removeintchecks` or `-removeintchecks+` prevents error checking and can make integer calculations faster.</span></span> <span data-ttu-id="f0193-114">但是，不进行错误检查时，如果数据类型容量溢出，则可能会存储不正确的结果，而不会引发错误。</span><span class="sxs-lookup"><span data-stu-id="f0193-114">However, without error checking, and if data type capacities are overflowed, incorrect results may be stored without raising an error.</span></span>|  
  
|<span data-ttu-id="f0193-115">若要在 Visual Studio 集成开发环境中设置 -removeintchecks</span><span class="sxs-lookup"><span data-stu-id="f0193-115">To set -removeintchecks in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="f0193-116">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="f0193-116">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="f0193-117">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="f0193-117">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="f0193-118">2.单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="f0193-118">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="f0193-119">3.单击“高级”  按钮。</span><span class="sxs-lookup"><span data-stu-id="f0193-119">3.  Click the **Advanced** button.</span></span><br /><span data-ttu-id="f0193-120">4.修改“不做整数溢出检查”  框的值。</span><span class="sxs-lookup"><span data-stu-id="f0193-120">4.  Modify the value of the **Remove integer overflow checks** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f0193-121">示例</span><span class="sxs-lookup"><span data-stu-id="f0193-121">Example</span></span>  

 <span data-ttu-id="f0193-122">下面的代码编译 `Test.vb` 并关闭整数溢出错误检查。</span><span class="sxs-lookup"><span data-stu-id="f0193-122">The following code compiles `Test.vb` and turns off integer overflow-error checking.</span></span>  
  
```console
vbc -removeintchecks+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="f0193-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0193-123">See also</span></span>

- [<span data-ttu-id="f0193-124">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="f0193-124">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="f0193-125">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="f0193-125">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
