---
description: 了解详细信息： <permission> (Visual Basic)
title: <permission>
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: 7a227e97051002c834c96297d3028f08e3ed07ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700255"
---
# <a name="permission-visual-basic"></a><span data-ttu-id="a905e-103">\<permission> (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a905e-103">\<permission> (Visual Basic)</span></span>

<span data-ttu-id="a905e-104">指定成员所需的权限。</span><span class="sxs-lookup"><span data-stu-id="a905e-104">Specifies a required permission for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a905e-105">语法</span><span class="sxs-lookup"><span data-stu-id="a905e-105">Syntax</span></span>  
  
```xml  
<permission cref="member">description</permission>  
```  
  
## <a name="parameters"></a><span data-ttu-id="a905e-106">参数</span><span class="sxs-lookup"><span data-stu-id="a905e-106">Parameters</span></span>  

 `member`  
 <span data-ttu-id="a905e-107">对可从当前编译环境调用的成员或字段的引用。</span><span class="sxs-lookup"><span data-stu-id="a905e-107">A reference to a member or field that is available to be called from the current compilation environment.</span></span> <span data-ttu-id="a905e-108">编译器检查是否存在给定的代码元素，并将 `member` 转换为输出 XML 中规范的元素名称。</span><span class="sxs-lookup"><span data-stu-id="a905e-108">The compiler checks that the given code element exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="a905e-109">用 `member` 引号将 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="a905e-109">Enclose `member` in quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="a905e-110">对成员访问权限的说明。</span><span class="sxs-lookup"><span data-stu-id="a905e-110">A description of the access to the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a905e-111">备注</span><span class="sxs-lookup"><span data-stu-id="a905e-111">Remarks</span></span>  

 <span data-ttu-id="a905e-112">使用 `<permission>` 标记来记录成员的访问。</span><span class="sxs-lookup"><span data-stu-id="a905e-112">Use the `<permission>` tag to document the access of a member.</span></span> <span data-ttu-id="a905e-113">使用 <xref:System.Security.PermissionSet> 类指定对成员的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a905e-113">Use the <xref:System.Security.PermissionSet> class to specify access to a member.</span></span>  
  
 <span data-ttu-id="a905e-114">使用 [-doc](../../reference/command-line-compiler/doc.md) 进行编译以便将文档注释处理到文件中。</span><span class="sxs-lookup"><span data-stu-id="a905e-114">Compile with [-doc](../../reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a905e-115">示例</span><span class="sxs-lookup"><span data-stu-id="a905e-115">Example</span></span>  

 <span data-ttu-id="a905e-116">此示例使用 `<permission>` 标记来描述 <xref:System.Security.Permissions.FileIOPermission> 方法所需的 `ReadFile` 。</span><span class="sxs-lookup"><span data-stu-id="a905e-116">This example uses the `<permission>` tag to describe that the <xref:System.Security.Permissions.FileIOPermission> is required by the `ReadFile` method.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#7)]  
  
## <a name="see-also"></a><span data-ttu-id="a905e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a905e-117">See also</span></span>

- [<span data-ttu-id="a905e-118">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="a905e-118">XML Comment Tags</span></span>](index.md)
