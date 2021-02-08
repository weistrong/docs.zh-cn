---
description: 了解详细信息： ICorPublishProcess：： IsManaged 方法
title: ICorPublishProcess::IsManaged 方法
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
ms.openlocfilehash: 55f620a896efd87c2f154ac68ef2db1a1b0a1ebc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790498"
---
# <a name="icorpublishprocessismanaged-method"></a>ICorPublishProcess::IsManaged 方法

获取一个值，该值指示此 [ICorPublishProcess](icorpublishprocess-interface.md) 引用的进程是否已知具有托管代码。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
## <a name="parameters"></a>参数  

 `pbManaged`  
 弄一个指向布尔值的指针，该布尔值指示进程是否具有托管代码。 `true`如果进程具有托管代码，则该值为; 否则为 `false` 。  
  
## <a name="remarks"></a>备注  

 由于的当前版本 `ICorPublishProcess` 只允许访问具有托管代码的进程，因此 `IsManaged` 总是返回 `true` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** CorPub，CorPub  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorPublishProcess 接口](icorpublishprocess-interface.md)
