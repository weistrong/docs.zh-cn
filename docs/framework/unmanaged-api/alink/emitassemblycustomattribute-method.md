---
description: 了解详细信息： EmitAssemblyCustomAttribute 方法
title: EmitAssemblyCustomAttribute 方法
ms.date: 03/30/2017
api_name:
- IALink.EmitAssemblyCustomAttribute
- EmitAssemblyCustomAttribute
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssemblyCustomAttribute
helpviewer_keywords:
- EmitAssemblyCustomAttribute method
ms.assetid: b72f5409-79af-4fa7-90a7-7630eec170f1
topic_type:
- apiref
ms.openlocfilehash: c91eb563c14b442a22db8f328287c10e5cc9a63c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638322"
---
# <a name="emitassemblycustomattribute-method"></a><span data-ttu-id="ab599-103">EmitAssemblyCustomAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="ab599-103">EmitAssemblyCustomAttribute Method</span></span>

<span data-ttu-id="ab599-104">调用以设置程序集级别的自定义特性。</span><span class="sxs-lookup"><span data-stu-id="ab599-104">Call to set assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab599-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab599-105">Syntax</span></span>  
  
```cpp  
HRESULT EmitAssemblyCustomAttribute(  
    mdAssembly   AssemblyID,  
    mdToken      FileToken,  
    mdToken      tkType,  
    void const*  pCustomValue,  
    DWORD        cbCustomValue,  
    BOOL         bSecurity,  
    BOOL         bAllowMulti  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab599-106">参数</span><span class="sxs-lookup"><span data-stu-id="ab599-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="ab599-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="ab599-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="ab599-108">定义属性的文件。</span><span class="sxs-lookup"><span data-stu-id="ab599-108">File that defiles the attribute.</span></span> <span data-ttu-id="ab599-109">如果不 `AssemblyID` 指示未绑定的 .netmodule，则可以为 NULL。</span><span class="sxs-lookup"><span data-stu-id="ab599-109">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `tkType`  
 <span data-ttu-id="ab599-110">自定义属性的类型。</span><span class="sxs-lookup"><span data-stu-id="ab599-110">Type of the custom attribute.</span></span>  
  
 `pCustomValue`  
 <span data-ttu-id="ab599-111">自定义值数据。</span><span class="sxs-lookup"><span data-stu-id="ab599-111">Custom value data.</span></span>  
  
 `cbCustomValue`  
 <span data-ttu-id="ab599-112">自定义值数据的长度。</span><span class="sxs-lookup"><span data-stu-id="ab599-112">Length of custom value data.</span></span>  
  
 `bSecurity`  
 <span data-ttu-id="ab599-113">如果自定义属性与程序集签名相关，则为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="ab599-113">TRUE if the custom attribute is related to assembly signing.</span></span>  
  
 `bAllowMulti`  
 <span data-ttu-id="ab599-114">如果要发出多个属性，则为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="ab599-114">TRUE if multiple attributes are to be emitted.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab599-115">返回值</span><span class="sxs-lookup"><span data-stu-id="ab599-115">Return Value</span></span>  

 <span data-ttu-id="ab599-116">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="ab599-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab599-117">要求</span><span class="sxs-lookup"><span data-stu-id="ab599-117">Requirements</span></span>  

 <span data-ttu-id="ab599-118">需要 alink</span><span class="sxs-lookup"><span data-stu-id="ab599-118">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab599-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab599-119">See also</span></span>

- [<span data-ttu-id="ab599-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="ab599-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="ab599-121">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="ab599-121">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="ab599-122">ALink API</span><span class="sxs-lookup"><span data-stu-id="ab599-122">ALink API</span></span>](index.md)
