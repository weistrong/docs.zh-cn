---
description: 了解详细信息： ISymUnmanagedSourceServerModule 接口
title: ISymUnmanagedSourceServerModule 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule
helpviewer_keywords:
- ISymUnmanagedSourceServerModule interface [.NET Framework debugging]
ms.assetid: a19b23bd-2061-476e-b67d-252f57404f8b
topic_type:
- apiref
ms.openlocfilehash: c837af4cda443ec93bfbaa2d73feeb2b8f8a2803
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763119"
---
# <a name="isymunmanagedsourceservermodule-interface"></a>ISymUnmanagedSourceServerModule 接口

提供模块的源服务器数据。 通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetSourceServerData 方法](isymunmanagedsourceservermodule-getsourceserverdata-method.md)|返回模块的源服务器数据。|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
