---
description: 了解详细信息：。 （成员访问）(Entity SQL)
title: . （成员访问）(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4733e3b2-3efa-4b96-b591-ac31350e96ad
ms.openlocfilehash: 94833d3525c7d17cadaef15065b3dcbdb43a6ded
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739373"
---
# <a name="-member-access-entity-sql"></a><span data-ttu-id="c05cd-105">.</span><span class="sxs-lookup"><span data-stu-id="c05cd-105">.</span></span> <span data-ttu-id="c05cd-106">（成员访问）(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c05cd-106">(Member Access) (Entity SQL)</span></span>

<span data-ttu-id="c05cd-107">点运算符 (。 ) 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 成员访问运算符。</span><span class="sxs-lookup"><span data-stu-id="c05cd-107">The dot operator (.) is the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] member access operator.</span></span> <span data-ttu-id="c05cd-108">使用成员访问运算符可生成结构化概念模型类型实例的属性或字段的值。</span><span class="sxs-lookup"><span data-stu-id="c05cd-108">You use the member access operator to yield the value of a property or field of an instance of structural conceptual model type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c05cd-109">语法</span><span class="sxs-lookup"><span data-stu-id="c05cd-109">Syntax</span></span>  
  
```sql  
expression.identifier  
```  
  
## <a name="arguments"></a><span data-ttu-id="c05cd-110">参数</span><span class="sxs-lookup"><span data-stu-id="c05cd-110">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="c05cd-111">结构化概念模型类型的实例。</span><span class="sxs-lookup"><span data-stu-id="c05cd-111">An instance of a structural conceptual model type.</span></span>  
  
 `identifier`  
 <span data-ttu-id="c05cd-112">属于对象实例的属性或字段。</span><span class="sxs-lookup"><span data-stu-id="c05cd-112">A property or field that belongs to an object instance.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c05cd-113">备注</span><span class="sxs-lookup"><span data-stu-id="c05cd-113">Remarks</span></span>  

 <span data-ttu-id="c05cd-114">点 (.) 运算符可以用于从记录中提取字段，类似于提取复杂类型或实体类型的属性。</span><span class="sxs-lookup"><span data-stu-id="c05cd-114">The dot (.) operator may be used to extract fields from a record, similar to extracting properties of a complex or entity type.</span></span> <span data-ttu-id="c05cd-115">例如，如果类型 Name 的 n 是类型 Person 的成员，而 p 是类型 Person 的实例，则 p.n 是合法的成员访问表达式，该表达式生成类型为 Name 的值。</span><span class="sxs-lookup"><span data-stu-id="c05cd-115">For example, if n of type Name is a member of type Person, and p is an instance of type Person, then p.n is a legal member access expression that yields a value of type Name.</span></span>  
  
 `select p.Name.FirstName from LOB.Person as p`  
  
## <a name="see-also"></a><span data-ttu-id="c05cd-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="c05cd-116">See also</span></span>

- [<span data-ttu-id="c05cd-117">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="c05cd-117">Entity SQL Reference</span></span>](entity-sql-reference.md)
