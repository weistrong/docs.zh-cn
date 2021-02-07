---
description: 了解详细信息：如何：使用事务对数据提交进行方括号
title: 如何：通过使用事务对数据提交进行分类
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 94044a31-de90-479b-935a-8159b4ae5c5a
ms.openlocfilehash: a1bbebfcdb4b65e83c4ac6dc9b87b06f33f2cb41
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739022"
---
# <a name="how-to-bracket-data-submissions-by-using-transactions"></a><span data-ttu-id="b10ce-103">如何：通过使用事务对数据提交进行分类</span><span class="sxs-lookup"><span data-stu-id="b10ce-103">How to: Bracket Data Submissions by Using Transactions</span></span>

<span data-ttu-id="b10ce-104">您可以使用 <xref:System.Transactions.TransactionScope> 来封闭您提交到数据库的数据。</span><span class="sxs-lookup"><span data-stu-id="b10ce-104">You can use <xref:System.Transactions.TransactionScope> to bracket your submissions to the database.</span></span> <span data-ttu-id="b10ce-105">有关详细信息，请参阅 [事务支持](transaction-support.md)。</span><span class="sxs-lookup"><span data-stu-id="b10ce-105">For more information, see [Transaction Support](transaction-support.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="b10ce-106">示例</span><span class="sxs-lookup"><span data-stu-id="b10ce-106">Example</span></span>  

 <span data-ttu-id="b10ce-107">下面的代码将数据库提交数据封闭在 <xref:System.Transactions.TransactionScope> 中。</span><span class="sxs-lookup"><span data-stu-id="b10ce-107">The following code encloses the database submission in a <xref:System.Transactions.TransactionScope>.</span></span>  
  
 [!code-csharp[DLinqSubmittingChanges#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#3)]
 [!code-vb[DLinqSubmittingChanges#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="b10ce-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="b10ce-108">See also</span></span>

- [<span data-ttu-id="b10ce-109">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="b10ce-109">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
- [<span data-ttu-id="b10ce-110">进行和提交数据更改</span><span class="sxs-lookup"><span data-stu-id="b10ce-110">Making and Submitting Data Changes</span></span>](making-and-submitting-data-changes.md)
- [<span data-ttu-id="b10ce-111">事务支持</span><span class="sxs-lookup"><span data-stu-id="b10ce-111">Transaction Support</span></span>](transaction-support.md)
