---
description: 详细了解：<inheritdoc>（C# 编程指南）
title: <inheritdoc> - C# 编程指南
ms.date: 01/21/2020
f1_keywords:
- inheritdoc
- <inheritdoc>
helpviewer_keywords:
- <inheritdoc> C# XML tag
- inheritdoc C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 960bdfbcec1e3f6a89675273f63b6d398e44947e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719391"
---
# <a name="inheritdoc-c-programming-guide"></a><span data-ttu-id="4de4a-103">\<inheritdoc>（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="4de4a-103">\<inheritdoc> (C# Programming Guide)</span></span>

## <a name="syntax"></a><span data-ttu-id="4de4a-104">语法</span><span class="sxs-lookup"><span data-stu-id="4de4a-104">Syntax</span></span>  
  
```xml  
<inheritdoc/>
```  

## <a name="inheritdoc"></a><span data-ttu-id="4de4a-105">InheritDoc</span><span class="sxs-lookup"><span data-stu-id="4de4a-105">InheritDoc</span></span>

<span data-ttu-id="4de4a-106">继承基类、接口和类似方法中的 XML 注释。</span><span class="sxs-lookup"><span data-stu-id="4de4a-106">Inherit XML comments from base classes, interfaces, and similar methods.</span></span> <span data-ttu-id="4de4a-107">这样不必复制和粘贴重复的 XML 注释，并自动保持 XML 注释同步。</span><span class="sxs-lookup"><span data-stu-id="4de4a-107">This eliminates unwanted copying and pasting of duplicate XML comments and automatically keeps XML comments synchronized.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4de4a-108">备注</span><span class="sxs-lookup"><span data-stu-id="4de4a-108">Remarks</span></span>  

<span data-ttu-id="4de4a-109">在基类或接口中添加 XML 注释，并让 InheritDoc 将注释复制到实现类中。</span><span class="sxs-lookup"><span data-stu-id="4de4a-109">Add your XML comments in base classes or interfaces and let InheritDoc copy the comments to implementing classes.</span></span>

<span data-ttu-id="4de4a-110">向同步方法添加 XML 注释，并让 InheritDoc 将注释复制到相同方法的异步版本中。</span><span class="sxs-lookup"><span data-stu-id="4de4a-110">Add your XML comments to your synchronous methods and let InheritDoc copy the comments to your asynchronous versions of the same methods.</span></span>  

<span data-ttu-id="4de4a-111">如果要从特定成员复制注释，可以使用 `cref` 特性来指定成员。</span><span class="sxs-lookup"><span data-stu-id="4de4a-111">If you want to copy the comments from a specific member you can use the `cref` attribute to specify the member.</span></span>
  
## <a name="examples"></a><span data-ttu-id="4de4a-112">示例</span><span class="sxs-lookup"><span data-stu-id="4de4a-112">Examples</span></span>

[!code-csharp[csProgGuideDocComments#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#16)]  

[!code-csharp[csProgGuideDocComments#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#17)]  

## <a name="see-also"></a><span data-ttu-id="4de4a-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4de4a-113">See also</span></span>

- [<span data-ttu-id="4de4a-114">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="4de4a-114">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="4de4a-115">建议的文档注释标记</span><span class="sxs-lookup"><span data-stu-id="4de4a-115">Recommended Tags for Documentation Comments</span></span>](./recommended-tags-for-documentation-comments.md)
