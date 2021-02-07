---
description: 了解详细信息： ISymUnmanagedVariable 接口
title: ISymUnmanagedVariable 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable
helpviewer_keywords:
- ISymUnmanagedVariable interface [.NET Framework debugging]
ms.assetid: 704c69ba-77bc-40d7-8c0c-400061686321
topic_type:
- apiref
ms.openlocfilehash: 15b6c7018f92ad4c82abb9e5b4e52bf428b3f54b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762690"
---
# <a name="isymunmanagedvariable-interface"></a><span data-ttu-id="8644d-103">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="8644d-103">ISymUnmanagedVariable Interface</span></span>

<span data-ttu-id="8644d-104">表示变量，如参数、局部变量或字段。</span><span class="sxs-lookup"><span data-stu-id="8644d-104">Represents a variable, such as a parameter, a local variable, or a field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8644d-105">方法</span><span class="sxs-lookup"><span data-stu-id="8644d-105">Methods</span></span>  
  
|<span data-ttu-id="8644d-106">方法</span><span class="sxs-lookup"><span data-stu-id="8644d-106">Method</span></span>|<span data-ttu-id="8644d-107">说明</span><span class="sxs-lookup"><span data-stu-id="8644d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8644d-108">GetAddressField1 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-108">GetAddressField1 Method</span></span>](isymunmanagedvariable-getaddressfield1-method.md)|<span data-ttu-id="8644d-109">获取此变量的第一个地址字段。</span><span class="sxs-lookup"><span data-stu-id="8644d-109">Gets the first address field for this variable.</span></span> <span data-ttu-id="8644d-110">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="8644d-110">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="8644d-111">GetAddressField2 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-111">GetAddressField2 Method</span></span>](isymunmanagedvariable-getaddressfield2-method.md)|<span data-ttu-id="8644d-112">获取此变量的第二个地址字段。</span><span class="sxs-lookup"><span data-stu-id="8644d-112">Gets the second address field for this variable.</span></span> <span data-ttu-id="8644d-113">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="8644d-113">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="8644d-114">GetAddressField3 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-114">GetAddressField3 Method</span></span>](isymunmanagedvariable-getaddressfield3-method.md)|<span data-ttu-id="8644d-115">获取此变量的第三个地址字段。</span><span class="sxs-lookup"><span data-stu-id="8644d-115">Gets the third address field for this variable.</span></span> <span data-ttu-id="8644d-116">其含义取决于地址的类型。</span><span class="sxs-lookup"><span data-stu-id="8644d-116">Its meaning depends on the kind of address.</span></span>|  
|[<span data-ttu-id="8644d-117">GetAddressKind 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-117">GetAddressKind Method</span></span>](isymunmanagedvariable-getaddresskind-method.md)|<span data-ttu-id="8644d-118">获取此变量的地址类型。</span><span class="sxs-lookup"><span data-stu-id="8644d-118">Gets the kind of address of this variable.</span></span>|  
|[<span data-ttu-id="8644d-119">GetAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-119">GetAttributes Method</span></span>](isymunmanagedvariable-getattributes-method.md)|<span data-ttu-id="8644d-120">获取此变量的特性标志。</span><span class="sxs-lookup"><span data-stu-id="8644d-120">Gets the attribute flags for this variable.</span></span>|  
|[<span data-ttu-id="8644d-121">GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-121">GetEndOffset Method</span></span>](isymunmanagedvariable-getendoffset-method.md)|<span data-ttu-id="8644d-122">获取此变量在其父级内的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="8644d-122">Gets the end offset of this variable within its parent.</span></span>|  
|[<span data-ttu-id="8644d-123">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-123">GetName Method</span></span>](isymunmanagedvariable-getname-method.md)|<span data-ttu-id="8644d-124">获取此变量的名称。</span><span class="sxs-lookup"><span data-stu-id="8644d-124">Gets the name of this variable.</span></span>|  
|[<span data-ttu-id="8644d-125">GetSignature 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-125">GetSignature Method</span></span>](isymunmanagedvariable-getsignature-method.md)|<span data-ttu-id="8644d-126">获取此变量的签名。</span><span class="sxs-lookup"><span data-stu-id="8644d-126">Gets the signature of this variable.</span></span>|  
|[<span data-ttu-id="8644d-127">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="8644d-127">GetStartOffset Method</span></span>](isymunmanagedvariable-getstartoffset-method.md)|<span data-ttu-id="8644d-128">获取此变量在其父级内的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="8644d-128">Gets the start offset of this variable within its parent.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8644d-129">要求</span><span class="sxs-lookup"><span data-stu-id="8644d-129">Requirements</span></span>  

 <span data-ttu-id="8644d-130">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="8644d-130">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8644d-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="8644d-131">See also</span></span>

- [<span data-ttu-id="8644d-132">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="8644d-132">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
