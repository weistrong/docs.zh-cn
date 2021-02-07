---
description: 了解详细信息： ICorDebugFrame：： GetCode 方法
title: ICorDebugFrame::GetCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCode
helpviewer_keywords:
- GetCode method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetCode method [.NET Framework debugging]
ms.assetid: fbaa0794-a031-4015-8beb-2749e47ac340
topic_type:
- apiref
ms.openlocfilehash: f45e0a29530a8b4ddbeaa92db4489a030ac1ae79
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693000"
---
# <a name="icordebugframegetcode-method"></a><span data-ttu-id="eecc3-103">ICorDebugFrame::GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="eecc3-103">ICorDebugFrame::GetCode Method</span></span>

<span data-ttu-id="eecc3-104">获取一个指针，该指针指向与此堆栈帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="eecc3-104">Gets a pointer to the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eecc3-105">语法</span><span class="sxs-lookup"><span data-stu-id="eecc3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCode (  
    [out] ICorDebugCode      **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eecc3-106">参数</span><span class="sxs-lookup"><span data-stu-id="eecc3-106">Parameters</span></span>  

 `ppCode`  
 <span data-ttu-id="eecc3-107">弄指向 ICorDebugCode 对象的地址的指针，该对象表示与此帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="eecc3-107">[out] A pointer to the address of an ICorDebugCode object that represents the code associated with this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eecc3-108">要求</span><span class="sxs-lookup"><span data-stu-id="eecc3-108">Requirements</span></span>  

 <span data-ttu-id="eecc3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eecc3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eecc3-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eecc3-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eecc3-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eecc3-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eecc3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eecc3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
