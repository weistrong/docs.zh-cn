---
description: 了解详细信息： SetPEKind 方法
title: SetPEKind 方法
ms.date: 03/30/2017
api_name:
- IALink2.SetPEKind
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetPEKind
helpviewer_keywords:
- SetPEKind method
ms.assetid: 050e77ee-3014-45c0-9e29-2ebe29347b0d
topic_type:
- apiref
ms.openlocfilehash: 4154e9e80b7f88b6951c9aa8da5fc23d340c96dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662294"
---
# <a name="setpekind-method"></a><span data-ttu-id="1dbd0-103">SetPEKind 方法</span><span class="sxs-lookup"><span data-stu-id="1dbd0-103">SetPEKind Method</span></span>

<span data-ttu-id="1dbd0-104">确定可移植的可执行文件类型（特定于计算机或计算机不可知）。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-104">Determines the portable executable type, either machine-specific or machine-agnostic.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dbd0-105">语法</span><span class="sxs-lookup"><span data-stu-id="1dbd0-105">Syntax</span></span>  
  
```cpp  
HRESULT SetPEKind(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwPEKind,  
    DWORD dwMachine  
) PURE;
```  
  
## <a name="parameters"></a><span data-ttu-id="1dbd0-106">参数</span><span class="sxs-lookup"><span data-stu-id="1dbd0-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="1dbd0-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="1dbd0-108">要为其设置 PE 类型的文件的标记。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-108">Token of file for which the PE type is to be set.</span></span> <span data-ttu-id="1dbd0-109">如果不 `AssemblyID` 指示未绑定的 .netmodule，则可以为 NULL。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-109">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `dwPEKind`  
 <span data-ttu-id="1dbd0-110">PE 的类型，如 [CorPEKind 枚举](../metadata/corpekind-enumeration.md)所示。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-110">The type of PE, as indicated by the [CorPEKind Enumeration](../metadata/corpekind-enumeration.md).</span></span>  
  
 `dwMachine`  
 <span data-ttu-id="1dbd0-111">目标计算机体系结构，如 NT 标头中所示。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-111">The target machine architecture, as indicated in the NT header.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1dbd0-112">返回值</span><span class="sxs-lookup"><span data-stu-id="1dbd0-112">Return Value</span></span>  

 <span data-ttu-id="1dbd0-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dbd0-114">要求</span><span class="sxs-lookup"><span data-stu-id="1dbd0-114">Requirements</span></span>  

 <span data-ttu-id="1dbd0-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="1dbd0-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dbd0-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="1dbd0-116">See also</span></span>

- [<span data-ttu-id="1dbd0-117">GetPEKind 方法</span><span class="sxs-lookup"><span data-stu-id="1dbd0-117">GetPEKind Method</span></span>](../metadata/imetadataimport2-getpekind-method.md)
- [<span data-ttu-id="1dbd0-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="1dbd0-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="1dbd0-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="1dbd0-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="1dbd0-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="1dbd0-120">ALink API</span></span>](index.md)
