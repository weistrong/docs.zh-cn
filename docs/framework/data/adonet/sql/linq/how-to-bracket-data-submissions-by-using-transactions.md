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
# <a name="how-to-bracket-data-submissions-by-using-transactions"></a>如何：通过使用事务对数据提交进行分类

您可以使用 <xref:System.Transactions.TransactionScope> 来封闭您提交到数据库的数据。 有关详细信息，请参阅 [事务支持](transaction-support.md)。  
  
## <a name="example"></a>示例  

 下面的代码将数据库提交数据封闭在 <xref:System.Transactions.TransactionScope> 中。  
  
 [!code-csharp[DLinqSubmittingChanges#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#3)]
 [!code-vb[DLinqSubmittingChanges#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>请参阅

- [下载示例数据库](downloading-sample-databases.md)
- [进行和提交数据更改](making-and-submitting-data-changes.md)
- [事务支持](transaction-support.md)
