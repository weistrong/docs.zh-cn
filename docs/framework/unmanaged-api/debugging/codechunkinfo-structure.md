---
description: 了解详细信息： CodeChunkInfo 结构
title: CodeChunkInfo 结构
ms.date: 03/30/2017
api_name:
- CodeChunkInfo
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CodeChunkInfo
helpviewer_keywords:
- CodeChunkInfo structure [.NET Framework debugging]
ms.assetid: 0f482454-8517-48de-ba7a-d7aedab13bb5
topic_type:
- apiref
ms.openlocfilehash: 017a9ee8c608d4efae98eb0a342a3371ef8ec310
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712345"
---
# <a name="codechunkinfo-structure"></a><span data-ttu-id="c6440-103">CodeChunkInfo 结构</span><span class="sxs-lookup"><span data-stu-id="c6440-103">CodeChunkInfo Structure</span></span>

<span data-ttu-id="c6440-104">表示内存中的单一代码块。</span><span class="sxs-lookup"><span data-stu-id="c6440-104">Represents a single chunk of code in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6440-105">语法</span><span class="sxs-lookup"><span data-stu-id="c6440-105">Syntax</span></span>  
  
```cpp  
typedef struct _CodeChunkInfo {  
    CORDB_ADDRESS startAddr;  
    ULONG32       length;  
} CodeChunkInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="c6440-106">成员</span><span class="sxs-lookup"><span data-stu-id="c6440-106">Members</span></span>  
  
|<span data-ttu-id="c6440-107">成员</span><span class="sxs-lookup"><span data-stu-id="c6440-107">Member</span></span>|<span data-ttu-id="c6440-108">说明</span><span class="sxs-lookup"><span data-stu-id="c6440-108">Description</span></span>|  
|------------|-----------------|  
|`startAddr`|<span data-ttu-id="c6440-109">一个 `CORDB_ADDRESS` 值，该值指定块区的起始地址。</span><span class="sxs-lookup"><span data-stu-id="c6440-109">A `CORDB_ADDRESS` value that specifies the starting address of the chunk.</span></span>|  
|`length`|<span data-ttu-id="c6440-110">块区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c6440-110">The size, in bytes, of the chunk.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c6440-111">备注</span><span class="sxs-lookup"><span data-stu-id="c6440-111">Remarks</span></span>  

 <span data-ttu-id="c6440-112">单个代码块是本机代码区域，它是代码对象（例如函数）的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6440-112">The single chunk of code is a region of native code that is part of a code object such as a function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6440-113">要求</span><span class="sxs-lookup"><span data-stu-id="c6440-113">Requirements</span></span>  

 <span data-ttu-id="c6440-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c6440-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6440-115">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="c6440-115">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="c6440-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c6440-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c6440-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6440-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6440-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6440-118">See also</span></span>

- [<span data-ttu-id="c6440-119">GetCodeChunks 方法</span><span class="sxs-lookup"><span data-stu-id="c6440-119">GetCodeChunks Method</span></span>](icordebugcode2-getcodechunks-method.md)
- [<span data-ttu-id="c6440-120">调试结构</span><span class="sxs-lookup"><span data-stu-id="c6440-120">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="c6440-121">调试</span><span class="sxs-lookup"><span data-stu-id="c6440-121">Debugging</span></span>](index.md)
