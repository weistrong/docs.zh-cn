---
description: 了解详细信息： ISymUnmanagedENCUpdate：： GetLocalVariables 方法
title: ISymUnmanagedENCUpdate::GetLocalVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables method [.NET Framework debugging]
- GetLocalVariables method [.NET Framework debugging]
ms.assetid: 5c8840be-ffea-447f-9c8d-178f1eaf8d06
topic_type:
- apiref
ms.openlocfilehash: bc034603dd6a09ea78dad789e11ea951d65e839b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721458"
---
# <a name="isymunmanagedencupdategetlocalvariables-method"></a>ISymUnmanagedENCUpdate::GetLocalVariables 方法

获取局部变量。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetLocalVariables(  
    [in]  mdMethodDef  mdMethodToken,  
    [in]  ULONG        cLocals,  
    [out, size_is(cLocals), length_is(*pceltFetched)]  
        ISymUnmanagedVariable *rgLocals[],  
    [out] ULONG        *pceltFetched);  
```  
  
## <a name="parameters"></a>参数  

 `mdMethodToken`  
 中方法的元数据标记。  
  
 `cLocals`  
 中 `ULONG` 指示参数大小的 `rgLocals` 。  
  
 `rgLocals`  
 弄返回的 [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) 实例的数组。  
  
 `pceltFetched`  
 弄指向的指针 `ULONG` ，该指针接收 `rgLocals` 包含局部变量所需的缓冲区大小。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedENCUpdate 接口](isymunmanagedencupdate-interface.md)
