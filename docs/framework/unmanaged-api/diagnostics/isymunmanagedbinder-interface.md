---
description: 了解详细信息： ISymUnmanagedBinder 接口
title: ISymUnmanagedBinder 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder
helpviewer_keywords:
- ISymUnmanagedBinder interface [.NET Framework debugging]
ms.assetid: b22fbe19-b30f-4696-8175-e6b91da9edab
topic_type:
- apiref
ms.openlocfilehash: 14ebccb028ab3388a8058dd05504c56a6df74c95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689919"
---
# <a name="isymunmanagedbinder-interface"></a><span data-ttu-id="3a119-103">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="3a119-103">ISymUnmanagedBinder Interface</span></span>

<span data-ttu-id="3a119-104">表示非托管代码的符号绑定器。</span><span class="sxs-lookup"><span data-stu-id="3a119-104">Represents a symbol binder for unmanaged code.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="3a119-105">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="3a119-105">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3a119-106">方法</span><span class="sxs-lookup"><span data-stu-id="3a119-106">Methods</span></span>  
  
|<span data-ttu-id="3a119-107">方法</span><span class="sxs-lookup"><span data-stu-id="3a119-107">Method</span></span>|<span data-ttu-id="3a119-108">说明</span><span class="sxs-lookup"><span data-stu-id="3a119-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3a119-109">GetReaderForFile 方法</span><span class="sxs-lookup"><span data-stu-id="3a119-109">GetReaderForFile Method</span></span>](isymunmanagedbinder-getreaderforfile-method.md)|<span data-ttu-id="3a119-110">给定元数据接口和文件名后，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将读取与模块关联的调试符号。</span><span class="sxs-lookup"><span data-stu-id="3a119-110">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols associated with the module.</span></span>|  
|[<span data-ttu-id="3a119-111">GetReaderFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="3a119-111">GetReaderFromStream Method</span></span>](isymunmanagedbinder-getreaderfromstream-method.md)|<span data-ttu-id="3a119-112">给定元数据接口和包含符号存储区的流时，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 结构，该结构将从给定的符号存储区中读取调试符号。</span><span class="sxs-lookup"><span data-stu-id="3a119-112">Given a metadata interface and a stream that contains the symbol store, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols from the given symbol store.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3a119-113">要求</span><span class="sxs-lookup"><span data-stu-id="3a119-113">Requirements</span></span>  

 <span data-ttu-id="3a119-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3a119-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a119-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a119-115">See also</span></span>

- [<span data-ttu-id="3a119-116">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="3a119-116">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="3a119-117">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="3a119-117">ISymUnmanagedBinder2 Interface</span></span>](isymunmanagedbinder2-interface.md)
- [<span data-ttu-id="3a119-118">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="3a119-118">ISymUnmanagedBinder3 Interface</span></span>](isymunmanagedbinder3-interface.md)
