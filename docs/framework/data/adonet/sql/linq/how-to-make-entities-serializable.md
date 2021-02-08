---
description: 了解详细信息：如何：使实体可序列化
title: 如何：使实体可序列化
ms.date: 03/30/2017
ms.assetid: a6c5bf6e-064a-4f77-b74c-76b3a5dec309
ms.openlocfilehash: cb2253d7933f3584543b4b030bc8b5aa3cc62921
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785934"
---
# <a name="how-to-make-entities-serializable"></a><span data-ttu-id="d0e4c-103">如何：使实体可序列化</span><span class="sxs-lookup"><span data-stu-id="d0e4c-103">How to: Make Entities Serializable</span></span>

<span data-ttu-id="d0e4c-104">当您生成代码时，可以使实体可序列化。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-104">You can make entities serializable when you generate your code.</span></span> <span data-ttu-id="d0e4c-105">实体类使用 <xref:System.Runtime.Serialization.DataContractAttribute> 属性修饰，列使用 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性修饰。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-105">Entity classes are decorated with the <xref:System.Runtime.Serialization.DataContractAttribute> attribute, and columns with the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute.</span></span>  
  
 <span data-ttu-id="d0e4c-106">使用 Visual Studio 的开发人员可以使用对象关系设计器来实现此目的。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-106">Developers using Visual Studio can use the Object Relational Designer for this purpose.</span></span>  
  
 <span data-ttu-id="d0e4c-107">如果使用 SQLMetal 命令行工具，请将 **/serialization** 选项与参数一起使用 `unidirectional` 。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-107">If you are using the SQLMetal command-line tool, use the **/serialization** option with the `unidirectional` argument.</span></span> <span data-ttu-id="d0e4c-108">有关详细信息，请参阅 [SqlMetal.exe（代码生成工具）](../../../../tools/sqlmetal-exe-code-generation-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-108">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d0e4c-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0e4c-109">Example</span></span>  

 <span data-ttu-id="d0e4c-110">以下 SQLMetal 命令行会产生包含可序列化实体的文件。</span><span class="sxs-lookup"><span data-stu-id="d0e4c-110">The following SQLMetal command lines produce files that have serializable entities.</span></span>  
  
```console  
sqlmetal /code:nwserializable.vb /language:vb "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
```console  
sqlmetal /code:nwserializable.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
## <a name="see-also"></a><span data-ttu-id="d0e4c-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0e4c-111">See also</span></span>

- [<span data-ttu-id="d0e4c-112">序列化</span><span class="sxs-lookup"><span data-stu-id="d0e4c-112">Serialization</span></span>](serialization.md)
- [<span data-ttu-id="d0e4c-113">创建对象模型</span><span class="sxs-lookup"><span data-stu-id="d0e4c-113">Creating the Object Model</span></span>](creating-the-object-model.md)
