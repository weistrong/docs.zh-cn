---
description: 了解详细信息： SetManifestFile 方法
title: SetManifestFile 方法
ms.date: 03/30/2017
api_name:
- IALink3.SetManifestFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetManifestFile
helpviewer_keywords:
- SetManifestFile method
ms.assetid: 1b33de4c-19cb-4a36-a93f-8675b2a36d58
topic_type:
- apiref
ms.openlocfilehash: fe91c7f2b4e6f58a0a740de84e055ead49adb77d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662320"
---
# <a name="setmanifestfile-method"></a><span data-ttu-id="9f7fa-103">SetManifestFile 方法</span><span class="sxs-lookup"><span data-stu-id="9f7fa-103">SetManifestFile Method</span></span>

<span data-ttu-id="9f7fa-104">使您能够在创建程序集时指定或重置链接器使用的清单文件。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-104">Enables you to specify or reset the manifest file that the linker uses when it creates the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f7fa-105">语法</span><span class="sxs-lookup"><span data-stu-id="9f7fa-105">Syntax</span></span>  
  
```cpp  
HRESULT SetManifestFile(  
    LPCWSTR pszFile  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="9f7fa-106">参数</span><span class="sxs-lookup"><span data-stu-id="9f7fa-106">Parameters</span></span>  

 `pszFile`  
  
 <span data-ttu-id="9f7fa-107">其内容将放入 Win32 资源 blob 中的清单文件的名称。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-107">The name of the manifest file whose contents are put into the Win32 resources blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9f7fa-108">返回值</span><span class="sxs-lookup"><span data-stu-id="9f7fa-108">Return Value</span></span>  

 <span data-ttu-id="9f7fa-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9f7fa-110">备注</span><span class="sxs-lookup"><span data-stu-id="9f7fa-110">Remarks</span></span>  

 <span data-ttu-id="9f7fa-111">在请求 Win32ResBlob 之前调用此。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-111">Call this before asking for the Win32ResBlob.</span></span> <span data-ttu-id="9f7fa-112">参数的值 `pszFile` 是清单文件的名称，其内容读取并放入 Win32 资源中，其 ID 为 RT_MANIFEST。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-112">The value of the `pszFile` parameter is the name of the manifest file whose contents are read and put in the Win32 resources with ID of RT_MANIFEST.</span></span> <span data-ttu-id="9f7fa-113">使用 NULL 的参数调用时，将清除任何以前的读取清单。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-113">When called by using a parameter of NULL, any previously read manifest is cleared.</span></span> <span data-ttu-id="9f7fa-114">这样一来，就可以将链接器的状态重置为初始化时的状态。</span><span class="sxs-lookup"><span data-stu-id="9f7fa-114">This enables one to reset the state of the linker to that of initialization time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f7fa-115">要求</span><span class="sxs-lookup"><span data-stu-id="9f7fa-115">Requirements</span></span>  

 <span data-ttu-id="9f7fa-116">需要 aLink</span><span class="sxs-lookup"><span data-stu-id="9f7fa-116">Requires aLink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f7fa-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f7fa-117">See also</span></span>

- [<span data-ttu-id="9f7fa-118">IALink3 接口</span><span class="sxs-lookup"><span data-stu-id="9f7fa-118">IALink3 Interface</span></span>](ialink3-interface.md)
- [<span data-ttu-id="9f7fa-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="9f7fa-119">ALink API</span></span>](index.md)
- [<span data-ttu-id="9f7fa-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="9f7fa-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="9f7fa-121">Al.exe（程序集链接器）</span><span class="sxs-lookup"><span data-stu-id="9f7fa-121">Al.exe (Assembly Linker)</span></span>](../../tools/al-exe-assembly-linker.md)
