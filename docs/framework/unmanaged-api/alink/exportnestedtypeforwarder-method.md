---
description: 了解详细信息： ExportNestedTypeForwarder 方法
title: ExportNestedTypeForwarder 方法
ms.date: 03/30/2017
api_name:
- IALink.ExportNestedTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportNestedTypeForwarder
helpviewer_keywords:
- ExportNestedTypeForwarder method
ms.assetid: 886ea6c5-6b26-4b88-8bf6-448d6d191950
topic_type:
- apiref
ms.openlocfilehash: fd791e3fea76338f191fcf924d56720d257d2e8b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638101"
---
# <a name="exportnestedtypeforwarder-method"></a><span data-ttu-id="cf56e-103">ExportNestedTypeForwarder 方法</span><span class="sxs-lookup"><span data-stu-id="cf56e-103">ExportNestedTypeForwarder Method</span></span>

<span data-ttu-id="cf56e-104">将嵌套类型的类型转发器添加到给定程序集的类型表。</span><span class="sxs-lookup"><span data-stu-id="cf56e-104">Adds a type forwarder for a nested type to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf56e-105">语法</span><span class="sxs-lookup"><span data-stu-id="cf56e-105">Syntax</span></span>  
  
```cpp  
HRESULT ExportNestedTypeForwarder(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    mdExportedType  ParentType,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="cf56e-106">参数</span><span class="sxs-lookup"><span data-stu-id="cf56e-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="cf56e-107">要从中导出的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="cf56e-107">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="cf56e-108">定义类型的文件的文件标记或程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="cf56e-108">File token or assembly ID of file that defines the type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="cf56e-109">类型的标记。</span><span class="sxs-lookup"><span data-stu-id="cf56e-109">Token for the type.</span></span>  
  
 `ParentType`  
 <span data-ttu-id="cf56e-110">父类型的标记。</span><span class="sxs-lookup"><span data-stu-id="cf56e-110">Token of parent type.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="cf56e-111">要导出的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="cf56e-111">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="cf56e-112">`ComType` 标志，如 `tdPublic` 或 `tdNested` 。</span><span class="sxs-lookup"><span data-stu-id="cf56e-112">`ComType` flags such as `tdPublic` or `tdNested`.</span></span>  
  
 `pType`  
 <span data-ttu-id="cf56e-113">接收导出类型的令牌。</span><span class="sxs-lookup"><span data-stu-id="cf56e-113">Receives token of export type.</span></span> <span data-ttu-id="cf56e-114">这仅适用于发出嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="cf56e-114">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cf56e-115">返回值</span><span class="sxs-lookup"><span data-stu-id="cf56e-115">Return Value</span></span>  

 <span data-ttu-id="cf56e-116">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="cf56e-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf56e-117">要求</span><span class="sxs-lookup"><span data-stu-id="cf56e-117">Requirements</span></span>  

 <span data-ttu-id="cf56e-118">需要 alink</span><span class="sxs-lookup"><span data-stu-id="cf56e-118">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf56e-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="cf56e-119">See also</span></span>

- [<span data-ttu-id="cf56e-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="cf56e-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="cf56e-121">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="cf56e-121">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="cf56e-122">ALink API</span><span class="sxs-lookup"><span data-stu-id="cf56e-122">ALink API</span></span>](index.md)
