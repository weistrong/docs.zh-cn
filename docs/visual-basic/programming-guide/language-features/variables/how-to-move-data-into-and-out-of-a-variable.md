---
description: '了解详细信息：如何：将数据移入和移出变量 (Visual Basic) '
title: 如何：将数据移入和移出变量
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], retrieving values
- variables [Visual Basic], storing data
ms.assetid: 93744f46-bf78-4fa0-9640-1de01bc38d9a
ms.openlocfilehash: e75be83f82a3e1418099375eb52a2d2cc4fdbd18
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481813"
---
# <a name="how-to-move-data-into-and-out-of-a-variable-visual-basic"></a><span data-ttu-id="03f75-103">如何：将数据移入和移出变量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="03f75-103">How to: Move Data Into and Out of a Variable (Visual Basic)</span></span>

<span data-ttu-id="03f75-104">您可以通过将变量名称放在赋值语句的左侧来将值存储在变量中。</span><span class="sxs-lookup"><span data-stu-id="03f75-104">You store a value in a variable by putting the variable name on the left side of an assignment statement.</span></span>

## <a name="putting-data-in-a-variable"></a><span data-ttu-id="03f75-105">将数据放入变量</span><span class="sxs-lookup"><span data-stu-id="03f75-105">Putting Data in a Variable</span></span>

#### <a name="to-store-a-value-in-a-variable"></a><span data-ttu-id="03f75-106">将值存储在变量中</span><span class="sxs-lookup"><span data-stu-id="03f75-106">To store a value in a variable</span></span>

- <span data-ttu-id="03f75-107">使用赋值语句左侧的变量名称。</span><span class="sxs-lookup"><span data-stu-id="03f75-107">Use the variable name on the left side of an assignment statement.</span></span>

    <span data-ttu-id="03f75-108">下面的示例设置变量的值 `alpha` 。</span><span class="sxs-lookup"><span data-stu-id="03f75-108">The following example sets the value of the variable `alpha`.</span></span>

    ```vb
    alpha = (beta * 6.27) / (gamma + 2.1)
    ```

    <span data-ttu-id="03f75-109">赋值语句右侧生成的值存储在变量中。</span><span class="sxs-lookup"><span data-stu-id="03f75-109">The value generated on the right side of the assignment statement is stored in the variable.</span></span>

## <a name="getting-data-from-a-variable"></a><span data-ttu-id="03f75-110">从变量中获取数据</span><span class="sxs-lookup"><span data-stu-id="03f75-110">Getting Data from a Variable</span></span>

<span data-ttu-id="03f75-111">通过在表达式中包含变量名称来检索变量的值。</span><span class="sxs-lookup"><span data-stu-id="03f75-111">You retrieve a variable's value by including the variable name in an expression.</span></span>

#### <a name="to-retrieve-a-value-from-a-variable"></a><span data-ttu-id="03f75-112">从变量中检索值</span><span class="sxs-lookup"><span data-stu-id="03f75-112">To retrieve a value from a variable</span></span>

- <span data-ttu-id="03f75-113">在表达式中使用变量名。</span><span class="sxs-lookup"><span data-stu-id="03f75-113">Use the variable name in an expression.</span></span> <span data-ttu-id="03f75-114">可以在可以使用常量或文本的任何位置使用变量，但定义常量值的表达式除外。</span><span class="sxs-lookup"><span data-stu-id="03f75-114">You can use a variable anywhere you can use a constant or a literal, except in an expression that defines the value of a constant.</span></span>

  <span data-ttu-id="03f75-115">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="03f75-115">\-or-</span></span>

- <span data-ttu-id="03f75-116">使用等号后面的变量名 `=`) 在赋值语句中 (。</span><span class="sxs-lookup"><span data-stu-id="03f75-116">Use the variable name following the equal (`=`) sign in an assignment statement.</span></span>

  <span data-ttu-id="03f75-117">下面的示例读取变量的值 `startValue` ，然后 `counter` 在表达式中使用该变量的值。</span><span class="sxs-lookup"><span data-stu-id="03f75-117">The following example reads the value of the variable `startValue` and then uses the value of the variable `counter` in an expression.</span></span>

  ```vb
  counter = startValue
  cellValue = (counter + 5) ^ 2
  ```

  <span data-ttu-id="03f75-118">变量的值将作为常数加入表达式，然后将其存储在赋值语句左侧的变量或属性中。</span><span class="sxs-lookup"><span data-stu-id="03f75-118">The value of the variable participates in the expression just as a constant would, and then it is stored in the variable or property on the left side of the assignment statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="03f75-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="03f75-119">See also</span></span>

- [<span data-ttu-id="03f75-120">变量</span><span class="sxs-lookup"><span data-stu-id="03f75-120">Variables</span></span>](index.md)
- [<span data-ttu-id="03f75-121">变量声明</span><span class="sxs-lookup"><span data-stu-id="03f75-121">Variable Declaration</span></span>](variable-declaration.md)
- [<span data-ttu-id="03f75-122">对象变量</span><span class="sxs-lookup"><span data-stu-id="03f75-122">Object Variables</span></span>](object-variables.md)
