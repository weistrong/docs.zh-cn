---
description: 了解更多：不支持的功能
title: 不支持的功能
ms.date: 03/30/2017
ms.assetid: e480cfb5-697e-42c8-bed5-9264c945c4f9
ms.openlocfilehash: 5c44dd4aad2d2ee4ec5e00ce42f4de9400cea478
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680884"
---
# <a name="unsupported-functionality"></a><span data-ttu-id="89c03-103">不支持的功能</span><span class="sxs-lookup"><span data-stu-id="89c03-103">Unsupported Functionality</span></span>

<span data-ttu-id="89c03-104">在 LINQ to SQL 中，无法通过转换现有的公共语言运行库 (CLR) 和 .NET Framework 构造公开以下 SQL 功能：</span><span class="sxs-lookup"><span data-stu-id="89c03-104">In LINQ to SQL, the following SQL functionality cannot be exposed through translation of existing common language runtime (CLR) and .NET Framework constructs:</span></span>  
  
- `STDDEV`  
  
- `LIKE`  
  
     <span data-ttu-id="89c03-105">尽管通过直接转换，不支持 `LIKE`，但是 <xref:System.Data.Linq.SqlClient.SqlMethods> 类中仍存在相似的功能。</span><span class="sxs-lookup"><span data-stu-id="89c03-105">Although `LIKE` is not supported through direct translation, similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span> <span data-ttu-id="89c03-106">有关详细信息，请参阅 <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="89c03-106">For more information, see <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.</span></span>  
  
- `DATEDIFF`  
  
     <span data-ttu-id="89c03-107">LINQ to SQL 具有对 `DATEDIFF` 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="89c03-107">LINQ to SQL has limited support for `DATEDIFF`.</span></span> <span data-ttu-id="89c03-108"><xref:System.Data.Linq.SqlClient.SqlMethods> 类中存在相似的功能。</span><span class="sxs-lookup"><span data-stu-id="89c03-108">Similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span>  
  
- `ROUND`  
  
     <span data-ttu-id="89c03-109">LINQ to SQL 具有对 `ROUND` 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="89c03-109">LINQ to SQL has limited support for `ROUND`.</span></span> <span data-ttu-id="89c03-110">有关详细信息，请参阅 system.exception [方法](system-math-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="89c03-110">For more information, see [System.Math Methods](system-math-methods.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89c03-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="89c03-111">See also</span></span>

- [<span data-ttu-id="89c03-112">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="89c03-112">Data Types and Functions</span></span>](data-types-and-functions.md)
