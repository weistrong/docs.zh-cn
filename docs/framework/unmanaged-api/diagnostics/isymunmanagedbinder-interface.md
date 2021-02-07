---
description: 了解详细信息： ISymUnmanagedBinder 接口
title: ISymUnmanagedBinder 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder
helpviewer_keywords:
- ISymUnmanagedBinder interface [.NET Framework debugging]
ms.assetid: b22fbe19-b30f-4696-8175-e6b91da9edab
topic_type:
- apiref
ms.openlocfilehash: 14ebccb028ab3388a8058dd05504c56a6df74c95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689919"
---
# <a name="isymunmanagedbinder-interface"></a>ISymUnmanagedBinder 接口

表示非托管代码的符号绑定器。  
  
> [!IMPORTANT]
> 从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetReaderForFile 方法](isymunmanagedbinder-getreaderforfile-method.md)|给定元数据接口和文件名后，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将读取与模块关联的调试符号。|  
|[GetReaderFromStream 方法](isymunmanagedbinder-getreaderfromstream-method.md)|给定元数据接口和包含符号存储区的流时，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将从给定的符号存储区中读取调试符号。|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedBinder2 接口](isymunmanagedbinder2-interface.md)
- [ISymUnmanagedBinder3 接口](isymunmanagedbinder3-interface.md)
