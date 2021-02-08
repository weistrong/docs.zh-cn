---
description: 了解详细信息： <commonBehaviors>
title: <commonBehaviors>
ms.date: 03/30/2017
ms.assetid: 5260aeca-388d-4e82-94c0-124fa8054cf5
ms.openlocfilehash: 2fa7397a2833623728bcca286682178d1cf3e1df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802315"
---
# \<commonBehaviors>

<span data-ttu-id="b68f0-102">`commonBehaviors` 节只能在 machine.config 文件中定义。</span><span class="sxs-lookup"><span data-stu-id="b68f0-102">The `commonBehaviors` section can only be defined in the machine.config file.</span></span> <span data-ttu-id="b68f0-103">它定义了名为 `endpointBehaviors` 和 `serviceBehaviors` 的两个子集合。</span><span class="sxs-lookup"><span data-stu-id="b68f0-103">It defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="b68f0-104">每个集合分别定义计算机上所有 WCF 终结点和服务所使用的行为元素。</span><span class="sxs-lookup"><span data-stu-id="b68f0-104">Each collection defines behavior elements consumed by all WCF endpoints and services on the machine respectively.</span></span> <span data-ttu-id="b68f0-105">在 `endpointBehaviors` 中定义的行为只适用于客户端，在 `serviceBehaviors` 中定义的行为只适用于服务。</span><span class="sxs-lookup"><span data-stu-id="b68f0-105">Behaviors defined in `endpointBehaviors` are only applied to clients, and behaviors defined in `serviceBehaviors` are only applied to services.</span></span> <span data-ttu-id="b68f0-106">如果在 `commonBehaviors` 和 `behaviors` 节中都定义某行为，则 `behaviors` 节中的行为优先。</span><span class="sxs-lookup"><span data-stu-id="b68f0-106">If a behavior is defined in both `commonBehaviors` and `behaviors` sections, the behavior in the `behaviors` section is given preference.</span></span>
