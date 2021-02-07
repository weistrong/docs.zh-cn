---
description: 详细了解：模型定义函数
title: 模型定义函数
ms.date: 03/30/2017
ms.assetid: 8bb2edc8-e8e7-44c2-adc7-f44e11bda4f0
ms.openlocfilehash: 146ef4a8ad8c38897b8e56b6bc1485e1e40754cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723733"
---
# <a name="model-defined-function"></a><span data-ttu-id="67dee-103">模型定义函数</span><span class="sxs-lookup"><span data-stu-id="67dee-103">model-defined function</span></span>

<span data-ttu-id="67dee-104">*模型定义的函数* 是在概念模型中定义的函数。</span><span class="sxs-lookup"><span data-stu-id="67dee-104">A *model-defined function* is a function that is defined in a conceptual model.</span></span> <span data-ttu-id="67dee-105">模型定义函数的主体以 [实体 SQL](./ef/language-reference/entity-sql-language.md)表示，这允许独立于数据源中支持的规则或语言来表示函数。</span><span class="sxs-lookup"><span data-stu-id="67dee-105">The body of a model-defined function is expressed in [Entity SQL](./ef/language-reference/entity-sql-language.md), which allows for the function to be expressed independently of rules or languages supported in the data source.</span></span>  
  
 <span data-ttu-id="67dee-106">模型定义函数的定义包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="67dee-106">A definition for a model-defined function contains the following information:</span></span>  
  
- <span data-ttu-id="67dee-107">函数名称。</span><span class="sxs-lookup"><span data-stu-id="67dee-107">A function name.</span></span> <span data-ttu-id="67dee-108">（必需）</span><span class="sxs-lookup"><span data-stu-id="67dee-108">(Required)</span></span>  
  
- <span data-ttu-id="67dee-109">返回值的类型。</span><span class="sxs-lookup"><span data-stu-id="67dee-109">The type of the return value.</span></span> <span data-ttu-id="67dee-110">(可选)</span><span class="sxs-lookup"><span data-stu-id="67dee-110">(Optional)</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="67dee-111">如果未指定返回类型，则返回值为 void。</span><span class="sxs-lookup"><span data-stu-id="67dee-111">If no return type is specified, the return value is void.</span></span>  
  
- <span data-ttu-id="67dee-112">参数信息。</span><span class="sxs-lookup"><span data-stu-id="67dee-112">Parameter information.</span></span> <span data-ttu-id="67dee-113">(可选)</span><span class="sxs-lookup"><span data-stu-id="67dee-113">(Optional)</span></span>  
  
- <span data-ttu-id="67dee-114">定义函数主体的 [实体 SQL](./ef/language-reference/entity-sql-language.md) 表达式。</span><span class="sxs-lookup"><span data-stu-id="67dee-114">An [Entity SQL](./ef/language-reference/entity-sql-language.md) expression that defines the body of the function.</span></span>  
  
 <span data-ttu-id="67dee-115">请注意，模型定义函数不支持输出参数。</span><span class="sxs-lookup"><span data-stu-id="67dee-115">Note that model-defined functions do not support output parameters.</span></span> <span data-ttu-id="67dee-116">这一限制可以保证无法对模型定义函数进行编写。</span><span class="sxs-lookup"><span data-stu-id="67dee-116">This restriction is in place so that model-defined functions can be composed.</span></span>  
  
## <a name="example"></a><span data-ttu-id="67dee-117">示例</span><span class="sxs-lookup"><span data-stu-id="67dee-117">Example</span></span>  

 <span data-ttu-id="67dee-118">下图显示了一个具有三个实体类型的概念模型：`Book`、`Publisher` 和 `Author`。</span><span class="sxs-lookup"><span data-stu-id="67dee-118">The diagram below shows a conceptual model with three entity types: `Book`, `Publisher`, and `Author`.</span></span>  
  
 ![显示具有发布日期的模型的屏幕截图。](./media/model-defined-function/model-published-date-three-entity-types.gif)  
  
 <span data-ttu-id="67dee-120">[ADO.NET 实体框架](./ef/index.md)使用一种特定于域的语言 (DSL) 称为概念架构定义语言 ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) 来定义概念模型。</span><span class="sxs-lookup"><span data-stu-id="67dee-120">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) to define conceptual models.</span></span> <span data-ttu-id="67dee-121">下面的 CSDL 在概念模型中定义了一个函数，它返回自某个 `Book` 实例（如上图所示）出版以来的年数。</span><span class="sxs-lookup"><span data-stu-id="67dee-121">The following CSDL defines a function in the conceptual model that returns the numbers of years since an instance of a `Book` (in the diagram above) was published.</span></span>  
  
 [!code-xml[EDM_Example_Model#ModelDefinedFunction](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#modeldefinedfunction)]  
  
## <a name="see-also"></a><span data-ttu-id="67dee-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="67dee-122">See also</span></span>

- [<span data-ttu-id="67dee-123">实体数据模型关键概念</span><span class="sxs-lookup"><span data-stu-id="67dee-123">Entity Data Model Key Concepts</span></span>](entity-data-model-key-concepts.md)
- [<span data-ttu-id="67dee-124">实体数据模型</span><span class="sxs-lookup"><span data-stu-id="67dee-124">Entity Data Model</span></span>](entity-data-model.md)
- [<span data-ttu-id="67dee-125">实体数据模型：基元数据类型</span><span class="sxs-lookup"><span data-stu-id="67dee-125">Entity Data Model: Primitive Data Types</span></span>](entity-data-model-primitive-data-types.md)
