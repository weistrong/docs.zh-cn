---
description: 了解详细信息： IMetaDataDispenser 接口
title: IMetaDataDispenser 接口
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser
helpviewer_keywords:
- IMetaDataDispenser interface [.NET Framework metadata]
ms.assetid: 989840b3-9822-4ce5-a6c5-b375d3340a7a
topic_type:
- apiref
ms.openlocfilehash: 5ba37fc05a4e1897b100967d32b268f91a0e4402
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721003"
---
# <a name="imetadatadispenser-interface"></a>IMetaDataDispenser 接口

提供创建新的元数据范围或打开现有元数据范围的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[DefineScope 方法](imetadatadispenser-definescope-method.md)|在内存中创建新的区域，您可以在其中创建新的元数据。|  
|[OpenScope 方法](imetadatadispenser-openscope-method.md)|打开现有的磁盘上的文件，并将其元数据映射到内存。|  
|[OpenScopeOnMemory 方法](imetadatadispenser-openscopeonmemory-method.md)|打开包含现有元数据的内存区域。 也就是说，此方法将打开一个指定的内存区域，其中的现有数据将被视为元数据。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IMetaDataDispenserEx 接口](imetadatadispenserex-interface.md)
- [元数据接口](metadata-interfaces.md)
