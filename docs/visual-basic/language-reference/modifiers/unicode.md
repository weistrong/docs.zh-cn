---
description: '了解详细信息： Unicode (Visual Basic) '
title: Unicode
ms.date: 07/20/2015
f1_keywords:
- vb.Unicode
helpviewer_keywords:
- Unicode, external references
- Declare statement [Visual Basic], marshaling strings
- Unicode keyword [Visual Basic]
- Unicode, marshaling strings
ms.assetid: 0021d5ff-3209-444e-8497-420f3e6ee075
ms.openlocfilehash: b0c71d8fdefe3f0d240201e0d57265e5c6081d50
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700710"
---
# <a name="unicode-visual-basic"></a><span data-ttu-id="026d3-103">Unicode (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="026d3-103">Unicode (Visual Basic)</span></span>

<span data-ttu-id="026d3-104">指定 Visual Basic 应将所有字符串封送到 Unicode 值，而不考虑所声明的外部过程的名称。</span><span class="sxs-lookup"><span data-stu-id="026d3-104">Specifies that Visual Basic should marshal all strings to Unicode values regardless of the name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="026d3-105">调用在项目外部定义的过程时，Visual Basic 编译器无权访问它必须具有的信息，以便正确调用过程。</span><span class="sxs-lookup"><span data-stu-id="026d3-105">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it must have in order to call the procedure correctly.</span></span> <span data-ttu-id="026d3-106">此信息包括过程的位置、标识方法、调用序列和返回类型，以及它使用的字符串字符集。</span><span class="sxs-lookup"><span data-stu-id="026d3-106">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="026d3-107">[Declare 语句](../statements/declare-statement.md)创建对外部过程的引用并提供此必要信息。</span><span class="sxs-lookup"><span data-stu-id="026d3-107">The [Declare Statement](../statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="026d3-108">`charsetmodifier`语句中的部分 `Declare` 提供了字符集信息以在调用外部过程的过程中封送字符串。</span><span class="sxs-lookup"><span data-stu-id="026d3-108">The `charsetmodifier` part in the `Declare` statement supplies the character set information to marshal strings during a call to the external procedure.</span></span> <span data-ttu-id="026d3-109">它还会影响 Visual Basic 搜索外部文件的外部过程名称的方式。</span><span class="sxs-lookup"><span data-stu-id="026d3-109">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="026d3-110">`Unicode`修饰符指定 Visual Basic 应将所有字符串封送为 Unicode 值，并且应在搜索过程中查找过程而不修改其名称。</span><span class="sxs-lookup"><span data-stu-id="026d3-110">The `Unicode` modifier specifies that Visual Basic should marshal all strings to Unicode values and should look up the procedure without modifying its name during the search.</span></span>  
  
 <span data-ttu-id="026d3-111">如果未指定字符集修饰符， `Ansi` 则默认为。</span><span class="sxs-lookup"><span data-stu-id="026d3-111">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="026d3-112">备注</span><span class="sxs-lookup"><span data-stu-id="026d3-112">Remarks</span></span>  

 <span data-ttu-id="026d3-113">`Unicode`可以在此上下文中使用修饰符：</span><span class="sxs-lookup"><span data-stu-id="026d3-113">The `Unicode` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="026d3-114">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="026d3-114">Declare Statement</span></span>](../statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="026d3-115">智能设备开发人员说明</span><span class="sxs-lookup"><span data-stu-id="026d3-115">Smart Device Developer Notes</span></span>  

 <span data-ttu-id="026d3-116">不支持此关键字。</span><span class="sxs-lookup"><span data-stu-id="026d3-116">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="026d3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="026d3-117">See also</span></span>

- [<span data-ttu-id="026d3-118">Ansi</span><span class="sxs-lookup"><span data-stu-id="026d3-118">Ansi</span></span>](ansi.md)
- [<span data-ttu-id="026d3-119">Auto</span><span class="sxs-lookup"><span data-stu-id="026d3-119">Auto</span></span>](auto.md)
- [<span data-ttu-id="026d3-120">关键字</span><span class="sxs-lookup"><span data-stu-id="026d3-120">Keywords</span></span>](../keywords/index.md)
