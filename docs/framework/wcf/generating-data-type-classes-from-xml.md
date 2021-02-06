---
description: 了解详细信息：从 XML 生成数据类型类
title: 从 XML 生成数据类型类
ms.date: 03/30/2017
ms.assetid: e4e5e4e8-527f-44d1-92fa-8904a08784ea
ms.openlocfilehash: c79550b1e4804426267aef33860bc49d5d3b5efa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99632134"
---
# <a name="generating-data-type-classes-from-xml"></a><span data-ttu-id="c4fb0-103">从 XML 生成数据类型类</span><span class="sxs-lookup"><span data-stu-id="c4fb0-103">Generating Data Type Classes from XML</span></span>

<span data-ttu-id="c4fb0-104">.NET Framework 4.5 包含一项新功能，可用于从 XML 生成数据类型类。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-104">.NET Framework 4.5 includes a new feature to generate data type classes from XML.</span></span> <span data-ttu-id="c4fb0-105">本主题介绍如何为 .NET 博客 RSS 源自动生成数据类型。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-105">This topic describes how to automatically generate data types for the .NET Blog RSS feed.</span></span>  
  
### <a name="obtaining-the-xml-from-the-net-blog-rss-feed"></a><span data-ttu-id="c4fb0-106">从 .NET 博客 RSS 源获取 XML</span><span class="sxs-lookup"><span data-stu-id="c4fb0-106">Obtaining the XML from the .NET Blog RSS feed</span></span>  
  
1. <span data-ttu-id="c4fb0-107">在 Internet Explorer 中，导航到 [.Net 博客 rss 源](https://devblogs.microsoft.com/dotnet/feed/)。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-107">In Internet Explorer, navigate to the [.NET Blog RSS feed](https://devblogs.microsoft.com/dotnet/feed/).</span></span>  
  
2. <span data-ttu-id="c4fb0-108">右键单击该页并选择 " **查看源**"。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-108">Right-click the page and select **View Source**.</span></span>  
  
3. <span data-ttu-id="c4fb0-109">通过按 **ctrl + A** 选择所有文本，然后按 **ctrl + C** 复制，复制源的文本。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-109">Copy the text of the feed by pressing **Ctrl+A** to select all text, and **Ctrl+C** to copy.</span></span>  
  
### <a name="creating-the-data-types"></a><span data-ttu-id="c4fb0-110">创建数据类型</span><span class="sxs-lookup"><span data-stu-id="c4fb0-110">Creating the data types</span></span>  
  
1. <span data-ttu-id="c4fb0-111">打开要使用代理的代码文件。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-111">Open a code file where the proxy is to be used.</span></span> <span data-ttu-id="c4fb0-112">此文件应属于 .NET Framework 4.5 项目。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-112">This file should be part of a .NET Framework 4.5 project.</span></span>  
  
2. <span data-ttu-id="c4fb0-113">将游标放置于该文件中任何现有类之外的位置中。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-113">Place the cursor in a location in the file outside any existing classes.</span></span>  
  
3. <span data-ttu-id="c4fb0-114">选择 " **编辑**"、" **粘贴特殊**"、"将 **XML 粘贴为类**"。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-114">Select **Edit**, **Paste Special**, **Paste XML as Classes**.</span></span>  
  
4. <span data-ttu-id="c4fb0-115">将创建名为、、、和的类 `link` ， `rss` `rssChannel` `rssChannelImage` `rssChannelItem` `rssChannelItemGuid` 其中包含访问 RSS 源中的元素所需的成员。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-115">Classes called `link`, `rss`, `rssChannel`, `rssChannelImage`, `rssChannelItem` and `rssChannelItemGuid` are created with the necessary members for accessing the elements in the RSS feed.</span></span>  
  
### <a name="using-the-generated-classes"></a><span data-ttu-id="c4fb0-116">使用生成的类</span><span class="sxs-lookup"><span data-stu-id="c4fb0-116">Using the generated classes</span></span>  
  
1. <span data-ttu-id="c4fb0-117">一旦生成了类，这些类就可以像任何其他类一样在代码中使用。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-117">Once the classes are generated, they can be used in code like any other classes.</span></span> <span data-ttu-id="c4fb0-118">下面的代码示例返回 `rssChannelImage` 类的新实例。</span><span class="sxs-lookup"><span data-stu-id="c4fb0-118">The following code example returns a new instance of the `rssChannelImage` class.</span></span>  
  
    ```csharp
    var channelImage = new rssChannelImage()
    {
        title = "MyImage",
        link = "http://www.contoso.com/images/channelImage.jpg",
        url = "http://www.contoso.com/entries/myEntry.html"
    };  
    ```
