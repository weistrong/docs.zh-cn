---
description: 了解详细信息： ISymUnmanagedReader2 接口
title: ISymUnmanagedReader2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2
helpviewer_keywords:
- ISymUnmanagedReader2 interface [.NET Framework debugging]
ms.assetid: a01a881b-82a3-4b3e-a3a9-9dc305c2e5f7
topic_type:
- apiref
ms.openlocfilehash: 2e6d994a3252b7fb09b2915266e3142255878a88
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763613"
---
# <a name="isymunmanagedreader2-interface"></a><span data-ttu-id="74efd-103">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="74efd-103">ISymUnmanagedReader2 Interface</span></span>

<span data-ttu-id="74efd-104">表示一个符号读取器，该读取器提供对符号存储区中文档、方法和变量的访问。</span><span class="sxs-lookup"><span data-stu-id="74efd-104">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span> <span data-ttu-id="74efd-105">此接口扩展 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="74efd-105">This interface extends the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="74efd-106">方法</span><span class="sxs-lookup"><span data-stu-id="74efd-106">Methods</span></span>  
  
|<span data-ttu-id="74efd-107">方法</span><span class="sxs-lookup"><span data-stu-id="74efd-107">Method</span></span>|<span data-ttu-id="74efd-108">说明</span><span class="sxs-lookup"><span data-stu-id="74efd-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="74efd-109">GetMethodByVersionPreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="74efd-109">GetMethodByVersionPreRemap Method</span></span>](isymunmanagedreader2-getmethodbyversionpreremap-method.md)|<span data-ttu-id="74efd-110">在给定方法标记和编辑并继续版本号的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="74efd-110">Get a symbol reader method, given a method token and an edit-and-continue version number.</span></span>|  
|[<span data-ttu-id="74efd-111">GetMethodsInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="74efd-111">GetMethodsInDocument Method</span></span>](isymunmanagedreader2-getmethodsindocument-method.md)|<span data-ttu-id="74efd-112">获取所提供文档中包含行信息的每个方法。</span><span class="sxs-lookup"><span data-stu-id="74efd-112">Gets every method that has line information in the provided document.</span></span>|  
|[<span data-ttu-id="74efd-113">GetSymAttributePreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="74efd-113">GetSymAttributePreRemap Method</span></span>](isymunmanagedreader2-getsymattributepreremap-method.md)|<span data-ttu-id="74efd-114">根据名称获取自定义属性。</span><span class="sxs-lookup"><span data-stu-id="74efd-114">Gets a custom attribute based upon its name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="74efd-115">要求</span><span class="sxs-lookup"><span data-stu-id="74efd-115">Requirements</span></span>  

 <span data-ttu-id="74efd-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="74efd-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74efd-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="74efd-117">See also</span></span>

- [<span data-ttu-id="74efd-118">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="74efd-118">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="74efd-119">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="74efd-119">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
