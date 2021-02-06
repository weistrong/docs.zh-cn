---
description: 了解详细信息： <returns> (Visual Basic)
title: <returns>
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: ba5f1e231502a67e86ffbb92cf8868c3aecb05d2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640376"
---
# <a name="returns-visual-basic"></a><span data-ttu-id="a54c7-103">\<returns> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a54c7-103">\<returns> (Visual Basic)</span></span>

<span data-ttu-id="a54c7-104">指定属性或函数的返回值。</span><span class="sxs-lookup"><span data-stu-id="a54c7-104">Specifies the return value of the property or function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a54c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="a54c7-105">Syntax</span></span>  
  
```xml  
<returns>description</returns>  
```  
  
## <a name="parameters"></a><span data-ttu-id="a54c7-106">参数</span><span class="sxs-lookup"><span data-stu-id="a54c7-106">Parameters</span></span>  

 `description`  
 <span data-ttu-id="a54c7-107">返回值的说明。</span><span class="sxs-lookup"><span data-stu-id="a54c7-107">A description of the return value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a54c7-108">备注</span><span class="sxs-lookup"><span data-stu-id="a54c7-108">Remarks</span></span>  

 <span data-ttu-id="a54c7-109">`<returns>`在方法声明的注释中使用标记来描述返回值。</span><span class="sxs-lookup"><span data-stu-id="a54c7-109">Use the `<returns>` tag in the comment for a method declaration to describe the return value.</span></span>  
  
 <span data-ttu-id="a54c7-110">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="a54c7-110">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a54c7-111">示例</span><span class="sxs-lookup"><span data-stu-id="a54c7-111">Example</span></span>  

 <span data-ttu-id="a54c7-112">此示例使用 `<returns>` 标记解释函数返回的内容 `DoesRecordExist` 。</span><span class="sxs-lookup"><span data-stu-id="a54c7-112">This example uses the `<returns>` tag to explain what the `DoesRecordExist` function returns.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="a54c7-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a54c7-113">See also</span></span>

- [<span data-ttu-id="a54c7-114">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="a54c7-114">XML Comment Tags</span></span>](index.md)
