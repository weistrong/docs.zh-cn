---
description: '了解详细信息：在 Visual Studio 中调试表达式树 (Visual Basic) '
title: 在 Visual Studio 中调试表达式树
ms.date: 07/20/2015
ms.assetid: 492cc28f-b7a2-4c47-b582-b3c437b8a5d5
ms.openlocfilehash: 0221533a79dbc76be479380bd9b6e6df4156e288
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100459079"
---
# <a name="debugging-expression-trees-in-visual-studio-visual-basic"></a><span data-ttu-id="e4445-103">在 Visual Studio 中调试表达式树 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="e4445-103">Debugging Expression Trees in Visual Studio (Visual Basic)</span></span>

<span data-ttu-id="e4445-104">可以在调试应用程序时分析表达式树的结构和内容。</span><span class="sxs-lookup"><span data-stu-id="e4445-104">You can analyze the structure and content of expression trees when you debug your applications.</span></span> <span data-ttu-id="e4445-105">要快速了解表达式树结构，可以使用 `DebugView` 属性，该属性[使用特殊语法](debugview-syntax.md)表示表达式树。</span><span class="sxs-lookup"><span data-stu-id="e4445-105">To get a quick overview of the expression tree structure, you can use the `DebugView` property, which represents expression trees [using a special syntax](debugview-syntax.md).</span></span> <span data-ttu-id="e4445-106">（请注意，`DebugView` 仅在调试模式下可用。）</span><span class="sxs-lookup"><span data-stu-id="e4445-106">(Note that `DebugView` is available only in debug mode.)</span></span>  

![表达式树的 DebugView 的屏幕截图。](media/debugging-expression-trees-in-visual-studio/debugview-visual-basic.png)

<span data-ttu-id="e4445-108">由于 `DebugView` 是一个字符串，因此可以使用[内置文本可视化工具](/visualstudio/debugger/view-strings-visualizer#open-a-string-visualizer)在多行中进行查看，方法是从 `DebugView` 标签旁边的放大镜图标中选择“文本可视化工具”。</span><span class="sxs-lookup"><span data-stu-id="e4445-108">Since `DebugView` is a string, you can use the [built-in Text Visualizer](/visualstudio/debugger/view-strings-visualizer#open-a-string-visualizer) to view it across multiple lines, by selecting **Text Visualizer** from the magnifying glass icon next to the `DebugView` label.</span></span>

 ![应用于 DebugView 结果的文本可视化工具的屏幕截图。](media/debugging-expression-trees-in-visual-studio/string-visualizer-vb.png)

<span data-ttu-id="e4445-110">或者，可以为表达式树安装和使用[自定义可视化工具](/visualstudio/debugger/create-custom-visualizers-of-data)，例如：</span><span class="sxs-lookup"><span data-stu-id="e4445-110">Alternatively, you can install and use [a custom visualizer](/visualstudio/debugger/create-custom-visualizers-of-data) for expression trees, such as:</span></span>

- <span data-ttu-id="e4445-111">[可读表达式](https://github.com/agileobjects/ReadableExpressions)（[MIT 许可证](https://github.com/agileobjects/ReadableExpressions/blob/master/LICENSE.md)，可以从 [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1232914.ReadableExpressionsVisualizers) 中获取）使用各种呈现选项将表达式树呈现为可设置主题的 C# 代码：</span><span class="sxs-lookup"><span data-stu-id="e4445-111">[Readable Expressions](https://github.com/agileobjects/ReadableExpressions) ([MIT license](https://github.com/agileobjects/ReadableExpressions/blob/master/LICENSE.md), available at the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=vs-publisher-1232914.ReadableExpressionsVisualizers)), renders the expression tree as themeable C# code, with various rendering options:</span></span>

  ![可读表达式可视化工具的屏幕截图。](media/debugging-expression-trees-in-visual-studio/readable-expressions-visualizer.png)

- <span data-ttu-id="e4445-113">[表达式树可视化工具](https://github.com/zspitz/ExpressionTreeVisualizer/blob/master/README.md) ([MIT 许可证](https://github.com/zspitz/ExpressionTreeVisualizer/blob/master/LICENSE)) 提供表达式树及其各个节点的树视图;和可使用 Visual Basic 语法呈现表达式树：</span><span class="sxs-lookup"><span data-stu-id="e4445-113">[Expression Tree Visualizer](https://github.com/zspitz/ExpressionTreeVisualizer/blob/master/README.md) ([MIT license](https://github.com/zspitz/ExpressionTreeVisualizer/blob/master/LICENSE)) provides a tree view of the expression tree and its individual nodes; and can render the expression tree using Visual Basic syntax:</span></span>

  ![表达式树可视化工具的屏幕截图。](media/debugging-expression-trees-in-visual-studio/expression-tree-visualizer-vb.png)

### <a name="to-open-a-visualizer-for-an-expression-tree"></a><span data-ttu-id="e4445-115">打开表达式树的可视化工具</span><span class="sxs-lookup"><span data-stu-id="e4445-115">To open a visualizer for an expression tree</span></span>  
  
1. <span data-ttu-id="e4445-116">单击“数据提示”、“监视”窗口、“自动”窗口或“本地”窗口中表达式树旁边显示的放大镜图标   。</span><span class="sxs-lookup"><span data-stu-id="e4445-116">Click the magnifying glass icon that appears next to the expression tree in **DataTips**, a **Watch** window, the **Autos** window, or the **Locals** window.</span></span>  
  
    <span data-ttu-id="e4445-117">显示可用的可视化工具列表：</span><span class="sxs-lookup"><span data-stu-id="e4445-117">A list of available visualizers is displayed.:</span></span>

    ![用户从 Visual Studio 打开可视化工具的屏幕截图。](media/debugging-expression-trees-in-visual-studio/expression-tree-visualizers-vb.png)

2. <span data-ttu-id="e4445-119">单击要使用的可视化工具。</span><span class="sxs-lookup"><span data-stu-id="e4445-119">Click the visualizer you want to use.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4445-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4445-120">See also</span></span>

- [<span data-ttu-id="e4445-121">表达式树 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e4445-121">Expression Trees (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="e4445-122">在 Visual Studio 中进行调试</span><span class="sxs-lookup"><span data-stu-id="e4445-122">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugger-feature-tour)
- [<span data-ttu-id="e4445-123">创建自定义可视化工具</span><span class="sxs-lookup"><span data-stu-id="e4445-123">Create Custom Visualizers</span></span>](/visualstudio/debugger/create-custom-visualizers-of-data)
- [<span data-ttu-id="e4445-124">`DebugView` 语法</span><span class="sxs-lookup"><span data-stu-id="e4445-124">`DebugView` syntax</span></span>](debugview-syntax.md)
