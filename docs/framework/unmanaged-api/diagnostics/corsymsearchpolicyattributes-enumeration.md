---
description: 了解详细信息： CorSymSearchPolicyAttributes 枚举
title: CorSymSearchPolicyAttributes 枚举
ms.date: 03/30/2017
api_name:
- CorSymSearchPolicyAttributes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymSearchPolicyAttributes
helpviewer_keywords:
- CorSymSearchPolicyAttributes enumeration [.NET Framework debugging]
ms.assetid: 03abde84-930a-49d3-bac3-23abb34a0184
topic_type:
- apiref
ms.openlocfilehash: a9af0e96809ec8eba5c03c2e372e818c74914baf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800469"
---
# <a name="corsymsearchpolicyattributes-enumeration"></a><span data-ttu-id="c95c0-103">CorSymSearchPolicyAttributes 枚举</span><span class="sxs-lookup"><span data-stu-id="c95c0-103">CorSymSearchPolicyAttributes Enumeration</span></span>

<span data-ttu-id="c95c0-104">指定在搜索符号读取器时要使用的策略。</span><span class="sxs-lookup"><span data-stu-id="c95c0-104">Specifies the policy to be used when doing a search for a symbol reader.</span></span> <span data-ttu-id="c95c0-105">[ISymUnmanagedBinder2：： GetReaderForFile2](isymunmanagedbinder2-getreaderforfile2-method.md)和[ISymUnmanagedBinder3：： GetReaderFromCallback](isymunmanagedbinder3-getreaderfromcallback-method.md)方法使用这些常量。</span><span class="sxs-lookup"><span data-stu-id="c95c0-105">These constants are used by the [ISymUnmanagedBinder2::GetReaderForFile2](isymunmanagedbinder2-getreaderforfile2-method.md) and [ISymUnmanagedBinder3::GetReaderFromCallback](isymunmanagedbinder3-getreaderfromcallback-method.md) methods.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="c95c0-106">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="c95c0-106">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c95c0-107">语法</span><span class="sxs-lookup"><span data-stu-id="c95c0-107">Syntax</span></span>  
  
```cpp  
typedef enum CorSymSearchPolicyAttributes  
{  
    AllowRegistryAccess      = 0x1,
    AllowSymbolServerAccess  = 0x2,  
    AllowOriginalPathAccess  = 0x4,     //
    AllowReferencePathAccess = 0x8  
} CorSymSearchPolicyAttributes;  
```  
  
## <a name="members"></a><span data-ttu-id="c95c0-108">成员</span><span class="sxs-lookup"><span data-stu-id="c95c0-108">Members</span></span>  
  
|<span data-ttu-id="c95c0-109">成员</span><span class="sxs-lookup"><span data-stu-id="c95c0-109">Member</span></span>|<span data-ttu-id="c95c0-110">说明</span><span class="sxs-lookup"><span data-stu-id="c95c0-110">Description</span></span>|  
|------------|-----------------|  
|`AllowRegistryAccess`|<span data-ttu-id="c95c0-111">在注册表中查询符号搜索路径。</span><span class="sxs-lookup"><span data-stu-id="c95c0-111">Queries the registry for symbol search paths.</span></span>|  
|`AllowSymbolServerAccess`|<span data-ttu-id="c95c0-112">访问符号服务器。</span><span class="sxs-lookup"><span data-stu-id="c95c0-112">Accesses a symbol server.</span></span>|  
|`AllowOriginalPathAccess`|<span data-ttu-id="c95c0-113">搜索在调试目录中指定的路径。</span><span class="sxs-lookup"><span data-stu-id="c95c0-113">Searches the path specified in the Debug directory.</span></span>|  
|`AllowReferencePathAccess`|<span data-ttu-id="c95c0-114">搜索 .exe 文件所在位置的 PDB。</span><span class="sxs-lookup"><span data-stu-id="c95c0-114">Searches for the PDB in the place where the .exe file is.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c95c0-115">要求</span><span class="sxs-lookup"><span data-stu-id="c95c0-115">Requirements</span></span>  

 <span data-ttu-id="c95c0-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c95c0-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c95c0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="c95c0-117">See also</span></span>

- [<span data-ttu-id="c95c0-118">诊断符号存储区枚举</span><span class="sxs-lookup"><span data-stu-id="c95c0-118">Diagnostics Symbol Store Enumerations</span></span>](diagnostics-symbol-store-enumerations.md)
