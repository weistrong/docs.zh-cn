---
description: 了解详细信息： <code>(Visual Basic)
title: <code>
ms.date: 07/20/2015
helpviewer_keywords:
- code XML tag
- <code> XML tag
ms.assetid: 925e5342-be05-45f2-bf66-7398bbd6710e
ms.openlocfilehash: 80fc0988f60d9d82b9c88734f86b20ebccc80b7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787495"
---
# <a name="code-visual-basic"></a><span data-ttu-id="e6d4e-102">\<code> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e6d4e-102">\<code> (Visual Basic)</span></span>

<span data-ttu-id="e6d4e-103">指示文本为多行代码。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-103">Indicates that the text is multiple lines of code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6d4e-104">语法</span><span class="sxs-lookup"><span data-stu-id="e6d4e-104">Syntax</span></span>  
  
```xml  
<code>content</code>  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6d4e-105">参数</span><span class="sxs-lookup"><span data-stu-id="e6d4e-105">Parameters</span></span>  

 `content`  
 <span data-ttu-id="e6d4e-106">要标记为代码的文本。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-106">The text to mark as code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6d4e-107">备注</span><span class="sxs-lookup"><span data-stu-id="e6d4e-107">Remarks</span></span>  

 <span data-ttu-id="e6d4e-108">使用 `<code>` 标记将多行指示为代码。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-108">Use the `<code>` tag to indicate multiple lines as code.</span></span> <span data-ttu-id="e6d4e-109">用于 [\<c>](c.md) 指示应将说明内的文本标记为代码。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-109">Use [\<c>](c.md) to indicate that text within a description should be marked as code.</span></span>  
  
 <span data-ttu-id="e6d4e-110">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-110">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e6d4e-111">示例</span><span class="sxs-lookup"><span data-stu-id="e6d4e-111">Example</span></span>  

 <span data-ttu-id="e6d4e-112">此示例使用 \<code> 标记来包含用于使用字段的示例代码 `ID` 。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-112">This example uses the \<code> tag to include example code for using the `ID` field.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="e6d4e-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="e6d4e-113">See also</span></span>

- [<span data-ttu-id="e6d4e-114">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="e6d4e-114">XML Comment Tags</span></span>](index.md)
