---
description: 了解详细信息： Visual Basic 中属性和变量之间的差异
title: 属性和变量之间的差异
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- variables [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- variables [Visual Basic], definition
- Visual Basic code, variables
- Visual Basic code, properties
- properties [Visual Basic], values
- properties [Visual Basic], defined
- variables [Visual Basic], and properties
- properties [Visual Basic], and variables
ms.assetid: 7a03a8be-5381-431f-bd7c-16e887e4e07b
ms.openlocfilehash: 6118d37616f3df1f21dda8e3a6392b6a6f37a24e
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100464711"
---
# <a name="differences-between-properties-and-variables-in-visual-basic"></a><span data-ttu-id="1af94-103">Visual Basic 中属性和变量的差异</span><span class="sxs-lookup"><span data-stu-id="1af94-103">Differences Between Properties and Variables in Visual Basic</span></span>

<span data-ttu-id="1af94-104">变量和属性都表示可以访问的值。</span><span class="sxs-lookup"><span data-stu-id="1af94-104">Variables and properties both represent values that you can access.</span></span> <span data-ttu-id="1af94-105">但在存储和实现方面存在差异。</span><span class="sxs-lookup"><span data-stu-id="1af94-105">However, there are differences in storage and implementation.</span></span>  
  
## <a name="variables"></a><span data-ttu-id="1af94-106">变量</span><span class="sxs-lookup"><span data-stu-id="1af94-106">Variables</span></span>  

 <span data-ttu-id="1af94-107">*变量* 直接对应于内存位置。</span><span class="sxs-lookup"><span data-stu-id="1af94-107">A *variable* corresponds directly to a memory location.</span></span> <span data-ttu-id="1af94-108">使用单个声明语句定义变量。</span><span class="sxs-lookup"><span data-stu-id="1af94-108">You define a variable with a single declaration statement.</span></span> <span data-ttu-id="1af94-109">变量可以是在过程中定义的 *本地变量*，只能在该过程中使用，也可以是在模块、类或结构中定义但不在任何过程内的 *成员变量*。</span><span class="sxs-lookup"><span data-stu-id="1af94-109">A variable can be a *local variable*, defined inside a procedure and available only within that procedure, or it can be a *member variable*, defined in a module, class, or structure but not inside any procedure.</span></span> <span data-ttu-id="1af94-110">成员变量也称为 *字段*。</span><span class="sxs-lookup"><span data-stu-id="1af94-110">A member variable is also called a *field*.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="1af94-111">属性</span><span class="sxs-lookup"><span data-stu-id="1af94-111">Properties</span></span>  

 <span data-ttu-id="1af94-112">*属性* 是在模块、类或结构上定义的数据元素。</span><span class="sxs-lookup"><span data-stu-id="1af94-112">A *property* is a data element defined on a module, class, or structure.</span></span> <span data-ttu-id="1af94-113">使用和语句之间的代码块定义属性 `Property` `End Property` 。</span><span class="sxs-lookup"><span data-stu-id="1af94-113">You define a property with a code block between the `Property` and `End Property` statements.</span></span> <span data-ttu-id="1af94-114">代码块包含 `Get` 过程和 `Set` /或过程。</span><span class="sxs-lookup"><span data-stu-id="1af94-114">The code block contains a `Get` procedure, a `Set` procedure, or both.</span></span> <span data-ttu-id="1af94-115">这些过程称为 *属性过程* 或 *属性访问器*。</span><span class="sxs-lookup"><span data-stu-id="1af94-115">These procedures are called *property procedures* or *property accessors*.</span></span> <span data-ttu-id="1af94-116">除了检索或存储属性值以外，还可以执行自定义操作，如更新访问计数器。</span><span class="sxs-lookup"><span data-stu-id="1af94-116">In addition to retrieving or storing the property's value, they can also perform custom actions, such as updating an access counter.</span></span>  
  
## <a name="differences"></a><span data-ttu-id="1af94-117">差异</span><span class="sxs-lookup"><span data-stu-id="1af94-117">Differences</span></span>  

 <span data-ttu-id="1af94-118">下表显示了变量和属性之间的一些重要差异。</span><span class="sxs-lookup"><span data-stu-id="1af94-118">The following table shows some important differences between variables and properties.</span></span>  
  
|<span data-ttu-id="1af94-119">差异点</span><span class="sxs-lookup"><span data-stu-id="1af94-119">Point of difference</span></span>|<span data-ttu-id="1af94-120">变量</span><span class="sxs-lookup"><span data-stu-id="1af94-120">Variable</span></span>|<span data-ttu-id="1af94-121">properties</span><span class="sxs-lookup"><span data-stu-id="1af94-121">Property</span></span>|  
|-------------------------|--------------|--------------|  
|<span data-ttu-id="1af94-122">声明</span><span class="sxs-lookup"><span data-stu-id="1af94-122">Declaration</span></span>|<span data-ttu-id="1af94-123">单个声明语句</span><span class="sxs-lookup"><span data-stu-id="1af94-123">Single declaration statement</span></span>|<span data-ttu-id="1af94-124">代码块中的一系列语句</span><span class="sxs-lookup"><span data-stu-id="1af94-124">Series of statements in a code block</span></span>|  
|<span data-ttu-id="1af94-125">实现</span><span class="sxs-lookup"><span data-stu-id="1af94-125">Implementation</span></span>|<span data-ttu-id="1af94-126">单个存储位置</span><span class="sxs-lookup"><span data-stu-id="1af94-126">Single storage location</span></span>|<span data-ttu-id="1af94-127">可执行代码 (属性过程) </span><span class="sxs-lookup"><span data-stu-id="1af94-127">Executable code (property procedures)</span></span>|  
|<span data-ttu-id="1af94-128">存储</span><span class="sxs-lookup"><span data-stu-id="1af94-128">Storage</span></span>|<span data-ttu-id="1af94-129">直接与变量的值关联</span><span class="sxs-lookup"><span data-stu-id="1af94-129">Directly associated with variable's value</span></span>|<span data-ttu-id="1af94-130">通常，内部存储在属性的包含类或模块外部不可用</span><span class="sxs-lookup"><span data-stu-id="1af94-130">Typically has internal storage not available outside the property's containing class or module</span></span><br /><br /> <span data-ttu-id="1af94-131">属性的值不能作为存储元素<sup>1</sup>存在，也可能不存在。</span><span class="sxs-lookup"><span data-stu-id="1af94-131">Property's value might or might not exist as a stored element <sup>1</sup></span></span>|  
|<span data-ttu-id="1af94-132">可执行代码</span><span class="sxs-lookup"><span data-stu-id="1af94-132">Executable code</span></span>|<span data-ttu-id="1af94-133">无</span><span class="sxs-lookup"><span data-stu-id="1af94-133">None</span></span>|<span data-ttu-id="1af94-134">必须至少有一个过程</span><span class="sxs-lookup"><span data-stu-id="1af94-134">Must have at least one procedure</span></span>|  
|<span data-ttu-id="1af94-135">读写访问权限</span><span class="sxs-lookup"><span data-stu-id="1af94-135">Read and write access</span></span>|<span data-ttu-id="1af94-136">读/写或只读</span><span class="sxs-lookup"><span data-stu-id="1af94-136">Read/write or read-only</span></span>|<span data-ttu-id="1af94-137">读/写、只读或只写</span><span class="sxs-lookup"><span data-stu-id="1af94-137">Read/write, read-only, or write-only</span></span>|  
|<span data-ttu-id="1af94-138">除了接受或返回值外， (自定义操作) </span><span class="sxs-lookup"><span data-stu-id="1af94-138">Custom actions (in addition to accepting or returning value)</span></span>|<span data-ttu-id="1af94-139">不可用</span><span class="sxs-lookup"><span data-stu-id="1af94-139">Not possible</span></span>|<span data-ttu-id="1af94-140">可以在设置或检索属性值的过程中执行</span><span class="sxs-lookup"><span data-stu-id="1af94-140">Can be performed as part of setting or retrieving property value</span></span>|  
  
 <span data-ttu-id="1af94-141"><sup>1</sup> 与变量不同，属性的值可能不会直接对应于单个存储项。</span><span class="sxs-lookup"><span data-stu-id="1af94-141"><sup>1</sup> Unlike a variable, the value of a property might not correspond directly to a single item of storage.</span></span> <span data-ttu-id="1af94-142">为了方便或安全，存储区可能会拆分为若干个部分，或者值可能以加密形式存储。</span><span class="sxs-lookup"><span data-stu-id="1af94-142">The storage might be split into pieces for convenience or security, or the value might be stored in an encrypted form.</span></span> <span data-ttu-id="1af94-143">在这些情况下，该 `Get` 过程会组装部分或解密存储的值，并且该 `Set` 过程将加密新值或将其拆分为构成存储。</span><span class="sxs-lookup"><span data-stu-id="1af94-143">In these cases the `Get` procedure would assemble the pieces or decrypt the stored value, and the `Set` procedure would encrypt the new value or split it into the constituent storage.</span></span> <span data-ttu-id="1af94-144">属性值可以是暂时的，如一天中的时间，在这种情况下， `Get` 每次访问该属性时，该过程会动态计算该属性。</span><span class="sxs-lookup"><span data-stu-id="1af94-144">A property value might be ephemeral, like time of day, in which case the `Get` procedure would calculate it on the fly each time you access the property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1af94-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="1af94-145">See also</span></span>

- [<span data-ttu-id="1af94-146">Property 过程</span><span class="sxs-lookup"><span data-stu-id="1af94-146">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="1af94-147">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="1af94-147">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="1af94-148">Property Statement</span><span class="sxs-lookup"><span data-stu-id="1af94-148">Property Statement</span></span>](../../../language-reference/statements/property-statement.md)
- [<span data-ttu-id="1af94-149">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="1af94-149">Dim Statement</span></span>](../../../language-reference/statements/dim-statement.md)
- [<span data-ttu-id="1af94-150">如何：创建属性</span><span class="sxs-lookup"><span data-stu-id="1af94-150">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="1af94-151">如何：声明具有混合访问级别的属性</span><span class="sxs-lookup"><span data-stu-id="1af94-151">How to: Declare a Property with Mixed Access Levels</span></span>](./how-to-declare-a-property-with-mixed-access-levels.md)
- [<span data-ttu-id="1af94-152">如何：调用 Property 过程</span><span class="sxs-lookup"><span data-stu-id="1af94-152">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="1af94-153">如何：在 Visual Basic 中声明和调用默认属性</span><span class="sxs-lookup"><span data-stu-id="1af94-153">How to: Declare and Call a Default Property in Visual Basic</span></span>](./how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="1af94-154">如何：在属性中放置值</span><span class="sxs-lookup"><span data-stu-id="1af94-154">How to: Put a Value in a Property</span></span>](./how-to-put-a-value-in-a-property.md)
- [<span data-ttu-id="1af94-155">如何：从属性获取值</span><span class="sxs-lookup"><span data-stu-id="1af94-155">How to: Get a Value from a Property</span></span>](./how-to-get-a-value-from-a-property.md)
