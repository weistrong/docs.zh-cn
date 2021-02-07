---
description: 了解详细信息： SYMLINEDELTA 结构
title: SYMLINEDELTA 结构
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
ms.openlocfilehash: ae00d2be9809b48180d2cd99d05e410624033419
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761442"
---
# <a name="symlinedelta-structure"></a><span data-ttu-id="6ed5b-103">SYMLINEDELTA 结构</span><span class="sxs-lookup"><span data-stu-id="6ed5b-103">SYMLINEDELTA Structure</span></span>

<span data-ttu-id="6ed5b-104">向符号处理程序提供有关因编辑而移动的方法的信息。</span><span class="sxs-lookup"><span data-stu-id="6ed5b-104">Provides information to the symbol handler about methods that were moved as a result of edits.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ed5b-105">语法</span><span class="sxs-lookup"><span data-stu-id="6ed5b-105">Syntax</span></span>  
  
```cpp  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a><span data-ttu-id="6ed5b-106">成员</span><span class="sxs-lookup"><span data-stu-id="6ed5b-106">Members</span></span>  
  
|<span data-ttu-id="6ed5b-107">成员</span><span class="sxs-lookup"><span data-stu-id="6ed5b-107">Member</span></span>|<span data-ttu-id="6ed5b-108">说明</span><span class="sxs-lookup"><span data-stu-id="6ed5b-108">Description</span></span>|  
|------------|-----------------|  
|`mdMethod`|<span data-ttu-id="6ed5b-109">方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="6ed5b-109">The method's metadata token.</span></span>|  
|`delta`|<span data-ttu-id="6ed5b-110">此方法已移动的行数。</span><span class="sxs-lookup"><span data-stu-id="6ed5b-110">The number of lines the method was moved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6ed5b-111">要求</span><span class="sxs-lookup"><span data-stu-id="6ed5b-111">Requirements</span></span>  

 <span data-ttu-id="6ed5b-112">**标头：** CorSym .idl</span><span class="sxs-lookup"><span data-stu-id="6ed5b-112">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ed5b-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="6ed5b-113">See also</span></span>

- [<span data-ttu-id="6ed5b-114">诊断符号存储区结构</span><span class="sxs-lookup"><span data-stu-id="6ed5b-114">Diagnostics Symbol Store Structures</span></span>](diagnostics-symbol-store-structures.md)
