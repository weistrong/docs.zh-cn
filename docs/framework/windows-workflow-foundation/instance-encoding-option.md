---
description: 详细了解：实例编码选项
title: 实例编码选项
ms.date: 03/30/2017
ms.assetid: 89e4b029-4f68-438c-8117-9b21fe094ef4
ms.openlocfilehash: 8cca7fd536673ca99b1014173e172508e3d97b7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631159"
---
# <a name="instance-encoding-option"></a><span data-ttu-id="969cd-103">实例编码选项</span><span class="sxs-lookup"><span data-stu-id="969cd-103">Instance Encoding Option</span></span>

<span data-ttu-id="969cd-104">使用 SQL 工作流实例存储的 " **实例编码选项** " 属性，可以指定 sql 永久性提供程序是否应在将信息保存到持久性数据库中之前使用 GZip 算法压缩工作流实例状态信息。</span><span class="sxs-lookup"><span data-stu-id="969cd-104">The **Instance Encoding Option** property of the SQL Workflow Instance Store lets you specify whether the SQL persistence provider should compress the workflow instance state information using the GZip algorithm before saving the information into the persistence database.</span></span> <span data-ttu-id="969cd-105">此属性的允许值为 GZip 和 None。</span><span class="sxs-lookup"><span data-stu-id="969cd-105">The allowed values for this property are: GZip and None.</span></span> <span data-ttu-id="969cd-106">默认值为 None。</span><span class="sxs-lookup"><span data-stu-id="969cd-106">The default value is None.</span></span> <span data-ttu-id="969cd-107">以下列表对这两个选项进行了说明。</span><span class="sxs-lookup"><span data-stu-id="969cd-107">The following list describes these options.</span></span>  
  
1. <span data-ttu-id="969cd-108">**GZip**。</span><span class="sxs-lookup"><span data-stu-id="969cd-108">**GZip**.</span></span> <span data-ttu-id="969cd-109">在将状态信息持久保存到持久性数据库中之前，持久性提供程序使用 GZip 算法对该状态信息进行编码。</span><span class="sxs-lookup"><span data-stu-id="969cd-109">The persistence provider encodes the state information using the GZip algorithm before persisting the state information in the persistence database.</span></span>  
  
2. <span data-ttu-id="969cd-110">**无**。</span><span class="sxs-lookup"><span data-stu-id="969cd-110">**None**.</span></span> <span data-ttu-id="969cd-111">在将状态信息保存到持久性数据库中之前，持久性提供程序不会对该状态信息进行编码。</span><span class="sxs-lookup"><span data-stu-id="969cd-111">The persistence provider does not encode the state information before saving the information into the persistence database.</span></span>  
  
 <span data-ttu-id="969cd-112">使用 GZip 对工作流实例状态信息进行编码可减少 SQL 数据库中的内存消耗，并且还可减少网络消耗（如果数据库位于网络上的另一台计算机上，而不是位于运行工作流服务宿主的计算机上）。</span><span class="sxs-lookup"><span data-stu-id="969cd-112">Encoding workflow instance state information using the GZip reduces memory consumption in the SQL database and also reduces network consumption if the database resides on a different computer on the network from the computer on which the workflow service host is running.</span></span> <span data-ttu-id="969cd-113">一般的指导是，如果工作流实例的状态为小，则将 " **实例编码选项** " 属性设置为 " **无** "。</span><span class="sxs-lookup"><span data-stu-id="969cd-113">A general guidance is to set the **Instance Encoding Option** property to **None** if the workflow instance state is small.</span></span>
