---
description: 了解详细信息： _CorExeMain2 函数
title: _CorExeMain2 函数
ms.date: 03/30/2017
api_name:
- _CorExeMain2
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorExeMain2
helpviewer_keywords:
- _CorExeMain2 function [.NET Framework hosting]
ms.assetid: 72ea68b4-689f-4733-9416-9664b75e8892
topic_type:
- apiref
ms.openlocfilehash: 4629ea2f6c2ba13351c409bc382077eea926b507
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717090"
---
# <a name="_corexemain2-function"></a>_CorExeMain2 函数

执行指定的内存映射代码中的入口点。 此函数由操作系统加载程序调用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
__int32 STDMETHODCALLTYPE _CorExeMain2 (  
   [in] PBYTE           pUnmappedPE,  
   [in] DWORD           cUnmappedPE,  
   [in] __in LPWSTR     pImageNameIn,  
   [in] __in LPWSTR     pLoadersFileName,  
   [in] __in LPWSTR     pCmdLine  
);  
```  
  
## <a name="parameters"></a>参数  

 `pUnmappedPE`  
 中指向内存映射代码的指针。  
  
 `cUnmappedPE`  
 中可以容纳的元素数 `pUnmappedPE` 。  
  
 `pImageNameIn`  
 中指向可执行图像的名称的指针。  
  
 `pLoadersFileName`  
 中加载程序文件的名称。  
  
 `pCmdLine`  
 中命令行参数（如果有）。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据全局静态函数](../metadata/metadata-global-static-functions.md)
