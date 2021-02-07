---
description: 了解详细信息： ICorDebugNativeFrame：： GetLocalMemoryValue 方法
title: ICorDebugNativeFrame::GetLocalMemoryValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalMemoryValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalMemoryValue
helpviewer_keywords:
- GetLocalMemoryValue method [.NET Framework debugging]
- ICorDebugNativeFrame::GetLocalMemoryValue method [.NET Framework debugging]
ms.assetid: b600b3a2-9908-42d8-8093-ab6f39e9a2c9
topic_type:
- apiref
ms.openlocfilehash: 5fbdf9474ca8c5849b7d917ecddff491b329113b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729232"
---
# <a name="icordebugnativeframegetlocalmemoryvalue-method"></a>ICorDebugNativeFrame::GetLocalMemoryValue 方法

获取在此本机帧的指定内存位置中存储的参数或局部变量的值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetLocalMemoryValue (  
    [in]  CORDB_ADDRESS      address,  
    [in]  ULONG              cbSigBlob,  
    [in]  PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a>参数  

 `address`  
 中一个 `CORDB_ADDRESS` 值，该值指定包含值的内存位置。  
  
 `cbSigBlob`  
 中一个整数，指定参数引用的二进制元数据签名的大小 `pvSigBlob` 。  
  
 `pvSigBlob`  
 中一个 `PCCOR_SIGNATURE` 值，该值指向值类型的二进制元数据签名。  
  
 `ppValue`  
 弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示存储在指定内存位置中的检索到的值。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅
