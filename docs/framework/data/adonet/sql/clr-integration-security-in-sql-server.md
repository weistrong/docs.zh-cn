---
description: 了解详细信息： CLR Integration Security in SQL Server
title: SQL Server 中的 CLR 集成安全性
ms.date: 03/30/2017
ms.assetid: 489fe096-fd1d-42de-8438-bf7aed46aea2
ms.openlocfilehash: 5de552c0f5b869712d2038b53abd50b8ded04747
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718533"
---
# <a name="clr-integration-security-in-sql-server"></a><span data-ttu-id="90e52-103">SQL Server 中的 CLR 集成安全性</span><span class="sxs-lookup"><span data-stu-id="90e52-103">CLR Integration Security in SQL Server</span></span>

<span data-ttu-id="90e52-104">Microsoft SQL Server 提供 .NET Framework 的公共语言运行时 (CLR) 组件集成。</span><span class="sxs-lookup"><span data-stu-id="90e52-104">Microsoft SQL Server provides the integration of the common language runtime (CLR) component of the .NET Framework.</span></span> <span data-ttu-id="90e52-105">通过 CLR 集成，您可以使用任何 .NET Framework 语言（如 Microsoft Visual Basic .NET 或 Microsoft Visual C#）编写存储过程、触发器、用户定义的类型、用户定义的函数、用户定义的聚合以及流式表值函数。</span><span class="sxs-lookup"><span data-stu-id="90e52-105">CLR integration allows you to write stored procedures, triggers, user-defined types, user-defined functions, user-defined aggregates, and streaming table-valued functions, using any .NET Framework language, such as Microsoft Visual Basic .NET or Microsoft Visual C#.</span></span>  
  
 <span data-ttu-id="90e52-106">CLR 支持一种用于托管代码的安全模型，称为代码访问安全性 (CAS)。</span><span class="sxs-lookup"><span data-stu-id="90e52-106">The CLR supports a security model called code access security (CAS) for managed code.</span></span> <span data-ttu-id="90e52-107">在此模型中，将根据元数据中代码提供的证据向程序集授予权限。</span><span class="sxs-lookup"><span data-stu-id="90e52-107">In this model, permissions are granted to assemblies based on evidence supplied by the code in metadata.</span></span> <span data-ttu-id="90e52-108">SQL Server 将 SQL Server 的基于用户的安全模型与 CLR 的基于代码启用的安全模型相集成。</span><span class="sxs-lookup"><span data-stu-id="90e52-108">SQL Server integrates the user-based security model of SQL Server with the code access-based security model of the CLR.</span></span>  
  
## <a name="external-resources"></a><span data-ttu-id="90e52-109">外部资源</span><span class="sxs-lookup"><span data-stu-id="90e52-109">External Resources</span></span>  

 <span data-ttu-id="90e52-110">有关 CLR 与 SQL Server 集成的更多信息，请参见下列资源。</span><span class="sxs-lookup"><span data-stu-id="90e52-110">For more information on CLR integration with SQL Server, see the following resources.</span></span>  
  
|<span data-ttu-id="90e52-111">资源</span><span class="sxs-lookup"><span data-stu-id="90e52-111">Resource</span></span>|<span data-ttu-id="90e52-112">说明</span><span class="sxs-lookup"><span data-stu-id="90e52-112">Description</span></span>|  
|--------------|-----------------|  
|[<span data-ttu-id="90e52-113">代码访问安全性</span><span class="sxs-lookup"><span data-stu-id="90e52-113">Code Access Security</span></span>](../../../misc/code-access-security.md)|<span data-ttu-id="90e52-114">包含描述 .NET Framework 中 CAS 的主题。</span><span class="sxs-lookup"><span data-stu-id="90e52-114">Contains topics describing CAS in the .NET Framework.</span></span>|  
|[<span data-ttu-id="90e52-115">CLR 集成安全性</span><span class="sxs-lookup"><span data-stu-id="90e52-115">CLR Integration Security</span></span>](/sql/relational-databases/clr-integration/security/clr-integration-security)|<span data-ttu-id="90e52-116">讨论在 SQL Server 内部执行的托管代码的安全模型。</span><span class="sxs-lookup"><span data-stu-id="90e52-116">Discusses the security model for managed code executing inside of SQL Server.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="90e52-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="90e52-117">See also</span></span>

- [<span data-ttu-id="90e52-118">保证 ADO.NET 应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="90e52-118">Securing ADO.NET Applications</span></span>](../securing-ado-net-applications.md)
- [<span data-ttu-id="90e52-119">SQL Server 中的应用程序安全方案</span><span class="sxs-lookup"><span data-stu-id="90e52-119">Application Security Scenarios in SQL Server</span></span>](application-security-scenarios-in-sql-server.md)
- [<span data-ttu-id="90e52-120">SQL Server 公共语言运行时集成</span><span class="sxs-lookup"><span data-stu-id="90e52-120">SQL Server Common Language Runtime Integration</span></span>](sql-server-common-language-runtime-integration.md)
- [<span data-ttu-id="90e52-121">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="90e52-121">ADO.NET Overview</span></span>](../ado-net-overview.md)
