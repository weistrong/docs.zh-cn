---
description: 了解详细信息：空间函数
title: 空间函数
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: cde8f1b0fcf5904eb33fe061de69e566da2804dd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767877"
---
# <a name="spatial-functions"></a><span data-ttu-id="4145f-103">空间函数</span><span class="sxs-lookup"><span data-stu-id="4145f-103">Spatial Functions</span></span>

<span data-ttu-id="4145f-104">空间类型没有文本格式。</span><span class="sxs-lookup"><span data-stu-id="4145f-104">There is no literal format for spatial types.</span></span> <span data-ttu-id="4145f-105">但是，您可以使用规范实体实体框架函数，这些函数可使用已知文本格式的字符串来调用。</span><span class="sxs-lookup"><span data-stu-id="4145f-105">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="4145f-106">例如，以下函数调用会生成一个几何点：</span><span class="sxs-lookup"><span data-stu-id="4145f-106">For example, the following function call creates a geometry point:</span></span>  
  
```sql  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="4145f-107"><xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions>方法具有所有空间规范实体框架方法。</span><span class="sxs-lookup"><span data-stu-id="4145f-107">The <xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions> methods have all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="4145f-108">请单击相关方法以查看应向函数传递哪些参数。</span><span class="sxs-lookup"><span data-stu-id="4145f-108">Click on a method of interest to see what parameters should be passed to a function.</span></span>
