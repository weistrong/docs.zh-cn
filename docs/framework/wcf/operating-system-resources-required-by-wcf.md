---
description: 了解详细信息： WCF 所需的操作系统资源
title: WCF 所要求的操作系统资源
ms.date: 03/30/2017
ms.assetid: cdd9a331-53fe-4e0d-bdfe-782264aec5c9
ms.openlocfilehash: 717ab2074c0dcf840919c2bd8afa2641e106ac11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779213"
---
# <a name="operating-system-resources-required-by-wcf"></a><span data-ttu-id="9b673-103">WCF 所要求的操作系统资源</span><span class="sxs-lookup"><span data-stu-id="9b673-103">Operating System Resources Required by WCF</span></span>

<span data-ttu-id="9b673-104">Windows Communication Foundation (WCF) 依赖于操作系统提供的多个资源才能正常运行。</span><span class="sxs-lookup"><span data-stu-id="9b673-104">Windows Communication Foundation (WCF) depends on several resources that are provided by the operating system to function.</span></span> <span data-ttu-id="9b673-105">下表列出了这些资源：</span><span class="sxs-lookup"><span data-stu-id="9b673-105">The following table lists those resources:</span></span>

|<span data-ttu-id="9b673-106">资源</span><span class="sxs-lookup"><span data-stu-id="9b673-106">Resource</span></span>|<span data-ttu-id="9b673-107">说明</span><span class="sxs-lookup"><span data-stu-id="9b673-107">Description</span></span>|
|--------------|-----------------|
|<span data-ttu-id="9b673-108">Microsoft 分布式事务协调器 (MSDTC)</span><span class="sxs-lookup"><span data-stu-id="9b673-108">Microsoft Distributed Transaction Coordinator (MSDTC)</span></span>|<span data-ttu-id="9b673-109">支持 OleTx 事务所必需。</span><span class="sxs-lookup"><span data-stu-id="9b673-109">Required to support OleTx transactions.</span></span>|
|<span data-ttu-id="9b673-110">Internet 信息服务 (IIS)</span><span class="sxs-lookup"><span data-stu-id="9b673-110">Internet Information Services (IIS)</span></span>|<span data-ttu-id="9b673-111">如果希望使用 IIS 来承载应用程序，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b673-111">Required if you want to use IIS to host your application.</span></span>|
|<span data-ttu-id="9b673-112">Windows 进程激活服务 (WAS)</span><span class="sxs-lookup"><span data-stu-id="9b673-112">Windows Process Activation Service (WAS)</span></span>|<span data-ttu-id="9b673-113">如果希望使用 WAS 来承载应用程序，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="9b673-113">Required if you want to use WAS to host your application.</span></span>|
