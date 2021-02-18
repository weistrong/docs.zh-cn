---
description: 详细了解：-keyfile
title: -keyfile
ms.date: 03/10/2018
helpviewer_keywords:
- /keyfile compiler option [Visual Basic]
- keyfile compiler option [Visual Basic]
- -keyfile compiler option [Visual Basic]
ms.assetid: ffa82a4b-517a-4c6c-9889-5bae7b534bb8
ms.openlocfilehash: 6d19f136d5961e8a933380164a3a77055e1da329
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466934"
---
# <a name="-keyfile"></a><span data-ttu-id="63242-103">-keyfile</span><span class="sxs-lookup"><span data-stu-id="63242-103">-keyfile</span></span>

<span data-ttu-id="63242-104">指定包含密钥或密钥对的文件从而为程序集赋予强名称。</span><span class="sxs-lookup"><span data-stu-id="63242-104">Specifies a file containing a key or key pair to give an assembly a strong name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63242-105">语法</span><span class="sxs-lookup"><span data-stu-id="63242-105">Syntax</span></span>  
  
```console
-keyfile:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="63242-106">自变量</span><span class="sxs-lookup"><span data-stu-id="63242-106">Arguments</span></span>  

 `file`  
 <span data-ttu-id="63242-107">必需。</span><span class="sxs-lookup"><span data-stu-id="63242-107">Required.</span></span> <span data-ttu-id="63242-108">包含密钥的文件。</span><span class="sxs-lookup"><span data-stu-id="63242-108">File that contains the key.</span></span> <span data-ttu-id="63242-109">如果文件名包含空格，则将名称括在引号内 (" ")。</span><span class="sxs-lookup"><span data-stu-id="63242-109">If the file name contains a space, enclose the name in quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63242-110">备注</span><span class="sxs-lookup"><span data-stu-id="63242-110">Remarks</span></span>  

 <span data-ttu-id="63242-111">编译器在程序集清单中插入公钥，然后使用私钥对最终的程序集进行签名。</span><span class="sxs-lookup"><span data-stu-id="63242-111">The compiler inserts the public key into the assembly manifest and then signs the final assembly with the private key.</span></span> <span data-ttu-id="63242-112">若要生成密钥文件，请在命令行键入 `sn -k file`。</span><span class="sxs-lookup"><span data-stu-id="63242-112">To generate a key file, type `sn -k file` at the command line.</span></span> <span data-ttu-id="63242-113">有关详细信息，请参阅 [Sn.exe（强名称工具）](../../../framework/tools/sn-exe-strong-name-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="63242-113">For more information, see [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span></span>  
  
 <span data-ttu-id="63242-114">如果使用 `-target:module` 进行编译，密钥文件的名称将保存在模块中，并在使用 [-addmodule](addmodule.md) 编译程序集时包含到创建的程序集中。</span><span class="sxs-lookup"><span data-stu-id="63242-114">If you compile with `-target:module`, the name of the key file is held in the module and incorporated into the assembly that is created when you compile an assembly with [-addmodule](addmodule.md).</span></span>  
  
 <span data-ttu-id="63242-115">也可以使用 [-keycontainer](keycontainer.md) 将加密信息传递给编译器。</span><span class="sxs-lookup"><span data-stu-id="63242-115">You can also pass your encryption information to the compiler with [-keycontainer](keycontainer.md).</span></span> <span data-ttu-id="63242-116">如果需要部分签名的程序集，请使用 [-delaysign](delaysign.md)。</span><span class="sxs-lookup"><span data-stu-id="63242-116">Use [-delaysign](delaysign.md) if you want a partially signed assembly.</span></span>  
  
 <span data-ttu-id="63242-117">还可以将此选项指定为任何 Microsoft 中间语言模块的源代码中的自定义属性 (<xref:System.Reflection.AssemblyKeyFileAttribute>)。</span><span class="sxs-lookup"><span data-stu-id="63242-117">You can also specify this option as a custom attribute (<xref:System.Reflection.AssemblyKeyFileAttribute>) in the source code for any Microsoft intermediate language module.</span></span>  
  
 <span data-ttu-id="63242-118">如果在同一编译中同时指定 `-keyfile` 和 [-keycontainer](keycontainer.md)（通过命令行选项或通过自定义特性），则编译器将首先尝试密钥容器。</span><span class="sxs-lookup"><span data-stu-id="63242-118">In case both `-keyfile` and [-keycontainer](keycontainer.md) are specified (either by command-line option or by custom attribute) in the same compilation, the compiler first tries the key container.</span></span> <span data-ttu-id="63242-119">如果成功，则使用密钥容器中的信息对程序集签名。</span><span class="sxs-lookup"><span data-stu-id="63242-119">If that succeeds, then the assembly is signed with the information in the key container.</span></span> <span data-ttu-id="63242-120">如果编译器没有找到密钥容器，它将尝试用 `-keyfile` 指定的文件。</span><span class="sxs-lookup"><span data-stu-id="63242-120">If the compiler does not find the key container, it tries the file specified with `-keyfile`.</span></span> <span data-ttu-id="63242-121">如果成功，则使用密钥文件中的信息对程序集签名，并且将密钥信息安装到密钥容器中（类似于 `sn -i`），以便在下一次编译中，密钥容器选项将生效。</span><span class="sxs-lookup"><span data-stu-id="63242-121">If this succeeds, the assembly is signed with the information in the key file, and the key information is installed in the key container (similar to `sn -i`) so that on the next compilation, the key container will be valid.</span></span>  
  
 <span data-ttu-id="63242-122">请注意，密钥文件可能仅包含公钥。</span><span class="sxs-lookup"><span data-stu-id="63242-122">Note that a key file might contain only the public key.</span></span>  
  
 <span data-ttu-id="63242-123">有关对程序集签名的详细信息，请参阅[创建和使用具有强名称的程序集](../../../standard/assembly/create-use-strong-named.md)。</span><span class="sxs-lookup"><span data-stu-id="63242-123">See [Creating and Using Strong-Named Assemblies](../../../standard/assembly/create-use-strong-named.md) for more information on signing an assembly.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="63242-124">Visual Studio 开发环境内无法使用 `-keyfile` 选项；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="63242-124">The `-keyfile` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>

## <a name="example"></a><span data-ttu-id="63242-125">示例</span><span class="sxs-lookup"><span data-stu-id="63242-125">Example</span></span>

<span data-ttu-id="63242-126">下面的代码编译源文件 `Input.vb`，并指定一个密钥文件。</span><span class="sxs-lookup"><span data-stu-id="63242-126">The following code compiles source file `Input.vb` and specifies a key file.</span></span>

```console
vbc -keyfile:myfile.sn input.vb
```

## <a name="see-also"></a><span data-ttu-id="63242-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="63242-127">See also</span></span>

- [<span data-ttu-id="63242-128">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="63242-128">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="63242-129">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="63242-129">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="63242-130">-reference (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="63242-130">-reference (Visual Basic)</span></span>](reference.md)
- [<span data-ttu-id="63242-131">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="63242-131">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
