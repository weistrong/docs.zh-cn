---
description: 详细了解：-win32manifest (Visual Basic)
title: -win32manifest
ms.date: 03/13/2018
helpviewer_keywords:
- /win32manifest compiler option [Visual Basic]
- win32manifest compiler option [Visual Basic]
- -win32manifest compiler option [Visual Basic]
ms.assetid: 9e3191b4-90db-41c8-966a-28036fd20005
ms.openlocfilehash: d8b674d3eb101fdaa05cca7fa67ba0a43999ca37
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433505"
---
# <a name="-win32manifest-visual-basic"></a><span data-ttu-id="490b7-103">-win32manifest (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="490b7-103">-win32manifest (Visual Basic)</span></span>

<span data-ttu-id="490b7-104">标识用户定义的 Win32 应用程序清单文件要嵌入到项目的可移植可执行 (PE) 文件。</span><span class="sxs-lookup"><span data-stu-id="490b7-104">Identifies a user-defined Win32 application manifest file to be embedded into a project's portable executable (PE) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="490b7-105">语法</span><span class="sxs-lookup"><span data-stu-id="490b7-105">Syntax</span></span>  
  
```console  
-win32manifest: fileName  
```  
  
## <a name="arguments"></a><span data-ttu-id="490b7-106">自变量</span><span class="sxs-lookup"><span data-stu-id="490b7-106">Arguments</span></span>  
  
|<span data-ttu-id="490b7-107">术语</span><span class="sxs-lookup"><span data-stu-id="490b7-107">Term</span></span>|<span data-ttu-id="490b7-108">定义</span><span class="sxs-lookup"><span data-stu-id="490b7-108">Definition</span></span>|  
|---|---|  
|`fileName`|<span data-ttu-id="490b7-109">自定义清单文件的路径。</span><span class="sxs-lookup"><span data-stu-id="490b7-109">The path of the custom manifest file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="490b7-110">备注</span><span class="sxs-lookup"><span data-stu-id="490b7-110">Remarks</span></span>  

 <span data-ttu-id="490b7-111">默认情况下，Visual Basic 编译器嵌入指定“asInvoker”的请求执行级别的应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="490b7-111">By default, the Visual Basic compiler embeds an application manifest that specifies a requested execution level of asInvoker.</span></span> <span data-ttu-id="490b7-112">它在生成该可执行文件的同一文件夹中创建清单，如果使用 Visual Studio，该文件夹通常为 bin\Debug 或 bin\Release。</span><span class="sxs-lookup"><span data-stu-id="490b7-112">It creates the manifest in the same folder in which the executable file is built, typically the bin\Debug or bin\Release folder when you use Visual Studio.</span></span> <span data-ttu-id="490b7-113">如果要提供自定义清单（例如，指定 highestAvailable 或 requireAdministrator 的请求执行级别的清单），请使用此选项指定文件名。</span><span class="sxs-lookup"><span data-stu-id="490b7-113">If you want to supply a custom manifest, for example to specify a requested execution level of highestAvailable or requireAdministrator, use this option to specify the name of the file.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="490b7-114">此选项和 [-win32resource](win32resource.md) 选项是互斥的。</span><span class="sxs-lookup"><span data-stu-id="490b7-114">This option and the [-win32resource](win32resource.md) option are mutually exclusive.</span></span> <span data-ttu-id="490b7-115">如果尝试在同一命令行中同时使用这两个选项，将收到一个生成错误。</span><span class="sxs-lookup"><span data-stu-id="490b7-115">If you try to use both options in the same command line, you will get a build error.</span></span>  
  
 <span data-ttu-id="490b7-116">如果应用程序没有用于指定请求执行级别的应用程序清单，将受到 Windows Vista 的用户帐户控制功能下的文件/注册表虚拟化的影响。</span><span class="sxs-lookup"><span data-stu-id="490b7-116">An application that has no application manifest that specifies a requested execution level will be subject to file/registry virtualization under the User Account Control feature in Windows Vista.</span></span> <span data-ttu-id="490b7-117">有关虚拟化的详细信息，请参阅 [Windows Vista 上的 ClickOnce 部署](/visualstudio/deployment/clickonce-deployment-on-windows-vista)。</span><span class="sxs-lookup"><span data-stu-id="490b7-117">For more information about virtualization, see [ClickOnce Deployment on Windows Vista](/visualstudio/deployment/clickonce-deployment-on-windows-vista).</span></span>  
  
 <span data-ttu-id="490b7-118">如果满足以下任一条件，则应用程序会受到虚拟化的影响：</span><span class="sxs-lookup"><span data-stu-id="490b7-118">Your application will be subject to virtualization if either of the following conditions is true:</span></span>  
  
