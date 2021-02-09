---
description: 详细了解：操作说明：在 Visual Basic 中从注册表项中读取值
title: 如何：从注册表项读取值
ms.date: 07/20/2015
helpviewer_keywords:
- registry keys [Visual Basic], determining if a value exists in
- My.Computer.Registry object, examples
- registry [Visual Basic], determining if values exist
- registry keys [Visual Basic], reading from
- registry [Visual Basic], reading
ms.assetid: 775d0a57-68c9-464e-8949-9a39bd29cc64
ms.openlocfilehash: e062e40fe1c8876864e633079fc22e2c83cfb5d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797674"
---
# <a name="how-to-read-a-value-from-a-registry-key-in-visual-basic"></a><span data-ttu-id="c5428-103">如何：在 Visual Basic 中从注册表项中读取值</span><span class="sxs-lookup"><span data-stu-id="c5428-103">How to: Read a Value from a Registry Key in Visual Basic</span></span>

<span data-ttu-id="c5428-104">`My.Computer.Registry` 对象的 `GetValue` 方法可以用于读取 Windows 注册表中的值。</span><span class="sxs-lookup"><span data-stu-id="c5428-104">The `GetValue` method of the `My.Computer.Registry` object can be used to read values in the Windows registry.</span></span>  
  
 <span data-ttu-id="c5428-105">如果在下面的示例中，“Software\MyApp”项不存在，则引发异常。</span><span class="sxs-lookup"><span data-stu-id="c5428-105">If the key, "Software\MyApp" in the following example, does not exist, an exception is thrown.</span></span> <span data-ttu-id="c5428-106">如果在下面的示例中，`ValueName`“Name”不存在，则返回 `Nothing`。</span><span class="sxs-lookup"><span data-stu-id="c5428-106">If the `ValueName`,  "Name" in the following example, does not exist, `Nothing` is returned.</span></span>  
  
 <span data-ttu-id="c5428-107">`GetValue` 方法还可以用于确定特定注册表项中是否存在给定值。</span><span class="sxs-lookup"><span data-stu-id="c5428-107">The `GetValue` method can also be used to determine whether a given value exists in a specific registry key.</span></span>  
  
 <span data-ttu-id="c5428-108">代码从 Web 应用程序读取注册表时，当前用户取决于在 Web 应用程序中实现的身份验证和模拟。</span><span class="sxs-lookup"><span data-stu-id="c5428-108">When code reads the registry from a Web application, the current user is determined by the authentication and impersonation that is implemented in the Web application.</span></span>  
  
### <a name="to-read-a-value-from-a-registry-key"></a><span data-ttu-id="c5428-109">从注册表项读取值</span><span class="sxs-lookup"><span data-stu-id="c5428-109">To read a value from a registry key</span></span>  
  
