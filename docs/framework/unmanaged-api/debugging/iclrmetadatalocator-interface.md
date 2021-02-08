---
description: 了解详细信息： ICLRMetadataLocator 接口
title: ICLRMetadataLocator 接口
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator
helpviewer_keywords:
- ICLRMetadataLocator interface [.NET Framework debugging]
ms.assetid: 43c944f4-406a-4df6-981e-0eabb33dd5d0
topic_type:
- apiref
ms.openlocfilehash: 6e7fd45197294563e12da020379d1bd54b088698
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772597"
---
# <a name="iclrmetadatalocator-interface"></a>ICLRMetadataLocator 接口

由数据访问服务层用于在目标进程中查找程序集的元数据。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetMetadata 方法](iclrmetadatalocator-getmetadata-method.md)|从目标进程中检索图像的元数据。|  
  
## <a name="remarks"></a>备注  

 API 客户端（即调试器）必须针对特定的目标进程实现此接口。 例如，实时过程的实现与内存转储的实现不同。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** ClrData，ClrData  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
