---
description: 了解详细信息： ISymUnmanagedBinder2 接口
title: ISymUnmanagedBinder2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder2 Interface
helpviewer_keywords:
- ISymUnmanagedBinder2 interface [.NET Framework debugging]
ms.assetid: 7a59f405-73e8-4434-8bcc-a9dc45ea08e6
topic_type:
- apiref
ms.openlocfilehash: 73847cdc9366ec18974fac261cbbad4d7dc6ccc6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689880"
---
# <a name="isymunmanagedbinder2-interface"></a><span data-ttu-id="44ffd-103">ISymUnmanagedBinder2 接口</span><span class="sxs-lookup"><span data-stu-id="44ffd-103">ISymUnmanagedBinder2 Interface</span></span>

<span data-ttu-id="44ffd-104">表示非托管代码的符号联编程序，并扩展 [ISymUnmanagedBinder](isymunmanagedbinder-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="44ffd-104">Represents a symbol binder for unmanaged code, and extends the [ISymUnmanagedBinder](isymunmanagedbinder-interface.md) interface.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="44ffd-105">从不受信任的源中打开程序数据库 (PDB) 文件会带来安全风险。</span><span class="sxs-lookup"><span data-stu-id="44ffd-105">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="44ffd-106">方法</span><span class="sxs-lookup"><span data-stu-id="44ffd-106">Methods</span></span>  
  
|<span data-ttu-id="44ffd-107">方法</span><span class="sxs-lookup"><span data-stu-id="44ffd-107">Method</span></span>|<span data-ttu-id="44ffd-108">说明</span><span class="sxs-lookup"><span data-stu-id="44ffd-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="44ffd-109">GetReaderForFile2 方法</span><span class="sxs-lookup"><span data-stu-id="44ffd-109">GetReaderForFile2 Method</span></span>](isymunmanagedbinder2-getreaderforfile2-method.md)|<span data-ttu-id="44ffd-110">给定元数据接口和文件名后，将返回正确的 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口，该接口将读取与模块关联的调试符号。</span><span class="sxs-lookup"><span data-stu-id="44ffd-110">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface that will read the debugging symbols associated with the module.</span></span> <span data-ttu-id="44ffd-111">与 [ISymUnmanagedBinder：： GetReaderForFile](isymunmanagedbinder-getreaderforfile-method.md) 方法相比，提供的搜索范围更广。</span><span class="sxs-lookup"><span data-stu-id="44ffd-111">Provides a more extensive search than the [ISymUnmanagedBinder::GetReaderForFile](isymunmanagedbinder-getreaderforfile-method.md) method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="44ffd-112">要求</span><span class="sxs-lookup"><span data-stu-id="44ffd-112">Requirements</span></span>  

 <span data-ttu-id="44ffd-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="44ffd-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44ffd-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="44ffd-114">See also</span></span>

- [<span data-ttu-id="44ffd-115">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="44ffd-115">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="44ffd-116">ISymUnmanagedBinder 接口</span><span class="sxs-lookup"><span data-stu-id="44ffd-116">ISymUnmanagedBinder Interface</span></span>](isymunmanagedbinder-interface.md)
- [<span data-ttu-id="44ffd-117">ISymUnmanagedBinder3 接口</span><span class="sxs-lookup"><span data-stu-id="44ffd-117">ISymUnmanagedBinder3 Interface</span></span>](isymunmanagedbinder3-interface.md)
