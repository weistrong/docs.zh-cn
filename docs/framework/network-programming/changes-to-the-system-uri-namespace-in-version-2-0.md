---
description: 详细了解：对 2.0 版中的 System.Uri 命名空间的更改
title: 对 2.0 版中的 System.Uri 命名空间的更改
ms.date: 03/30/2017
ms.assetid: 35883fe9-2d09-4d8b-80ca-cf23a941e459
ms.openlocfilehash: 8b5e2f2b3b59fba96e20e40a4df18273a2f6034f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791616"
---
# <a name="changes-to-the-systemuri-namespace-in-version-20"></a><span data-ttu-id="41bfb-103">对 2.0 版中的 System.Uri 命名空间的更改</span><span class="sxs-lookup"><span data-stu-id="41bfb-103">Changes to the System.Uri namespace in version 2.0</span></span>

<span data-ttu-id="41bfb-104">对 <xref:System.Uri?displayProperty=nameWithType> 类进行了少量更改。</span><span class="sxs-lookup"><span data-stu-id="41bfb-104">Several changes were made to the <xref:System.Uri?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="41bfb-105">这些更改修复了不正确的行为、提高了可用性、增强了安全性。</span><span class="sxs-lookup"><span data-stu-id="41bfb-105">These changes fixed incorrect behavior, enhanced usability, and enhanced security.</span></span>

## <a name="obsolete-and-deprecated-members"></a><span data-ttu-id="41bfb-106">已过时和弃用的成员</span><span class="sxs-lookup"><span data-stu-id="41bfb-106">Obsolete and deprecated Members</span></span>

 <span data-ttu-id="41bfb-107">构造函数：</span><span class="sxs-lookup"><span data-stu-id="41bfb-107">Constructors:</span></span>

- <span data-ttu-id="41bfb-108">所有具有 `dontEscape` 参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="41bfb-108">All constructors that have a `dontEscape` parameter.</span></span>

 <span data-ttu-id="41bfb-109">方法：</span><span class="sxs-lookup"><span data-stu-id="41bfb-109">Methods:</span></span>

- <xref:System.Uri.CheckSecurity%2A>

- <xref:System.Uri.Escape%2A>

- <xref:System.Uri.Canonicalize%2A>

- <xref:System.Uri.Parse%2A>

- <xref:System.Uri.IsReservedCharacter%2A>

- <xref:System.Uri.IsBadFileSystemCharacter%2A>

- <xref:System.Uri.IsExcludedCharacter%2A>

- <xref:System.Uri.EscapeString%2A>

## <a name="changes"></a><span data-ttu-id="41bfb-110">更改</span><span class="sxs-lookup"><span data-stu-id="41bfb-110">Changes</span></span>

- <span data-ttu-id="41bfb-111">对于已知不含有查询部件（文件、ftp 等）的 URI 方案，“?”字符始终转义，不将它视为 <xref:System.Uri.Query%2A> 部件的开头。</span><span class="sxs-lookup"><span data-stu-id="41bfb-111">For URI schemes that are known to not have a query part (file, ftp, and others), the '?' character is always escaped and is not considered the beginning of a <xref:System.Uri.Query%2A> part.</span></span>

- <span data-ttu-id="41bfb-112">对于隐式文件 URI（采用 `c:\directory\file@name.txt` 形式），片段字符（“#”）始终转义，除非要求完全反转义或 <xref:System.Uri.LocalPath%2A> 为 `true`。</span><span class="sxs-lookup"><span data-stu-id="41bfb-112">For implicit file URIs (of the form `c:\directory\file@name.txt`), the fragment character ('#') is always escaped unless full unescaping is requested or <xref:System.Uri.LocalPath%2A> is `true`.</span></span>

- <span data-ttu-id="41bfb-113">删除了 UNC 主机名支持；采用了 IDN 规范来表示国际主机名。</span><span class="sxs-lookup"><span data-stu-id="41bfb-113">UNC hostname support was removed; the IDN specification for representing international hostnames was adopted.</span></span>

