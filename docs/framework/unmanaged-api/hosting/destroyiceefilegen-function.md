---
description: 了解详细信息： DestroyICeeFileGen 函数
title: DestroyICeeFileGen 函数
ms.date: 03/30/2017
api_name:
- DestroyICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- DestroyICeeFileGen
helpviewer_keywords:
- DestroyICeeFileGen function [.NET Framework hosting]
ms.assetid: dc1e2235-e721-4cb2-a0b8-6b0c030d7bab
topic_type:
- apiref
ms.openlocfilehash: 14ae990999247b90f16b10115dea3408b965a04a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785648"
---
# <a name="destroyiceefilegen-function"></a>DestroyICeeFileGen 函数

销毁 [ICeeFileGen](iceefilegen-class.md) 对象。  
  
 此函数已在 .NET Framework 4 中弃用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DestroyICeeFileGen (  
    [in] ICeeFileGen  **ceeFileGen  
);  
```  
  
## <a name="parameters"></a>参数  

 `ceeFileGen`  
 中 `ICeeFileGen` 要销毁的对象。  
  
## <a name="return-value"></a>返回值  

 此方法返回标准 COM 错误代码。  
  
## <a name="remarks"></a>备注  

 `DestroyICeeFileGen` 销毁 `ICeeFileGen` [CreateICeeFileGen](createiceefilegen-function.md) 函数创建的对象。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** ICeeFileGen  
  
 **库：** MSCorPE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md)
