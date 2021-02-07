---
description: 了解详细信息：自定义操作：概述
title: 自定义操作：概述
ms.date: 03/30/2017
ms.assetid: a3546296-1443-4b88-aa6e-d41011041ba7
ms.openlocfilehash: bdcaf482f49b9c55fb7a1834b19b683ac2fa16bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729596"
---
# <a name="customizing-operations-overview"></a><span data-ttu-id="1d6d5-103">自定义操作：概述</span><span class="sxs-lookup"><span data-stu-id="1d6d5-103">Customizing Operations: Overview</span></span>

<span data-ttu-id="1d6d5-104">默认情况下，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 会根据映射生成动态 SQL 来执行插入、更新和删除操作。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-104">By default, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] generates dynamic SQL for insert, update, and delete operations based on mapping.</span></span> <span data-ttu-id="1d6d5-105">但在实践中，您通常需要添加您自己的业务逻辑来提供安全、验证等。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-105">However, in practice you typically want to add your own business logic to provide for security, validation, and so forth.</span></span>  
  
 <span data-ttu-id="1d6d5-106">用于自定义这些操作的 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 技术包括：</span><span class="sxs-lookup"><span data-stu-id="1d6d5-106">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] techniques for customizing these operations include the following.</span></span>  
  
## <a name="loading-options"></a><span data-ttu-id="1d6d5-107">加载选项</span><span class="sxs-lookup"><span data-stu-id="1d6d5-107">Loading Options</span></span>  

 <span data-ttu-id="1d6d5-108">在您的查询中，您可以控制在连接到数据库时检索多少与您的主目标相关的数据。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-108">In your queries, you can control how much data related to your main target is retrieved when you connect to the database.</span></span> <span data-ttu-id="1d6d5-109">此功能主要通过使用 <xref:System.Data.Linq.DataLoadOptions> 实现。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-109">This functionality is implemented largely by using <xref:System.Data.Linq.DataLoadOptions>.</span></span> <span data-ttu-id="1d6d5-110">有关详细信息，请参阅 [延迟与立即加载](deferred-versus-immediate-loading.md)。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-110">For more information, see [Deferred versus Immediate Loading](deferred-versus-immediate-loading.md).</span></span>  
  
## <a name="partial-methods"></a><span data-ttu-id="1d6d5-111">分部方法</span><span class="sxs-lookup"><span data-stu-id="1d6d5-111">Partial Methods</span></span>  

 <span data-ttu-id="1d6d5-112">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 在其默认映射中提供了分部方法，以帮助您实现自己的业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-112">In its default mapping, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] provides partial methods to help you implement your business logic.</span></span> <span data-ttu-id="1d6d5-113">有关详细信息，请参阅 [使用分部方法添加业务逻辑](adding-business-logic-by-using-partial-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-113">For more information, see [Adding Business Logic By Using Partial Methods](adding-business-logic-by-using-partial-methods.md).</span></span>  
  
## <a name="stored-procedures-and-user-defined-functions"></a><span data-ttu-id="1d6d5-114">存储过程和用户定义的函数</span><span class="sxs-lookup"><span data-stu-id="1d6d5-114">Stored Procedures and User-Defined Functions</span></span>  

 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="1d6d5-115">支持使用存储过程和用户定义的函数。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-115">supports the use of stored procedures and user-defined functions.</span></span> <span data-ttu-id="1d6d5-116">存储过程经常用来自定义操作。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-116">Stored procedures are frequently used to customize operations.</span></span> <span data-ttu-id="1d6d5-117">有关详细信息，请参阅[存储过程](stored-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="1d6d5-117">For more information, see [Stored Procedures](stored-procedures.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d6d5-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d6d5-118">See also</span></span>

- [<span data-ttu-id="1d6d5-119">自定义插入、更新和删除操作</span><span class="sxs-lookup"><span data-stu-id="1d6d5-119">Customizing Insert, Update, and Delete Operations</span></span>](customizing-insert-update-and-delete-operations.md)
