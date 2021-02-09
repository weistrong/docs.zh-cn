---
description: 详细了解：读取和写入注册表 (Visual Basic)
title: 读取和写入注册表
ms.date: 07/20/2015
helpviewer_keywords:
- My.Computer.Registry object, tasks
- registry [Visual Basic], writing to
- registry [Visual Basic], reading
ms.assetid: a13da106-185b-41d7-b23c-416da65e21e4
ms.openlocfilehash: 0a9e32480845e617f6e4fde2f31c58eea8da4ee7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701542"
---
# <a name="reading-from-and-writing-to-the-registry-visual-basic"></a><span data-ttu-id="f640d-103">读取和写入注册表 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f640d-103">Reading from and Writing to the Registry (Visual Basic)</span></span>

<span data-ttu-id="f640d-104">本主题介绍与注册表相关的任务和概念性主题。</span><span class="sxs-lookup"><span data-stu-id="f640d-104">This topic describes task and conceptual topics that are associated with the registry.</span></span>  
  
 <span data-ttu-id="f640d-105">在 Visual Basic 中编程时，可以通过 Visual Basic 提供的函数或者通过 .NET 的注册表类访问注册表。</span><span class="sxs-lookup"><span data-stu-id="f640d-105">When programming in Visual Basic, you can choose to access the registry by means of either the functions provided by Visual Basic or the registry classes of .NET.</span></span> <span data-ttu-id="f640d-106">注册表托管有关操作系统的信息，以及有关计算机上托管的应用程序的信息。</span><span class="sxs-lookup"><span data-stu-id="f640d-106">The registry hosts information from the operating system as well as information from applications hosted on the machine.</span></span> <span data-ttu-id="f640d-107">对注册表进行操作时，如果允许对系统资源或受保护的信息进行不适当的访问，则可能会降低安全性。</span><span class="sxs-lookup"><span data-stu-id="f640d-107">Working with the registry may compromise security by allowing inappropriate access to system resources or protected information.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f640d-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="f640d-108">In This Section</span></span>  

 [<span data-ttu-id="f640d-109">如何：创建注册表项并设置其值</span><span class="sxs-lookup"><span data-stu-id="f640d-109">How to: Create a Registry Key and Set Its Value</span></span>](how-to-create-a-registry-key-and-set-its-value.md)  
 <span data-ttu-id="f640d-110">介绍如何使用 `My.Computer.Registry` 对象的 `CreateSubKey` 和 `SetValue` 方法创建注册表项并设置其值。</span><span class="sxs-lookup"><span data-stu-id="f640d-110">Describes how to use the `CreateSubKey` and `SetValue` methods of the `My.Computer.Registry` object to create a registry key and set its value.</span></span>  
  
 [<span data-ttu-id="f640d-111">如何：从注册表项读取值</span><span class="sxs-lookup"><span data-stu-id="f640d-111">How to: Read a Value from a Registry Key</span></span>](how-to-read-a-value-from-a-registry-key.md)  
 <span data-ttu-id="f640d-112">介绍如何使用 `My.Computer.Registry` 对象的 `GetValue` 方法读取注册表项的值。</span><span class="sxs-lookup"><span data-stu-id="f640d-112">Describes how to use the `GetValue` method of the `My.Computer.Registry` object to read a value from a registry key.</span></span>  
  
 [<span data-ttu-id="f640d-113">如何：删除注册表项</span><span class="sxs-lookup"><span data-stu-id="f640d-113">How to: Delete a Registry Key</span></span>](how-to-delete-a-registry-key.md)  
 <span data-ttu-id="f640d-114">介绍如何使用 `My.Computer.Registry.CurrentUser` 属性的 `DeleteSubKey` 方法删除注册表项。</span><span class="sxs-lookup"><span data-stu-id="f640d-114">Describes how to use the `DeleteSubKey` method of the `My.Computer.Registry.CurrentUser` property to delete a registry key.</span></span>  
  
 [<span data-ttu-id="f640d-115">使用 Microsoft.Win32 命名空间读取和写入注册表</span><span class="sxs-lookup"><span data-stu-id="f640d-115">Reading from and Writing to the Registry Using the Microsoft.Win32 Namespace</span></span>](reading-from-and-writing-to-the-registry-using-the-microsoft-win32-namespace.md)  
 <span data-ttu-id="f640d-116">介绍如何使用 .NET 的 `Registry` 和 `RegistryKey` 类访问注册表。</span><span class="sxs-lookup"><span data-stu-id="f640d-116">Describes how to use the `Registry` and `RegistryKey` classes of .NET to access the registry.</span></span>  
  
 [<span data-ttu-id="f640d-117">安全性与注册表</span><span class="sxs-lookup"><span data-stu-id="f640d-117">Security and the Registry</span></span>](security-and-the-registry.md)  
 <span data-ttu-id="f640d-118">讨论与注册表相关的安全问题。</span><span class="sxs-lookup"><span data-stu-id="f640d-118">Discusses security issues involving the registry.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="f640d-119">相关章节</span><span class="sxs-lookup"><span data-stu-id="f640d-119">Related Sections</span></span>  

 <xref:Microsoft.VisualBasic.MyServices.RegistryProxy>  
 <span data-ttu-id="f640d-120">列出并说明 `My.Computer.Registry` 对象的成员。</span><span class="sxs-lookup"><span data-stu-id="f640d-120">Lists and explains members of the `My.Computer.Registry` object.</span></span>  
  
 <xref:Microsoft.Win32.Registry>  
 <span data-ttu-id="f640d-121">提供 `Registry` 类的概述和指向各个注册表项和成员的链接。</span><span class="sxs-lookup"><span data-stu-id="f640d-121">Presents an overview of the `Registry` class, along with links to individual keys and members.</span></span>
