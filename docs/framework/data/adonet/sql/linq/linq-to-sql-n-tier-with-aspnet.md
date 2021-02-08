---
description: 了解详细信息： LINQ to SQL N 层与 ASP.NET
title: 具有 ASP.NET 的 LINQ to SQL N 层
ms.date: 03/30/2017
ms.assetid: f6cc863a-d6a6-4281-ba8b-197c01cf6c6f
ms.openlocfilehash: a455525f8f0bbef38487b058d89fd2c9b4dda377
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803792"
---
# <a name="linq-to-sql-n-tier-with-aspnet"></a><span data-ttu-id="0fe4e-103">具有 ASP.NET 的 LINQ to SQL N 层</span><span class="sxs-lookup"><span data-stu-id="0fe4e-103">LINQ to SQL N-Tier with ASP.NET</span></span>

<span data-ttu-id="0fe4e-104">在使用的 ASP.NET 应用程序中 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ，你将使用 <xref:System.Web.UI.WebControls.LinqDataSource> Web 服务器控件。</span><span class="sxs-lookup"><span data-stu-id="0fe4e-104">In ASP.NET applications that use [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], you use the <xref:System.Web.UI.WebControls.LinqDataSource> Web server control.</span></span> <span data-ttu-id="0fe4e-105">控件处理查询所必须满足的大部分逻辑 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ，将数据传递到浏览器，检索数据，然后将其提交到， [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.DataContext> 然后更新数据库。</span><span class="sxs-lookup"><span data-stu-id="0fe4e-105">The control handles most of the logic that it must have to query against [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], pass the data to the browser, retrieve it, and submit it to the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.DataContext> which then updates the database.</span></span> <span data-ttu-id="0fe4e-106">只需要在标记中配置该控件，然后由该控件处理 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 和浏览器之间的所有数据传输。</span><span class="sxs-lookup"><span data-stu-id="0fe4e-106">You just configure the control in the markup, and the control handles all the data transfer between [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] and the browser.</span></span> <span data-ttu-id="0fe4e-107">由于该控件处理与表示层之间的交互，并 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 处理与数据层之间的通信，因此，ASP.NET 多层应用程序中的主要焦点是编写自定义业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="0fe4e-107">Because the control handles the interactions with the presentation tier, and [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] handles the communication with the data tier, your main focus in ASP.NET multitier applications is on writing your custom business logic.</span></span>  
  
 <span data-ttu-id="0fe4e-108">有关的详细信息 `LINQDataSource` ，请参阅 [LinqDataSource Web 服务器控件概述](/previous-versions/aspnet/bb547113(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="0fe4e-108">For more information about `LINQDataSource`, see [LinqDataSource Web Server Control Overview](/previous-versions/aspnet/bb547113(v=vs.100)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fe4e-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fe4e-109">See also</span></span>

- [<span data-ttu-id="0fe4e-110">N 层和远程应用程序与 LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="0fe4e-110">N-Tier and Remote Applications with LINQ to SQL</span></span>](n-tier-and-remote-applications-with-linq-to-sql.md)
