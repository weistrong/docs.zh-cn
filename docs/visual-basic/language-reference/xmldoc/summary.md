---
description: 了解详细信息： <summary> (Visual Basic)
title: <summary>
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 4d4b1ecf0fa054eb625c1a3cf09c1cab4e661ef2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640285"
---
# <a name="summary-visual-basic"></a><span data-ttu-id="5fd46-103">\<summary> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5fd46-103">\<summary> (Visual Basic)</span></span>

<span data-ttu-id="5fd46-104">指定成员的摘要。</span><span class="sxs-lookup"><span data-stu-id="5fd46-104">Specifies the summary of the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fd46-105">语法</span><span class="sxs-lookup"><span data-stu-id="5fd46-105">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
## <a name="parameters"></a><span data-ttu-id="5fd46-106">参数</span><span class="sxs-lookup"><span data-stu-id="5fd46-106">Parameters</span></span>  

 `description`  
 <span data-ttu-id="5fd46-107">对象的摘要。</span><span class="sxs-lookup"><span data-stu-id="5fd46-107">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5fd46-108">备注</span><span class="sxs-lookup"><span data-stu-id="5fd46-108">Remarks</span></span>  

 <span data-ttu-id="5fd46-109">使用 `<summary>` 标记来描述类型或类型成员。</span><span class="sxs-lookup"><span data-stu-id="5fd46-109">Use the `<summary>` tag to describe a type or a type member.</span></span> <span data-ttu-id="5fd46-110">使用 [\<remarks>](remarks.md) 可针对某个类型说明添加补充信息。</span><span class="sxs-lookup"><span data-stu-id="5fd46-110">Use [\<remarks>](remarks.md) to add supplemental information to a type description.</span></span>  
  
 <span data-ttu-id="5fd46-111">标记的文本 `<summary>` 是有关 IntelliSense 中类型的唯一信息源，也会显示在对象浏览器中。</span><span class="sxs-lookup"><span data-stu-id="5fd46-111">The text for the `<summary>` tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser.</span></span> <span data-ttu-id="5fd46-112">有关对象浏览器的信息，请参阅 [查看代码的结构](/visualstudio/ide/viewing-the-structure-of-code)。</span><span class="sxs-lookup"><span data-stu-id="5fd46-112">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="5fd46-113">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="5fd46-113">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5fd46-114">示例</span><span class="sxs-lookup"><span data-stu-id="5fd46-114">Example</span></span>  

 <span data-ttu-id="5fd46-115">此示例使用 `<summary>` 标记来描述 `ResetCounter` 方法和 `Counter` 属性。</span><span class="sxs-lookup"><span data-stu-id="5fd46-115">This example uses the `<summary>` tag to describe the `ResetCounter` method and `Counter` property.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5fd46-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fd46-116">See also</span></span>

- [<span data-ttu-id="5fd46-117">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="5fd46-117">XML Comment Tags</span></span>](index.md)
