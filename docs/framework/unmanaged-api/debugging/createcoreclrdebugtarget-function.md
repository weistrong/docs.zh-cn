---
description: 了解详细信息： CreateCoreClrDebugTarget 函数
title: CreateCoreClrDebugTarget 函数
ms.date: 03/30/2017
api_name:
- CreateCorClrDebugTarget
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CreateCoreClrDebugTarget
helpviewer_keywords:
- remote debugging API [Silverlight]
- Silverlight, remote debugging
- CreateCoreClrDebugTarget function
ms.assetid: 1cf4ca8e-d9bb-4633-9adf-5e24315bf87a
topic_type:
- apiref
ms.openlocfilehash: 30a6af29e6e1a6ee2c827049a3c792f2d663a702
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661571"
---
# <a name="createcoreclrdebugtarget-function"></a><span data-ttu-id="aa8f1-103">CreateCoreClrDebugTarget 函数</span><span class="sxs-lookup"><span data-stu-id="aa8f1-103">CreateCoreClrDebugTarget Function</span></span>

<span data-ttu-id="aa8f1-104">创建与远程计算机上运行的调试器代理的连接，并返回一个 [ICoreClrDebugTarget](icoreclrdebugtarget-interface.md) 对象，该对象可用于查询远程计算机上正在运行的进程和已加载的运行时。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-104">Creates a connection to a debugger proxy that is running on a remote machine, and returns an [ICoreClrDebugTarget](icoreclrdebugtarget-interface.md) object that can be used to query running processes and loaded runtimes on the remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa8f1-105">语法</span><span class="sxs-lookup"><span data-stu-id="aa8f1-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateCoreClrDebugTarget (  
       [in]  DWORD    dwAddress,
       [out] ICoreClrDebugTarget**     ppTarget  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aa8f1-106">参数</span><span class="sxs-lookup"><span data-stu-id="aa8f1-106">Parameters</span></span>  

 `dwAddress`  
 <span data-ttu-id="aa8f1-107">[in] 远程目标计算机的 IPv4 地址。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-107">[in] IPv4 address of a remote target machine.</span></span>  
  
 `ppTarget`  
 <span data-ttu-id="aa8f1-108">弄指向将创建的 [ICoreClrDebugTarget](icoreclrdebugtarget-interface.md) 对象的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-108">[out] Pointer to a pointer to an [ICoreClrDebugTarget](icoreclrdebugtarget-interface.md) object that will be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aa8f1-109">返回值</span><span class="sxs-lookup"><span data-stu-id="aa8f1-109">Return Value</span></span>  

 <span data-ttu-id="aa8f1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa8f1-110">S_OK</span></span>  
 <span data-ttu-id="aa8f1-111">已成功确定该进程中的 CLR 的数目，并已正确填写相应的句柄数组和路径数组。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-111">The number of CLRs in the process was successfully determined, and the corresponding handle and path arrays were properly filled.</span></span>  
  
 <span data-ttu-id="aa8f1-112">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="aa8f1-112">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="aa8f1-113">无法为 `ppTarget` 分配足够的内存。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-113">Unable to allocate enough memory for `ppTarget`.</span></span>  
  
 <span data-ttu-id="aa8f1-114">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="aa8f1-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="aa8f1-115">其他故障。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-115">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa8f1-116">要求</span><span class="sxs-lookup"><span data-stu-id="aa8f1-116">Requirements</span></span>  

 <span data-ttu-id="aa8f1-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aa8f1-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa8f1-118">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="aa8f1-118">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="aa8f1-119">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="aa8f1-119">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="aa8f1-120">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="aa8f1-120">**.NET Framework Versions:** 3.5 SP1</span></span>
