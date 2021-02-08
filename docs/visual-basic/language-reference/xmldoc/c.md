---
description: '了解详细信息： <c> (Visual Basic) '
title: <c>
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 350a5dbf2dee2911c356a7c76a9bafbab35fd71e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787508"
---
# <a name="c-visual-basic"></a><span data-ttu-id="8a17c-102">\<c> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8a17c-102">\<c> (Visual Basic)</span></span>

<span data-ttu-id="8a17c-103">指示说明中的文本为代码。</span><span class="sxs-lookup"><span data-stu-id="8a17c-103">Indicates that text within a description is code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a17c-104">语法</span><span class="sxs-lookup"><span data-stu-id="8a17c-104">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a17c-105">参数</span><span class="sxs-lookup"><span data-stu-id="8a17c-105">Parameters</span></span>  
  
|<span data-ttu-id="8a17c-106">参数</span><span class="sxs-lookup"><span data-stu-id="8a17c-106">Parameter</span></span>|<span data-ttu-id="8a17c-107">说明</span><span class="sxs-lookup"><span data-stu-id="8a17c-107">Description</span></span>|  
|---|---|  
|`text`|<span data-ttu-id="8a17c-108">要指示为代码的文本。</span><span class="sxs-lookup"><span data-stu-id="8a17c-108">The text you would like to indicate as code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a17c-109">备注</span><span class="sxs-lookup"><span data-stu-id="8a17c-109">Remarks</span></span>  

 <span data-ttu-id="8a17c-110">使用 `<c>` 标记可以指示应将说明内的文本标记为代码。</span><span class="sxs-lookup"><span data-stu-id="8a17c-110">The `<c>` tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="8a17c-111">使用 [\<code>](code.md) 指示作为代码的多行文本。</span><span class="sxs-lookup"><span data-stu-id="8a17c-111">Use [\<code>](code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="8a17c-112">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="8a17c-112">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8a17c-113">示例</span><span class="sxs-lookup"><span data-stu-id="8a17c-113">Example</span></span>  

 <span data-ttu-id="8a17c-114">此示例使用 " `<c>` 摘要" 部分中的标记指示该 `Counter` 为代码。</span><span class="sxs-lookup"><span data-stu-id="8a17c-114">This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="8a17c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a17c-115">See also</span></span>

- [<span data-ttu-id="8a17c-116">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="8a17c-116">XML Comment Tags</span></span>](index.md)
