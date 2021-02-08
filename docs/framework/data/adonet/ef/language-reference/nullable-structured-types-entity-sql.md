---
description: '详细了解以下内容：可为 Null 的结构化类型 (实体 SQL) '
title: 可以为 null 的结构化类型 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: ae006fa9-997e-45bb-8a04-a7f62026171e
ms.openlocfilehash: bf303c9cd61fad2c2a8ffedf338bb3a8876db27b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802081"
---
# <a name="nullable-structured-types-entity-sql"></a><span data-ttu-id="7d00a-103">可以为 null 的结构化类型 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="7d00a-103">Nullable Structured Types (Entity SQL)</span></span>

<span data-ttu-id="7d00a-104">结构化类型的 `null` 实例是不存在的实例。</span><span class="sxs-lookup"><span data-stu-id="7d00a-104">A `null` instance of a structured type is an instance that does not exist.</span></span> <span data-ttu-id="7d00a-105">这不同于其中所有属性都具有 `null` 值的现有实例。</span><span class="sxs-lookup"><span data-stu-id="7d00a-105">This is different from an existing instance in which all properties have `null` values.</span></span>  
  
 <span data-ttu-id="7d00a-106">本主题介绍可以为 Null 的结构化类型，包括哪些类型可以为 null 以及哪些代码模式会产生可以为 Null 的结构化类型的 `null` 实例。</span><span class="sxs-lookup"><span data-stu-id="7d00a-106">This topic describes the nullable structured types, including which types are nullable and which code patterns produce `null` instances of structured nullable types.</span></span>  
  
## <a name="kinds-of-nullable-structured-types"></a><span data-ttu-id="7d00a-107">可以为 Null 的结构化类型的种类</span><span class="sxs-lookup"><span data-stu-id="7d00a-107">Kinds of Nullable Structured Types</span></span>  

 <span data-ttu-id="7d00a-108">有三种可以为 Null 的结构化类型：</span><span class="sxs-lookup"><span data-stu-id="7d00a-108">There are three kinds of nullable structure types:</span></span>  
  
- <span data-ttu-id="7d00a-109">行类型。</span><span class="sxs-lookup"><span data-stu-id="7d00a-109">Row types.</span></span>  
  
- <span data-ttu-id="7d00a-110">复杂类型。</span><span class="sxs-lookup"><span data-stu-id="7d00a-110">Complex types.</span></span>  
  
- <span data-ttu-id="7d00a-111">实体类型。</span><span class="sxs-lookup"><span data-stu-id="7d00a-111">Entity types.</span></span>  
  
## <a name="code-patterns-that-produce-null-instances-of-structured-types"></a><span data-ttu-id="7d00a-112">能够产生结构化类型的 null 实例的代码模式</span><span class="sxs-lookup"><span data-stu-id="7d00a-112">Code Patterns that Produce Null Instances of Structured Types</span></span>  

 <span data-ttu-id="7d00a-113">以下方案会产生 `null` 实例：</span><span class="sxs-lookup"><span data-stu-id="7d00a-113">The following scenarios produce `null` instances:</span></span>  
  
- <span data-ttu-id="7d00a-114">将 `null` 说明为结构化类型：</span><span class="sxs-lookup"><span data-stu-id="7d00a-114">Shaping `null` as a structured type:</span></span>  
  
    ```sql  
    TREAT (NULL AS StructuredType)  
    ```  
  
- <span data-ttu-id="7d00a-115">将基类型向上转换为派生类型：</span><span class="sxs-lookup"><span data-stu-id="7d00a-115">Upcasting of a base type to a derived type:</span></span>  
  
    ```sql  
    TREAT (BaseType AS DerivedType)  
    ```  
  
- <span data-ttu-id="7d00a-116">对 false 条件进行外部联接：</span><span class="sxs-lookup"><span data-stu-id="7d00a-116">Outer join on false condition:</span></span>  
  
    ```sql  
    Collection1 LEFT OUTER JOIN Collection2  
    ON FalseCondition  
    ```  
  
     <span data-ttu-id="7d00a-117">--或</span><span class="sxs-lookup"><span data-stu-id="7d00a-117">--or</span></span>  
  
    ```sql  
    Collection1 RIGHT OUTER JOIN Collection2  
    ON FalseCondition  
    ```  
  
     <span data-ttu-id="7d00a-118">--或</span><span class="sxs-lookup"><span data-stu-id="7d00a-118">--or</span></span>  
  
    ```sql  
    Collection1 FULL OUTER JOIN Collection2  
    ON FalseCondition  
    ```  
  
- <span data-ttu-id="7d00a-119">取消 `null` 引用的引用：</span><span class="sxs-lookup"><span data-stu-id="7d00a-119">Dereferencing a `null` reference:</span></span>  
  
    ```sql  
    DEREF(NullRef)  
    ```  
  
- <span data-ttu-id="7d00a-120">从空集合获取 ANYELEMENT：</span><span class="sxs-lookup"><span data-stu-id="7d00a-120">Obtaining ANYELEMENT from an empty collection:</span></span>  
  
    ```sql  
    ANYELEMENT(EmptyCollection)  
    ```  
  
- <span data-ttu-id="7d00a-121">检查结构化类型实例是否为 `null`：</span><span class="sxs-lookup"><span data-stu-id="7d00a-121">Checking for `null` instances of structured types:</span></span>  
  
    ```csharp  
    ...  
    for (int i = 0; i < reader.FieldCount; i++)  
    {  
        if (reader.IsDBNull(i))  
        {  
            Console.WriteLine("[NULL]");  
        }  
        else  
        {  
            Console.WriteLine(reader.GetValue(i).ToString());  
        }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7d00a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="7d00a-122">See also</span></span>

- [<span data-ttu-id="7d00a-123">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="7d00a-123">Entity SQL Overview</span></span>](entity-sql-overview.md)
