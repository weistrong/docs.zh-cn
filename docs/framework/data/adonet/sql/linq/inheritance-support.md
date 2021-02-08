---
description: 了解更多相关信息：继承支持
title: 层次结构支持
ms.date: 03/30/2017
ms.assetid: 19bb2794-b4e7-402e-8307-1d1517381a08
ms.openlocfilehash: ff6956441ab72f720151e42bd9358c8df1170e09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803862"
---
# <a name="inheritance-support"></a><span data-ttu-id="2ffdc-103">层次结构支持</span><span class="sxs-lookup"><span data-stu-id="2ffdc-103">Inheritance Support</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="2ffdc-104">支持 *单表映射*。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-104">supports *single-table mapping*.</span></span> <span data-ttu-id="2ffdc-105">换言之，整个继承层次结构存储在单个数据库表中。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-105">In other words, a complete inheritance hierarchy is stored in a single database table.</span></span> <span data-ttu-id="2ffdc-106">该表包含整个层次结构的所有可能数据列的平展联合。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-106">The table contains the flattened union of all possible data columns for the whole hierarchy.</span></span> <span data-ttu-id="2ffdc-107"> (联合是指将两个表组合成一个表，该表中有两个原始表中存在的行。每行 ) 的列中的 null 值不适用于行所表示的实例类型。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-107">(A union is the result of combining two tables into one table that has the rows that were present in either of the original tables.) Each row has nulls in the columns that do not apply to the type of the instance represented by the row.</span></span>  
  
 <span data-ttu-id="2ffdc-108">单表映射策略是最简单的继承表示形式，为许多不同类别的查询提供了良好的性能特征。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-108">The single-table mapping strategy is the simplest representation of inheritance and provides good performance characteristics for many different categories of queries.</span></span>  
  
 <span data-ttu-id="2ffdc-109">若要在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中实现这种映射，必须在继承层次结构的根类中指定属性 (Attribute) 和属性 (Attribute) 的属性 (Property)。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-109">To implement this mapping in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], you must specify the attributes and attribute properties on the root class of the inheritance hierarchy.</span></span> <span data-ttu-id="2ffdc-110">有关详细信息，请参阅 [如何：映射继承层次结构](how-to-map-inheritance-hierarchies.md)。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-110">For more information, see [How to: Map Inheritance Hierarchies](how-to-map-inheritance-hierarchies.md).</span></span>  
  
 <span data-ttu-id="2ffdc-111">使用 Visual Studio 的开发人员还可以使用对象关系设计器来映射继承层次结构。</span><span class="sxs-lookup"><span data-stu-id="2ffdc-111">Developers using Visual Studio can also use the Object Relational Designer to map inheritance hierarchies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ffdc-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="2ffdc-112">See also</span></span>

- [<span data-ttu-id="2ffdc-113">背景信息</span><span class="sxs-lookup"><span data-stu-id="2ffdc-113">Background Information</span></span>](background-information.md)
