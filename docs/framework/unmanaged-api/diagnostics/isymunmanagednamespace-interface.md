---
description: 了解详细信息： ISymUnmanagedNamespace 接口
title: ISymUnmanagedNamespace 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace
helpviewer_keywords:
- ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: d42bea4e-5848-4e43-a883-69af7a313ce9
topic_type:
- apiref
ms.openlocfilehash: ff2cd2286ab006411a70ff9aa32c4f0265a73995
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709836"
---
# <a name="isymunmanagednamespace-interface"></a><span data-ttu-id="cd26e-103">ISymUnmanagedNamespace 接口</span><span class="sxs-lookup"><span data-stu-id="cd26e-103">ISymUnmanagedNamespace Interface</span></span>

<span data-ttu-id="cd26e-104">表示命名空间。</span><span class="sxs-lookup"><span data-stu-id="cd26e-104">Represents a namespace.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cd26e-105">方法</span><span class="sxs-lookup"><span data-stu-id="cd26e-105">Methods</span></span>  
  
|<span data-ttu-id="cd26e-106">方法</span><span class="sxs-lookup"><span data-stu-id="cd26e-106">Method</span></span>|<span data-ttu-id="cd26e-107">说明</span><span class="sxs-lookup"><span data-stu-id="cd26e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cd26e-108">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="cd26e-108">GetName Method</span></span>](isymunmanagednamespace-getname-method.md)|<span data-ttu-id="cd26e-109">获取此命名空间的名称。</span><span class="sxs-lookup"><span data-stu-id="cd26e-109">Gets the name of this namespace.</span></span>|  
|[<span data-ttu-id="cd26e-110">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="cd26e-110">GetNamespaces Method</span></span>](isymunmanagednamespace-getnamespaces-method.md)|<span data-ttu-id="cd26e-111">获取此命名空间的子级。</span><span class="sxs-lookup"><span data-stu-id="cd26e-111">Gets the children of this namespace.</span></span>|  
|[<span data-ttu-id="cd26e-112">GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="cd26e-112">GetVariables Method</span></span>](isymunmanagednamespace-getvariables-method.md)|<span data-ttu-id="cd26e-113">返回在此命名空间中的全局范围内定义的所有变量。</span><span class="sxs-lookup"><span data-stu-id="cd26e-113">Returns all variables defined at global scope within this namespace.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cd26e-114">要求</span><span class="sxs-lookup"><span data-stu-id="cd26e-114">Requirements</span></span>  

 <span data-ttu-id="cd26e-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="cd26e-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd26e-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd26e-116">See also</span></span>

- [<span data-ttu-id="cd26e-117">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="cd26e-117">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
