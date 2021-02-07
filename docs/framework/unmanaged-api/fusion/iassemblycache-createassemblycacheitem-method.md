---
description: 了解详细信息： IAssemblyCache：： CreateAssemblyCacheItem 方法
title: IAssemblyCache::CreateAssemblyCacheItem 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCache.CreateAssemblyCacheItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::CreateAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCache::CreateAssemblyCacheItem method [.NET Framework fusion]
- CreateAssemblyCacheItem method [.NET Framework fusion]
ms.assetid: 017a7ba5-aaaf-44e2-9cbe-ceebef259df0
topic_type:
- apiref
ms.openlocfilehash: 3377901d358bcf643ce0d30336c1c0cd8089e50c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760974"
---
# <a name="iassemblycachecreateassemblycacheitem-method"></a>IAssemblyCache::CreateAssemblyCacheItem 方法

获取对新的 [IAssemblyCacheItem](iassemblycacheitem-interface.md) 对象的引用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateAssemblyCacheItem (  
    [in]  DWORD dwFlags,  
    [in]  PVOID pvReserved,  
    [out] IAssemblyCacheItem **ppAsmItem,  
    [in, optional] LPCWSTR pszAssemblyName  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwFlags`  
 中在合成 .idl 中定义的标志。 支持以下值：  
  
-  (0x00000001) IASSEMBLYCACHE_INSTALL_FLAG_REFRESH  
  
- IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)   
  
 `pvReserved`  
 中保留以供将来进行扩展。 `pvReserved` 必须为空引用。  
  
 `ppAsmItem`  
 弄返回的 `IAssemblyCacheItem` 指针。  
  
 `pszAssemblyName`  
 [in，可选]Uncanonicalized，以逗号分隔的 `name=value` 对。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyCache 接口](iassemblycache-interface.md)
- [IAssemblyCacheItem 接口](iassemblycacheitem-interface.md)
