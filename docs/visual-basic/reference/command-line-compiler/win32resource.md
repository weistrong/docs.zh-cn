---
description: 详细了解：-win32resource
title: -win32resource
ms.date: 03/13/2018
f1_keywords:
- -win32resource
- win32resource
helpviewer_keywords:
- /win32resource compiler option [Visual Basic]
- -win32resource compiler option [Visual Basic]
- win32resource compiler option [Visual Basic]
ms.assetid: e226946d-19ce-4cc9-91f5-aed24f77aa2b
ms.openlocfilehash: a6f14fd2eb1349940c1e208a5baaa4205647f666
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433479"
---
# <a name="-win32resource"></a><span data-ttu-id="866b4-103">-win32resource</span><span class="sxs-lookup"><span data-stu-id="866b4-103">-win32resource</span></span>

<span data-ttu-id="866b4-104">在输出文件中插入 Win32 资源文件。</span><span class="sxs-lookup"><span data-stu-id="866b4-104">Inserts a Win32 resource file in the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="866b4-105">语法</span><span class="sxs-lookup"><span data-stu-id="866b4-105">Syntax</span></span>  
  
```console  
-win32resource:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="866b4-106">自变量</span><span class="sxs-lookup"><span data-stu-id="866b4-106">Arguments</span></span>  

 `filename`  
 <span data-ttu-id="866b4-107">要添加到输出文件的资源文件的名称。</span><span class="sxs-lookup"><span data-stu-id="866b4-107">The name of the resource file to add to your output file.</span></span> <span data-ttu-id="866b4-108">如果文件名包含空格，则将名称括在引号 (" ") 内。</span><span class="sxs-lookup"><span data-stu-id="866b4-108">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="866b4-109">备注</span><span class="sxs-lookup"><span data-stu-id="866b4-109">Remarks</span></span>  

 <span data-ttu-id="866b4-110">可以使用 Microsoft Windows 资源编译器 (RC) 创建 Win32 资源文件。</span><span class="sxs-lookup"><span data-stu-id="866b4-110">You can create a Win32 resource file with the Microsoft Windows Resource Compiler (RC).</span></span>  
  
 <span data-ttu-id="866b4-111">Win32 资源可以包含版本或位图（图标）信息，这些信息有助于在文件资源管理器  中标识你的应用程序。</span><span class="sxs-lookup"><span data-stu-id="866b4-111">A Win32 resource can contain version or bitmap (icon) information that helps identify your application in **File Explorer**.</span></span> <span data-ttu-id="866b4-112">如果不指定 `-win32resource`，编译器将根据程序集版本生成版本信息。</span><span class="sxs-lookup"><span data-stu-id="866b4-112">If you do not specify `-win32resource`, the compiler generates version information based on the assembly version.</span></span> <span data-ttu-id="866b4-113">`-win32resource` 和 `-win32icon` 选项互斥。</span><span class="sxs-lookup"><span data-stu-id="866b4-113">The `-win32resource` and `-win32icon` options are mutually exclusive.</span></span>  
  
 <span data-ttu-id="866b4-114">请参阅 [-linkresource (Visual Basic)](linkresource.md) 以引用 .NET Framework 资源文件，或参阅 [-resource (Visual Basic)](resource.md) 以附加 .NET Framework 资源文件。</span><span class="sxs-lookup"><span data-stu-id="866b4-114">See [-linkresource (Visual Basic)](linkresource.md) to reference a .NET Framework resource file, or [-resource (Visual Basic)](resource.md) to attach a .NET Framework resource file.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="866b4-115">`-win32resource` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="866b4-115">The `-win32resource` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="866b4-116">示例</span><span class="sxs-lookup"><span data-stu-id="866b4-116">Example</span></span>  

 <span data-ttu-id="866b4-117">下面的代码编译 `In.vb` 并附加 Win32 资源文件 `Rf.res`：</span><span class="sxs-lookup"><span data-stu-id="866b4-117">The following code compiles `In.vb` and attaches a Win32 resource file, `Rf.res`:</span></span>  
  
```console  
vbc -win32resource:rf.res in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="866b4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="866b4-118">See also</span></span>

- [<span data-ttu-id="866b4-119">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="866b4-119">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="866b4-120">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="866b4-120">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
