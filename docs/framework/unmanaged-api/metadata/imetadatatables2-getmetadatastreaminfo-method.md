---
description: 了解详细信息： IMetaDataTables2：： GetMetaDataStreamInfo 方法
title: IMetaDataTables2::GetMetaDataStreamInfo 方法
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStreamInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStreamInfo
helpviewer_keywords:
- GetMetaDataStreamInfo method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStreamInfo method [.NET Framework metadata]
ms.assetid: 8b280627-cc74-4789-95da-1fefc966de05
topic_type:
- apiref
ms.openlocfilehash: 323c31931cc97f18ff09df83c57153a3629d0a10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799234"
---
# <a name="imetadatatables2getmetadatastreaminfo-method"></a>IMetaDataTables2::GetMetaDataStreamInfo 方法

获取指定索引处的元数据流的名称、大小和内容。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetMetaDataStreamInfo (  
   [in]  ULONG        ix,  
   [out] const char   **ppchName,  
   [out] const void   **ppv,  
   [out] ULONG        *pcb  
);  
```  
  
## <a name="parameters"></a>参数  

 `ix`  
 中请求的元数据流的索引。  
  
 `ppchName`  
 弄指向流名称的指针。  
  
 `ppv`  
 弄指向元数据流的指针。  
  
 `pcb`  
 弄的大小（以字节为单位） `ppv` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataTables2 接口](imetadatatables2-interface.md)
- [IMetaDataTables 接口](imetadatatables-interface.md)
