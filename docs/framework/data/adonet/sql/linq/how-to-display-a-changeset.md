---
description: 了解详细信息：如何：显示变更集
title: 如何：显示变更集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 126e7245-c5a0-4ebf-800d-cc1fcf9cd0ab
ms.openlocfilehash: e5ff7aebcc74ded1300433a3bf7b280db3a11b28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786012"
---
# <a name="how-to-display-a-changeset"></a><span data-ttu-id="3b90e-103">如何：显示变更集</span><span class="sxs-lookup"><span data-stu-id="3b90e-103">How to: Display a ChangeSet</span></span>

<span data-ttu-id="3b90e-104">可以通过使用 <xref:System.Data.Linq.DataContext> 来查看由 <xref:System.Data.Linq.DataContext.GetChangeSet%2A> 跟踪的更改。</span><span class="sxs-lookup"><span data-stu-id="3b90e-104">You can view changes tracked by a <xref:System.Data.Linq.DataContext> by using <xref:System.Data.Linq.DataContext.GetChangeSet%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3b90e-105">示例</span><span class="sxs-lookup"><span data-stu-id="3b90e-105">Example</span></span>  

 <span data-ttu-id="3b90e-106">下面的示例检索所在城市为伦敦的客户，将其所在城市更改为巴黎，然后将所做的更改提交回数据库。</span><span class="sxs-lookup"><span data-stu-id="3b90e-106">The following example retrieves customers whose city is London, changes the city to Paris, and submits the changes back to the database.</span></span>  
  
 [!code-csharp[DLinqDebuggingSupport#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#2)]
 [!code-vb[DLinqDebuggingSupport#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#2)]  
  
 <span data-ttu-id="3b90e-107">执行此代码所得到的输出与如下内容类似。</span><span class="sxs-lookup"><span data-stu-id="3b90e-107">Output from this code appears similar to the following.</span></span> <span data-ttu-id="3b90e-108">请注意，结尾处的摘要显示做了八项更改。</span><span class="sxs-lookup"><span data-stu-id="3b90e-108">Note that the summary at the end shows that eight changes were made.</span></span>  

 ```console
CustomerID: AROUT
   Original value: London
   Updated value: Paris
CustomerID: BSBEV
   Original value: London
   Updated value: Paris
CustomerID: CONSH
   Original value: London
   Updated value: Paris
CustomerID: EASTC
   Original value: London
   Updated value: Paris
CustomerID: NORTS
    Original value: London
    Updated value: Paris
CustomerID: PARIS
    Original value: London
    Updated value: Paris
CustomerID: SEVES
    Original value: London
    Updated value: Paris
CustomerID: SPECD
    Original value: London
    Updated value: Paris
Total changes: {Added: 0, Removed: 0, Modified: 8}
```
  
## <a name="see-also"></a><span data-ttu-id="3b90e-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b90e-109">See also</span></span>

- [<span data-ttu-id="3b90e-110">调试支持</span><span class="sxs-lookup"><span data-stu-id="3b90e-110">Debugging Support</span></span>](debugging-support.md)
