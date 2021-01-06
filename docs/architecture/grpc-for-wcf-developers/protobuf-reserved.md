---
title: Protobuf 保留字段-WCF 开发人员 gRPC
description: 了解有关跨版本兼容性的保留字段。
ms.date: 12/15/2020
ms.openlocfilehash: d82043d619c5b3b81091ae4ea381e4778c1cf6ba
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938515"
---
# <a name="protobuf-reserved-fields"></a><span data-ttu-id="b6ec3-103">Protobuf 保留字段</span><span class="sxs-lookup"><span data-stu-id="b6ec3-103">Protobuf reserved fields</span></span>

<span data-ttu-id="b6ec3-104">协议缓冲区中的向后兼容性保证 (Protobuf) 依赖于字段编号始终表示相同的数据项。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-104">The backward-compatibility guarantees in Protocol Buffer (Protobuf) rely on field numbers always representing the same data item.</span></span> <span data-ttu-id="b6ec3-105">如果从服务的新版本的消息中删除字段，则永远不应重复使用该字段号。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-105">If a field is removed from a message in a new version of the service, that field number should never be reused.</span></span> <span data-ttu-id="b6ec3-106">可以通过使用关键字强制执行此行为 `reserved` 。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-106">You can enforce this behavior by using the `reserved` keyword.</span></span>

<span data-ttu-id="b6ec3-107">如果 `displayName` `marketId` 已从前面定义的消息中删除了和字段 `Stock` ，则应该保留其字段编号，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-107">If the `displayName` and `marketId` fields were removed from the `Stock` message defined earlier, their field numbers should be reserved as in the following example.</span></span>

```protobuf
syntax "proto3";

message Stock {

    reserved 3, 4;
    int32 id = 1;
    string symbol = 2;

}
```

<span data-ttu-id="b6ec3-108">你还可以使用 `reserved` 关键字作为以后可能添加的字段的占位符。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-108">You can also use the `reserved` keyword as a placeholder for fields that might be added in the future.</span></span> <span data-ttu-id="b6ec3-109">您可以使用关键字将连续的字段编号表示为范围 `to` 。</span><span class="sxs-lookup"><span data-stu-id="b6ec3-109">You can express contiguous field numbers as a range by using the `to` keyword.</span></span>

```protobuf
syntax "proto3";

message Info {

    reserved 2, 9 to 11, 15;
    // ...
}
```

>[!div class="step-by-step"]
><span data-ttu-id="b6ec3-110">[上一页](protobuf-repeated.md)
>[下一页](protobuf-any-oneof.md)</span><span class="sxs-lookup"><span data-stu-id="b6ec3-110">[Previous](protobuf-repeated.md)
[Next](protobuf-any-oneof.md)</span></span>
