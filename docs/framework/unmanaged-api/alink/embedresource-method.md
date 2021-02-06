---
description: 了解详细信息： EmbedResource 方法
title: EmbedResource 方法
ms.date: 03/30/2017
api_name:
- IALink.EmbedResource
- EmbedResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmbedResource
helpviewer_keywords:
- EmbedResource method
ms.assetid: 667bd954-6dc6-4020-a3cb-0e8224179993
topic_type:
- apiref
ms.openlocfilehash: f7896172e7416048352788caf7e092096924b7af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638348"
---
# <a name="embedresource-method"></a>EmbedResource 方法

声明嵌入的资源。 此方法并不实际嵌入资源。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EmbedResource(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    LPCWSTR     pszResourceName,  
    DWORD       dwOffset,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a>参数  

 `AssemblyID`  
 程序集的 ID。  
  
 `FileToken`  
 包含资源的文件的文件标记或程序集 ID。  
  
 `pszResourceName`  
 资源的名称。  
  
 `dwOffset`  
 RVA 中资源的偏移量。  
  
 `dwFlags`  
 辅助功能标志 `mrPublic` ，例如和 `mrPrivate` 。 这些标志可能会传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。  
  
## <a name="return-value"></a>返回值  

 如果方法成功，则返回 S_OK。  
  
## <a name="requirements"></a>要求  

 需要 alink。  
  
## <a name="see-also"></a>请参阅

- [IALink 接口](ialink-interface.md)
- [IALink2 接口](ialink2-interface.md)
- [ALink API](index.md)
