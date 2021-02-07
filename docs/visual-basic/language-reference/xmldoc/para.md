---
description: 了解详细信息： <para> (Visual Basic)
title: <para>
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: 51dd9ff300d980b4c0576566cad5d17375889ba1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740764"
---
# <a name="para-visual-basic"></a><span data-ttu-id="3f534-103">\<para> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3f534-103">\<para> (Visual Basic)</span></span>

<span data-ttu-id="3f534-104">指定将内容的格式设置为段落。</span><span class="sxs-lookup"><span data-stu-id="3f534-104">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f534-105">语法</span><span class="sxs-lookup"><span data-stu-id="3f534-105">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
## <a name="parameters"></a><span data-ttu-id="3f534-106">参数</span><span class="sxs-lookup"><span data-stu-id="3f534-106">Parameters</span></span>  

 `content`  
 <span data-ttu-id="3f534-107">段落文本。</span><span class="sxs-lookup"><span data-stu-id="3f534-107">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f534-108">备注</span><span class="sxs-lookup"><span data-stu-id="3f534-108">Remarks</span></span>  

 <span data-ttu-id="3f534-109">`<para>` 标记用于标记内，例如 [\<summary>](summary.md)、[\<remarks>](remarks.md) 或 [\<returns>](returns.md)，允许向文本添加结构。</span><span class="sxs-lookup"><span data-stu-id="3f534-109">The `<para>` tag is for use inside a tag, such as [\<summary>](summary.md), [\<remarks>](remarks.md), or [\<returns>](returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="3f534-110">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="3f534-110">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f534-111">示例</span><span class="sxs-lookup"><span data-stu-id="3f534-111">Example</span></span>  

 <span data-ttu-id="3f534-112">此示例使用 `<para>` 标记将方法的 "备注" 部分拆分为 `UpdateRecord` 两个段落。</span><span class="sxs-lookup"><span data-stu-id="3f534-112">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="3f534-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f534-113">See also</span></span>

- [<span data-ttu-id="3f534-114">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="3f534-114">XML Comment Tags</span></span>](index.md)
