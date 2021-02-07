---
description: 了解详细信息： ISymUnmanagedWriter3 接口
title: ISymUnmanagedWriter3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3
helpviewer_keywords:
- ISymUnmanagedWriter3 interface [.NET Framework debugging]
ms.assetid: a034c21e-e371-4360-b470-29e88288948f
topic_type:
- apiref
ms.openlocfilehash: 586220af85f193b43acf0578706d9f67e3e83386
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761728"
---
# <a name="isymunmanagedwriter3-interface"></a>ISymUnmanagedWriter3 接口

表示符号编写器，并提供定义文档、序列点、词法范围和变量的方法。 此接口扩展 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[Commit 方法](isymunmanagedwriter3-commit-method.md)|将迄今为止写入的更改提交到流。|  
|[OpenMethod2 方法](isymunmanagedwriter3-openmethod2-method.md)|打开方法并在图像中提供其实际节偏移量。|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
- [ISymUnmanagedWriter2 接口](isymunmanagedwriter2-interface.md)