- <span data-ttu-id="c5428-110">使用 `GetValue` 方法（指定路径和名称）可从注册表项读取值。</span><span class="sxs-lookup"><span data-stu-id="c5428-110">Use the `GetValue` method, specifying the path and name) to read a value from registry key.</span></span> <span data-ttu-id="c5428-111">下面的示例从 `HKEY_CURRENT_USER\Software\MyApp` 读取值 `Name` 并将它显示在消息框中。</span><span class="sxs-lookup"><span data-stu-id="c5428-111">The following example reads the value `Name` from `HKEY_CURRENT_USER\Software\MyApp` and displays it in a message box.</span></span>  
  
     [!code-vb[VbResourceTasks#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#4)]  
  
 <span data-ttu-id="c5428-112">此代码示例也可作为 IntelliSense 代码片段。</span><span class="sxs-lookup"><span data-stu-id="c5428-112">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="c5428-113">在代码片段选取器中，它位于“Windows 操作系统”>“注册表”中。</span><span class="sxs-lookup"><span data-stu-id="c5428-113">In the code snippet picker, it is located in **Windows Operating System > Registry**.</span></span> <span data-ttu-id="c5428-114">有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="c5428-114">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
### <a name="to-determine-whether-a-value-exists-in-a-registry-key"></a><span data-ttu-id="c5428-115">确定值是否存在于注册表项中</span><span class="sxs-lookup"><span data-stu-id="c5428-115">To determine whether a value exists in a registry key</span></span>  
  
- <span data-ttu-id="c5428-116">使用 `GetValue` 方法可检索值。</span><span class="sxs-lookup"><span data-stu-id="c5428-116">Use the `GetValue` method to retrieve the value.</span></span> <span data-ttu-id="c5428-117">下面的代码检查值是否存在并在它不存在时返回消息。</span><span class="sxs-lookup"><span data-stu-id="c5428-117">The following code checks whether the value exists and returns a message if it does not.</span></span>  
  
     [!code-vb[VbResourceTasks#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#12)]  
  
## <a name="robust-programming"></a><span data-ttu-id="c5428-118">可靠编程</span><span class="sxs-lookup"><span data-stu-id="c5428-118">Robust Programming</span></span>  

 <span data-ttu-id="c5428-119">注册表包含用于存储数据的顶层（或根）项。</span><span class="sxs-lookup"><span data-stu-id="c5428-119">The registry holds top-level, or root, keys that are used to store data.</span></span> <span data-ttu-id="c5428-120">例如，HKEY_LOCAL_MACHINE 根项用于存储所有用户使用的计算机级别设置，而 HKEY_CURRENT_USER 用于存储特定于单个用户的数据。</span><span class="sxs-lookup"><span data-stu-id="c5428-120">For instance, the HKEY_LOCAL_MACHINE root key is used for storing machine-level settings used by all users, while HKEY_CURRENT_USER is used for storing data specific to an individual user.</span></span>  
  
 <span data-ttu-id="c5428-121">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="c5428-121">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="c5428-122">密钥名称是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="c5428-122">The name of the key is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="c5428-123">用户没有从注册表项 (<xref:System.Security.SecurityException>) 进行读取的权限。</span><span class="sxs-lookup"><span data-stu-id="c5428-123">The user does not have permissions to read from registry keys (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="c5428-124">项名称超过 255 个字符的限制 (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="c5428-124">The key name exceeds the 255-character limit (<xref:System.ArgumentException>).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="c5428-125">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="c5428-125">.NET Framework Security</span></span>  

 <span data-ttu-id="c5428-126">若要运行此进程，程序集需要 <xref:System.Security.Permissions.RegistryPermission> 类授予的特权等级。</span><span class="sxs-lookup"><span data-stu-id="c5428-126">To run this process, your assembly requires a privilege level granted by the <xref:System.Security.Permissions.RegistryPermission> class.</span></span> <span data-ttu-id="c5428-127">如果在部分信任上下文中运行，该进程可能会因特权不足而引发异常。</span><span class="sxs-lookup"><span data-stu-id="c5428-127">If you are running in a partial-trust context, the process might throw an exception due to insufficient privileges.</span></span> <span data-ttu-id="c5428-128">同样，用户必须具有用于创建或写入设置的正确 ACL。</span><span class="sxs-lookup"><span data-stu-id="c5428-128">Similarly, the user must have the correct ACLs for creating or writing to settings.</span></span> <span data-ttu-id="c5428-129">例如，具有代码访问安全性权限的本地应用程序可能没有操作系统权限。</span><span class="sxs-lookup"><span data-stu-id="c5428-129">For example, a local application that has the code access security permission might not have operating system permission.</span></span> <span data-ttu-id="c5428-130">有关详细信息，请参阅 [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md)。</span><span class="sxs-lookup"><span data-stu-id="c5428-130">For more information, see [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5428-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5428-131">See also</span></span>

- <xref:Microsoft.VisualBasic.MyServices.RegistryProxy>
- <xref:Microsoft.Win32.RegistryHive>
- [<span data-ttu-id="c5428-132">读取和写入注册表</span><span class="sxs-lookup"><span data-stu-id="c5428-132">Reading from and Writing to the Registry</span></span>](reading-from-and-writing-to-the-registry.md)
