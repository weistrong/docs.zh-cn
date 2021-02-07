---
description: 了解详细信息： ISymUnmanagedBinder3 接口
title: ISymUnmanagedBinder3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3 Interface
helpviewer_keywords:
- ISymUnmanagedBinder3 interface [.NET Framework debugging]
ms.assetid: 37527a84-4b03-4f08-8135-94d898599089
topic_type:
- apiref
ms.openlocfilehash: 6d2172fb119076cea6d0f912fb3f403d36856599
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689828"
---
# <a name="isymunmanagedbinder3-interface"></a>ISymUnmanagedBinder3 接口

扩展符号联编程序接口。 通过对实现接口的对象调用来获取此接口 `QueryInterface` `ISymUnmanagedBinder` 。  
  
> [!IMPORTANT]
> 从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetReaderFromCallback 方法](isymunmanagedbinder3-getreaderfromcallback-method.md)|允许用户通过回调来实现或提供， `IID_IDiaReadExeAtRVACallback` `IID_IDiaReadExeAtOffsetCallback` 以从内存中获取调试目录信息|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedBinder 接口](isymunmanagedbinder-interface.md)
- [ISymUnmanagedBinder2 接口](isymunmanagedbinder2-interface.md)
