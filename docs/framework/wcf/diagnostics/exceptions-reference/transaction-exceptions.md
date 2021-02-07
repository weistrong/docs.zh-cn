---
description: 了解详细信息：事务异常
title: 事务异常
ms.date: 03/30/2017
ms.assetid: 1d27ed51-7eda-477f-9eca-94fa129f3e07
ms.openlocfilehash: edea932ca12fcd05994c979555e7eb9c0d00e969
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99686058"
---
# <a name="transaction-exceptions"></a>事务异常

本主题列出了 Windows Communication Foundation (WCF) 事务生成的所有异常。  
  
## <a name="exception-list"></a>异常列表  
  
|资源代码|资源字符串|  
|-------------------|---------------------|  
|SFxCannotHaveDifferentTransactionProtocolsInOneBinding|从元数据导入的策略信息指定各个操作的不同 TransactionProtocol 值。 每个终结点仅支持一个 TransactionProtocol。|  
|SFxTransactionAutoCompleteFalseAndInstanceContextMode|TransactionAutoComplete 不能为 false，除非服务的 InstanceContextMode 为 PerSession。 在指定约定和操作的实现上发现错误。|  
|SFxTransactionInvalidSetTransactionComplete|仅当 TransactionAutoComplete 设置为 false 且 TransactionScopeRequired 设置为 true 时，才能在操作中调用 OperationContext.SetTransactionComplete。 这种方案无效，当前事务已终止。|  
|TransactionFlowRequiredIssuedTokens|若要对事务进行流处理，还必须支持对已颁发的令牌进行流处理。|  
|TrustDriverVersionDoesNotSupportIssuedTokens|配置的 Trust 版本不支持已颁发的令牌。 请使用 WSTrustFeb2005 或更高版本。|
