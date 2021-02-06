---
description: 了解有关以下方面的详细信息：终结点：未授权的安全调用
title: 终结点：未授权的安全调用次数
ms.date: 03/30/2017
ms.assetid: d25095ff-9ff0-4c69-a674-4e6a9fe3f4dc
ms.openlocfilehash: 258c984e8a7986594b6da6f5c2a8c030907f82ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655469"
---
# <a name="endpoint-security-calls-not-authorized"></a>终结点：未授权的安全调用次数

计数器名称：Security Calls Not Authorized（未授权的安全调用次数）。  
  
## <a name="description"></a>说明  

 当 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> 方法返回 `false` 时，此计数器将递增。 它指示传入的消息来自有效的用户并得到了良好保护，但该用户没有获得执行特定任务的授权。
