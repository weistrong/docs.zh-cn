---
description: 了解详细信息：在联合方案中混合信任协议
title: 在联合方案中混合信任协议
ms.date: 03/30/2017
ms.assetid: d7b5fee9-2246-4b09-b8d7-9e63cb817279
ms.openlocfilehash: f882b3728ed791f611a9f71f32840e68d8e17a1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733718"
---
# <a name="mixing-trust-protocols-in-federated-scenarios"></a><span data-ttu-id="da4da-103">在联合方案中混合信任协议</span><span class="sxs-lookup"><span data-stu-id="da4da-103">Mixing Trust Protocols in Federated Scenarios</span></span>

<span data-ttu-id="da4da-104">联合客户端与服务进行通信时，有些服务的信任版本与安全令牌服务 (STS) 的信任版本不同。</span><span class="sxs-lookup"><span data-stu-id="da4da-104">There may be scenarios in which federated clients communicate with a service and a Security Token Service (STS) that do not have the same trust version.</span></span> <span data-ttu-id="da4da-105">服务 WSDL 包含的 `RequestSecurityTokenTemplate` 断言可能具有与 STS 不同版本的 WS-Trust 元素。</span><span class="sxs-lookup"><span data-stu-id="da4da-105">The service WSDL can contain a `RequestSecurityTokenTemplate` assertion with WS-Trust elements that are of different versions than the STS.</span></span> <span data-ttu-id="da4da-106">在这种情况下，Windows Communication Foundation (WCF) 客户端会转换从接收的 WS-Trust 元素， `RequestSecurityTokenTemplate` 以便与 STS 信任版本相匹配。</span><span class="sxs-lookup"><span data-stu-id="da4da-106">In such cases, a Windows Communication Foundation (WCF) client converts the WS-Trust elements received from the `RequestSecurityTokenTemplate` to match the STS trust version.</span></span> <span data-ttu-id="da4da-107">WCF 只处理标准绑定的不匹配信任版本。</span><span class="sxs-lookup"><span data-stu-id="da4da-107">WCF handles mismatched trust versions only for standard bindings.</span></span> <span data-ttu-id="da4da-108">WCF 识别的所有标准算法参数均为标准绑定的一部分。</span><span class="sxs-lookup"><span data-stu-id="da4da-108">All standard algorithm parameters that are recognized by WCF are part of the standard binding.</span></span> <span data-ttu-id="da4da-109">本主题介绍了在服务与 STS 之间具有各种信任设置的 WCF 行为。</span><span class="sxs-lookup"><span data-stu-id="da4da-109">This topic describes the WCF behavior with various trust settings between the service and the STS.</span></span>  
  
## <a name="rp-feb-2005-and-sts-feb-2005"></a><span data-ttu-id="da4da-110">RP Feb 2005 和 STS Feb 2005</span><span class="sxs-lookup"><span data-stu-id="da4da-110">RP Feb 2005 and STS Feb 2005</span></span>  

 <span data-ttu-id="da4da-111">依赖方 (RP) 的 WSDL 在 `RequestSecurityTokenTemplate` 节中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="da4da-111">The WSDL for Relying Party (RP) contains the following elements within the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
 <span data-ttu-id="da4da-112">客户端配置文件包含一个参数列表。</span><span class="sxs-lookup"><span data-stu-id="da4da-112">The client configuration file contains a list of parameters.</span></span>  
  
 <span data-ttu-id="da4da-113">WCF 无法区分客户端和服务参数;它添加所有参数，并以 `RequestSecurityTokenTemplate` (RST) 发送它们。</span><span class="sxs-lookup"><span data-stu-id="da4da-113">WCF cannot differentiate between the client and service parameters; it adds all the parameters and sends them in the `RequestSecurityTokenTemplate` (RST).</span></span>  
  
## <a name="rp-trust-13-and-sts-trust-13"></a><span data-ttu-id="da4da-114">RP Trust 1.3 和 STS Trust 1.3</span><span class="sxs-lookup"><span data-stu-id="da4da-114">RP Trust 1.3 and STS Trust 1.3</span></span>  

 <span data-ttu-id="da4da-115">RP 的 WSDL 在 `RequestSecurityTokenTemplate` 节中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="da4da-115">The WSDL for RP contains the following elements within the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
- `KeyWrapAlgorithm`  
  
 <span data-ttu-id="da4da-116">客户端配置文件包含一个 `secondaryParameters` 元素，该元素包装 RP 所指定的参数。</span><span class="sxs-lookup"><span data-stu-id="da4da-116">The client configuration file contains a `secondaryParameters` element that wraps the parameters specified by the RP.</span></span>  
  
 <span data-ttu-id="da4da-117">`EncryptionAlgorithm` `CanonicalizationAlgorithm` `KeyWrapAlgorithm` 如果元素存在于元素内，WCF 将从 RST 的顶级元素中移除和元素 `SecondaryParameters` 。</span><span class="sxs-lookup"><span data-stu-id="da4da-117">WCF removes the `EncryptionAlgorithm`, `CanonicalizationAlgorithm` and `KeyWrapAlgorithm` elements from the top-level element under the RST if these are present inside the `SecondaryParameters` element.</span></span> <span data-ttu-id="da4da-118">WCF 将 `SecondaryParameters` 元素追加到未修改的传出 RST。</span><span class="sxs-lookup"><span data-stu-id="da4da-118">WCF appends the `SecondaryParameters` element to the outgoing RST unmodified.</span></span>  
  
