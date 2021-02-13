---
title: 中断性变更：TreeNodeCollection.Item(Int32) 为正在使用的节点抛出 ArgumentException
description: 了解 .NET 6.0 中的中断性变更，即如果要分配的节点已分配给 TreeView，TreeNodeCollection.Item(Int32) 现在会抛出 ArgumentException。
ms.date: 01/19/2021
ms.openlocfilehash: efd6ca5d594b2aa64e10cce2cef6c0e1c411bb1e
ms.sourcegitcommit: f2ab02d9a780819ca2e5310bbcf5cfe5b7993041
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "99506465"
---
# <a name="treenodecollectionitem-throws-exception-if-node-is-assigned-elsewhere"></a><span data-ttu-id="2c215-103">如果节点被分配到其他地方，则 TreeNodeCollection.Item 抛出异常</span><span class="sxs-lookup"><span data-stu-id="2c215-103">TreeNodeCollection.Item throws exception if node is assigned elsewhere</span></span>

<span data-ttu-id="2c215-104">如果要分配的节点已绑定到另一个 <xref:System.Windows.Forms.TreeView> 或位于不同索引上的此 <xref:System.Windows.Forms.TreeView>，则 <xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=nameWithType> 会抛出 <xref:System.ArgumentException>。</span><span class="sxs-lookup"><span data-stu-id="2c215-104"><xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=nameWithType> throws an <xref:System.ArgumentException> if the node being assigned is already bound to another <xref:System.Windows.Forms.TreeView> or to this <xref:System.Windows.Forms.TreeView> at a different index.</span></span>

## <a name="change-description"></a><span data-ttu-id="2c215-105">更改描述</span><span class="sxs-lookup"><span data-stu-id="2c215-105">Change description</span></span>

<span data-ttu-id="2c215-106">在旧版 .NET 中，可以将树节点分配到集合，即使它已绑定到 <xref:System.Windows.Forms.TreeView>。</span><span class="sxs-lookup"><span data-stu-id="2c215-106">In previous .NET versions, you can assign a tree node to a collection even if it's already bound to a <xref:System.Windows.Forms.TreeView>.</span></span> <span data-ttu-id="2c215-107">这可能会导致重复的节点。</span><span class="sxs-lookup"><span data-stu-id="2c215-107">This can lead to duplicated nodes.</span></span> <span data-ttu-id="2c215-108">自 .NET 6.0 起，如果要分配的节点已绑定到另一个 <xref:System.Windows.Forms.TreeView> 或位于不同索引上的此 <xref:System.Windows.Forms.TreeView>，则 <xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=nameWithType> 会抛出 <xref:System.ArgumentException>。</span><span class="sxs-lookup"><span data-stu-id="2c215-108">Starting in .NET 6.0, <xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=nameWithType> throws an <xref:System.ArgumentException> if the node being assigned is already bound to another <xref:System.Windows.Forms.TreeView> or to this <xref:System.Windows.Forms.TreeView> at a different index.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="2c215-109">更改原因</span><span class="sxs-lookup"><span data-stu-id="2c215-109">Reason for change</span></span>

<span data-ttu-id="2c215-110">验证输入参数是否与其他 `TreeNodeCollection` API 的行为一致。</span><span class="sxs-lookup"><span data-stu-id="2c215-110">Validating the input parameter is consistent with the behavior of other `TreeNodeCollection` APIs.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="2c215-111">引入的版本</span><span class="sxs-lookup"><span data-stu-id="2c215-111">Version introduced</span></span>

<span data-ttu-id="2c215-112">.NET 6.0 预览版 1</span><span class="sxs-lookup"><span data-stu-id="2c215-112">.NET 6.0 Preview 1</span></span>

## <a name="recommended-action"></a><span data-ttu-id="2c215-113">建议的操作</span><span class="sxs-lookup"><span data-stu-id="2c215-113">Recommended action</span></span>

<span data-ttu-id="2c215-114">在将 `TreeNode` 分配到集合之前，请务必先取消绑定它。</span><span class="sxs-lookup"><span data-stu-id="2c215-114">Make sure to unbind a `TreeNode` before assigning it to the collection.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="2c215-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="2c215-115">Affected APIs</span></span>

<xref:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)?displayProperty=fullName>

<!--

### Affected APIs

- `P:System.Windows.Forms.TreeNodeCollection.Item(System.Int32)`

### Category

Windows Forms

-->
