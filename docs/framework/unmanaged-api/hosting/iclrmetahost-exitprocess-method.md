---
description: 了解详细信息： ICLRMetaHost：： ExitProcess 方法
title: ICLRMetaHost::ExitProcess 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.ExitProcess
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::ExitProcess
helpviewer_keywords:
- ICLRMetaHost::ExitProcess method [.NET Framework hosting]
- ExitProcess method, ICLRMetaHost interface [.NET Framework hosting]
ms.assetid: b4df98cc-4e4e-407b-b8f4-e0076afef3a4
topic_type:
- apiref
ms.openlocfilehash: 3bc832538a5ad2b457de758fc35a632b09c02974
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689152"
---
# <a name="iclrmetahostexitprocess-method"></a>ICLRMetaHost::ExitProcess 方法

尝试正常关闭所有加载的运行时，然后终止进程。 取代 [CorExitProcess](corexitprocess-function.md) 函数。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ExitProcess (  
    [in] INT32 iExitCode);  
```  
  
## <a name="parameters"></a>参数  

 `iExitCode`  
 中进程的退出代码。  
  
## <a name="return-value"></a>返回值  

 此方法从不返回，因此其返回值未定义。  
  
## <a name="remarks"></a>备注  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** MetaHost  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRMetaHost 接口](iclrmetahost-interface.md)
- [承载](index.md)
