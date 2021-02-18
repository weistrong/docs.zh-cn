---
description: 详细了解：-baseaddress
title: -baseaddress
ms.date: 08/09/2018
f1_keywords:
- /baseaddress
- baseaddress
helpviewer_keywords:
- -baseaddress compiler option [Visual Basic]
- /baseaddress compiler option [Visual Basic]
- baseaddress compiler option [Visual Basic]
ms.assetid: c982bcf2-46e5-47a2-bc8f-a5cc32b7dc47
ms.openlocfilehash: eaa2992c126ebb83b20cfdbef3ab995a30ee25fd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468312"
---
# <a name="-baseaddress"></a><span data-ttu-id="12ac2-103">-baseaddress</span><span class="sxs-lookup"><span data-stu-id="12ac2-103">-baseaddress</span></span>

<span data-ttu-id="12ac2-104">创建 DLL 时指定默认基址。</span><span class="sxs-lookup"><span data-stu-id="12ac2-104">Specifies a default base address when creating a DLL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12ac2-105">语法</span><span class="sxs-lookup"><span data-stu-id="12ac2-105">Syntax</span></span>  
  
```console  
-baseaddress:address  
```  
  
## <a name="arguments"></a><span data-ttu-id="12ac2-106">自变量</span><span class="sxs-lookup"><span data-stu-id="12ac2-106">Arguments</span></span>  
  
|<span data-ttu-id="12ac2-107">术语</span><span class="sxs-lookup"><span data-stu-id="12ac2-107">Term</span></span>|<span data-ttu-id="12ac2-108">定义</span><span class="sxs-lookup"><span data-stu-id="12ac2-108">Definition</span></span>|  
|---|---|  
|`address`|<span data-ttu-id="12ac2-109">必需。</span><span class="sxs-lookup"><span data-stu-id="12ac2-109">Required.</span></span> <span data-ttu-id="12ac2-110">DLL 的基址。</span><span class="sxs-lookup"><span data-stu-id="12ac2-110">The base address for the DLL.</span></span> <span data-ttu-id="12ac2-111">此地址必须指定为十六进制数。</span><span class="sxs-lookup"><span data-stu-id="12ac2-111">This address must be specified as a hexadecimal number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="12ac2-112">备注</span><span class="sxs-lookup"><span data-stu-id="12ac2-112">Remarks</span></span>  

 <span data-ttu-id="12ac2-113">DLL 的默认基址由 .NET Framework 设置。</span><span class="sxs-lookup"><span data-stu-id="12ac2-113">The default base address for a DLL is set by the .NET Framework.</span></span>  
  
 <span data-ttu-id="12ac2-114">请注意，此地址中的低序字将被舍入取整。</span><span class="sxs-lookup"><span data-stu-id="12ac2-114">Be aware that the lower-order word in this address is rounded.</span></span> <span data-ttu-id="12ac2-115">例如，如果指定 0x11110001，它将被舍入为 0x11110000。</span><span class="sxs-lookup"><span data-stu-id="12ac2-115">For example, if you specify 0x11110001, it is rounded to 0x11110000.</span></span>  
  
 <span data-ttu-id="12ac2-116">若要完成 DLL 的签名过程，请使用强名称工具 (Sn.exe) 的 `–R` 选项。</span><span class="sxs-lookup"><span data-stu-id="12ac2-116">To complete the signing process for a DLL, use the `–R` option of the Strong Naming tool (Sn.exe).</span></span>  
  
 <span data-ttu-id="12ac2-117">如果目标不是 DLL，则忽略此选项。</span><span class="sxs-lookup"><span data-stu-id="12ac2-117">This option is ignored if the target is not a DLL.</span></span>  
  
|<span data-ttu-id="12ac2-118">在 Visual Studio IDE 中设置 --baseaddress</span><span class="sxs-lookup"><span data-stu-id="12ac2-118">To set -baseaddress in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="12ac2-119">1.在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="12ac2-119">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="12ac2-120">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="12ac2-120">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="12ac2-121">2.单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="12ac2-121">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="12ac2-122">3.单击 **“高级”** 。</span><span class="sxs-lookup"><span data-stu-id="12ac2-122">3.  Click **Advanced**.</span></span><br /><span data-ttu-id="12ac2-123">4.修改“DLL 基址”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="12ac2-123">4.  Modify the value in the **DLL base address:** box.</span></span> <span data-ttu-id="12ac2-124">**注意：**    “DLL 基址:”  框为只读，除非目标是 DLL。</span><span class="sxs-lookup"><span data-stu-id="12ac2-124">**Note:**      The **DLL base address:** box is read-only unless the target is a DLL.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="12ac2-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="12ac2-125">See also</span></span>

- [<span data-ttu-id="12ac2-126">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="12ac2-126">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="12ac2-127">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="12ac2-127">-target (Visual Basic)</span></span>](target.md)
- [<span data-ttu-id="12ac2-128">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="12ac2-128">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- <span data-ttu-id="12ac2-129">[Sn.exe（强名称工具）](../../../framework/tools/sn-exe-strong-name-tool.md)）</span><span class="sxs-lookup"><span data-stu-id="12ac2-129">[Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))</span></span>
