---
description: 了解更多：对象标识
title: 对象标识
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c788f2f9-65cc-4455-9907-e8388a268e00
ms.openlocfilehash: 1e525250e37e697e33ee53ea59b973882633ec15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695510"
---
# <a name="object-identity"></a><span data-ttu-id="c43da-103">对象标识</span><span class="sxs-lookup"><span data-stu-id="c43da-103">Object Identity</span></span>

<span data-ttu-id="c43da-104">运行库中的对象具有唯一标识。</span><span class="sxs-lookup"><span data-stu-id="c43da-104">Objects in the runtime have unique identities.</span></span> <span data-ttu-id="c43da-105">引用同一对象的两个变量实际上是引用此对象的同一实例。</span><span class="sxs-lookup"><span data-stu-id="c43da-105">Two variables that refer to the same object actually refer to the same instance of the object.</span></span> <span data-ttu-id="c43da-106">因为这一事实，您通过一个变量做出更改后，立即就可以通过另一个变量看到这些更改。</span><span class="sxs-lookup"><span data-stu-id="c43da-106">Because of this fact, changes that you make by way of a path through one variable are immediately visible through the other.</span></span>  
  
 <span data-ttu-id="c43da-107">关系数据库表中的行不具有唯一标识。</span><span class="sxs-lookup"><span data-stu-id="c43da-107">Rows in a relational database table do not have unique identities.</span></span> <span data-ttu-id="c43da-108">由于每一行都具有唯一的主键，因此任何两行都不会共用同一键值。</span><span class="sxs-lookup"><span data-stu-id="c43da-108">Because each row has a unique primary key, no two rows share the same key value.</span></span> <span data-ttu-id="c43da-109">但是，这一事实仅限于数据库表的内容。</span><span class="sxs-lookup"><span data-stu-id="c43da-109">However, this fact constrains only the contents of the database table.</span></span>  
  
 <span data-ttu-id="c43da-110">实际上，通常都是将数据从数据库中提取出来放入另一层中，应用程序在该层对数据进行处理。</span><span class="sxs-lookup"><span data-stu-id="c43da-110">In reality, data is most often brought out of the database and into a different tier, where an application works with it.</span></span> <span data-ttu-id="c43da-111">这就是 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 支持的模型。</span><span class="sxs-lookup"><span data-stu-id="c43da-111">This is the model that [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] supports.</span></span> <span data-ttu-id="c43da-112">将数据作为行从数据库中提取出来时，您不期望表示相同数据的两行实际上对应于相同的行实例。</span><span class="sxs-lookup"><span data-stu-id="c43da-112">When data is brought out of the database as rows, you have no expectation that two rows that represent the same data actually correspond to the same row instances.</span></span> <span data-ttu-id="c43da-113">如果您查询特定客户两次，您将获得两行数据。</span><span class="sxs-lookup"><span data-stu-id="c43da-113">If you query for a specific customer two times, you get two rows of data.</span></span> <span data-ttu-id="c43da-114">每一行包含相同的信息。</span><span class="sxs-lookup"><span data-stu-id="c43da-114">Each row contains the same information.</span></span>  
  
 <span data-ttu-id="c43da-115">对于对象，您的期望则大不一样。</span><span class="sxs-lookup"><span data-stu-id="c43da-115">With objects you expect something very different.</span></span> <span data-ttu-id="c43da-116">您期望在您反复向 <xref:System.Data.Linq.DataContext> 索取相同的信息时，它实际上会为您提供同一对象实例。</span><span class="sxs-lookup"><span data-stu-id="c43da-116">You expect that if you ask the <xref:System.Data.Linq.DataContext> for the same information repeatedly, it will in fact give you the same object instance.</span></span> <span data-ttu-id="c43da-117">您之所以期望这种行为，是因为对象对您的应用程序而言有着特殊的含义，您期望它们的行为像实物一样。</span><span class="sxs-lookup"><span data-stu-id="c43da-117">You expect this behavior because objects have special meaning for your application and you expect them to behave like objects.</span></span> <span data-ttu-id="c43da-118">您将它们设计为层次结构或关系图。</span><span class="sxs-lookup"><span data-stu-id="c43da-118">You designed them as hierarchies or graphs.</span></span> <span data-ttu-id="c43da-119">您希望像检索实物一样检索它们，而不希望仅仅因为您多次索要同一内容而收到大量的复制实例。</span><span class="sxs-lookup"><span data-stu-id="c43da-119">You expect to retrieve them as such and not to receive multitudes of replicated instances just because you asked for the same thing more than one time.</span></span>  
  
 <span data-ttu-id="c43da-120">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，<xref:System.Data.Linq.DataContext> 管理对象标识。</span><span class="sxs-lookup"><span data-stu-id="c43da-120">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Data.Linq.DataContext> manages object identity.</span></span> <span data-ttu-id="c43da-121">只要您从数据库中检索新行，该行就会由其主键记录到标识表中，并且会创建一个新的对象。</span><span class="sxs-lookup"><span data-stu-id="c43da-121">Whenever you retrieve a new row from the database, the row is logged in an identity table by its primary key, and a new object is created.</span></span> <span data-ttu-id="c43da-122">只要您检索该行，就会将原始对象实例传递回应用程序。</span><span class="sxs-lookup"><span data-stu-id="c43da-122">Whenever you retrieve that same row, the original object instance is handed back to the application.</span></span> <span data-ttu-id="c43da-123">通过这种方式，<xref:System.Data.Linq.DataContext> 将数据库看到的标识（即主键）的概念转换成相应语言看到的标识（即实例）的概念。</span><span class="sxs-lookup"><span data-stu-id="c43da-123">In this manner the <xref:System.Data.Linq.DataContext> translates the concept of identity as seen by the database (that is, primary keys) into the concept of identity seen by the language (that is, instances).</span></span> <span data-ttu-id="c43da-124">应用程序只看到处于第一次检索时的状态的对象。</span><span class="sxs-lookup"><span data-stu-id="c43da-124">The application only sees the object in the state that it was first retrieved.</span></span> <span data-ttu-id="c43da-125">新数据如果不同，则会被丢弃。</span><span class="sxs-lookup"><span data-stu-id="c43da-125">The new data, if different, is discarded.</span></span> <span data-ttu-id="c43da-126">有关详细信息，请参阅 [从标识缓存中检索对象](retrieving-objects-from-the-identity-cache.md)。</span><span class="sxs-lookup"><span data-stu-id="c43da-126">For more information, see [Retrieving Objects from the Identity Cache](retrieving-objects-from-the-identity-cache.md).</span></span>  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="c43da-127">使用此方法来管理本地对象的完整性，以支持开放式更新。</span><span class="sxs-lookup"><span data-stu-id="c43da-127">uses this approach to manage the integrity of local objects in order to support optimistic updates.</span></span> <span data-ttu-id="c43da-128">由于在最初创建对象后唯一发生的更改是由应用程序做出的，因此应用程序的意向是很明确的。</span><span class="sxs-lookup"><span data-stu-id="c43da-128">Because the only changes that occur after the object is at first created are those made by the application, the intent of the application is clear.</span></span> <span data-ttu-id="c43da-129">如果在中间阶段外部某一方做了更改，则在调用 `SubmitChanges()` 时会识别出这些更改。</span><span class="sxs-lookup"><span data-stu-id="c43da-129">If changes by an outside party have occurred in the interim, they are identified at the time `SubmitChanges()` is called.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c43da-130">如果查询请求的对象易被识别为已检索到的对象，则不会执行查询。</span><span class="sxs-lookup"><span data-stu-id="c43da-130">If the object requested by the query is easily identifiable as one already retrieved, no query is executed.</span></span> <span data-ttu-id="c43da-131">标识表用作以前检索到的所有对象的缓存。</span><span class="sxs-lookup"><span data-stu-id="c43da-131">The identity table acts as a cache of all previously retrieved objects.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="c43da-132">示例</span><span class="sxs-lookup"><span data-stu-id="c43da-132">Examples</span></span>  
  
