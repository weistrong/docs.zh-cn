---
description: 了解详细信息： SetAssemblyProps 方法
title: SetAssemblyProps 方法
ms.date: 03/30/2017
api_name:
- IALink.SetAssemblyProps
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyProps
helpviewer_keywords:
- SetAssemblyProps method
ms.assetid: a3d7cf29-1414-49e6-8aae-9b3283c4f5f0
topic_type:
- apiref
ms.openlocfilehash: 212d8aad22ac1cb231db46f20ff65de2339a21aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662346"
---
# <a name="setassemblyprops-method"></a><span data-ttu-id="b1b6d-103">SetAssemblyProps 方法</span><span class="sxs-lookup"><span data-stu-id="b1b6d-103">SetAssemblyProps Method</span></span>

<span data-ttu-id="b1b6d-104">分配程序集级别属性。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-104">Assigns assembly-level properties.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1b6d-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1b6d-105">Syntax</span></span>  
  
```cpp  
HRESULT SetAssemblyProps(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    AssemblyOptions Option,  
    VARIANT         Value  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1b6d-106">参数</span><span class="sxs-lookup"><span data-stu-id="b1b6d-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="b1b6d-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="b1b6d-108">定义属性的文件。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-108">File that defines the property.</span></span> <span data-ttu-id="b1b6d-109">如果不 `AssemblyID` 指示未绑定的 .netmodule，则可以为 NULL。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-109">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `Option`  
 <span data-ttu-id="b1b6d-110">指示要修改的选项。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-110">Indicates the option to modify.</span></span>  
  
 `Value`  
 <span data-ttu-id="b1b6d-111">选项的新值。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-111">New value of the option.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b1b6d-112">返回值</span><span class="sxs-lookup"><span data-stu-id="b1b6d-112">Return Value</span></span>  

 <span data-ttu-id="b1b6d-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1b6d-114">要求</span><span class="sxs-lookup"><span data-stu-id="b1b6d-114">Requirements</span></span>  

 <span data-ttu-id="b1b6d-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="b1b6d-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1b6d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1b6d-116">See also</span></span>

- [<span data-ttu-id="b1b6d-117">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="b1b6d-117">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="b1b6d-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="b1b6d-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="b1b6d-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="b1b6d-119">ALink API</span></span>](index.md)
