---
description: 详细了解：Tlbexp 帮助器函数（非托管 API 参考）
title: Tlbexp 帮助器函数（非托管 API 参考）
ms.date: 03/30/2017
helpviewer_keywords:
- exporter tool [.NET Framework]
- TlbRef.dll
- Tlbexp.exe
- Type Library Exporter
ms.assetid: 5c0a3d14-5f26-4267-94a9-82c30f8db09a
ms.openlocfilehash: 8d5aacbe63d111b0b53f6bc76357a37ee4660d0c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646252"
---
# <a name="tlbexp-helper-functions-unmanaged-api-reference"></a><span data-ttu-id="2e5f4-103">Tlbexp 帮助器函数（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="2e5f4-103">Tlbexp Helper Functions (Unmanaged API Reference)</span></span>

<span data-ttu-id="2e5f4-104">[类型库导出程序工具](../../tools/tlbexp-exe-type-library-exporter.md) (Tlbexp.exe) 加载一个名为“TlbRef.dll”的动态链接库。</span><span class="sxs-lookup"><span data-stu-id="2e5f4-104">The [Type Library Exporter tool](../../tools/tlbexp-exe-type-library-exporter.md) (Tlbexp.exe) loads a dynamic link library named TlbRef.dll.</span></span> <span data-ttu-id="2e5f4-105">此 DLL 包含两个 helper 函数和导出程序工具在程序集到类型库转换过程中使用的接口。</span><span class="sxs-lookup"><span data-stu-id="2e5f4-105">This DLL contains two helper functions and an interface that the exporter tool uses during the assembly-to-type-library conversion process.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2e5f4-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="2e5f4-106">In This Section</span></span>  

 [<span data-ttu-id="2e5f4-107">GetTypeLibInfo 函数</span><span class="sxs-lookup"><span data-stu-id="2e5f4-107">GetTypeLibInfo Function</span></span>](gettypelibinfo-function.md)  
 <span data-ttu-id="2e5f4-108">提供类型库的本地化和操作系统信息。</span><span class="sxs-lookup"><span data-stu-id="2e5f4-108">Provides localization and operating system information for a type library.</span></span>  
  
 [<span data-ttu-id="2e5f4-109">LoadTypeLibWithResolver 函数</span><span class="sxs-lookup"><span data-stu-id="2e5f4-109">LoadTypeLibWithResolver Function</span></span>](loadtypelibwithresolver-function.md)  
 <span data-ttu-id="2e5f4-110">通过使用 [ITypeLibResolver 接口](itypelibresolver-interface.md)的实现来加载类型库，以解析任何引用的类型库。</span><span class="sxs-lookup"><span data-stu-id="2e5f4-110">Loads a type library by using an implementation of the [ITypeLibResolver interface](itypelibresolver-interface.md) to resolve any referenced type libraries.</span></span>  
  
 [<span data-ttu-id="2e5f4-111">ITypeLibResolver 接口</span><span class="sxs-lookup"><span data-stu-id="2e5f4-111">ITypeLibResolver Interface</span></span>](itypelibresolver-interface.md)  
 <span data-ttu-id="2e5f4-112">提供 [ResolveTypeLib 方法](resolvetypelib-method.md)，这会返回一个类型库的完全限定的路径。</span><span class="sxs-lookup"><span data-stu-id="2e5f4-112">Provides the [ResolveTypeLib method](resolvetypelib-method.md), which returns the fully qualified path of a type library.</span></span>
