---
description: 了解详细信息： <typeparam> (Visual Basic)
title: <typeparam>
ms.date: 07/20/2015
helpviewer_keywords:
- typeparam XML tag
- <typeparam> XML tag
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
ms.openlocfilehash: efb4394ee2badcf52bac75d7d9e317c732789746
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640259"
---
# <a name="typeparam-visual-basic"></a><span data-ttu-id="0ebd5-103">\<typeparam> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0ebd5-103">\<typeparam> (Visual Basic)</span></span>

<span data-ttu-id="0ebd5-104">定义类型参数名称和说明。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-104">Defines a type parameter name and description.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ebd5-105">语法</span><span class="sxs-lookup"><span data-stu-id="0ebd5-105">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
## <a name="parameters"></a><span data-ttu-id="0ebd5-106">parameters</span><span class="sxs-lookup"><span data-stu-id="0ebd5-106">Parameters</span></span>  

 `name`  
 <span data-ttu-id="0ebd5-107">类型参数的名称。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-107">The name of the type parameter.</span></span> <span data-ttu-id="0ebd5-108">用双引号 (" ") 将名称引起来。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-108">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="0ebd5-109">类型参数的说明。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-109">A description of the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0ebd5-110">备注</span><span class="sxs-lookup"><span data-stu-id="0ebd5-110">Remarks</span></span>  

 <span data-ttu-id="0ebd5-111">在 `<typeparam>` 泛型类型或泛型成员声明的注释中使用标记来描述一个类型参数。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-111">Use the `<typeparam>` tag in the comment for a generic type or generic member declaration to describe one of the type parameters.</span></span>  
  
 <span data-ttu-id="0ebd5-112">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-112">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ebd5-113">示例</span><span class="sxs-lookup"><span data-stu-id="0ebd5-113">Example</span></span>  

 <span data-ttu-id="0ebd5-114">此示例使用 `<typeparam>` 标记来描述 `id` 参数。</span><span class="sxs-lookup"><span data-stu-id="0ebd5-114">This example uses the `<typeparam>` tag to describe the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#8)]  
  
## <a name="see-also"></a><span data-ttu-id="0ebd5-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ebd5-115">See also</span></span>

- [<span data-ttu-id="0ebd5-116">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="0ebd5-116">XML Comment Tags</span></span>](index.md)
