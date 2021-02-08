---
description: 了解更多：建模和映射
title: 建模和映射
ms.date: 03/30/2017
ms.assetid: ec8a9515-3708-4cde-a688-4d8e6975f150
ms.openlocfilehash: 063cac072b7a205a471cd808fc85ad9a3ac71288
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794996"
---
# <a name="modeling-and-mapping"></a><span data-ttu-id="85e68-103">建模和映射</span><span class="sxs-lookup"><span data-stu-id="85e68-103">Modeling and Mapping</span></span>

<span data-ttu-id="85e68-104">在实体框架中，可以定义概念模型、存储模型以及这两者之间的映射，以最适合应用程序的方式进行。</span><span class="sxs-lookup"><span data-stu-id="85e68-104">In the Entity Framework, you can define the conceptual model, storage model, and the mapping between the two in the way that best suits your application.</span></span> <span data-ttu-id="85e68-105">使用 Visual Studio 中的实体数据模型工具可创建。数据库或图形模型中的[edmx 文件](/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)) ，然后在数据库或模型发生更改时更新该文件。</span><span class="sxs-lookup"><span data-stu-id="85e68-105">The Entity Data Model Tools in Visual Studio allow you to create an .[edmx file](/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)) from a database or a graphical model and then update that file when either the database or model changes.</span></span>  
  
 <span data-ttu-id="85e68-106">实体框架4.1 开始，还可使用 Code First 开发以编程方式创建模型。</span><span class="sxs-lookup"><span data-stu-id="85e68-106">Starting with the Entity Framework 4.1 you can also create a model programmatically using Code First development.</span></span> <span data-ttu-id="85e68-107">对于 Code First 开发，有两种不同的方案。</span><span class="sxs-lookup"><span data-stu-id="85e68-107">There are two different scenarios for Code First development.</span></span> <span data-ttu-id="85e68-108">在两种情况下，开发人员通过对 .NET Framework 类定义进行编码来定义模型，然后可选择使用数据注释或 fluent API 指定其他映射或配置。</span><span class="sxs-lookup"><span data-stu-id="85e68-108">In both cases, the developer defines a model by coding .NET Framework class definitions, and then optionally specifies additional mapping or configuration by using Data Annotations or the fluent API.</span></span>  
  
 <span data-ttu-id="85e68-109">有关详细信息，请参阅[创建模型](/ef/ef6/modeling/)。</span><span class="sxs-lookup"><span data-stu-id="85e68-109">For more information, see [Creating a Model](/ef/ef6/modeling/).</span></span>  
  
 <span data-ttu-id="85e68-110">你还可以使用 .NET Framework 附带的 EDM 生成器。</span><span class="sxs-lookup"><span data-stu-id="85e68-110">You can also use the EDM Generator, which is included with the .NET Framework.</span></span> <span data-ttu-id="85e68-111">EdmGen.exe 从现有数据源生成 .csdl、 .ssdl 和 .msl 文件。</span><span class="sxs-lookup"><span data-stu-id="85e68-111">The EdmGen.exe generates the .csdl, .ssdl, and .msl files from an existing data source.</span></span> <span data-ttu-id="85e68-112">也可以手动创建模型和映射内容。</span><span class="sxs-lookup"><span data-stu-id="85e68-112">You can also manually create the model and mapping content.</span></span> <span data-ttu-id="85e68-113">有关详细信息，请参阅 [EDM 生成器 ( # A0) ](edm-generator-edmgen-exe.md)。</span><span class="sxs-lookup"><span data-stu-id="85e68-113">For more information, see [EDM Generator (EdmGen.exe)](edm-generator-edmgen-exe.md).</span></span>
