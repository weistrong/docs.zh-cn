---
description: 了解详细信息： GetWin32ResBlob 方法
title: GetWin32ResBlob 方法
ms.date: 03/30/2017
api_name:
- IALink.GetWin32ResBlob
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetWin32ResBlob
helpviewer_keywords:
- GetWin32ResBlob method
ms.assetid: 36997e04-f9f6-4254-a041-6767ac6c51d9
topic_type:
- apiref
ms.openlocfilehash: e1140b14bfba56dfac03c443a537d6d2188575b8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718260"
---
# <a name="getwin32resblob-method"></a><span data-ttu-id="6bae4-103">GetWin32ResBlob 方法</span><span class="sxs-lookup"><span data-stu-id="6bae4-103">GetWin32ResBlob Method</span></span>

<span data-ttu-id="6bae4-104">检索 Win32 资源 blob。</span><span class="sxs-lookup"><span data-stu-id="6bae4-104">Retrieves Win32 resource blob.</span></span> <span data-ttu-id="6bae4-105">在设置程序集选项后调用此方法。</span><span class="sxs-lookup"><span data-stu-id="6bae4-105">Call this method after setting assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bae4-106">语法</span><span class="sxs-lookup"><span data-stu-id="6bae4-106">Syntax</span></span>  
  
```cpp  
HRESULT GetWin32ResBlob(  
    mdAssembly    AssemblyID,  
    mdToken       FileToken,  
    BOOL          fDll,  
    LPCWSTR       pszIconFile,  
    const void**  ppResBlob,  
    DWORD*        pcbResBlob  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="6bae4-107">参数</span><span class="sxs-lookup"><span data-stu-id="6bae4-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="6bae4-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="6bae4-108">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="6bae4-109">用于检索构造 Win32 版本资源时要使用的文件名的文件标记</span><span class="sxs-lookup"><span data-stu-id="6bae4-109">File token used to retrieve the filename to be used when constructing the Win32 Version resource</span></span>  
  
 `fDll`  
 <span data-ttu-id="6bae4-110">如果文件是 DLL，则为 TRUE; 对于 EXE，则为 false。</span><span class="sxs-lookup"><span data-stu-id="6bae4-110">TRUE if file is a DLL, false for an EXE.</span></span>  
  
 `pszIconFile`  
 <span data-ttu-id="6bae4-111">要插入资源 blob 的可选图标。</span><span class="sxs-lookup"><span data-stu-id="6bae4-111">Optional icon to insert into the resource blob.</span></span>  
  
 `ppResBlob`  
 <span data-ttu-id="6bae4-112">接收资源 blob。</span><span class="sxs-lookup"><span data-stu-id="6bae4-112">Receives the resource blob.</span></span>  
  
 `pcbResBlob`  
 <span data-ttu-id="6bae4-113">接收 blob 的大小。</span><span class="sxs-lookup"><span data-stu-id="6bae4-113">Receives the size of the blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6bae4-114">返回值</span><span class="sxs-lookup"><span data-stu-id="6bae4-114">Return Value</span></span>  

 <span data-ttu-id="6bae4-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="6bae4-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bae4-116">要求</span><span class="sxs-lookup"><span data-stu-id="6bae4-116">Requirements</span></span>  

 <span data-ttu-id="6bae4-117">需要 alink</span><span class="sxs-lookup"><span data-stu-id="6bae4-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bae4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bae4-118">See also</span></span>

- [<span data-ttu-id="6bae4-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="6bae4-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="6bae4-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="6bae4-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="6bae4-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="6bae4-121">ALink API</span></span>](index.md)
