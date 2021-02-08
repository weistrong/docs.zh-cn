---
description: 了解详细信息： InitDbgTransportManager 函数
title: InitDbgTransportManager 函数
ms.date: 03/30/2017
api_name:
- InitDbgTransportManager
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- InitDbgTransportManager
helpviewer_keywords:
- remote debugging API [Silverlight]
- InitDbgTransportManager function
- Silverlight, remote debugging
ms.assetid: a30102ff-c52e-48c9-b3a9-aa14286a42b2
topic_type:
- apiref
ms.openlocfilehash: 19cdfcbe3a5b120c11fc781476410833997b8c6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790433"
---
# <a name="initdbgtransportmanager-function"></a><span data-ttu-id="18647-103">InitDbgTransportManager 函数</span><span class="sxs-lookup"><span data-stu-id="18647-103">InitDbgTransportManager Function</span></span>

<span data-ttu-id="18647-104">初始化传输管理器以连接到进程和运行时枚举的远程目标。</span><span class="sxs-lookup"><span data-stu-id="18647-104">Initializes the transport manager to connect to a remote target for process and runtime enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18647-105">语法</span><span class="sxs-lookup"><span data-stu-id="18647-105">Syntax</span></span>  
  
```cpp  
HRESULT InitDbgTransportManager ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="18647-106">返回值</span><span class="sxs-lookup"><span data-stu-id="18647-106">Return Value</span></span>  

 <span data-ttu-id="18647-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="18647-107">S_OK</span></span>  
 <span data-ttu-id="18647-108">成功。</span><span class="sxs-lookup"><span data-stu-id="18647-108">Success.</span></span>  
  
 <span data-ttu-id="18647-109">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="18647-109">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="18647-110">该函数不能为传输管理器分配内存。</span><span class="sxs-lookup"><span data-stu-id="18647-110">The function was unable to allocate memory for a transport manager.</span></span>  
  
 <span data-ttu-id="18647-111">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="18647-111">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="18647-112">其他故障。</span><span class="sxs-lookup"><span data-stu-id="18647-112">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18647-113">要求</span><span class="sxs-lookup"><span data-stu-id="18647-113">Requirements</span></span>  

 <span data-ttu-id="18647-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="18647-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18647-115">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="18647-115">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="18647-116">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="18647-116">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="18647-117">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="18647-117">**.NET Framework Versions:** 3.5 SP1</span></span>
