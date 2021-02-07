---
description: 了解详细信息： ISymUnmanagedSourceServerModule：： GetSourceServerData 方法
title: ISymUnmanagedSourceServerModule::GetSourceServerData 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule.GetSourceServerData
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData
helpviewer_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData method [.NET Framework debugging]
- GetSourceServerData method [.NET Framework debugging]
ms.assetid: 20bdf8ff-2d15-4c64-8950-6888f642d6c0
topic_type:
- apiref
ms.openlocfilehash: cdba764534000273170ccd693a3fbc7b5df9c3c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763158"
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a>ISymUnmanagedSourceServerModule::GetSourceServerData 方法

返回模块的源服务器数据。 调用方必须使用来释放资源 `CoTaskMemFree` 。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
## <a name="parameters"></a>参数  

 `pDataByteCount`  
 弄指向的指针， `ULONG32` 该指针接收源服务器数据的大小（以字节为单位）。  
  
 `ppData`  
 弄指向返回值的指针 `pDataByteCount` 。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedSourceServerModule 接口](isymunmanagedsourceservermodule-interface.md)
