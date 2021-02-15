---
description: 了解详细信息：在 FileName 中指定的文件不是有效的 XML 文件
title: 在 FileName 中指定的文件不是有效的 XML 文件
ms.date: 07/20/2015
ms.assetid: c4c30bf3-e0ad-4bc8-89e0-2c3e49e9793b
ms.openlocfilehash: c7d521986f3489345117a3947ed1e9b459af897e
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472977"
---
# <a name="file-specified-in-filename-is-not-a-valid-xml-file"></a><span data-ttu-id="43204-103">在 FileName 中指定的文件不是有效的 XML 文件</span><span class="sxs-lookup"><span data-stu-id="43204-103">File specified in FileName is not a valid XML file</span></span>

<span data-ttu-id="43204-104">所提供的文件名称不是有效的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="43204-104">The file name that you supplied is not a valid XML file.</span></span> <span data-ttu-id="43204-105">若要指定允许的 XML 文档的结构和内容，可使用文档类型定义 (DTD)、Microsoft XML 数据缩减 (XDR) 架构或 XML 架构定义语言 (XSD) 架构。</span><span class="sxs-lookup"><span data-stu-id="43204-105">To specify the allowed structure and content of an XML document, you can use a Document Type Definition (DTD), a Microsoft XML-Data Reduced (XDR) schema, or an XML Schema definition language (XSD) schema.</span></span> <span data-ttu-id="43204-106">XSD 架构是在 .NET Framework 中指定 XML 语法的首选方式。</span><span class="sxs-lookup"><span data-stu-id="43204-106">XSD schemas are the preferred way to specify XML grammars in the .NET Framework.</span></span>

> [!NOTE]
> <span data-ttu-id="43204-107">在某些较早版本的 Visual Studio 中，“XML 设计器”  是针对类型化数据集和 XML 架构的设计器。</span><span class="sxs-lookup"><span data-stu-id="43204-107">In some earlier versions of Visual Studio, the **XML Designer** is the designer for typed datasets and XML schema.</span></span> <span data-ttu-id="43204-108">“XML 设计器”  仍可用于创建和编辑 XML 架构文件。</span><span class="sxs-lookup"><span data-stu-id="43204-108">The **XML Designer** can still be used to create and edit XML schema files.</span></span> <span data-ttu-id="43204-109">但是，在 Visual Studio 2012 中，用于创建和编辑类型化数据集的设计器是 **数据集设计器**。</span><span class="sxs-lookup"><span data-stu-id="43204-109">However, in Visual Studio 2012, the designer for creating and editing typed datasets is the **Dataset Designer**.</span></span> <span data-ttu-id="43204-110">有关详细信息，请参阅 [创建和编辑类型化数据集](/previous-versions/visualstudio/visual-studio-2013/314t4see(v=vs.120))。</span><span class="sxs-lookup"><span data-stu-id="43204-110">For more information, see [Creating and Editing Typed Datasets](/previous-versions/visualstudio/visual-studio-2013/314t4see(v=vs.120)).</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="43204-111">更正此错误</span><span class="sxs-lookup"><span data-stu-id="43204-111">To correct this error</span></span>

- <span data-ttu-id="43204-112">检查你所提供的文件名是否正确。</span><span class="sxs-lookup"><span data-stu-id="43204-112">Check that you are supplying the correct file name.</span></span>

- <span data-ttu-id="43204-113">通过将你想要检查的 XML 文件加载到“XML 设计器” 中，检查指定文件是否包含有效的 XML。</span><span class="sxs-lookup"><span data-stu-id="43204-113">Check that the specified file contains valid XML by loading the XML file that you want to check into the **XML Designer**.</span></span> <span data-ttu-id="43204-114">从“XML”  菜单上，单击“验证 XML” 。</span><span class="sxs-lookup"><span data-stu-id="43204-114">From the **XML** menu, click **Validate XML**.</span></span> <span data-ttu-id="43204-115">错误都显示在“输出列表” 中。</span><span class="sxs-lookup"><span data-stu-id="43204-115">Errors are displayed in the **Task List**.</span></span>

- <span data-ttu-id="43204-116">如果 XML 文件具有关联的 XML 架构，请检查显示在已定义结构中的元素，以及单个元素的内容是否符合架构中指定的已声明的数据类型。</span><span class="sxs-lookup"><span data-stu-id="43204-116">If the XML file has an associated XML Schema, check that the elements appear in the defined structure and that the content of the individual elements conforms to the declared data types specified in the schema.</span></span>

## <a name="see-also"></a><span data-ttu-id="43204-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="43204-117">See also</span></span>

- <xref:System.Xml>
- [<span data-ttu-id="43204-118">如何：分析文件路径</span><span class="sxs-lookup"><span data-stu-id="43204-118">How to: Parse File Paths</span></span>](../developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)
