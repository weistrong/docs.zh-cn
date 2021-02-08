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
# <a name="spatial-functions"></a>空间函数

空间类型没有文本格式。 但是，您可以使用规范实体实体框架函数，这些函数可使用已知文本格式的字符串来调用。 例如，以下函数调用会生成一个几何点：  
  
```sql  
GeometryFromText('POINT (43 -73)')  
```  
  
 <xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions>方法具有所有空间规范实体框架方法。 请单击相关方法以查看应向函数传递哪些参数。
