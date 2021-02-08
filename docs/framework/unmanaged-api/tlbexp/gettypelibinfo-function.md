---
description: 了解详细信息： GetTypeLibInfo 函数
title: GetTypeLibInfo 函数
ms.date: 03/30/2017
api_name:
- GetTypeLibInfo
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- GetTypeLibInfo
helpviewer_keywords:
- GetTypeLibInfo function [.NET Framework]
ms.assetid: a1c4d165-9bdc-4ca8-940e-292d4ffcc338
topic_type:
- apiref
ms.openlocfilehash: 61a830f3ce81345634da377f6fc815a307700e9e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794463"
---
# <a name="gettypelibinfo-function"></a><span data-ttu-id="eebc6-103">GetTypeLibInfo 函数</span><span class="sxs-lookup"><span data-stu-id="eebc6-103">GetTypeLibInfo Function</span></span>

<span data-ttu-id="eebc6-104">通过检查指定类型库的 [TLIBATTR](/windows/win32/api/oaidl/ns-oaidl-tlibattr) 结构来返回相关信息。</span><span class="sxs-lookup"><span data-stu-id="eebc6-104">Returns information about the specified type library by examining its [TLIBATTR](/windows/win32/api/oaidl/ns-oaidl-tlibattr) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eebc6-105">语法</span><span class="sxs-lookup"><span data-stu-id="eebc6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTypeLibInfo(  
    [in]   LPWSTR     szFile,  
    [out]  GUID      *pTypeLibID,  
    [out]  LCID      *pTypeLibLCID,  
    [out]  SYSKIND   *pTypeLibPlatform,  
    [out]  USHORT    *pTypeLibMajorVer,  
    [out]  USHORT    *pTypeLibMinorVer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eebc6-106">参数</span><span class="sxs-lookup"><span data-stu-id="eebc6-106">Parameters</span></span>  

 `szFile`  
 <span data-ttu-id="eebc6-107">中类型库的文件名。</span><span class="sxs-lookup"><span data-stu-id="eebc6-107">[in] The file name of the type library.</span></span>  
  
 `pTypeLibID`  
 <span data-ttu-id="eebc6-108">弄类型库的 GUID。</span><span class="sxs-lookup"><span data-stu-id="eebc6-108">[out] The GUID of the type library.</span></span>  
  
 `pTypeLibLCID`  
 <span data-ttu-id="eebc6-109">弄类型库的本地化 ID。</span><span class="sxs-lookup"><span data-stu-id="eebc6-109">[out] The localization ID of the type library.</span></span>  
  
 `pTypeLibPlatform`  
 <span data-ttu-id="eebc6-110">弄标识库的目标操作系统的 [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) 标志。</span><span class="sxs-lookup"><span data-stu-id="eebc6-110">[out] A [SYSKIND](/windows/win32/api/oaidl/ne-oaidl-syskind) flag that identifies the target operating system for the type library.</span></span> <span data-ttu-id="eebc6-111">常用值为 SYS_WIN32 和 SYS_WIN64。</span><span class="sxs-lookup"><span data-stu-id="eebc6-111">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pTypeLibMajorVer`  
 <span data-ttu-id="eebc6-112">弄类型库的主版本号。</span><span class="sxs-lookup"><span data-stu-id="eebc6-112">[out] The major version number of the type library.</span></span> <span data-ttu-id="eebc6-113">例如，对于版本 *x. y*，主版本号是 *x*。</span><span class="sxs-lookup"><span data-stu-id="eebc6-113">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `pTypeLibMinorVer`  
 <span data-ttu-id="eebc6-114">弄类型库的次版本号。</span><span class="sxs-lookup"><span data-stu-id="eebc6-114">[out] The minor version number of the type library.</span></span> <span data-ttu-id="eebc6-115">例如，对于版本 *x. y*，次版本号为 *y*。</span><span class="sxs-lookup"><span data-stu-id="eebc6-115">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eebc6-116">备注</span><span class="sxs-lookup"><span data-stu-id="eebc6-116">Remarks</span></span>  

 <span data-ttu-id="eebc6-117">`GetTypeLibInfo`函数由[Tlbexp.exe (类型库导出程序) ](../../tools/tlbexp-exe-type-library-exporter.md)调用。</span><span class="sxs-lookup"><span data-stu-id="eebc6-117">The `GetTypeLibInfo` function is called by the [Tlbexp.exe (Type Library Exporter)](../../tools/tlbexp-exe-type-library-exporter.md).</span></span> <span data-ttu-id="eebc6-118">此工具将生成一个类型库，该类型库描述公共语言运行时中的类型 (CLR) 程序集。</span><span class="sxs-lookup"><span data-stu-id="eebc6-118">This tool generates a type library that describes the types in a common language runtime (CLR) assembly.</span></span>  
  
 <span data-ttu-id="eebc6-119">如果任何参数为 null，则函数返回 `HRESULT` 的 `E_POINTER` 。</span><span class="sxs-lookup"><span data-stu-id="eebc6-119">If any parameter is null, the function returns an `HRESULT` of `E_POINTER`.</span></span> <span data-ttu-id="eebc6-120">否则，它将返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="eebc6-120">Otherwise, it returns `S_OK`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eebc6-121">要求</span><span class="sxs-lookup"><span data-stu-id="eebc6-121">Requirements</span></span>  

 <span data-ttu-id="eebc6-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="eebc6-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eebc6-123">**标头：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="eebc6-123">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="eebc6-124">**库：** TlbRef</span><span class="sxs-lookup"><span data-stu-id="eebc6-124">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="eebc6-125">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eebc6-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eebc6-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="eebc6-126">See also</span></span>

- [<span data-ttu-id="eebc6-127">Tlbexp Helper 函数</span><span class="sxs-lookup"><span data-stu-id="eebc6-127">Tlbexp Helper Functions</span></span>](index.md)
- [<span data-ttu-id="eebc6-128">LoadTypeLibEx 函数</span><span class="sxs-lookup"><span data-stu-id="eebc6-128">LoadTypeLibEx Function</span></span>](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
