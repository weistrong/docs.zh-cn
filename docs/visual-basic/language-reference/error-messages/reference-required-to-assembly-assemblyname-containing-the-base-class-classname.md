---
description: 了解有关以下内容的详细信息： BC30007：需要对程序集 " <assemblyname> " （包含基类 ""）的引用<classname>
title: 需要对程序集“<assemblyname>”（包含基类“<classname>”）的引用
ms.date: 07/20/2015
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
ms.openlocfilehash: f01795d3e8147015f9f46697b047a8c63099ff32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792045"
---
# <a name="bc30007-reference-required-to-assembly-assemblyname-containing-the-base-class-classname"></a><span data-ttu-id="4f3ee-103">BC30007：需要对 \<assemblyname> 包含基类 "" 的程序集 "" 的引用 \<classname></span><span class="sxs-lookup"><span data-stu-id="4f3ee-103">BC30007: Reference required to assembly '\<assemblyname>' containing the base class '\<classname>'</span></span>

<span data-ttu-id="4f3ee-104">需要对 \<assemblyname> 包含基类 "" 的程序集 "" 的引用 \<classname> 。</span><span class="sxs-lookup"><span data-stu-id="4f3ee-104">Reference required to assembly '\<assemblyname>' containing the base class '\<classname>'.</span></span> <span data-ttu-id="4f3ee-105">请向项目中添加一个。</span><span class="sxs-lookup"><span data-stu-id="4f3ee-105">Add one to your project.</span></span>

 <span data-ttu-id="4f3ee-106">该类是在动态链接库 (DLL) 或未在项目中直接引用的程序集中定义的。</span><span class="sxs-lookup"><span data-stu-id="4f3ee-106">The class is defined in a dynamic-link library (DLL) or assembly that is not directly referenced in your project.</span></span> <span data-ttu-id="4f3ee-107">如果类是在多个 DLL 或程序集中定义的，则 Visual Basic 编译器需要引用以避免多义性。</span><span class="sxs-lookup"><span data-stu-id="4f3ee-107">The Visual Basic compiler requires a reference to avoid ambiguity in case the class is defined in more than one DLL or assembly.</span></span>

 <span data-ttu-id="4f3ee-108">**错误 ID：** BC30007</span><span class="sxs-lookup"><span data-stu-id="4f3ee-108">**Error ID:** BC30007</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4f3ee-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4f3ee-109">To correct this error</span></span>

- <span data-ttu-id="4f3ee-110">将未引用的 DLL 或程序集名称包括在项目引用中。</span><span class="sxs-lookup"><span data-stu-id="4f3ee-110">Include the name of the unreferenced DLL or assembly in your project references.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f3ee-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f3ee-111">See also</span></span>

- [<span data-ttu-id="4f3ee-112">管理项目中的引用</span><span class="sxs-lookup"><span data-stu-id="4f3ee-112">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)
- [<span data-ttu-id="4f3ee-113">Troubleshooting Broken References</span><span class="sxs-lookup"><span data-stu-id="4f3ee-113">Troubleshooting Broken References</span></span>](/visualstudio/ide/troubleshooting-broken-references)
