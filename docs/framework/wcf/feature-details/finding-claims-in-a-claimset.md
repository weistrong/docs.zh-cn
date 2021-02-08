---
description: 了解详细信息：在 ClaimSet 中查找声明
title: 在 ClaimSet 中查找声明
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- claims [WCF], finding in a claimset
- claims [WCF]
ms.assetid: a76ce107-aeb3-47d0-bfa9-134c53664e20
ms.openlocfilehash: 3ac4553e50f98f54e0a23aa9d759d7ae2f7caa8c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802926"
---
# <a name="finding-claims-in-a-claimset"></a><span data-ttu-id="08375-103">在 ClaimSet 中查找声明</span><span class="sxs-lookup"><span data-stu-id="08375-103">Finding Claims in a ClaimSet</span></span>

<span data-ttu-id="08375-104">在使用基于声明的授权时，一项常见任务就是检查 <xref:System.IdentityModel.Claims.ClaimSet> 的内容以查找特定类型的声明。</span><span class="sxs-lookup"><span data-stu-id="08375-104">Examining the content of a <xref:System.IdentityModel.Claims.ClaimSet> for particular types of claims is a common task when using claim-based authorization.</span></span> <span data-ttu-id="08375-105">若要检查 <xref:System.IdentityModel.Claims.ClaimSet> 以查找是否存在特定声明，请使用 <xref:System.IdentityModel.Claims.ClaimSet.FindClaims%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="08375-105">To examine a <xref:System.IdentityModel.Claims.ClaimSet> for the presence of particular claims, use the <xref:System.IdentityModel.Claims.ClaimSet.FindClaims%2A> method.</span></span> <span data-ttu-id="08375-106">相对于直接在 <xref:System.IdentityModel.Claims.ClaimSet> 上循环，该方法可以提供更好的性能。</span><span class="sxs-lookup"><span data-stu-id="08375-106">This method provides better performance than iterating directly over the <xref:System.IdentityModel.Claims.ClaimSet>.</span></span> <span data-ttu-id="08375-107">下面的示例演示此用法。</span><span class="sxs-lookup"><span data-stu-id="08375-107">The following example demonstrates this usage.</span></span> <span data-ttu-id="08375-108">请注意，`claimType` 和 `claimRight` 参数可以为 `null`。</span><span class="sxs-lookup"><span data-stu-id="08375-108">Note that the `claimType` and `claimRight` parameters can be `null`.</span></span> <span data-ttu-id="08375-109">在此例中，这些参数将与所有声明类型以及声明权限相匹配。</span><span class="sxs-lookup"><span data-stu-id="08375-109">In that case, the parameters will match all claim types and claim rights.</span></span>  
  
## <a name="example"></a><span data-ttu-id="08375-110">示例</span><span class="sxs-lookup"><span data-stu-id="08375-110">Example</span></span>  

 [!code-csharp[c_FindClaimsPerf#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_findclaimsperf/cs/c_findclaimsperf.cs#2)]
 [!code-vb[c_FindClaimsPerf#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_findclaimsperf/vb/c_findclaimsperf.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="08375-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="08375-111">See also</span></span>

- [<span data-ttu-id="08375-112">使用标识模型管理声明和授权</span><span class="sxs-lookup"><span data-stu-id="08375-112">Managing Claims and Authorization with the Identity Model</span></span>](managing-claims-and-authorization-with-the-identity-model.md)
