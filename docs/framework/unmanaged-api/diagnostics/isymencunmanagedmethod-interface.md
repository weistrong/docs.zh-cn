---
description: 了解详细信息： ISymENCUnmanagedMethod 接口
title: ISymENCUnmanagedMethod 接口
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod
helpviewer_keywords:
- ISymENCUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: faebf594-67d5-4abf-b9c1-547fd3a1ff87
topic_type:
- apiref
ms.openlocfilehash: 59dd56c20279b2507fc4432182d0abb5b3e9c289
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790316"
---
# <a name="isymencunmanagedmethod-interface"></a>ISymENCUnmanagedMethod 接口

提供 "编辑并继续" 功能的信息。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetDocumentsForMethod 方法](isymencunmanagedmethod-getdocumentsformethod-method.md)|获取此方法在中具有线条的文档。|  
|[GetDocumentsForMethodCount 方法](isymencunmanagedmethod-getdocumentsformethodcount-method.md)|获取此方法在中包含行的文档数。|  
|[GetFileNameFromOffset 方法](isymencunmanagedmethod-getfilenamefromoffset-method.md)|获取与偏移量关联的行的文件名。|  
|[GetLineFromOffset 方法](isymencunmanagedmethod-getlinefromoffset-method.md)|获取与偏移量关联的行信息。|  
|[GetSourceExtentInDocument 方法](isymencunmanagedmethod-getsourceextentindocument-method.md)|获取特定文档中该方法的最小起始行和最大结束行。|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
