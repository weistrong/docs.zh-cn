---
description: 了解详细信息：实例完成操作
title: 实例完成操作
ms.date: 03/30/2017
ms.assetid: 90cc99d2-9fef-42fd-bcbf-a56917993721
ms.openlocfilehash: 84405ca9869369e4fe00b0049d628671a79a9f68
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792682"
---
# <a name="instance-completion-action"></a><span data-ttu-id="62934-103">实例完成操作</span><span class="sxs-lookup"><span data-stu-id="62934-103">Instance Completion Action</span></span>

<span data-ttu-id="62934-104">利用 SQL 工作流实例存储的 " **实例完成操作** " 属性，您可以指定在实例完成之后是否从持久性数据库中删除工作流实例的数据和元数据。</span><span class="sxs-lookup"><span data-stu-id="62934-104">The **Instance Completion Action** property of the SQL Workflow Instance Store lets you specify whether the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span> <span data-ttu-id="62934-105">此属性的允许值为 **DeleteAll** 和 **DeleteNothing**。</span><span class="sxs-lookup"><span data-stu-id="62934-105">The allowed values for this property are **DeleteAll** and **DeleteNothing**.</span></span> <span data-ttu-id="62934-106">以下列表对这两个选项进行了说明：</span><span class="sxs-lookup"><span data-stu-id="62934-106">The following list describes these options:</span></span>

- <span data-ttu-id="62934-107">**DeleteAll（默认值）。**</span><span class="sxs-lookup"><span data-stu-id="62934-107">**DeleteAll (default).**</span></span> <span data-ttu-id="62934-108">如果该属性的值设置为 DeleteAll，则在工作流实例完成之后会将从持久性数据库中删除该实例的数据和元数据。</span><span class="sxs-lookup"><span data-stu-id="62934-108">If the value of the property is set to DeleteAll, the data and metadata of workflow instances is deleted from the persistence database after the instances are completed.</span></span>

- <span data-ttu-id="62934-109">**DeleteNothing。**</span><span class="sxs-lookup"><span data-stu-id="62934-109">**DeleteNothing.**</span></span> <span data-ttu-id="62934-110">如果该属性的值设置为 DeleteNothing，则即使在工作流实例完成之后也会将该实例的数据和元数据保留在持久性数据库中。</span><span class="sxs-lookup"><span data-stu-id="62934-110">If the value of the property is set to DeleteNothing, the data and metadata of workflow instances is kept in the persistence database even after the instances are completed.</span></span>

  > [!CAUTION]
  > <span data-ttu-id="62934-111">实例完成之后继续保留实例状态信息会导致持久性数据库增大。</span><span class="sxs-lookup"><span data-stu-id="62934-111">Keeping instance state information after the instances are completed causes the persistence database to grow in size.</span></span> <span data-ttu-id="62934-112">随着数据库的增大，持久性子系统执行数据库操作所花费的时间会越来越长，因此需要定期从持久性数据库中清除实例状态信息，以使服务在满足您的性能需求的级别执行。</span><span class="sxs-lookup"><span data-stu-id="62934-112">As the size of the database grows the database operations that the persistence subsystem performs take longer, so you need to purge the instance state information from the persistence database periodically to have services perform at the level that satisfy your performance needs.</span></span>
