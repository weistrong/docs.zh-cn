---
description: 了解详细信息： ICorDebugRemoteTarget 接口
title: ICorDebugRemoteTarget 接口
ms.date: 03/30/2017
api_name:
- ICorDebugRemoteTarget
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget
helpviewer_keywords:
- ICorDebugRemoteTarget interface [.NET Framework debugging]
ms.assetid: bd9936a6-cc24-4869-8761-0988664464e6
topic_type:
- apiref
ms.openlocfilehash: c6567ebb76c7a3c415c9978dc50941cb0b8985a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717870"
---
# <a name="icordebugremotetarget-interface"></a><span data-ttu-id="a1f58-103">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="a1f58-103">ICorDebugRemoteTarget Interface</span></span>

<span data-ttu-id="a1f58-104">介绍能够让开发人员在公共语言运行时 (CLR) 环境中调试基于 Silverlight 的应用程序的方法。</span><span class="sxs-lookup"><span data-stu-id="a1f58-104">Provides methods that enable developers to debug Silverlight-based applications in the common language runtime (CLR) environment.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1f58-105">语法</span><span class="sxs-lookup"><span data-stu-id="a1f58-105">Syntax</span></span>  
  
```cpp  
interface ICorDebugRemoteTarget  : IUnknown  
{  
    HRESULT GetHostName (  
        [in]  ULONG32                    cchHostName,  
        [out] ULONG32*                   pcchHostName,  
        [out, size_is(cchHostName),  
              length_is(*pcchHostName)]  
                  WCHAR szHostName[]  
        );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a1f58-106">方法</span><span class="sxs-lookup"><span data-stu-id="a1f58-106">Methods</span></span>  
  
|<span data-ttu-id="a1f58-107">方法</span><span class="sxs-lookup"><span data-stu-id="a1f58-107">Method</span></span>|<span data-ttu-id="a1f58-108">说明</span><span class="sxs-lookup"><span data-stu-id="a1f58-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a1f58-109">ICorDebugRemoteTarget::GetHostName 方法</span><span class="sxs-lookup"><span data-stu-id="a1f58-109">ICorDebugRemoteTarget::GetHostName Method</span></span>](icordebugremotetarget-gethostname-method.md)|<span data-ttu-id="a1f58-110">返回远程计算机的主机名或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="a1f58-110">Returns the host name or the IP address of a remote machine.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a1f58-111">备注</span><span class="sxs-lookup"><span data-stu-id="a1f58-111">Remarks</span></span>  

 <span data-ttu-id="a1f58-112">在 Windows 95、Windows 98、Windows ME 或非 x86 平台（例如 IA-64 和 AMD64）上，不支持混合模式（即托管和本机代码）调试。</span><span class="sxs-lookup"><span data-stu-id="a1f58-112">Mixed-mode (that is, managed and native code) debugging is not supported on Windows 95, Windows 98, or Windows ME, or on non-x86 platforms (such as IA-64 and AMD64).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1f58-113">要求</span><span class="sxs-lookup"><span data-stu-id="a1f58-113">Requirements</span></span>  

 <span data-ttu-id="a1f58-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a1f58-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1f58-115">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="a1f58-115">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="a1f58-116">**库：** ： corguids.lib</span><span class="sxs-lookup"><span data-stu-id="a1f58-116">**Library:** : CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1f58-117">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="a1f58-117">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1f58-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1f58-118">See also</span></span>

- [<span data-ttu-id="a1f58-119">ICorDebugRemote 接口</span><span class="sxs-lookup"><span data-stu-id="a1f58-119">ICorDebugRemote Interface</span></span>](icordebugremote-interface.md)
- [<span data-ttu-id="a1f58-120">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="a1f58-120">ICorDebug Interface</span></span>](icordebug-interface.md)
- [<span data-ttu-id="a1f58-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="a1f58-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
