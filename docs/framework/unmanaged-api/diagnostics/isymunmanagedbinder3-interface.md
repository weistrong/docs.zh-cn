---
description: 了解详细信息： ISymUnmanagedBinder3 接口
title: ISymUnmanagedBinder3 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3 Interface
helpviewer_keywords:
- ISymUnmanagedBinder3 interface [.NET Framework debugging]
ms.assetid: 37527a84-4b03-4f08-8135-94d898599089
topic_type:
- apiref
ms.openlocfilehash: 6d2172fb119076cea6d0f912fb3f403d36856599
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689828"
---
# <a name="isymunmanagedbinder3-interface"></a><span data-ttu-id="64f2c-103">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="64f2c-103">ISymUnmanagedBinder3 Interface</span></span>

<span data-ttu-id="64f2c-104">扩展符号联编程序接口。</span><span class="sxs-lookup"><span data-stu-id="64f2c-104">Extends the symbol binder interface.</span></span> <span data-ttu-id="64f2c-105">通过对实现接口的对象调用来获取此接口 `QueryInterface` `ISymUnmanagedBinder` 。</span><span class="sxs-lookup"><span data-stu-id="64f2c-105">Obtain this interface by calling `QueryInterface` on an object that implements the `ISymUnmanagedBinder` interface.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="64f2c-106">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="64f2c-106">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="64f2c-107">方法</span><span class="sxs-lookup"><span data-stu-id="64f2c-107">Methods</span></span>  
  
|<span data-ttu-id="64f2c-108">方法</span><span class="sxs-lookup"><span data-stu-id="64f2c-108">Method</span></span>|<span data-ttu-id="64f2c-109">说明</span><span class="sxs-lookup"><span data-stu-id="64f2c-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="64f2c-110">GetReaderFromCallback 方法</span><span class="sxs-lookup"><span data-stu-id="64f2c-110">GetReaderFromCallback Method</span></span>](isymunmanagedbinder3-getreaderfromcallback-method.md)|<span data-ttu-id="64f2c-111">允许用户通过回调来实现或提供， `IID_IDiaReadExeAtRVACallback` `IID_IDiaReadExeAtOffsetCallback` 以从内存中获取调试目录信息</span><span class="sxs-lookup"><span data-stu-id="64f2c-111">Allows the user to implement or supply via callback either an `IID_IDiaReadExeAtRVACallback` or `IID_IDiaReadExeAtOffsetCallback` to obtain the Debug directory information from memory</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="64f2c-112">要求</span><span class="sxs-lookup"><span data-stu-id="64f2c-112">Requirements</span></span>  

 <span data-ttu-id="64f2c-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="64f2c-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64f2c-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="64f2c-114">See also</span></span>

- [<span data-ttu-id="64f2c-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="64f2c-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="64f2c-116">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="64f2c-116">ISymUnmanagedBinder Interface</span></span>](isymunmanagedbinder-interface.md)
- [<span data-ttu-id="64f2c-117">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="64f2c-117">ISymUnmanagedBinder2 Interface</span></span>](isymunmanagedbinder2-interface.md)