### <a name="object-caching-example-1"></a><span data-ttu-id="c43da-133">对象缓存示例 1</span><span class="sxs-lookup"><span data-stu-id="c43da-133">Object Caching Example 1</span></span>  

 <span data-ttu-id="c43da-134">在此示例中，如果您执行同一查询两次，则您每次都会收到对内存中同一对象的引用。</span><span class="sxs-lookup"><span data-stu-id="c43da-134">In this example, if you execute the same query two times, you receive a reference to the same object in memory every time.</span></span>  
  
 [!code-csharp[DLinqObjectIdentity#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqObjectIdentity/cs/Program.cs#1)]
 [!code-vb[DLinqObjectIdentity#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqObjectIdentity/vb/Module1.vb#1)]  
  
### <a name="object-caching-example-2"></a><span data-ttu-id="c43da-135">对象缓存示例 2</span><span class="sxs-lookup"><span data-stu-id="c43da-135">Object Caching Example 2</span></span>  

 <span data-ttu-id="c43da-136">在此示例中，如果您执行返回数据库中同一行的不同查询，则您每次都会收到对内存中同一对象的引用。</span><span class="sxs-lookup"><span data-stu-id="c43da-136">In this example, if you execute different queries that return the same row from the database, you receive a reference to the same object in memory every time.</span></span>  
  
 [!code-csharp[DLinqObjectIdentity#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqObjectIdentity/cs/Program.cs#2)]
 [!code-vb[DLinqObjectIdentity#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqObjectIdentity/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="c43da-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="c43da-137">See also</span></span>

- [<span data-ttu-id="c43da-138">背景信息</span><span class="sxs-lookup"><span data-stu-id="c43da-138">Background Information</span></span>](background-information.md)
