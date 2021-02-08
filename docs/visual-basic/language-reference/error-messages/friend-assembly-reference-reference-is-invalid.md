---
description: 了解详细信息： BC31535：友元程序集引用 <reference> 无效
title: 友元程序集引用 <reference> 无效
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: e3e08edede9bee4710c415a61592857229ea4f35
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796192"
---
# <a name="bc31535-friend-assembly-reference-reference-is-invalid"></a><span data-ttu-id="cab2f-103">BC31535：友元程序集引用 \<reference> 无效</span><span class="sxs-lookup"><span data-stu-id="cab2f-103">BC31535: Friend assembly reference \<reference> is invalid</span></span>

<span data-ttu-id="cab2f-104">友元程序集引用 \<reference> 无效。</span><span class="sxs-lookup"><span data-stu-id="cab2f-104">Friend assembly reference \<reference> is invalid.</span></span> <span data-ttu-id="cab2f-105">用强名称签名的程序集必须在他们的 InternalsVisibleTo 声明中指定一个公钥。</span><span class="sxs-lookup"><span data-stu-id="cab2f-105">Strong-name signed assemblies must specify a public key in their InternalsVisibleTo declarations.</span></span>

 <span data-ttu-id="cab2f-106">传递给特性构造函数的程序集名称 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> 标识强名称程序集，但不包括 `PublicKey` 特性。</span><span class="sxs-lookup"><span data-stu-id="cab2f-106">The assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor identifies a strong-named assembly, but it does not include a `PublicKey` attribute.</span></span>

 <span data-ttu-id="cab2f-107">**错误 ID：** BC31535</span><span class="sxs-lookup"><span data-stu-id="cab2f-107">**Error ID:** BC31535</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="cab2f-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="cab2f-108">To correct this error</span></span>

1. <span data-ttu-id="cab2f-109">确定强名称友元程序集的公钥。</span><span class="sxs-lookup"><span data-stu-id="cab2f-109">Determine the public key for the strong-named friend assembly.</span></span> <span data-ttu-id="cab2f-110">使用属性将公钥包含为传递给特性构造函数的程序集名称的一部分 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> `PublicKey` 。</span><span class="sxs-lookup"><span data-stu-id="cab2f-110">Include the public key as part of the assembly name passed to the <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> attribute constructor by using the `PublicKey` attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="cab2f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="cab2f-111">See also</span></span>

- <xref:System.Reflection.AssemblyName>
- [<span data-ttu-id="cab2f-112">友元程序集</span><span class="sxs-lookup"><span data-stu-id="cab2f-112">Friend Assemblies</span></span>](../../../standard/assembly/friend.md)