1. <span data-ttu-id="490b7-119">使用 `-nowin32manifest` 选项，并且在随后的生成步骤中未提供清单，或者没有通过使用 `-win32resource` 选项将其包含在 Windows 资源 (.res) 文件中。</span><span class="sxs-lookup"><span data-stu-id="490b7-119">You use the `-nowin32manifest` option and you do not provide a manifest in a later build step or as part of a Windows Resource (.res) file by using the `-win32resource` option.</span></span>  
  
2. <span data-ttu-id="490b7-120">提供的自定义清单未指定请求执行级别。</span><span class="sxs-lookup"><span data-stu-id="490b7-120">You provide a custom manifest that does not specify a requested execution level.</span></span>  
  
 <span data-ttu-id="490b7-121">Visual Studio 创建默认 .manifest 文件，并将它与可执行文件一起存储在“调试”和“发布”目录中。</span><span class="sxs-lookup"><span data-stu-id="490b7-121">Visual Studio creates a default .manifest file and stores it in the debug and release directories alongside the executable file.</span></span> <span data-ttu-id="490b7-122">可以通过在项目设计器的“应用程序”  选项卡上单击“查看 UAC 设置”  来查看或编辑默认的 app.manifest 文件。</span><span class="sxs-lookup"><span data-stu-id="490b7-122">You can view or edit the default app.manifest file by clicking **View UAC Settings** on the **Application** tab in the Project Designer.</span></span> <span data-ttu-id="490b7-123">有关详细信息，请参阅 [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)（应用程序页、项目设计器 (Visual Basic)。</span><span class="sxs-lookup"><span data-stu-id="490b7-123">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
 <span data-ttu-id="490b7-124">提供应用程序清单的操作，可以作为自定义生成后步骤，也可以通过使用 `-nowin32manifest` 选项作为 Win32 资源文件的组成部分。</span><span class="sxs-lookup"><span data-stu-id="490b7-124">You can provide the application manifest as a custom post-build step or as part of a Win32 resource file by using the `-nowin32manifest` option.</span></span> <span data-ttu-id="490b7-125">如果希望应用程序受到 Windows Vista 的文件或注册表虚拟化的影响，请使用该选项。</span><span class="sxs-lookup"><span data-stu-id="490b7-125">Use that same option if you want your application to be subject to file or registry virtualization on Windows Vista.</span></span> <span data-ttu-id="490b7-126">这将阻止编译器在 PE 文件中创建和嵌入默认清单。</span><span class="sxs-lookup"><span data-stu-id="490b7-126">This will prevent the compiler from creating and embedding a default manifest in the PE file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="490b7-127">示例</span><span class="sxs-lookup"><span data-stu-id="490b7-127">Example</span></span>  

 <span data-ttu-id="490b7-128">下例演示了 Visual Basic 编译器插入到 PE 中的默认清单。</span><span class="sxs-lookup"><span data-stu-id="490b7-128">The following example shows the default manifest that the Visual Basic compiler inserts into a PE.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="490b7-129">编译器将一个标准应用程序名称“MyApplication.app”插入到清单 XML 中。</span><span class="sxs-lookup"><span data-stu-id="490b7-129">The compiler inserts a standard application name MyApplication.app into the manifest XML.</span></span> <span data-ttu-id="490b7-130">这是一种使应用程序可以在 Windows Server 2003 Service Pack 3 上运行的解决方法。</span><span class="sxs-lookup"><span data-stu-id="490b7-130">This is a workaround to enable applications to run on Windows Server 2003 Service Pack 3.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" standalone="yes"?>  
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">  
  <assemblyIdentity version="1.0.0.0" name="MyApplication.app"/>  
  <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">  
    <security>  
      <requestedPrivileges xmlns="urn:schemas-microsoft-com:asm.v3">  
        <requestedExecutionLevel level="asInvoker"/>  
      </requestedPrivileges>  
    </security>  
  </trustInfo>  
</assembly>  
```  
  
## <a name="see-also"></a><span data-ttu-id="490b7-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="490b7-131">See also</span></span>

- [<span data-ttu-id="490b7-132">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="490b7-132">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="490b7-133">-nowin32manifest (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="490b7-133">-nowin32manifest (Visual Basic)</span></span>](nowin32manifest.md)
