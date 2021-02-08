---
description: 了解详细信息： ICorRuntimeHost：： GetConfiguration 方法
title: ICorRuntimeHost::GetConfiguration 方法
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type:
- apiref
ms.openlocfilehash: d3e3f065c3957fb29daa11ed7c46858a53865c91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784829"
---
# <a name="icorruntimehostgetconfiguration-method"></a>ICorRuntimeHost::GetConfiguration 方法

获取一个对象，该对象允许主机指定 (CLR) 的公共语言运行时的回调配置。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
## <a name="parameters"></a>参数  

 `pConfiguration`  
 弄指向可用于配置 CLR 的 [ICorConfiguration](icorconfiguration-interface.md) 对象地址的指针。  
  
## <a name="remarks"></a>备注  

 必须在初始化之前配置 CLR;否则，该 `GetConfiguration` 方法将返回一个 HRESULT，指示错误。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：** 1.0、1。1  
  
## <a name="see-also"></a>请参阅

- [ICorRuntimeHost 接口](icorruntimehost-interface.md)
