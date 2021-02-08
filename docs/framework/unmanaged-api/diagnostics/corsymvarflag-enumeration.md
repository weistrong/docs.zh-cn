---
description: 了解详细信息： CorSymVarFlag 枚举
title: CorSymVarFlag 枚举
ms.date: 03/30/2017
api_name:
- CorSymVarFlag
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymVarFlag
helpviewer_keywords:
- CorSymVarFlag enumeration [.NET Framework debugging]
ms.assetid: c3f7d307-4047-4f9a-be8c-f152fca42fd0
topic_type:
- apiref
ms.openlocfilehash: 28f4b4775e20703e5dcaa7daf69affd3548aa3f2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800456"
---
# <a name="corsymvarflag-enumeration"></a><span data-ttu-id="07711-103">CorSymVarFlag 枚举</span><span class="sxs-lookup"><span data-stu-id="07711-103">CorSymVarFlag Enumeration</span></span>

<span data-ttu-id="07711-104">指示变量是否是编译器生成的。</span><span class="sxs-lookup"><span data-stu-id="07711-104">Indicates whether a variable is compiler-generated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07711-105">语法</span><span class="sxs-lookup"><span data-stu-id="07711-105">Syntax</span></span>  
  
```cpp  
typedef enum CorSymVarFlag
{  
    VAR_IS_COMP_GEN = 1  
} CorSymVarFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="07711-106">成员</span><span class="sxs-lookup"><span data-stu-id="07711-106">Members</span></span>  
  
|<span data-ttu-id="07711-107">成员</span><span class="sxs-lookup"><span data-stu-id="07711-107">Member</span></span>|<span data-ttu-id="07711-108">说明</span><span class="sxs-lookup"><span data-stu-id="07711-108">Description</span></span>|  
|------------|-----------------|  
|`VAR_IS_COMP_GEN`|<span data-ttu-id="07711-109">指示给定变量是编译器生成的。</span><span class="sxs-lookup"><span data-stu-id="07711-109">Indicates that the given variable is compiler-generated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="07711-110">要求</span><span class="sxs-lookup"><span data-stu-id="07711-110">Requirements</span></span>  

 <span data-ttu-id="07711-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="07711-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07711-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="07711-112">See also</span></span>

- [<span data-ttu-id="07711-113">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="07711-113">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)
