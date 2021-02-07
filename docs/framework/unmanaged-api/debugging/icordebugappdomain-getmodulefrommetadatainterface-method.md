---
description: 了解详细信息： ICorDebugAppDomain：： GetModuleFromMetaDataInterface 方法
title: ICorDebugAppDomain::GetModuleFromMetaDataInterface 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetModuleFromMetaDataInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDataInterface
helpviewer_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDatainterface method [.NET Framework debugging]
- GetModuleFromMetaDatainterface method [.NET Framework debugging]
ms.assetid: f35225b3-5dda-4d5a-913d-b3373e9ab81e
topic_type:
- apiref
ms.openlocfilehash: 7b0c74bd04024f9f4bf26b5ee8abe18a3a7059e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754233"
---
# <a name="icordebugappdomaingetmodulefrommetadatainterface-method"></a><span data-ttu-id="b8eb8-103">ICorDebugAppDomain::GetModuleFromMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="b8eb8-103">ICorDebugAppDomain::GetModuleFromMetaDataInterface Method</span></span>

<span data-ttu-id="b8eb8-104">获取与给定的元数据接口相对应的模块。</span><span class="sxs-lookup"><span data-stu-id="b8eb8-104">Gets the module that corresponds to the given metadata interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8eb8-105">语法</span><span class="sxs-lookup"><span data-stu-id="b8eb8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleFromMetaDataInterface (  
    [in] IUnknown           *pIMetaData,  
    [out] ICorDebugModule  **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8eb8-106">参数</span><span class="sxs-lookup"><span data-stu-id="b8eb8-106">Parameters</span></span>  

 `pIMetaData`  
 <span data-ttu-id="b8eb8-107">中指向对象的指针，该对象为 [元数据接口](../metadata/metadata-interfaces.md)之一。</span><span class="sxs-lookup"><span data-stu-id="b8eb8-107">[in] A pointer to an object that is one of the [Metadata interfaces](../metadata/metadata-interfaces.md).</span></span>  
  
 `ppModule`  
 <span data-ttu-id="b8eb8-108">弄指向 ICorDebugModule 对象的地址的指针，该对象表示与给定的元数据接口相对应的模块。</span><span class="sxs-lookup"><span data-stu-id="b8eb8-108">[out] A pointer to the address of an ICorDebugModule object that represents the module corresponding to the given metadata interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8eb8-109">要求</span><span class="sxs-lookup"><span data-stu-id="b8eb8-109">Requirements</span></span>  

 <span data-ttu-id="b8eb8-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b8eb8-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8eb8-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b8eb8-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b8eb8-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8eb8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8eb8-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8eb8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
