---
description: '了解详细信息：常量 (非托管 API 参考) '
title: 常量（非托管 API 参考）
ms.date: 03/30/2017
helpviewer_keywords:
- constants for unmanaged API [.NET Framework]
- native API reference [.NET Framework], constants
- unmanaged API reference [.NET Framework], constants
ms.assetid: 77526f65-b71c-4483-9d19-3a3751fd8a45
ms.openlocfilehash: 39641b4a98f921a3e8a004f536e0683cb81ab74e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772791"
---
# <a name="constants-unmanaged-api-reference"></a><span data-ttu-id="cfae4-103">常量（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="cfae4-103">Constants (Unmanaged API Reference)</span></span>

<span data-ttu-id="cfae4-104">本主题介绍 CorSym 中定义的语言类型、语言供应商和文档类型常量。</span><span class="sxs-lookup"><span data-stu-id="cfae4-104">This topic describes the language type, language vendor, and document type constants that are defined in CorSym.idl.</span></span>  
  
## <a name="language-type-constants"></a><span data-ttu-id="cfae4-105">语言类型常量</span><span class="sxs-lookup"><span data-stu-id="cfae4-105">Language Type Constants</span></span>  

 <span data-ttu-id="cfae4-106">下表显示了语言类型常量，它们表示标识编程语言的 Guid。</span><span class="sxs-lookup"><span data-stu-id="cfae4-106">The following table shows language type constants, which represent GUIDs that identify programming languages.</span></span>  
  
|<span data-ttu-id="cfae4-107">符号</span><span class="sxs-lookup"><span data-stu-id="cfae4-107">Symbol</span></span>|<span data-ttu-id="cfae4-108">说明</span><span class="sxs-lookup"><span data-stu-id="cfae4-108">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="cfae4-109">CorSym_LanguageType_C</span><span class="sxs-lookup"><span data-stu-id="cfae4-109">CorSym_LanguageType_C</span></span>|<span data-ttu-id="cfae4-110">指示 C 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-110">Indicates the C language.</span></span>|  
|<span data-ttu-id="cfae4-111">CorSym_LanguageType_CPlusPlus</span><span class="sxs-lookup"><span data-stu-id="cfae4-111">CorSym_LanguageType_CPlusPlus</span></span>|<span data-ttu-id="cfae4-112">指示 c + + 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-112">Indicates the C++ language.</span></span>|  
|<span data-ttu-id="cfae4-113">CorSym_LanguageType_CSharp</span><span class="sxs-lookup"><span data-stu-id="cfae4-113">CorSym_LanguageType_CSharp</span></span>|<span data-ttu-id="cfae4-114">指示 c # 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-114">Indicates the C# language.</span></span>|  
|<span data-ttu-id="cfae4-115">CorSym_LanguageType_Basic</span><span class="sxs-lookup"><span data-stu-id="cfae4-115">CorSym_LanguageType_Basic</span></span>|<span data-ttu-id="cfae4-116">指示基本语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-116">Indicates the Basic language.</span></span>|  
|<span data-ttu-id="cfae4-117">CorSym_LanguageType_Java</span><span class="sxs-lookup"><span data-stu-id="cfae4-117">CorSym_LanguageType_Java</span></span>|<span data-ttu-id="cfae4-118">指示 Java 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-118">Indicates the Java language.</span></span>|  
|<span data-ttu-id="cfae4-119">CorSym_LanguageType_Cobol</span><span class="sxs-lookup"><span data-stu-id="cfae4-119">CorSym_LanguageType_Cobol</span></span>|<span data-ttu-id="cfae4-120">指示 COBOL 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-120">Indicates the COBOL language.</span></span>|  
|<span data-ttu-id="cfae4-121">CorSym_LanguageType_Pascal</span><span class="sxs-lookup"><span data-stu-id="cfae4-121">CorSym_LanguageType_Pascal</span></span>|<span data-ttu-id="cfae4-122">指示 Pascal 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-122">Indicates the Pascal language.</span></span>|  
|<span data-ttu-id="cfae4-123">CorSym_LanguageType_ILAssembly</span><span class="sxs-lookup"><span data-stu-id="cfae4-123">CorSym_LanguageType_ILAssembly</span></span>|<span data-ttu-id="cfae4-124">指示 Microsoft 中间语言 (MSIL) 程序集代码。</span><span class="sxs-lookup"><span data-stu-id="cfae4-124">Indicates the Microsoft intermediate language (MSIL) assembly code.</span></span>|  
|<span data-ttu-id="cfae4-125">CorSym_LanguageType_JScript</span><span class="sxs-lookup"><span data-stu-id="cfae4-125">CorSym_LanguageType_JScript</span></span>|<span data-ttu-id="cfae4-126">指示 JScript 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-126">Indicates the JScript language.</span></span>|  
|<span data-ttu-id="cfae4-127">CorSym_LanguageType_SMC</span><span class="sxs-lookup"><span data-stu-id="cfae4-127">CorSym_LanguageType_SMC</span></span>|<span data-ttu-id="cfae4-128">指示 SMC 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-128">Indicates the SMC language.</span></span>|  
|<span data-ttu-id="cfae4-129">CorSym_LanguageType_MCPlusPlus</span><span class="sxs-lookup"><span data-stu-id="cfae4-129">CorSym_LanguageType_MCPlusPlus</span></span>|<span data-ttu-id="cfae4-130">指示为 .NET Framework 启用的 c + + 语言。</span><span class="sxs-lookup"><span data-stu-id="cfae4-130">Indicates the C++ language enabled for the .NET Framework.</span></span>|  
  
