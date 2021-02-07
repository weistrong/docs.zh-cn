---
description: 了解详细信息： TransactionFlowBindingElement
title: TransactionFlowBindingElement
ms.date: 03/30/2017
ms.assetid: 0a9656fe-2400-45ca-ad79-92715c8cf190
ms.openlocfilehash: 6a96a83c563affdaef01a12d64bc1c13ab2f719e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757132"
---
# <a name="transactionflowbindingelement"></a><span data-ttu-id="f28c0-103">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="f28c0-103">TransactionFlowBindingElement</span></span>

<span data-ttu-id="f28c0-104">TransactionFlowBindingElement</span><span class="sxs-lookup"><span data-stu-id="f28c0-104">TransactionFlowBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f28c0-105">语法</span><span class="sxs-lookup"><span data-stu-id="f28c0-105">Syntax</span></span>  
  
```csharp
class TransactionFlowBindingElement : BindingElement  
{  
  string IssuedTokens;  
  string TransactionProtocol;  
  boolean Transactions;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f28c0-106">方法</span><span class="sxs-lookup"><span data-stu-id="f28c0-106">Methods</span></span>  

 <span data-ttu-id="f28c0-107">TransactionFlowBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="f28c0-107">The TransactionFlowBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f28c0-108">属性</span><span class="sxs-lookup"><span data-stu-id="f28c0-108">Properties</span></span>  

 <span data-ttu-id="f28c0-109">TransactionFlowBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="f28c0-109">The TransactionFlowBindingElement class has the following properties:</span></span>  
  
### <a name="issuedtokens"></a><span data-ttu-id="f28c0-110">IssuedTokens</span><span class="sxs-lookup"><span data-stu-id="f28c0-110">IssuedTokens</span></span>  

 <span data-ttu-id="f28c0-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f28c0-111">Data type: string</span></span>  
  
 <span data-ttu-id="f28c0-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f28c0-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f28c0-113">指定对已颁发的安全令牌标头（来自 WS-Trust 的 IssuedTokens）的要求。</span><span class="sxs-lookup"><span data-stu-id="f28c0-113">Specifies the requirement for an issued security tokens header (IssuedTokens from WS-Trust).</span></span>  
  
### <a name="transactionprotocol"></a><span data-ttu-id="f28c0-114">TransactionProtocol</span><span class="sxs-lookup"><span data-stu-id="f28c0-114">TransactionProtocol</span></span>  

 <span data-ttu-id="f28c0-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f28c0-115">Data type: string</span></span>  
  
 <span data-ttu-id="f28c0-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f28c0-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f28c0-117">对事务进行流处理时使用的事务处理协议。</span><span class="sxs-lookup"><span data-stu-id="f28c0-117">The transactions protocol used by the service to flow transactions.</span></span>  
  
### <a name="transactions"></a><span data-ttu-id="f28c0-118">事务</span><span class="sxs-lookup"><span data-stu-id="f28c0-118">Transactions</span></span>  

 <span data-ttu-id="f28c0-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="f28c0-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="f28c0-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f28c0-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f28c0-121">指示是否支持传入事务。</span><span class="sxs-lookup"><span data-stu-id="f28c0-121">Indicates whether the incoming transaction is supported.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f28c0-122">要求</span><span class="sxs-lookup"><span data-stu-id="f28c0-122">Requirements</span></span>  
  
|<span data-ttu-id="f28c0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f28c0-123">MOF</span></span>|<span data-ttu-id="f28c0-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="f28c0-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f28c0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f28c0-125">Namespace</span></span>|<span data-ttu-id="f28c0-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="f28c0-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f28c0-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="f28c0-127">See also</span></span>

- <xref:System.ServiceModel.Channels.TransactionFlowBindingElement>
