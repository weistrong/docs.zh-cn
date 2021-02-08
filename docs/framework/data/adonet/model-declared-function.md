---
description: 详细了解：模型声明函数
title: 模型声明函数
ms.date: 03/30/2017
ms.assetid: aba87f13-5685-4f6b-ad14-918e8a7d5c2a
ms.openlocfilehash: c9a5cedb8c9706aa0d299635f60f762b92ca6d78
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786259"
---
# <a name="model-declared-function"></a><span data-ttu-id="2e8cd-103">模型声明函数</span><span class="sxs-lookup"><span data-stu-id="2e8cd-103">model-declared function</span></span>

<span data-ttu-id="2e8cd-104">*模型声明函数* 是在概念模型中声明的、但未在该概念模型中定义的函数。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-104">A *model-declared function* is a function that is declared in a conceptual model, but is not defined in that conceptual model.</span></span> <span data-ttu-id="2e8cd-105">该函数可能是在承载或存储环境中定义的。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-105">The function might be defined in the hosting or storage environment.</span></span> <span data-ttu-id="2e8cd-106">例如，模型声明函数可能映射至在数据库中定义的函数，从而在概念模型中提供服务器端的功能。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-106">For example, a model-declared function might be mapped to a function that is defined in a database, thus exposing server-side functionality in the conceptual model.</span></span>  
  
 <span data-ttu-id="2e8cd-107">模型声明函数的声明包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="2e8cd-107">The declaration of a model-declared function contains the following information:</span></span>  
  
- <span data-ttu-id="2e8cd-108">函数的名称。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-108">The name of the function.</span></span> <span data-ttu-id="2e8cd-109">（必需）</span><span class="sxs-lookup"><span data-stu-id="2e8cd-109">(Required)</span></span>  
  
- <span data-ttu-id="2e8cd-110">返回值的类型。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-110">The type of the return value.</span></span> <span data-ttu-id="2e8cd-111">(可选)</span><span class="sxs-lookup"><span data-stu-id="2e8cd-111">(Optional)</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="2e8cd-112">如果未指定返回值，则返回类型为 void。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-112">If no return value is specified, the return type is void.</span></span>  
  
- <span data-ttu-id="2e8cd-113">参数信息，包括参数名和类型。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-113">Parameter information, including parameter name and type.</span></span> <span data-ttu-id="2e8cd-114">(可选)</span><span class="sxs-lookup"><span data-stu-id="2e8cd-114">(Optional)</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e8cd-115">示例</span><span class="sxs-lookup"><span data-stu-id="2e8cd-115">Example</span></span>  

 <span data-ttu-id="2e8cd-116">[ADO.NET 实体框架](./ef/index.md)使用一种特定于域的语言 (DSL) 称为概念架构定义语言 ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) 来定义概念模型。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-116">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) to define conceptual models.</span></span> <span data-ttu-id="2e8cd-117">在 CSDL 中，模型声明函数的一个实现是使用 [FunctionImport 元素](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#functionimport-element-csdl))  (函数导入。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-117">In CSDL, one implementation of a model-declared function is a function import (using the [FunctionImport element](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#functionimport-element-csdl)).</span></span> <span data-ttu-id="2e8cd-118">下面的 CSDL 定义了一个实体容器，其中包含一个函数导入定义。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-118">The following CSDL defines an entity container with a function import definition.</span></span> <span data-ttu-id="2e8cd-119">请注意，由于未指定返回类型，因而该函数的返回类型为 void。</span><span class="sxs-lookup"><span data-stu-id="2e8cd-119">Note that the return type for the function is void since no return type is specified.</span></span>  
  
 [!code-xml[EDM_Example_Model#FunctionImport](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#functionimport)]  
  
## <a name="see-also"></a><span data-ttu-id="2e8cd-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e8cd-120">See also</span></span>

- [<span data-ttu-id="2e8cd-121">实体数据模型关键概念</span><span class="sxs-lookup"><span data-stu-id="2e8cd-121">Entity Data Model Key Concepts</span></span>](entity-data-model-key-concepts.md)
- [<span data-ttu-id="2e8cd-122">实体数据模型</span><span class="sxs-lookup"><span data-stu-id="2e8cd-122">Entity Data Model</span></span>](entity-data-model.md)
