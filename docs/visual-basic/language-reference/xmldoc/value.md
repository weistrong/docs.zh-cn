---
description: 了解详细信息： <value> (Visual Basic)
title: <value>
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: 80a3ef875eea4418d28d60dac1818f3390c361ee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640246"
---
# <a name="value-visual-basic"></a><span data-ttu-id="42c3d-103">\<value> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="42c3d-103">\<value> (Visual Basic)</span></span>

<span data-ttu-id="42c3d-104">指定属性的说明。</span><span class="sxs-lookup"><span data-stu-id="42c3d-104">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42c3d-105">语法</span><span class="sxs-lookup"><span data-stu-id="42c3d-105">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
## <a name="parameters"></a><span data-ttu-id="42c3d-106">参数</span><span class="sxs-lookup"><span data-stu-id="42c3d-106">Parameters</span></span>  

 `property-description`  
 <span data-ttu-id="42c3d-107">属性的说明。</span><span class="sxs-lookup"><span data-stu-id="42c3d-107">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="42c3d-108">备注</span><span class="sxs-lookup"><span data-stu-id="42c3d-108">Remarks</span></span>  

 <span data-ttu-id="42c3d-109">使用 `<value>` 标记来描述属性。</span><span class="sxs-lookup"><span data-stu-id="42c3d-109">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="42c3d-110">请注意，当您使用 Visual Studio 开发环境中的代码向导添加属性时，它将 [\<summary>](summary.md) 为新属性添加标记。</span><span class="sxs-lookup"><span data-stu-id="42c3d-110">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](summary.md) tag for the new property.</span></span> <span data-ttu-id="42c3d-111">然后，应手动添加 `<value>` 标记，以描述属性表示的值。</span><span class="sxs-lookup"><span data-stu-id="42c3d-111">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="42c3d-112">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="42c3d-112">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="42c3d-113">示例</span><span class="sxs-lookup"><span data-stu-id="42c3d-113">Example</span></span>  

 <span data-ttu-id="42c3d-114">此示例使用 `<value>` 标记来描述属性包含的值 `Counter` 。</span><span class="sxs-lookup"><span data-stu-id="42c3d-114">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="42c3d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="42c3d-115">See also</span></span>

- [<span data-ttu-id="42c3d-116">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="42c3d-116">XML Comment Tags</span></span>](index.md)
