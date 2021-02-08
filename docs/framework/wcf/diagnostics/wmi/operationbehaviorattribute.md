---
description: 了解详细信息： OperationBehaviorAttribute
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: c1f1b80134163ee65d5015e52017f5bb455aeac7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803056"
---
# <a name="operationbehaviorattribute"></a>OperationBehaviorAttribute

OperationBehaviorAttribute  
  
## <a name="syntax"></a>语法  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a>方法  

 OperationBehaviorAttribute 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 OperationBehaviorAttribute 类具有下列属性：  
  
### <a name="autodisposeparameters"></a>AutoDisposeParameters  

 数据类型：Boolean  
  
 访问类型：只读  
  
 参数自动释放功能的状态。  
  
### <a name="impersonation"></a>模拟  

 数据类型：字符串  
  
 访问类型：只读  
  
 指示操作支持的调用方模拟级别。  
  
### <a name="releaseinstancemode"></a>ReleaseInstanceMode  

 数据类型：字符串  
  
 访问类型：只读  
  
 指示操作调用过程中何时回收对象。  
  
### <a name="transactionautocomplete"></a>TransactionAutoComplete  

 数据类型：Boolean  
  
 访问类型：只读  
  
 指示在未发生未处理的异常的情况下是否自动提交当前事务。  
  
### <a name="transactionscoperequired"></a>TransactionScopeRequired  

 数据类型：Boolean  
  
 访问类型：只读  
  
 指示操作是否需要事务处理。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.OperationBehaviorAttribute>
