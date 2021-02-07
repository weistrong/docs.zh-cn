---
description: 了解有关以下方面的详细信息： System.object 方法
title: System.Object 方法
ms.date: 03/30/2017
ms.assetid: 5397fca0-689e-443e-802f-e1cbdc866427
ms.openlocfilehash: 88ba4cf7cfc7dc9bea565b4689f77d088d424c44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681313"
---
# <a name="systemobject-methods"></a><span data-ttu-id="ddd97-103">System.Object 方法</span><span class="sxs-lookup"><span data-stu-id="ddd97-103">System.Object Methods</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="ddd97-104">支持以下 <xref:System.Object> 方法。</span><span class="sxs-lookup"><span data-stu-id="ddd97-104">supports the following <xref:System.Object> methods.</span></span>  
  
|||  
|-|-|  
|<xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType>|<xref:System.Object.Equals%28System.Object%2CSystem.Object%29?displayProperty=nameWithType>|  
|<xref:System.Object.ToString?displayProperty=nameWithType>||  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="ddd97-105">不支持以下 <xref:System.Object> 方法。</span><span class="sxs-lookup"><span data-stu-id="ddd97-105">does not support the following <xref:System.Object> methods.</span></span>  
  
|||  
|-|-|  
|<xref:System.Object.GetHashCode?displayProperty=nameWithType>|<xref:System.Object.ReferenceEquals%28System.Object%2CSystem.Object%29?displayProperty=nameWithType>|  
|<xref:System.Object.MemberwiseClone?displayProperty=nameWithType>|<xref:System.Object.GetType?displayProperty=nameWithType>|  
|<span data-ttu-id="ddd97-106">用于二进制类型（如 <xref:System.Object.ToString?displayProperty=nameWithType>、`BINARY`、`VARBINARY` 和 `IMAGE`）的 `TIMESTAMP`。</span><span class="sxs-lookup"><span data-stu-id="ddd97-106"><xref:System.Object.ToString?displayProperty=nameWithType> for binary types such as `BINARY`, `VARBINARY`, `IMAGE`, and `TIMESTAMP`.</span></span>||  
  
## <a name="differences-from-net"></a><span data-ttu-id="ddd97-107">与 .NET 的差异</span><span class="sxs-lookup"><span data-stu-id="ddd97-107">Differences from .NET</span></span>  

 <span data-ttu-id="ddd97-108">Double 的输出 <xref:System.Object.ToString?displayProperty=nameWithType> 使用 sql `CONVERT` (NVARCHAR (30) ， @x ，2) sql 上。</span><span class="sxs-lookup"><span data-stu-id="ddd97-108">The output of <xref:System.Object.ToString?displayProperty=nameWithType> for double uses SQL `CONVERT`(NVARCHAR(30), @x, 2) on SQL.</span></span> <span data-ttu-id="ddd97-109">在这种情况下 SQL 始终使用 16 位科学记数法（例如，用“0.000000000000000e+000”表示 0）。</span><span class="sxs-lookup"><span data-stu-id="ddd97-109">SQL always uses 16 digits and scientific notation in this case (for example, "0.000000000000000e+000" for 0).</span></span> <span data-ttu-id="ddd97-110">因此，<xref:System.Object.ToString?displayProperty=nameWithType> 转换与 .NET Framework 中的 <xref:System.Convert.ToString%2A?displayProperty=nameWithType> 产生的字符串不同。</span><span class="sxs-lookup"><span data-stu-id="ddd97-110">As a result, <xref:System.Object.ToString?displayProperty=nameWithType> conversion does not produce the same string as <xref:System.Convert.ToString%2A?displayProperty=nameWithType> in the .NET Framework.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddd97-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="ddd97-111">See also</span></span>

- [<span data-ttu-id="ddd97-112">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="ddd97-112">Data Types and Functions</span></span>](data-types-and-functions.md)
