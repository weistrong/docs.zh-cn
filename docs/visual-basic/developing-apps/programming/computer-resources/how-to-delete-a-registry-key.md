---
description: 详细了解：操作说明：在 Visual Basic 中删除注册表项
title: 如何：删除注册表项
ms.date: 07/20/2015
f1_keywords:
- vb.DeleteSetting
helpviewer_keywords:
- GetSetting function [Visual Basic]
- registry [Visual Basic], deleting values
- GetAllSettings function
- registry keys [Visual Basic], deleting
- registry [Visual Basic], deleting keys
- examples [Visual Basic], registry
ms.assetid: ab9aca0e-42b0-4ff7-8ff9-845a4bfdf9f2
ms.openlocfilehash: ca99855d30c2dd697c789bb4017429b906b3b63d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797713"
---
# <a name="how-to-delete-a-registry-key-in-visual-basic"></a><span data-ttu-id="b2975-103">如何：在 Visual Basic 中删除注册表项</span><span class="sxs-lookup"><span data-stu-id="b2975-103">How to: Delete a Registry Key in Visual Basic</span></span>

<span data-ttu-id="b2975-104"><xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%29> 和 <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%2CSystem.Boolean%29> 方法可以用于删除注册表项。</span><span class="sxs-lookup"><span data-stu-id="b2975-104">The <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%29> and <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%2CSystem.Boolean%29> methods can be used to delete registry keys.</span></span>  
  
## <a name="procedure"></a><span data-ttu-id="b2975-105">过程</span><span class="sxs-lookup"><span data-stu-id="b2975-105">Procedure</span></span>  
  
#### <a name="to-delete-a-registry-key"></a><span data-ttu-id="b2975-106">删除注册表项</span><span class="sxs-lookup"><span data-stu-id="b2975-106">To delete a registry key</span></span>  
  
- <span data-ttu-id="b2975-107">使用 `DeleteSubKey` 方法删除注册表项。</span><span class="sxs-lookup"><span data-stu-id="b2975-107">Use the `DeleteSubKey` method to delete a registry key.</span></span> <span data-ttu-id="b2975-108">此示例将删除 CurrentUser 配置单元中的软件/TestApp 项。</span><span class="sxs-lookup"><span data-stu-id="b2975-108">This example deletes the key Software/TestApp in the CurrentUser hive.</span></span> <span data-ttu-id="b2975-109">可在代码中更改为相应的字符串，或使它依赖于用户提供的信息。</span><span class="sxs-lookup"><span data-stu-id="b2975-109">You can change this in the code to the appropriate string, or have it rely on user-supplied information.</span></span>  
  
     [!code-vb[VbResourceTasks#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#19)]  
  
## <a name="robust-programming"></a><span data-ttu-id="b2975-110">可靠编程</span><span class="sxs-lookup"><span data-stu-id="b2975-110">Robust Programming</span></span>  

 <span data-ttu-id="b2975-111">如果键/值对不存在，`DeleteSubKey` 方法将返回一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="b2975-111">The `DeleteSubKey` method returns an empty string if the key/value pair does not exist.</span></span>  
  
 <span data-ttu-id="b2975-112">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="b2975-112">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="b2975-113">密钥名称是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="b2975-113">The name of the key is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="b2975-114">用户没有删除注册表项的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="b2975-114">The user does not have permissions to delete registry keys (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="b2975-115">项名称超过 255 个字符的限制 (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="b2975-115">The key name exceeds the 255-character limit (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="b2975-116">注册表项为只读 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="b2975-116">The registry key is read-only (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="b2975-117">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="b2975-117">.NET Framework Security</span></span>  

 <span data-ttu-id="b2975-118">如果未授予足够的运行时权限 (<xref:System.Security.Permissions.RegistryPermission>) 或用户没有用于创建或写入设置的适当访问权限（由 ACL 确定），则注册表调用将失败。</span><span class="sxs-lookup"><span data-stu-id="b2975-118">Registry calls fail if either sufficient run-time permissions are not granted (<xref:System.Security.Permissions.RegistryPermission>) or if the user does not have the correct access (as determined by the ACLs) for creating or writing to settings.</span></span> <span data-ttu-id="b2975-119">例如，具有代码访问安全性权限的本地应用程序可能没有操作系统权限。</span><span class="sxs-lookup"><span data-stu-id="b2975-119">For example, a local application that has the code access security permission might not have operating system permission.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2975-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2975-120">See also</span></span>

- <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%2A>
- <xref:Microsoft.Win32.RegistryKey>
- [<span data-ttu-id="b2975-121">安全性与注册表</span><span class="sxs-lookup"><span data-stu-id="b2975-121">Security and the Registry</span></span>](security-and-the-registry.md)
- [<span data-ttu-id="b2975-122">读取和写入注册表</span><span class="sxs-lookup"><span data-stu-id="b2975-122">Reading from and Writing to the Registry</span></span>](reading-from-and-writing-to-the-registry.md)
