---
description: '了解详细信息： <socket> 元素 (网络设置) '
title: <socket> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/socket
- http://schemas.microsoft.com/.NetConfiguration/v2.0#socket
helpviewer_keywords:
- <socket> element
- socket element
ms.assetid: 366c634c-7d16-478f-aedf-053eda94a1a0
ms.openlocfilehash: 564d6566bf6f6b1997b986cb6c0d85f841195e55
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740127"
---
# <a name="socket-element-network-settings"></a><span data-ttu-id="1efa0-103">\<socket> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="1efa0-103">\<socket> Element (Network Settings)</span></span>

<span data-ttu-id="1efa0-104">指定套接字操作是否使用完成端口。</span><span class="sxs-lookup"><span data-stu-id="1efa0-104">Specifies whether socket operations use completion ports.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<settings>**](settings-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<socket>**

## <a name="syntax"></a><span data-ttu-id="1efa0-105">语法</span><span class="sxs-lookup"><span data-stu-id="1efa0-105">Syntax</span></span>  
  
```xml  
<socket  
  alwaysUseCompletionPortsForConnect="true|false"  
  alwaysUseCompletionPortsForAccept="true|false"  
  ipProtectionLevel="EdgeRestricted|Restricted|Unrestricted|Unspecified"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1efa0-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1efa0-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1efa0-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1efa0-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1efa0-108">特性</span><span class="sxs-lookup"><span data-stu-id="1efa0-108">Attributes</span></span>  
  
|<span data-ttu-id="1efa0-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1efa0-109">**Attribute**</span></span>|<span data-ttu-id="1efa0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1efa0-110">**Description**</span></span>|  
|-------------------|---------------------|  
|`alwaysUseCompletionPortsForAccept`|<span data-ttu-id="1efa0-111">指示套接字是否应始终对接受方法调用使用完成端口。</span><span class="sxs-lookup"><span data-stu-id="1efa0-111">Indicates whether the socket should always use completion ports for Accept method calls.</span></span> <span data-ttu-id="1efa0-112">默认值是 `false`。</span><span class="sxs-lookup"><span data-stu-id="1efa0-112">The default value is `false`.</span></span>|  
|`alwaysUseCompletionPortsForConnect`|<span data-ttu-id="1efa0-113">指示套接字是否应始终对连接方法调用使用完成端口。</span><span class="sxs-lookup"><span data-stu-id="1efa0-113">Indicates whether the socket should always use completion ports for Connect method calls.</span></span> <span data-ttu-id="1efa0-114">默认值是 `false`。</span><span class="sxs-lookup"><span data-stu-id="1efa0-114">The default value is `false`.</span></span>|  
|`ipProtectionLevel`|<span data-ttu-id="1efa0-115">指定要用于 <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> 套接字的默认。</span><span class="sxs-lookup"><span data-stu-id="1efa0-115">Specifies the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> to use for a socket.</span></span> <span data-ttu-id="1efa0-116">默认值取决于 Windows 的版本。</span><span class="sxs-lookup"><span data-stu-id="1efa0-116">The default value depends on the version of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1efa0-117">子元素</span><span class="sxs-lookup"><span data-stu-id="1efa0-117">Child Elements</span></span>  

 <span data-ttu-id="1efa0-118">无。</span><span class="sxs-lookup"><span data-stu-id="1efa0-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1efa0-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1efa0-119">Parent Elements</span></span>  
  
|<span data-ttu-id="1efa0-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="1efa0-120">**Element**</span></span>|<span data-ttu-id="1efa0-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1efa0-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="1efa0-122">设置</span><span class="sxs-lookup"><span data-stu-id="1efa0-122">settings</span></span>](settings-element-network-settings.md)|<span data-ttu-id="1efa0-123">配置 <xref:System.Net> 命名空间的基本网络选项。</span><span class="sxs-lookup"><span data-stu-id="1efa0-123">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1efa0-124">备注</span><span class="sxs-lookup"><span data-stu-id="1efa0-124">Remarks</span></span>  

 <span data-ttu-id="1efa0-125">`alwaysUseCompletionPortsForAccept` 和 `alwaysUseCompletionPortsForConnect` 特性用于指定 <xref:System.Net.Sockets?displayProperty=nameWithType>.namespace 中的类在使用完全端口时的默认行为。</span><span class="sxs-lookup"><span data-stu-id="1efa0-125">The `alwaysUseCompletionPortsForAccept` and `alwaysUseCompletionPortsForConnect` attributes are used to specify the default behavior regarding the use of completion ports by the classes in the <xref:System.Net.Sockets?displayProperty=nameWithType>.namespace.</span></span> <span data-ttu-id="1efa0-126">对于高性能服务器应用程序，建议使用完成端口。</span><span class="sxs-lookup"><span data-stu-id="1efa0-126">Completion ports are recommended for high performance server applications.</span></span>  
  
 <span data-ttu-id="1efa0-127">和特性的默认值 `alwaysUseCompletionPortsForAccept` `alwaysUseCompletionPortsForConnect` 为 **false**。</span><span class="sxs-lookup"><span data-stu-id="1efa0-127">The default value for the `alwaysUseCompletionPortsForAccept` and `alwaysUseCompletionPortsForConnect` attributes is **false**.</span></span>  
  
 <span data-ttu-id="1efa0-128"><xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForAccept%2A>可用于 `alwaysUseCompletionPortsForAccept` 从适用的配置文件中获取特性的当前值。</span><span class="sxs-lookup"><span data-stu-id="1efa0-128">The <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForAccept%2A> can be used to get the current value of the `alwaysUseCompletionPortsForAccept` attribute from applicable configuration files.</span></span> <span data-ttu-id="1efa0-129"><xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForConnect%2A>可用于 `alwaysUseCompletionPortsForConnect` 从适用的配置文件中获取特性的当前值。</span><span class="sxs-lookup"><span data-stu-id="1efa0-129">The <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForConnect%2A> can be used to get the current value of the `alwaysUseCompletionPortsForConnect` attribute from applicable configuration files.</span></span>  
  
 <span data-ttu-id="1efa0-130">`ipProtectionLevel`特性指定 <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> 要用于套接字的默认。</span><span class="sxs-lookup"><span data-stu-id="1efa0-130">The `ipProtectionLevel` attribute specifies the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> to use for a socket.</span></span> <span data-ttu-id="1efa0-131"><xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A>属性允许将 IPv6 套接字的限制配置为指定的作用域，如具有相同的链接本地或站点本地前缀的地址。</span><span class="sxs-lookup"><span data-stu-id="1efa0-131">The <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> property enables configuration of a restriction for an IPv6 socket to a specified scope, such as addresses with the same link local or site local prefix.</span></span> <span data-ttu-id="1efa0-132">此选项使应用程序可以对 IPv6 套接字设置访问限制。</span><span class="sxs-lookup"><span data-stu-id="1efa0-132">This option enables applications to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="1efa0-133">通过应用此类限制，可让在专用局域网上运行的应用程序能够通过简单的方式很好地增强自身的安全性，以便防范外部攻击。</span><span class="sxs-lookup"><span data-stu-id="1efa0-133">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="1efa0-134">此选项扩大或缩小侦听套接字的范围，在适当的时候启用从公共用户和私有用户进行的不受限制的访问，或根据需要限制对同一站点的访问。</span><span class="sxs-lookup"><span data-stu-id="1efa0-134">This option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>  
  
 <span data-ttu-id="1efa0-135">此 `ipProtectionLevel` 属性设置只影响初始传入流量：</span><span class="sxs-lookup"><span data-stu-id="1efa0-135">This `ipProtectionLevel` attribute setting affects only initial incoming traffic:</span></span>  
  
- <span data-ttu-id="1efa0-136">在套接字上侦听传入连接的 TCP 服务器。</span><span class="sxs-lookup"><span data-stu-id="1efa0-136">A TCP server listening for incoming connections on a socket.</span></span>  
  
- <span data-ttu-id="1efa0-137">在套接字上接收数据包的 UDP 应用程序。</span><span class="sxs-lookup"><span data-stu-id="1efa0-137">A UDP application receiving a packet on a socket.</span></span>  
  
 <span data-ttu-id="1efa0-138">此配置设置不会影响已建立的 TCP 连接 (流量在两个方向上都不受限制) 并且不会影响应用程序发送 UDP 数据包。</span><span class="sxs-lookup"><span data-stu-id="1efa0-138">This configuration setting does not affect already established TCP connections (traffic is unrestricted in both directions) and does not affect an application sending UDP packets.</span></span>  
  
 <span data-ttu-id="1efa0-139">属性设置的可能值与 `ipProtectionLevel` 枚举中指定的已定义保护级别相对应，如下所示 <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> ：</span><span class="sxs-lookup"><span data-stu-id="1efa0-139">The possible values for the `ipProtectionLevel` attribute setting correspond with the defined protection levels specified in the <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> enumeration as follows:</span></span>  
  
|<span data-ttu-id="1efa0-140">**特性值**</span><span class="sxs-lookup"><span data-stu-id="1efa0-140">**Attribute Value**</span></span>|<span data-ttu-id="1efa0-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="1efa0-141">**Description**</span></span>|  
|-|-|  
|<span data-ttu-id="1efa0-142">EdgeRestricted</span><span class="sxs-lookup"><span data-stu-id="1efa0-142">EdgeRestricted</span></span>|<span data-ttu-id="1efa0-143">IP 保护级别是“边缘受限的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-143">The IP protection level is edge restricted.</span></span> <span data-ttu-id="1efa0-144">此值应由设计为在 Internet 上运行的应用程序使用。</span><span class="sxs-lookup"><span data-stu-id="1efa0-144">This value would be used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="1efa0-145">此设置不允许使用 Windows Teredo 实现的网络地址转换 (NAT) 遍历。</span><span class="sxs-lookup"><span data-stu-id="1efa0-145">This setting does not allow Network Address Translation (NAT) traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="1efa0-146">这些应用程序可能会绕过 IPv4 防火墙，因此，必须加强应用程序的安全性以防范针对开放端口的 Internet 攻击。</span><span class="sxs-lookup"><span data-stu-id="1efa0-146">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span> <span data-ttu-id="1efa0-147">在 Windows Server 2003 和 Windows XP 中，针对套接字的 IP 保护级别的默认值是“边缘受限的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-147">On Windows Server 2003 and Windows XP, the default value for the IP Protection level on a socket is edge restricted.</span></span>|  
|<span data-ttu-id="1efa0-148">受限制</span><span class="sxs-lookup"><span data-stu-id="1efa0-148">Restricted</span></span>|<span data-ttu-id="1efa0-149">IP 保护级别是“受限的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-149">The IP protection level is restricted.</span></span> <span data-ttu-id="1efa0-150">此值应由未实现 Internet 方案的 Intranet 应用程序使用。</span><span class="sxs-lookup"><span data-stu-id="1efa0-150">This value would be used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="1efa0-151">一般情况下，不会针对 Internet 样式的攻击来对这些应用程序进行测试或加强安全性。</span><span class="sxs-lookup"><span data-stu-id="1efa0-151">These applications are generally not tested or hardened against Internet-style attacks.</span></span> <span data-ttu-id="1efa0-152">此设置将限制仅接收链接本地的通信。</span><span class="sxs-lookup"><span data-stu-id="1efa0-152">This setting will limit the received traffic to link-local only.</span></span>|  
|<span data-ttu-id="1efa0-153">非受限</span><span class="sxs-lookup"><span data-stu-id="1efa0-153">Unrestricted</span></span>|<span data-ttu-id="1efa0-154">IP 保护级别是“不受限的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-154">The IP protection level is unrestricted.</span></span> <span data-ttu-id="1efa0-155">此值应由设计为在 Internet 上运行的应用程序使用，包括利用 Windows 中内置的 IPv6 NAT 遍历功能（例如，Teredo）的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1efa0-155">This value would be used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="1efa0-156">这些应用程序可能会绕过 IPv4 防火墙，因此，必须加强应用程序的安全性以防范针对开放端口的 Internet 攻击。</span><span class="sxs-lookup"><span data-stu-id="1efa0-156">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span> <span data-ttu-id="1efa0-157">在 Windows Server 2008 R2 和 Windows Vista 中，针对套接字的 IP 保护级别的默认值是“不受限的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-157">On Windows Server 2008 R2 and Windows Vista, the default value for the IP Protection level on a socket is unrestricted.</span></span>|  
|<span data-ttu-id="1efa0-158">未指定</span><span class="sxs-lookup"><span data-stu-id="1efa0-158">Unspecified</span></span>|<span data-ttu-id="1efa0-159">IP 保护级别是“未指定的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-159">The IP protection level is unspecified.</span></span> <span data-ttu-id="1efa0-160">在 Windows 7 和 Windows Server 2008 R2 中，针对套接字的 IP 保护级别的默认值是“未指定的”。</span><span class="sxs-lookup"><span data-stu-id="1efa0-160">On Windows 7 and Windows Server 2008 R2, the default value for the IP Protection level on a socket is unspecified.</span></span>|  
  
 <span data-ttu-id="1efa0-161">`ipProtectionLevel`**未指定** 该属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="1efa0-161">The default value for the `ipProtectionLevel` attribute is **Unspecified**.</span></span>  
  
 <span data-ttu-id="1efa0-162"><xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A>属性可用于 `ipProtectionLevel` 从适用的配置文件中获取特性的当前值。</span><span class="sxs-lookup"><span data-stu-id="1efa0-162">The <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> property can be used to get the current value of the `ipProtectionLevel` attribute from applicable configuration files.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="1efa0-163">配置文件</span><span class="sxs-lookup"><span data-stu-id="1efa0-163">Configuration Files</span></span>  

 <span data-ttu-id="1efa0-164">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="1efa0-164">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1efa0-165">示例</span><span class="sxs-lookup"><span data-stu-id="1efa0-165">Example</span></span>  

 <span data-ttu-id="1efa0-166">下面的示例演示如何指定应使用完成端口，并且默认值 <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> 应为 "无限制"。</span><span class="sxs-lookup"><span data-stu-id="1efa0-166">The following example shows how to specify that completion ports should be used and that the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> should be unrestricted.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <socket  
        alwaysUseCompletionPortsForAccept="true"  
        alwaysUseCompletionPortsForConnect="true"  
        ipProtectionLevel="Unrestricted"  
       />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1efa0-167">请参阅</span><span class="sxs-lookup"><span data-stu-id="1efa0-167">See also</span></span>

- <xref:System.Net?displayProperty=nameWithType>
- <xref:System.Net.Configuration.SocketElement?displayProperty=nameWithType>
- <xref:System.Net.Sockets?displayProperty=nameWithType>
- <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType>
- <xref:System.Net.Sockets.SocketOptionName.IPProtectionLevel?displayProperty=nameWithType>
- [<span data-ttu-id="1efa0-168">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="1efa0-168">Network Settings Schema</span></span>](index.md)