## <a name="rp-trust-feb-2005-and-sts-trust-13"></a><span data-ttu-id="da4da-119">RP Trust Feb 2005 和 STS Trust 1.3</span><span class="sxs-lookup"><span data-stu-id="da4da-119">RP Trust Feb 2005 and STS Trust 1.3</span></span>  

 <span data-ttu-id="da4da-120">RP 的 WSDL 在 `RequestSecurityTokenTemplate` 节中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="da4da-120">The WSDL for RP contains the following elements in the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
 <span data-ttu-id="da4da-121">客户端配置文件包含一个参数列表。</span><span class="sxs-lookup"><span data-stu-id="da4da-121">The client configuration file contains a list of parameters.</span></span>  
  
 <span data-ttu-id="da4da-122">在客户端配置文件中，WCF 无法区分服务参数和客户端参数。</span><span class="sxs-lookup"><span data-stu-id="da4da-122">From the client configuration file, WCF cannot differentiate between the service and client parameters.</span></span> <span data-ttu-id="da4da-123">因此，WCF 会将所有参数转换为信任版本1.3 命名空间。</span><span class="sxs-lookup"><span data-stu-id="da4da-123">Therefore WCF converts all the parameters to a Trust version 1.3 namespace.</span></span>  
  
 <span data-ttu-id="da4da-124">WCF 处理 `KeyType` 、 `KeySize` 和元素， `TokenType` 如下所示：</span><span class="sxs-lookup"><span data-stu-id="da4da-124">WCF handles the `KeyType`, `KeySize`, and `TokenType` elements as follows:</span></span>  
  
- <span data-ttu-id="da4da-125">下载 WSDL，创建绑定，并从 RP 参数分配 `KeyType`、`KeySize` 和 `TokenType`。</span><span class="sxs-lookup"><span data-stu-id="da4da-125">Download the WSDL, create the binding, and assign `KeyType`, `KeySize`, and `TokenType` from the RP parameters.</span></span> <span data-ttu-id="da4da-126">随后会生成客户端配置文件。</span><span class="sxs-lookup"><span data-stu-id="da4da-126">The client configuration file is then generated.</span></span>  
  
- <span data-ttu-id="da4da-127">客户端现在可以更改配置文件中的任何参数。</span><span class="sxs-lookup"><span data-stu-id="da4da-127">The client can now change any parameter in the configuration file.</span></span>  
  
- <span data-ttu-id="da4da-128">在运行时，WCF 会将指定的所有参数都复制到 `AdditionalTokenParameters` 客户端配置文件的节中（和除外）， `KeyType` `KeySize` `TokenType` 因为这些参数在配置文件生成过程中进行考虑。</span><span class="sxs-lookup"><span data-stu-id="da4da-128">During runtime, WCF copies all parameters specified into the `AdditionalTokenParameters` section of the client configuration file except `KeyType`, `KeySize` and `TokenType`, because these parameters are accounted for during the configuration file generation.</span></span>  
  
## <a name="rp-trust-13-and-sts-trust-feb-2005"></a><span data-ttu-id="da4da-129">RP Trust 1.3 和 STS Trust Feb 2005</span><span class="sxs-lookup"><span data-stu-id="da4da-129">RP Trust 1.3 and STS Trust Feb 2005</span></span>  

 <span data-ttu-id="da4da-130">RP 的 WSDL 在 `RequestSecurityTokenTemplate` 节中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="da4da-130">The WSDL for RP contains the following elements in the `RequestSecurityTokenTemplate` section:</span></span>  
  
- `CanonicalizationAlgorithm`  
  
- `EncryptionAlgorithm`  
  
- `EncryptWith`  
  
- `SignWith`  
  
- `KeySize`  
  
- `KeyType`  
  
- `KeyWrapAlgorithm`  
  
 <span data-ttu-id="da4da-131">客户端配置文件包含一个 `secondaryParamters` 元素，该元素包装 RP 所指定的参数。</span><span class="sxs-lookup"><span data-stu-id="da4da-131">The client configuration file contains a `secondaryParamters` element that wraps the parameters specified by the RP.</span></span>  
  
 <span data-ttu-id="da4da-132">WCF 将部分中指定的所有参数复制 `SecondaryParameters` 到顶层 RST 元素，但不会将其转换为 2005 WS-Trust 命名空间。</span><span class="sxs-lookup"><span data-stu-id="da4da-132">WCF copies all the parameters specified within the `SecondaryParameters` section to the top-level RST element, but does not convert them to the 2005 WS-Trust namespace.</span></span>
