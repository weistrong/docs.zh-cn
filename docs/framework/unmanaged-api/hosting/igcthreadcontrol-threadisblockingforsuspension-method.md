---
description: 了解详细信息： IGCThreadControl：： ThreadIsBlockingForSuspension 方法
title: IGCThreadControl::ThreadIsBlockingForSuspension 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForSuspension
helpviewer_keywords:
- IGCThreadControl::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: ed5b5b58-7db7-46b5-9e2c-278db7159cee
topic_type:
- apiref
ms.openlocfilehash: 13023a75ab1c438abebbeb16fd9fe7c4b95c37ab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709199"
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a>IGCThreadControl::ThreadIsBlockingForSuspension 方法

通知宿主正在进行调用的线程将要阻止，可能用于垃圾回收或其他挂起。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a>备注  

 宿主可以在回调内选择 `ThreadIsBlockingForSuspension` 是否重新计划线程。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IGCThreadControl 接口](igcthreadcontrol-interface.md)
