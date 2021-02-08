---
description: 了解详细信息：安全性
title: 安全
ms.date: 03/30/2017
ms.assetid: 737ec121-bfc5-4b75-a504-2d53c2c8af39
ms.openlocfilehash: 8f095292deac77c1c72cf87a93064569f7dab982
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798090"
---
# <a name="security"></a><span data-ttu-id="90354-103">安全</span><span class="sxs-lookup"><span data-stu-id="90354-103">Security</span></span>

<span data-ttu-id="90354-104">SQL 工作流实例存储使用以下数据库安全角色确保安全访问持久性数据库中的实例状态信息。</span><span class="sxs-lookup"><span data-stu-id="90354-104">The SQL Workflow Instance Store uses the following database security roles to secure access to instance state information in the persistence database.</span></span>  
  
- <span data-ttu-id="90354-105">**DurableInstancing. system.activities.durableinstancing.instancestoreusers**。</span><span class="sxs-lookup"><span data-stu-id="90354-105">**System.Activities.DurableInstancing.InstanceStoreUsers**.</span></span> <span data-ttu-id="90354-106">此角色具有对公共视图的读写访问权以及对创建、加载和保存实例所涉及的存储过程的执行权限。</span><span class="sxs-lookup"><span data-stu-id="90354-106">This role has read and write access to public views and execution rights to stored procedures that are involved in creating, loading and saving instances.</span></span>  
  
- <span data-ttu-id="90354-107">**DurableInstancing. InstanceStoreObservers**。</span><span class="sxs-lookup"><span data-stu-id="90354-107">**System.Activities.DurableInstancing.InstanceStoreObservers**.</span></span> <span data-ttu-id="90354-108">此角色具有对公共视图的只读访问权。</span><span class="sxs-lookup"><span data-stu-id="90354-108">This role has read-only access to public views.</span></span>  
  
- <span data-ttu-id="90354-109">**DurableInstancing. WorkflowActivationUsers**。</span><span class="sxs-lookup"><span data-stu-id="90354-109">**System.Activities.DurableInstancing.WorkflowActivationUsers**.</span></span> <span data-ttu-id="90354-110">此角色对在实例激活过程中涉及的存储过程具有执行权限。</span><span class="sxs-lookup"><span data-stu-id="90354-110">This role has execution rights to stored procedures that are involved in the instance activation process.</span></span> <span data-ttu-id="90354-111">有关实例激活的详细信息，请参阅 [实例激活](instance-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="90354-111">For more information about instance activation, see [Instance Activation](instance-activation.md).</span></span> <span data-ttu-id="90354-112">应将泛型宿主 (的用户帐户（例如 Windows Server AppFabric) 运行的宿主功能的工作流管理服务）添加到此数据库角色。</span><span class="sxs-lookup"><span data-stu-id="90354-112">The user account under which a generic host (such as the Workflow Management Service of the hosting features of Windows Server AppFabric) runs should be added to this database role.</span></span>  
  
 <span data-ttu-id="90354-113">有关 Windows Server App Fabric 的持久性存储安全的详细信息，请参阅 [App fabric 中的持久性存储的安全配置](/previous-versions/appfabric/ff431727(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="90354-113">For more information about security for persistence stores with Windows Server App Fabric, see [Security Configuration for Persistence Stores in App Fabric](/previous-versions/appfabric/ff431727(v=azure.10))</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="90354-114">有权访问自己存在实例存储区中的实例数据的客户端对同一实例存储区中所有其他实例也具有访问权限。</span><span class="sxs-lookup"><span data-stu-id="90354-114">A client that has access to its own instance data in the instance store has access to all other instances in the same instance store.</span></span> <span data-ttu-id="90354-115">实例存储区不支持在实例级别指定安全权限。</span><span class="sxs-lookup"><span data-stu-id="90354-115">The instance store does not support specifying security permissions at the instance level.</span></span> <span data-ttu-id="90354-116">您应创建单独的实例存储区并映射不同的组/用户，使他们有权访问的存储区有所不同。</span><span class="sxs-lookup"><span data-stu-id="90354-116">You should create separate instance stores and map different groups/users to have access to different stores.</span></span>
