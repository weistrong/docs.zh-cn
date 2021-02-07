---
description: 了解详细信息： RunDll32ShimW 函数
title: RunDll32ShimW 函数
ms.date: 03/30/2017
api_name:
- RunDll32ShimW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- RunDll32ShimW
helpviewer_keywords:
- RunDll32ShimW function [.NET Framework hosting]
ms.assetid: 9ea07b57-96e2-44df-8711-8fe6c119087f
topic_type:
- apiref
ms.openlocfilehash: d01021358a6cddf15d1a0e1b223c9acff3c64ff7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679480"
---
# <a name="rundll32shimw-function"></a><span data-ttu-id="2c94f-103">RunDll32ShimW 函数</span><span class="sxs-lookup"><span data-stu-id="2c94f-103">RunDll32ShimW Function</span></span>

<span data-ttu-id="2c94f-104">执行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="2c94f-104">Executes the specified command.</span></span>  
  
 <span data-ttu-id="2c94f-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="2c94f-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c94f-106">语法</span><span class="sxs-lookup"><span data-stu-id="2c94f-106">Syntax</span></span>  
  
```cpp  
HRESULT RunDll32ShimW (  
    [in] HWND        hwnd,  
    [in] HINSTANCE   hinst,  
    [in] LPCWSTR     lpszCmdLine,  
    [in] int         nCmdShow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2c94f-107">参数</span><span class="sxs-lookup"><span data-stu-id="2c94f-107">Parameters</span></span>  

 `hwnd`  
 <span data-ttu-id="2c94f-108">中将在其中显示命令输出的窗口的句柄。</span><span class="sxs-lookup"><span data-stu-id="2c94f-108">[in] A handle to a window in which the command output will be displayed.</span></span>  
  
 `hinst`  
 <span data-ttu-id="2c94f-109">中包含命令的库的句柄。</span><span class="sxs-lookup"><span data-stu-id="2c94f-109">[in] A handle to the library that contains the command.</span></span>  
  
 `lpszCmdLine`  
 <span data-ttu-id="2c94f-110">中一个字符串，指定要执行的命令。</span><span class="sxs-lookup"><span data-stu-id="2c94f-110">[in] A string that specifies the command to be executed.</span></span>  
  
 `nCmdShow`  
 <span data-ttu-id="2c94f-111">中一个整数，指定 "输出" 窗口的显示模式。</span><span class="sxs-lookup"><span data-stu-id="2c94f-111">[in] An integer that specifies the display mode for the output window.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c94f-112">要求</span><span class="sxs-lookup"><span data-stu-id="2c94f-112">Requirements</span></span>  

 <span data-ttu-id="2c94f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2c94f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2c94f-114">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="2c94f-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2c94f-115">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2c94f-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2c94f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c94f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c94f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c94f-117">See also</span></span>

- [<span data-ttu-id="2c94f-118">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="2c94f-118">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
