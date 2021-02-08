---
description: 了解详细信息： ICLRRuntimeInfo：： LoadErrorString 方法
title: ICLRRuntimeInfo::LoadErrorString 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.LoadErrorString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::LoadErrorString
helpviewer_keywords:
- ICLRRuntimeInfo::LoadErrorString method [.NET Framework hosting]
- LoadErrorString method [.NET Framework hosting]
ms.assetid: 52c543ab-9ef5-4ee7-b836-c0ffc35cd45b
topic_type:
- apiref
ms.openlocfilehash: 0523b5b89072db50c83c52065c22e9df7167a027
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785063"
---
# <a name="iclrruntimeinfoloaderrorstring-method"></a>ICLRRuntimeInfo::LoadErrorString 方法

将 HRESULT 值转换为指定区域性的适当错误消息。  
  
 此方法取代了以下函数：  
  
- [LoadStringRC](loadstringrc-function.md)  
  
- [LoadStringRCEx](loadstringrcex-function.md)  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT LoadErrorString(  
     [in] UINT iResourceID,  
     [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
     [in, out]  DWORD *pcchBuffer,  
     [in, lcid] LONG iLocaleID);  
```  
  
## <a name="parameters"></a>参数  

 `iResourceID`  
 中要转换的 HRESULT。  
  
 `pwzBuffer`  
 弄与给定的 HRESULT 关联的消息字符串。  
  
 `pcchBuffer`  
 [in，out] `pwzbuffer` 用于避免缓冲区溢出的的大小。 如果 `pwzbuffer` 为 null，则 `pcchBuffer` 提供的预期大小 `pwzbuffer` 允许预先分配。  
  
 `iLocaleID`  
 中区域性标识符。 若要使用默认区域性，则必须指定-1。  
  
## <a name="return-value"></a>返回值  

 此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|该方法已成功完成。|  
|E_POINTER|`pcchBuffer` 为 null。|  
|E_INVALIDARG|`pwzBuffer` 为 null。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** MetaHost  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRRuntimeInfo 接口](iclrruntimeinfo-interface.md)
- [承载接口](hosting-interfaces.md)
- [承载](index.md)