## <a name="language-vendor-constants"></a><span data-ttu-id="cfae4-131">语言供应商常量</span><span class="sxs-lookup"><span data-stu-id="cfae4-131">Language Vendor Constants</span></span>  

 <span data-ttu-id="cfae4-132">下表显示了语言供应商常量，它们表示标识编程语言供应商的 Guid。</span><span class="sxs-lookup"><span data-stu-id="cfae4-132">The following table shows language vendor constants, which represent GUIDs that identify programming language vendors.</span></span>  
  
|<span data-ttu-id="cfae4-133">符号</span><span class="sxs-lookup"><span data-stu-id="cfae4-133">Symbol</span></span>|<span data-ttu-id="cfae4-134">说明</span><span class="sxs-lookup"><span data-stu-id="cfae4-134">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="cfae4-135">CorSym_LanguageVendor_Microsoft</span><span class="sxs-lookup"><span data-stu-id="cfae4-135">CorSym_LanguageVendor_Microsoft</span></span>|<span data-ttu-id="cfae4-136">指示 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cfae4-136">Indicates Microsoft.</span></span>|  
  
## <a name="document-type-constants"></a><span data-ttu-id="cfae4-137">文档类型常量</span><span class="sxs-lookup"><span data-stu-id="cfae4-137">Document Type Constants</span></span>  

 <span data-ttu-id="cfae4-138">下表显示了文档类型常量，它们表示标识文档类型的 Guid。</span><span class="sxs-lookup"><span data-stu-id="cfae4-138">The following table shows document type constants, which represent GUIDs that identify document types.</span></span>  
  
|<span data-ttu-id="cfae4-139">符号</span><span class="sxs-lookup"><span data-stu-id="cfae4-139">Symbol</span></span>|<span data-ttu-id="cfae4-140">说明</span><span class="sxs-lookup"><span data-stu-id="cfae4-140">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="cfae4-141">CorSym_DocumentType_Text</span><span class="sxs-lookup"><span data-stu-id="cfae4-141">CorSym_DocumentType_Text</span></span>|<span data-ttu-id="cfae4-142">指示文本文档。</span><span class="sxs-lookup"><span data-stu-id="cfae4-142">Indicates a text document.</span></span>|  
|<span data-ttu-id="cfae4-143">CorSym_DocumentType_MC</span><span class="sxs-lookup"><span data-stu-id="cfae4-143">CorSym_DocumentType_MC</span></span>|<span data-ttu-id="cfae4-144">指示非文本文档。</span><span class="sxs-lookup"><span data-stu-id="cfae4-144">Indicates a non-text document.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cfae4-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cfae4-145">See also</span></span>

- [<span data-ttu-id="cfae4-146">非托管 API 参考</span><span class="sxs-lookup"><span data-stu-id="cfae4-146">Unmanaged API Reference</span></span>](index.md)
