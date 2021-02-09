---
description: 详细了解：访问用户数据 (Visual Basic)
title: 访问用户数据
ms.date: 07/20/2015
helpviewer_keywords:
- domain names [Visual Basic], retrieving
- data [Visual Basic], accessing user data
- My.User object [Visual Basic], tasks
- user data [Visual Basic], domain
- user names [Visual Basic], retrieving
- user data [Visual Basic], accessing
- login names [Visual Basic]
- examples [Visual Basic], accessing user data
ms.assetid: 32492a15-ee59-4a63-a1f1-9b24cc13140a
ms.openlocfilehash: 4f7f7a8cb121b74a2680f29c0aa14491f6e38434
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797869"
---
# <a name="accessing-user-data-visual-basic"></a><span data-ttu-id="7b5c8-103">访问用户数据 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7b5c8-103">Accessing User Data (Visual Basic)</span></span>

<span data-ttu-id="7b5c8-104">本部分包含有关处理 `My.User` 对象的主题以及可通过该操作完成的任务。</span><span class="sxs-lookup"><span data-stu-id="7b5c8-104">This section contains topics dealing with the `My.User` object and tasks that you can accomplish with it.</span></span>  
  
 <span data-ttu-id="7b5c8-105">`My.User` 对象通过返回实现 <xref:System.Security.Principal.IPrincipal> 接口的对象，提供有关登录用户的信息的访问权限。</span><span class="sxs-lookup"><span data-stu-id="7b5c8-105">The `My.User` object provides access to information about the logged-on user by returning an object that implements the <xref:System.Security.Principal.IPrincipal> interface.</span></span>  
  
## <a name="tasks"></a><span data-ttu-id="7b5c8-106">任务</span><span class="sxs-lookup"><span data-stu-id="7b5c8-106">Tasks</span></span>  
  
|<span data-ttu-id="7b5c8-107">功能</span><span class="sxs-lookup"><span data-stu-id="7b5c8-107">To</span></span>|<span data-ttu-id="7b5c8-108">查看</span><span class="sxs-lookup"><span data-stu-id="7b5c8-108">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="7b5c8-109">获取用户的登录名</span><span class="sxs-lookup"><span data-stu-id="7b5c8-109">Get the user's login name</span></span>|<xref:Microsoft.VisualBasic.ApplicationServices.User.Name%2A>|  
|<span data-ttu-id="7b5c8-110">如果应用程序使用 Windows 身份验证，则获取用户的域名</span><span class="sxs-lookup"><span data-stu-id="7b5c8-110">Get the user's domain name, if the application uses Windows authentication</span></span>|<xref:Microsoft.VisualBasic.ApplicationServices.User.CurrentPrincipal>|  
|<span data-ttu-id="7b5c8-111">确定用户的角色</span><span class="sxs-lookup"><span data-stu-id="7b5c8-111">Determine the user's role</span></span>|<xref:Microsoft.VisualBasic.ApplicationServices.User.IsInRole%2A>|  
  
## <a name="see-also"></a><span data-ttu-id="7b5c8-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b5c8-112">See also</span></span>

- <xref:Microsoft.VisualBasic.ApplicationServices.User>
