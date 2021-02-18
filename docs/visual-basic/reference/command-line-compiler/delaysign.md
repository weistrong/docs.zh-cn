---
description: 详细了解：-delaysign
title: -delaysign
ms.date: 03/10/2018
helpviewer_keywords:
- delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
ms.assetid: c76e61a4-1884-4252-9fb2-377f99caa690
ms.openlocfilehash: fc3e52f63431da870355e369e6ffeb8b7b14c5ab
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100461497"
---
# <a name="-delaysign"></a><span data-ttu-id="9bbee-103">-delaysign</span><span class="sxs-lookup"><span data-stu-id="9bbee-103">-delaysign</span></span>

<span data-ttu-id="9bbee-104">指定程序集是完全签名的还是部分签名的。</span><span class="sxs-lookup"><span data-stu-id="9bbee-104">Specifies whether the assembly will be fully or partially signed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbee-105">语法</span><span class="sxs-lookup"><span data-stu-id="9bbee-105">Syntax</span></span>

```console
-delaysign[+ | -]
```

## <a name="arguments"></a><span data-ttu-id="9bbee-106">自变量</span><span class="sxs-lookup"><span data-stu-id="9bbee-106">Arguments</span></span>

<span data-ttu-id="9bbee-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="9bbee-107">`+` &#124; `-`</span></span>  
<span data-ttu-id="9bbee-108">可选。</span><span class="sxs-lookup"><span data-stu-id="9bbee-108">Optional.</span></span> <span data-ttu-id="9bbee-109">如果需要完全签名的程序集，则使用 `-delaysign-`。</span><span class="sxs-lookup"><span data-stu-id="9bbee-109">Use `-delaysign-` if you want a fully signed assembly.</span></span> <span data-ttu-id="9bbee-110">如果希望将公钥置于程序集中，并为签名的哈希保留空间，请使用 `-delaysign+`。</span><span class="sxs-lookup"><span data-stu-id="9bbee-110">Use `-delaysign+` if you want to place the public key in the assembly and reserve space for the signed hash.</span></span> <span data-ttu-id="9bbee-111">默认值为 `-delaysign-`。</span><span class="sxs-lookup"><span data-stu-id="9bbee-111">The default is `-delaysign-`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bbee-112">备注</span><span class="sxs-lookup"><span data-stu-id="9bbee-112">Remarks</span></span>

<span data-ttu-id="9bbee-113">除非与 [-keyfile](keyfile.md) 或 [-keycontainer](keycontainer.md) 一同使用，否则 `-delaysign` 选项将不起作用。</span><span class="sxs-lookup"><span data-stu-id="9bbee-113">The `-delaysign` option has no effect unless used with [-keyfile](keyfile.md) or [-keycontainer](keycontainer.md).</span></span>

<span data-ttu-id="9bbee-114">在请求完全签名的程序集时，编译器会对包含清单（程序集元数据）的文件进行哈希处理，并使用私钥对哈希进行签名。</span><span class="sxs-lookup"><span data-stu-id="9bbee-114">When you request a fully signed assembly, the compiler hashes the file that contains the manifest (assembly metadata) and signs that hash with the private key.</span></span> <span data-ttu-id="9bbee-115">产生的数字签名存储在包含清单的文件中。</span><span class="sxs-lookup"><span data-stu-id="9bbee-115">The resulting digital signature is stored in the file that contains the manifest.</span></span> <span data-ttu-id="9bbee-116">在对程序集延迟签名时，编译器不会计算和存储签名，而是在文件中保留空间，以便稍后可添加签名。</span><span class="sxs-lookup"><span data-stu-id="9bbee-116">When an assembly is delay signed, the compiler does not compute and store the signature but reserves space in the file so the signature can be added later.</span></span>

<span data-ttu-id="9bbee-117">例如，通过使用 `-delaysign+`，组织中的开发人员可以分发程序集的未签名测试版本，测试人员可以将该版本注册到全局程序集缓存并使用。</span><span class="sxs-lookup"><span data-stu-id="9bbee-117">For example, by using `-delaysign+`, a developer in an organization can distribute unsigned test versions of an assembly that testers can register with the global assembly cache and use.</span></span> <span data-ttu-id="9bbee-118">在程序集上完成工作后，负责组织私钥的人员可以对程序集进行完全签名。</span><span class="sxs-lookup"><span data-stu-id="9bbee-118">When work on the assembly is completed, the person responsible for the organization's private key can fully sign the assembly.</span></span> <span data-ttu-id="9bbee-119">此区室化可防止组织私钥泄露，同时允许所有开发人员处理程序集。</span><span class="sxs-lookup"><span data-stu-id="9bbee-119">This compartmentalization protects the organization's private key from disclosure, while allowing all developers to work on the assemblies.</span></span>

<span data-ttu-id="9bbee-120">有关对程序集签名的详细信息，请参阅[创建和使用具有强名称的程序集](../../../standard/assembly/create-use-strong-named.md)。</span><span class="sxs-lookup"><span data-stu-id="9bbee-120">See [Creating and Using Strong-Named Assemblies](../../../standard/assembly/create-use-strong-named.md) for more information on signing an assembly.</span></span>

### <a name="to-set--delaysign-in-the-visual-studio-integrated-development-environment"></a><span data-ttu-id="9bbee-121">在 Visual Studio 集成开发环境中设置 -delaysign</span><span class="sxs-lookup"><span data-stu-id="9bbee-121">To set -delaysign in the Visual Studio integrated development environment</span></span>

1. <span data-ttu-id="9bbee-122">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="9bbee-122">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="9bbee-123">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="9bbee-123">On the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="9bbee-124">单击“签名”选项卡。 </span><span class="sxs-lookup"><span data-stu-id="9bbee-124">Click the **Signing** tab.</span></span>

3. <span data-ttu-id="9bbee-125">设置“仅延迟签名”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="9bbee-125">Set the value in the **Delay sign only** box.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bbee-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="9bbee-126">See also</span></span>

- [<span data-ttu-id="9bbee-127">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="9bbee-127">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="9bbee-128">-keyfile</span><span class="sxs-lookup"><span data-stu-id="9bbee-128">-keyfile</span></span>](keyfile.md)
- [<span data-ttu-id="9bbee-129">-keycontainer</span><span class="sxs-lookup"><span data-stu-id="9bbee-129">-keycontainer</span></span>](keycontainer.md)
- [<span data-ttu-id="9bbee-130">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="9bbee-130">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