- <span data-ttu-id="41bfb-114"><xref:System.Uri.LocalPath%2A> 始终返回完全反转义的字符串。</span><span class="sxs-lookup"><span data-stu-id="41bfb-114"><xref:System.Uri.LocalPath%2A> always returns a completely unescaped string.</span></span>

- <span data-ttu-id="41bfb-115"><xref:System.Uri.ToString%2A> 不反转义已转义的 %、? 或 # 字符。</span><span class="sxs-lookup"><span data-stu-id="41bfb-115"><xref:System.Uri.ToString%2A> does not unescape an escaped '%', '?', or '#' character.</span></span>

- <span data-ttu-id="41bfb-116"><xref:System.Uri.Equals%2A> 在相等性检查现在包含 <xref:System.Uri.Query%2A> 部件。</span><span class="sxs-lookup"><span data-stu-id="41bfb-116"><xref:System.Uri.Equals%2A> now includes the <xref:System.Uri.Query%2A> part in the equality check.</span></span>

- <span data-ttu-id="41bfb-117">运算符 == 和 != 已重写并链接到 <xref:System.Uri.Equals%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="41bfb-117">Operators "==" and "!=" are overridden and linked to the <xref:System.Uri.Equals%2A> method.</span></span>

- <span data-ttu-id="41bfb-118"><xref:System.Uri.IsLoopback%2A> 现在产生一致的结果。</span><span class="sxs-lookup"><span data-stu-id="41bfb-118"><xref:System.Uri.IsLoopback%2A> now produces consistent results.</span></span>

- <span data-ttu-id="41bfb-119">URI“`file:///path`”不再转换为 `file://path`。</span><span class="sxs-lookup"><span data-stu-id="41bfb-119">The URI "`file:///path`" is no longer translated into `file://path`.</span></span>

- <span data-ttu-id="41bfb-120">现在，“#”被识别为主机名终止符。</span><span class="sxs-lookup"><span data-stu-id="41bfb-120">"#" is now recognized as a host name terminator.</span></span> <span data-ttu-id="41bfb-121">即，`http://contoso.com#fragment` 现在转换为 `http://contoso.com/#fragment`。</span><span class="sxs-lookup"><span data-stu-id="41bfb-121">That is, `http://contoso.com#fragment` is now converted to `http://contoso.com/#fragment`.</span></span>

- <span data-ttu-id="41bfb-122">结合基 URI 与片段时的 bug 已修复。</span><span class="sxs-lookup"><span data-stu-id="41bfb-122">A bug when combining a base URI with a fragment has been fixed.</span></span>

- <span data-ttu-id="41bfb-123"><xref:System.Uri.HostNameType%2A> 中的 bug 已修复。</span><span class="sxs-lookup"><span data-stu-id="41bfb-123">A bug in <xref:System.Uri.HostNameType%2A> is fixed.</span></span>

- <span data-ttu-id="41bfb-124">NNTP 分析中的 bug 已修复。</span><span class="sxs-lookup"><span data-stu-id="41bfb-124">A bug in NNTP parsing is fixed.</span></span>

- <span data-ttu-id="41bfb-125">HTTP:contoso.com 形式的 URI 现引发分析异常。</span><span class="sxs-lookup"><span data-stu-id="41bfb-125">A URI of the form HTTP:contoso.com now throws a parsing exception.</span></span>

- <span data-ttu-id="41bfb-126">Framework 正确处理 URI 中的用户信息。</span><span class="sxs-lookup"><span data-stu-id="41bfb-126">The Framework correctly handles userinfo in a URI.</span></span>

- <span data-ttu-id="41bfb-127">URI 路径压缩已修复，所以断开的 URI 不能遍历根以上的文件系统。</span><span class="sxs-lookup"><span data-stu-id="41bfb-127">URI path compression is fixed so that a broken URI cannot traverse the file system above the root.</span></span>

## <a name="see-also"></a><span data-ttu-id="41bfb-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41bfb-128">See also</span></span>

- <xref:System.Uri?displayProperty=nameWithType>
