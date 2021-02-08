---
description: 了解详细信息： IDebugAutoAttach：： AutoAttach 方法
title: IDebugAutoAttach::AutoAttach 方法
ms.date: 03/30/2017
api_name:
- IDebugAutoAttach.AutoAttach
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IDebugAutoAttach::AutoAttach
helpviewer_keywords:
- AutoAttach method [.NET Framework debugging]
- IDebugAutoAttach::AutoAttach method [.NET Framework debugging]
ms.assetid: 3cf3bd9c-7d88-4afa-a476-94cdc7609aa6
topic_type:
- apiref
ms.openlocfilehash: 8abd35b1d94fc074d4dafe424c52c274b1de1541
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800352"
---
# <a name="idebugautoattachautoattach-method"></a><span data-ttu-id="d59a9-103">IDebugAutoAttach::AutoAttach 方法</span><span class="sxs-lookup"><span data-stu-id="d59a9-103">IDebugAutoAttach::AutoAttach Method</span></span>

<span data-ttu-id="d59a9-104">执行服务器调用的调试器自动附加。</span><span class="sxs-lookup"><span data-stu-id="d59a9-104">Performs server-invoked debugger auto attach.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d59a9-105">语法</span><span class="sxs-lookup"><span data-stu-id="d59a9-105">Syntax</span></span>  
  
```cpp  
HRESULT AutoAttach  
(  
    [in]  REFGUID   guidPort,  
    [in]  DWORD     dwPid,  
    [in]  AUTOATTACH_PROGRAM_TYPE dwProgramType,  
    [in]  DWORD     dwProgramId,  
    [in]  LPCWSTR   pszSessionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d59a9-106">参数</span><span class="sxs-lookup"><span data-stu-id="d59a9-106">Parameters</span></span>  

 `guidPort`  
 <span data-ttu-id="d59a9-107">中始终设置为 `GUID_NULL` 。</span><span class="sxs-lookup"><span data-stu-id="d59a9-107">[in] Always set to `GUID_NULL`.</span></span>  
  
 `dwPid`  
 <span data-ttu-id="d59a9-108">中进程 ID，通常通过函数检索 `GetCurrentProcessId` 。</span><span class="sxs-lookup"><span data-stu-id="d59a9-108">[in] Process ID, normally retrieved with the `GetCurrentProcessId` function.</span></span>  
  
 `dwProgramType`  
 <span data-ttu-id="d59a9-109">中程序类型： `AUTOATTACH_PROGRAM_WIN32` 、 `AUTOATTACH_PROGRAM_COMPLUS` 或 `AUTOATTACH_PROGRAM_UNKNOWN` 。</span><span class="sxs-lookup"><span data-stu-id="d59a9-109">[in] Program type: `AUTOATTACH_PROGRAM_WIN32`, `AUTOATTACH_PROGRAM_COMPLUS`, or `AUTOATTACH_PROGRAM_UNKNOWN`.</span></span>  
  
 `dwProgramId`  
 <span data-ttu-id="d59a9-110">中程序 ID。</span><span class="sxs-lookup"><span data-stu-id="d59a9-110">[in] Program ID.</span></span>  
  
 `pszSessionId`  
 <span data-ttu-id="d59a9-111">中调试谓词传递的字符串。</span><span class="sxs-lookup"><span data-stu-id="d59a9-111">[in] String passed by the debug verb.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d59a9-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d59a9-112">Return Value</span></span>  

 <span data-ttu-id="d59a9-113">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="d59a9-113">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d59a9-114">要求</span><span class="sxs-lookup"><span data-stu-id="d59a9-114">Requirements</span></span>  

 <span data-ttu-id="d59a9-115">**标头：** DbgAutoAttach</span><span class="sxs-lookup"><span data-stu-id="d59a9-115">**Header:** DbgAutoAttach.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d59a9-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d59a9-116">See also</span></span>

- [<span data-ttu-id="d59a9-117">IDebugAutoAttach 接口</span><span class="sxs-lookup"><span data-stu-id="d59a9-117">IDebugAutoAttach Interface</span></span>](idebugautoattach-interface.md)
