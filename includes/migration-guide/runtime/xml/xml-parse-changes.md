---
ms.openlocfilehash: dfa8235fcfd868b80d3a610bddb492899519e289
ms.sourcegitcommit: 81f1bba2c97a67b5ca76bcc57b37333ffca60c7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "97009043"
---
### <a name="xml-parsing-changes"></a><span data-ttu-id="21bf9-101">XML 分析更改</span><span class="sxs-lookup"><span data-stu-id="21bf9-101">XML parsing changes</span></span>

| <span data-ttu-id="21bf9-102">名称</span><span class="sxs-lookup"><span data-stu-id="21bf9-102">Name</span></span>    | <span data-ttu-id="21bf9-103">值</span><span class="sxs-lookup"><span data-stu-id="21bf9-103">Value</span></span>   |
|:--------|:--------|
| <span data-ttu-id="21bf9-104">范围</span><span class="sxs-lookup"><span data-stu-id="21bf9-104">Scope</span></span>   | <span data-ttu-id="21bf9-105">次要</span><span class="sxs-lookup"><span data-stu-id="21bf9-105">Minor</span></span>   |
| <span data-ttu-id="21bf9-106">Version</span><span class="sxs-lookup"><span data-stu-id="21bf9-106">Version</span></span> | <span data-ttu-id="21bf9-107">4.5.2</span><span class="sxs-lookup"><span data-stu-id="21bf9-107">4.5.2</span></span>   |
| <span data-ttu-id="21bf9-108">类型</span><span class="sxs-lookup"><span data-stu-id="21bf9-108">Type</span></span>    | <span data-ttu-id="21bf9-109">运行时</span><span class="sxs-lookup"><span data-stu-id="21bf9-109">Runtime</span></span> |

#### <a name="details"></a><span data-ttu-id="21bf9-110">详细信息</span><span class="sxs-lookup"><span data-stu-id="21bf9-110">Details</span></span>

<span data-ttu-id="21bf9-111">出于安全原因，XML 分析 API 中引入了以下更改：</span><span class="sxs-lookup"><span data-stu-id="21bf9-111">For security reasons, the following changes were introduced into XML parsing APIS:</span></span>

- <span data-ttu-id="21bf9-112">初始化 <xref:System.Xml.XmlReaderSettings> 时，<xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities?displayProperty=nameWithType> 设置为 1 千万。</span><span class="sxs-lookup"><span data-stu-id="21bf9-112"><xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities?displayProperty=nameWithType> is set to 10 million when <xref:System.Xml.XmlReaderSettings> is initialized.</span></span>
- <span data-ttu-id="21bf9-113">默认情况下，<xref:System.Xml.XmlReaderSettings.XmlResolver?displayProperty=nameWithType> 设置为 `null`。</span><span class="sxs-lookup"><span data-stu-id="21bf9-113"><xref:System.Xml.XmlReaderSettings.XmlResolver?displayProperty=nameWithType> is set to `null` by default.</span></span>

> [!NOTE]
> <span data-ttu-id="21bf9-114">所有 XML 分析器都使用 <xref:System.Xml.XmlReaderSettings>，因此尽管此更改有助于 <xref:System.Xml.XmlReader> 的情况，但它也会影响其他情况。</span><span class="sxs-lookup"><span data-stu-id="21bf9-114"><xref:System.Xml.XmlReaderSettings> is used by all XML parsers, so while this change helps the <xref:System.Xml.XmlReader> case, it also affects other scenarios.</span></span>

#### <a name="suggestion"></a><span data-ttu-id="21bf9-115">建议</span><span class="sxs-lookup"><span data-stu-id="21bf9-115">Suggestion</span></span>

<span data-ttu-id="21bf9-116">若要恢复到以前的行为，可以在注册表中设置一个值。</span><span class="sxs-lookup"><span data-stu-id="21bf9-116">To revert to the previous behavior, you can set a value in the registry.</span></span> <span data-ttu-id="21bf9-117">将名为 `EnableLegacyXmlSettings` 的 DWORD 值添加到 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\XML` 注册表项，并将其值设置为 `1`。</span><span class="sxs-lookup"><span data-stu-id="21bf9-117">Add a DWORD value named `EnableLegacyXmlSettings` to the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\XML` registry key, and set its value to `1`.</span></span> <span data-ttu-id="21bf9-118">还可以改为在 HKEY_CURRENT_USER 配置单元中添加注册表值。</span><span class="sxs-lookup"><span data-stu-id="21bf9-118">You can also add the registry value in the HKEY_CURRENT_USER hive instead.</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="21bf9-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="21bf9-119">Affected APIs</span></span>

- <xref:System.Xml.XmlReaderSettings.MaxCharactersFromEntities?displayProperty=fullName>
- <xref:System.Xml.XmlReaderSettings.XmlResolver?displayProperty=fullName>

<span data-ttu-id="21bf9-120">此外，任何直接或间接依赖于 <xref:System.Xml.XmlResolver> 的 XML API 都会受到影响。</span><span class="sxs-lookup"><span data-stu-id="21bf9-120">In addition, any XML API that depends on <xref:System.Xml.XmlResolver>, either directly or indirectly, is affected.</span></span>

<!--

#### Affected APIs

- `P:System.Xml.XmlReaderSettings.MaxCharactersFromEntities`
- `P:System.Xml.XmlReaderSettings.XmlResolver`

-->
