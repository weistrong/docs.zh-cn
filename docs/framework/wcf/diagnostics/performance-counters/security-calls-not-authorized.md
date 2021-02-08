---
description: 了解详细信息：未授权的安全调用
title: Security Calls Not Authorized（未授权的安全调用次数）
ms.date: 03/30/2017
ms.assetid: cb6acdcd-7336-42e1-9ae8-ac891336cd58
ms.openlocfilehash: 80dc161f2be5a678e80860410f1b6adbde7bfb71
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803407"
---
# <a name="security-calls-not-authorized"></a>Security Calls Not Authorized（未授权的安全调用次数）

计数器名称：Security Calls Not Authorized（未授权的安全调用次数）。  
  
## <a name="description"></a>说明  

 当 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> 方法返回 `false` 时，此计数器将递增。 它指示传入的消息来自有效的用户并得到了良好保护，但该用户没有获得执行特定任务的授权。
